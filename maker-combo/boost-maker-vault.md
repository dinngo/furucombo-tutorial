# Boost Maker vault

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*wpcQ_szohs42IBUFEmHe8w.png" alt=""><figcaption><p>Boost Maker Vault</p></figcaption></figure>

In this article, we will walk you through how to open a Maker vault and a strategy on how to increase a vault collateral’s exposure to multiply the potential return. For this strategy, you make a profit when the collateral’s price surges. On the other side, and this is very important, you might get liquidated when the price goes down.

## Content

* [What is Maker vault, and how to open one?](boost-maker-vault.md#what-is-maker-vault-and-how-to-open-one)
* [What is boost strategy?](boost-maker-vault.md#what-is-boost-strategy)
  * [Basic level: Build manually](boost-maker-vault.md#1-basic-level-build-manually)
  * [Advanced Level: Build Manually with Flashloan](boost-maker-vault.md#2-advanced-level-build-manually-with-flashloan)
  * [Pro Level: Skip building](boost-maker-vault.md#3-pro-level-skip-building)

## What is Maker vault, and how to open one?

The Maker Vault is a core component of the Maker Protocol, which facilitates the generation of DAI against locked up collateral. All DAI in circulation are created by Vaults. Users create DAI by generating it against their collateral and in-turn destroy DAI when repaying their generated DAI balance.

Everyone can open a Maker vault by locking accepted collateral such as ETH, USDC, BAT, etc., and generating DAI as your debt position. Each collateral type on Maker has its own risk parameters; therefore, how much DAI you can generate from your vault depends on each vault’s liquidation ratio.

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*kWo9qfAHsKu6r8OfgbOMBw.png" alt=""><figcaption><p>Collateral Type list from Oasis.app</p></figcaption></figure>

Take ETH-A vault as an example. You may generate up to 2/3 of ETH value in DAI. To open a new vault, you may go to [Maker Oasis Barrow](https://oasis.app/borrow) or even better, you use [Furucombo](https://furucombo.app/combo)! Just go to the menu and select “New Vault” under Maker section.

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*ADhzVESrpNfZMn2IATma8g.png" alt=""><figcaption><p>Open a new Maker vault.</p></figcaption></figure>

## What is boost strategy?

Boost Maker vault is a strategy to increase the exposure of a vault collaterals. Some calls this strategy “Leveraged CDP”, “Boost Vault Exposure”, “Increase Vault Exposure”, etc. Just think of this strategy as boosting both your collateral and your debt at the same time. When your collateral increases, you get to generate more DAI. Then you use those DAI to buy more collateral and send back to your vault. Your collateral increases again! So you generate more DAI again, buy more collateral… and repeat. Overall, the approach is to multiply the exposure of the collateral asset to profit from price surges without any upfront capitals.

## How to build this strategy?

There are three ways of building this strategy:

* Basic level: You build it manually by simply using your current vault position.
* Advanced level: You use flashloan to create higher exposure.
* Pro level: Skip building. Just use Furucombo’s latest feature on the [Explore Page](https://furucombo.app/explore/combo\_maker\_00003).

Below, we’ll take you through how these three approaches work using ETH as collateral as example.

### **1) Basic level: Build manually**

```
Step 1: Generate DAI from the Maker vault
Step 2: Use the DAI generated to buy collateral
Step 3: Deposit the newly bought collateral back into the vault
Step 4: Repeat 1–3 till achieving the target collateralized ratio
```

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*hEHS5GemQrtq0XKb84kMwQ.png" alt=""><figcaption><p>Build manually to boost Maker vault</p></figcaption></figure>

### **2) Advanced Level: Build Manually with Flashloan**

Same approach as the basic level, but using Flashlaon to borrow DAI and swap them to collateral all at once. Hence, you only need to calculate the total of DAI that you can generate from the vault and the amount of collateral you can purchase using the DAI generated.

```
Step 1: Borrow ETH from flashloan
Step 2: Deposit ETH to Maker vault to increase the borrowing limit
Step 3: Generate DAI from the vault
Step 4: Swap DAI to ETH 
Step 5: Repay Flashloan with fee
```

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*DmktJP1koqPi1YOtTcW9og.png" alt=""><figcaption><p>Build Manually with Flashloan to boost Maker vault</p></figcaption></figure>

### **3) Pro Level: Skip building**

Furucombo has simplified the advanced way into a [setup form](https://furucombo.app/explore/combo\_maker\_00003). Thus, you can boost your vault with ease by selecting the vault number you want to leverage the position and entering the amount of debt you want to generate. In the setup form, you can also clearly see the vault’s before-and-after change.

```
Step 1: Select vault number
Step 2: Enter the amount of DAI you want to generate
Step 3: Approve & Send the transaction
```

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*TzwAPc0OA_N400yZ2lKowQ.png" alt=""><figcaption><p>Pro Level: Skip building</p></figcaption></figure>

* Use the Boost Setup form [here](https://furucombo.app/explore/combo\_maker\_00003)
* Other useful resource: [Maker Boost calculator sheet](https://go.furucombo.app/l8oLh)

***

> 🎉 Bravo! You’ve leveraged your collateral’s position. Don’t forget to share your result on Twitter. 🎉

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*fdpwHpSa-wOpSY88Vy14BQ.gif" alt=""><figcaption></figcaption></figure>

## Contact us

If you experience issues that are not covered in this guide, please reach out to the team directly through telegram.

* Discord: [discord.furucombo.app](https://discord.furucombo.app/)
* Twitter: [@furucombo](https://twitter.com/furucombo)
* Recommend Read: [Beginner’s guide to Furucombo](https://tutorial.furucombo.app/getting-started/beginners-guide)

\
