---
description: What’s a flash loan, and how do you do a flash loan with no coding?
---

# Flashloan Combo

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*TL8j_UTbbMcQQiNs" alt=""><figcaption><p>Tutorial | Flashloan combo</p></figcaption></figure>

## Contents

* [What is Flashloan?](flashloan-combo.md#what-is-flashloan)
* [What are Flash Loans used for?](flashloan-combo.md#what-are-flash-loans-used-for)
* [How do I use a Flash Loan?](flashloan-combo.md#how-do-i-use-a-flash-loan)

## **What is Flashloan?**

Flash Loans are introduced by the [Aave](https://app.aave.com/home), an open-source lending protocol for anyone to deposit and borrow cryptographic assets. Essentially, flashloans let users borrow any amount up to the total liquidity available without any collateral, so long as the loan is repaid in the same transaction. If the loan is not repaid, the whole transaction will be reverted. With flashloan, anyone can access a massive amount of liquidity, and use the loan with other protocols however they want. You can become a ‘whale’ without any capital.

At the time of writing, there are three pools providing flashloans:

* **Aave:** 17 tokens available with 0.09% fee
* **dYdX:** 3 tokens available zero fee \*
* **Uniswap V2:** 100+ tokens available with 0.3% fee

```
* Note that flashloan on dydx is not a consumer feature. It is achieved by developers chaining Withdraw, Call and Deposit actions.
```

## What are Flash Loans used for?

So, flashloan sounds like a very good deal. What exactly can you use it for? [Marc Zeller](https://twitter.com/lemiscate) from Aave has written a very nice piece demonstrating some of the top use cases for flashloan.

[**Sneak peek at Flash Loans**\
_Aave protocol launched a bit less than a month ago and is already gaining traction with a bit more than 11M$ in…_medium.com](https://medium.com/aave/sneak-peek-at-flash-loans-f2b28a394d62)

We summarize the use cases:

* Arbitrage trades
* Collateral swap
* Self-hedging
* Self-liquidation
* (Debt) Interest rate swap
* (Debt) Curreny swap

The most popular use case by far is _**Arbitrage trades**_. For those unfamiliar, arbitrage is the strategy of making a profit from price differences between different markets. To make a significant amount of profit, you will need substantial capital to get started. And this, is where the magic happens — We use flashloan to generate free money with no upfront cost.

## How do I use a Flash Loan?

### **Before we get started**

There are some important things to understand:

> For arbitrage traders, Furucombo lowers the barriers-to-entry for building money legos, providing all the necessary elements to create arbitrage strategies including the so far coder-only flashloans. But, please keep in mind that Furucombo does _**NOT**_ find arbitrage opportunities for you. You will have to find it yourself. ✊🏻

Enough with the disclaimer. Let’s get to the checklist. 👇🏻

```
1️⃣ Find an arbitrage opportunity >0.09% to cover flashloan's fee
2️⃣ Have some ETH in your wallet enough to pay for gas
```

On Furucombo, there are two pools supported, Uniswap (V1) and Kyberswap. The example we use in the following is an arbitrage opportunity found between KyberSwap and Uniswap V1 a few months ago.

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*Y1JOUlV7boLecbi9YRmpBA.png" alt=""><figcaption></figcaption></figure>

<pre><code>Rate difference: 20+%
1 DAI = 0.9927 sUSD on Kyberswap
1 DAI = 0.8057 sUSD on Uniswap
<strong>👉🏻 Buy low sell high: Buy sUSD on Uniswap and sell it on Kyberswap
</strong></code></pre>

Now you found the rate difference, let’s start creating the combo. The complete combo should look like this:

```
1️⃣ Borrow 100DAI from Flashloan
2️⃣ Swap 100DAI to 122.83649sUSD on Uniswap
3️⃣ Swap 122.83649sUSD to 122.83429DAI on Kyberswap
4️⃣ Repay 100.09DAI to Flashloan
5️⃣ You keep 22.74429DAI profit.
```

## **Step by step**

### 1. Go to [Furucombo](https://furucombo.app/)

### 2. Add a Uniswap cube

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*8l3EqTp3Tk4D9v8OS4ceuA.png" alt=""><figcaption></figcaption></figure>

```
1️⃣ Click the cube with '+' symbol 
2️⃣ Choose 'Swap Token' under Uniswap section
3️⃣ Enter Input: 100DAI
4️⃣ Output generated from Uniswap: 122.83649sUSD
5️⃣ Click 'Set'
```

### 3. Add a Kyberswap cube

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*e-v-jWbGEs_-znXgxybVKA.png" alt=""><figcaption></figcaption></figure>

```
1️⃣ Click the cube with '+' symbol 
2️⃣ Choose 'Swap Token' under Kyberswap section
3️⃣ Enter Input: 122.83649 sUSD
4️⃣ Output generated from Kyberswap: 122.83429 DAI
5️⃣ Click 'Set'
```

<pre data-overflow="wrap"><code><strong>💡 Tips: If your input is according to the previous cube's output, enter slightly lower amount instead of the exact amount. This way, you can avoid combo failure due to rate difference. 
</strong></code></pre>

### 4. Add Flashloan cube

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*F_b0egiieYC7ddH68hiDJw.png" alt=""><figcaption></figcaption></figure>

```
1️⃣ Click the cube with '+' symbol 
2️⃣ Choose 'flashloan' under Aave section
3️⃣ Enter amount: 100DAI
4️⃣ Click 'Set'
5️⃣ Two cubes appear. 1st cube is borrow 100DAI and 2nd cube is payback 100.09DAI.
```

### 5. Drag flashloan’s 1st cube to the top

{% code overflow="wrap" %}
```
This is simply adjusting the execution order. You want to borrow from flashloan at the very beginning to have the upfront capital. So, just click and drag the borrow cube to the top and keep the payback cube at the bottom.
```
{% endcode %}

{% code overflow="wrap" %}
```
The final combo would look like...
```
{% endcode %}

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*xJR5X5GnVNelOFB6GlKBvA.png" alt=""><figcaption></figcaption></figure>

### 6. Connect wallet

### 7. Send out

> 🎉 Bravo! You’ve made money with zero captial. _Don’t forget to share your result on Twitter._ 🎉

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*Kfym6hUWLOi4tXxA" alt=""><figcaption></figcaption></figure>

#### Contact us

If you experience issues that are not covered in this guide, please reach out to the team directly through telegram.

* Discord: [discord.furucombo.app](https://discord.furucombo.app/)
* Twitter: [@furucombo](https://twitter.com/furucombo)
* Recommend Read: [Beginner’s guide to Furucombo](https://tutorial.furucombo.app/getting-started/beginners-guide)

\
