# Wallets And Auth

The site uses RainbowKit for Ethereum wallets and stuff. Thanks to RainbowKit you can sign in with Ethereum wallets on your desktop and mobile.  You can now upload files to Arweave using ArDrive Turbo credits right on your phone, without ever having to use a computer.

## How Sign-In Works

Connect your wallet, and the server sends back a one-time sign-in message. Your wallet asks you to sign it — signing is free, no gas, nothing leaves your wallet but the signature. The server verifies it and you're in. There are no passwords anywhere in this flow; your keys are the only way in.

## The Signed Message

That popup isn't random text — it's a **Sign-In with Ethereum (ERC-4361)** message, the Ethereum standard for "log in with your wallet." It binds the sign-in to your address, the site's domain, and a one-time nonce that expires in 10 minutes:

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

## Why This Is Above Spec

- **The server authors every message.** Clients never write the text — the server mints the challenge and requires the signature to match it byte for byte. A swapped domain, a different address, or a message the server never issued fails even with a valid signature.
- **EIP-191 with an ERC-1271 fallback.** Regular wallets are verified through offline signature recovery; smart contract wallets (Safe, Argent) are verified on-chain, so they work too.
- **The door is wallet-only.** Nonces are server-issued, tracked in the database, and expire in 10 minutes. Minting is rate limited, and password login is disabled at the server entirely.

The short version: logging in proves you hold the private key for your address, and nothing else can stand in for it.
