# FAQ

## I'm seeing a scary warning when logging in with Metamask

**Don't panic.** This is Metamask being overly cautious about decentralized sites, not a security issue.

Here's what's happening: Your site lives on Arweave (the permanent web), but Metamask was designed for traditional websites. When you access the site through different gateways like "listen.ar.io" or other ARNS addresses, Metamask throws a tantrum because it can't match the server signature with the URL.

**The fix is simple:** Use the specific gateway `contractwizard.arweave.net` and the warning disappears. This is the URL that matches what the server expects.

**Why this happens:** Metamask wants the server and frontend URLs to match perfectly. Since Arweave sites can be accessed through multiple gateways, this creates a mismatch that triggers the warning. It's like having multiple front doors to the same house, perfectly safe, but confusing for a guard who only knows about one entrance.

**The future:** Eventually, Metamask will get hip to how Arweave works and stop being so neurotic about decentralized hosting. Until then, bookmark `contractwizard.arweave.net` and you're golden.

Top: ![](<../.gitbook/assets/Screenshot 2025-07-31 at 9.58.21 AM.png>) Bottom:  ![](<../.gitbook/assets/Screenshot 2025-07-31 at 9.58.31 AM.png>)   Warnings: ![](<../.gitbook/assets/Screenshot 2025-07-31 at 9.58.45 AM (1).png>)  :  ![](<../.gitbook/assets/Screenshot 2025-07-31 at 9.58.58 AM.png>)



## Why are none of the pictures loading?

**Your ISP is being a buzzkill.** Some internet providers (especially in Australia and similar freedom-loving countries) block Arweave because they don't understand the permanent web yet.

**The solution:** Fire up a VPN and watch everything load perfectly. This isn't a bug in the site, it's your ISP playing gatekeeper to the decentralized future.

## Is this some kind of crypto scam?

**Nope.** This is an open-source project building infrastructure for musicians to own their digital masters. No token sales, no roadmaps to the moon, no celebrity endorsements. Just tools that let artists create verifiable originals and distribute copies without rent-seeking middlemen.

The Contract Wizard has been live on mainnet since 2023, the code is on GitHub, and everything is designed to work forever even if I disappear tomorrow. That's the opposite of a scam, it's antifragile infrastructure.
