# Wallets And Auth

The site uses RainbowKit for Ethereum wallets and stuff. Thanks to RainbowKit you can sign in with Ethereum wallets on your desktop and mobile. You can now upload files to Arweave using ArDrive Turbo credits right on your phone, without ever having to use a computer.

## How Sign-In Works

1. **Connect your wallet.** RainbowKit handles MetaMask, WalletConnect, Coinbase Wallet, and friends.
2. **The server sends you a challenge.** The Parse backend (apetapes.xyz) generates a one-time sign-in message bound to your wallet address. Nothing is signed until you've seen exactly what you're agreeing to.
3. **You sign it.** Your wallet asks for a signature. Signing is free — no gas, no transaction, nothing leaves your wallet but the signature.
4. **The server verifies it.** If the signature checks out, you get a session. There are no passwords anywhere in this flow — your keys are the only way in.

## The Signed Message

That popup your wallet shows isn't random text. It's a **Sign-In with Ethereum (ERC-4361)** message — an Ethereum standard that defines exactly what a sign-in request should look like, so wallets can display it honestly and servers can verify it rigorously:

```
Apetapes.xyz wants you to sign in with your Ethereum account:
0xYourAddress...

Please sign this message to log in to The Contract Wizard.

URI: https://apetapes.xyz
Version: 1
Chain ID: 1
Nonce: 9f86d081884c7d659a2feaa0c55ad015
Issued At: 2026-09-01T12:00:00.000Z
Expiration Time: 2026-09-01T12:10:00.000Z
```

Every line means something:

| Field | What it protects |
|---|---|
| `Apetapes.xyz` (domain) | Your wallet shows you who is asking. A phishing site can't fake this line — the server, not the page, writes it. |
| Address | Binds the signature to your specific wallet. |
| `Nonce` | A fresh 128-bit random value per sign-in, stored server-side. Replaying an old signature doesn't work. |
| `Issued At` / `Expiration Time` | Challenges expire 10 minutes after minting. |
| `Chain ID` | The chain you connected on. |

## Why This Is Above Spec

ERC-4361 asks a server to check the message format, recover the signer, and track nonces. The backend does all of that, plus a few things the spec doesn't require:

- **The server authors every message.** The backend never parses a message the client sent — it compares your signature against the exact challenge it minted, byte for byte. A modified message (swapped domain, different address) fails even with a valid signature, and messages the server never issued fail outright. There is no message-format edge case to get wrong because clients don't get to author the message.
- **The signature must recover to the challenge's address.** Signing your own challenge and submitting it with someone else's account id is rejected (impersonation).
- **EIP-191 recovery with an ERC-1271 fallback.** Normal wallet signatures are verified offline via `ecrecover` over the raw message. Smart contract wallets (Safe, Argent) can't sign that way — for them the server asks the chain via `isValidSignature`, so those wallets work too (on Ethereum, Polygon, Base, Zora, and Sepolia).
- **Challenges are rate limited** per client IP, and nonces are single-challenge rows in the database with a unique index — not a value the server hopes it remembers.
- **Password login is disabled at the server.** Wallet accounts don't have usable passwords; the signature is the only credential that opens an account.
- **The whole flow has a regression harness** that boots the real server and attacks it — tampered messages, self-minted challenges, impersonation, replays, expired challenges — and fails the build if any of them get through.

The short version: logging in proves you hold the private key for your address, and nothing else can stand in for it.
