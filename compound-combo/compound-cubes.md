# Compound Cubes



<figure><img src="https://cdn-images-1.medium.com/max/1440/1*sToqNsNE5Duwf_KQ6xZVXA.png" alt=""><figcaption><p>Compound Cubes</p></figcaption></figure>

One of the top use cases on Furucombo is to manage the DeFi portfolio among lending services, as the composability is beyond comparison.

With the launch of the long-awaited Compound borrow cube, we have pushed the flexibility to the next level. You can now do whatever you want with your Compound position on Furucombo.

Here we would like to recap the most used Compound combos in 2020, introduce the newly released Compound smart borrow cubes, and share the new combos you can make with the latest release.

## Content:

* ****[**Most used Compound combos in 2020**](compound-cubes.md#most-used-compound-combos-in-2020)****
* ****[**What are Compound smart cubes?**](compound-cubes.md#what-are-compound-smart-cubes)****
* ****[**New Compound combos with smart cubes**](compound-cubes.md#new-compound-combos-with-smart-cubes)****

## Most used Compound combos in 2020

### **1. Self-Liquidation Combo (**[Shortcut](https://furucombo.app/combo/c0ga39145c7c72kf03qg?refreshPrice=1))

* **😮 What:** To close Compound debt position without any upfront funds.
* **🕗 When:** When your collateral ratio is in danger.
* 🤔 **How:** It will use your collateral to pay off ALL the debts on Compound powered by flashloan.

### **2. cToken Swap Combo (**[Shortcut](https://furucombo.app/explore/combo\_compound\_00001))

* **😮 What:** To swap cToken with ease
* **🕗 When:** Whenever you want to change cToken position, for higher APY or for other purposes.
* 🤔 **How:** It will withdraw and swap the original ctoken, and then supply the new token to Compound. We even have a super combo to further simplify the process.

***

## What are Compound smart cubes?

The smart cubes are advanced features on Furucombo and only users with a DSProxy smart wallet can use them. You can easily create a DSProxy smart wallet on Furucombo within 3 transactions, and you can skip 1 of them if you have ever created a vault on Maker or a smart wallet on DeFi Saver.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*swwmMmF5NBoK2WRL" alt=""><figcaption><p>Smart wallet setup</p></figcaption></figure>

Okay, so why do we need a smart wallet to use Compound borrow cube? Because if we don’t, when people using Furucombo to create collateral-and-debt positions on Compound, all positions would be mixed together as Compound protocol could only see it as 1 smart contract’s position, which is the Furucombo proxy contract. But with the smart wallet structure, users’ individual positions will be recorded under each smart wallet, and could be controlled only by the owner of the smart wallet. The related smart contract has been audited by Haechi with zero critical issues found. Check the report here [https://docs.furucombo.app/resources/audit](https://docs.furucombo.app/resources/audit)

Once you create the smart wallet and create your Compound collateral-and-debt position, you would see a dashboard for the position in the wallet tab, and you could then use the Compound smart cubes to manage the position.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*8zhkjxH6zYXzq70v" alt=""><figcaption><p>Compound smart wallet dashboard</p></figcaption></figure>

Reminder: The Compound collateral-and-debt position is manageable under both Furucombo and DeFi Saver as we share the same DSProxy structure.

***

## New Compound combos with smart cubes

### **1. Supply to borrow combo**

* **😮 What:** To create a debt position on Compound.
* **🕗 When:** Whenever you like.
* 🤔 **How:** Supply tokens with your own wallet, then do the borrow with your smart wallet.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*NgWisCTmiMuevnR6" alt=""><figcaption><p>Compound Smart Borrow</p></figcaption></figure>

### **2. Debt swap combo (**[Shortcut](https://furucombo.app/combo/c0gf2nhmvubc72hld9rg?refreshPrice=1))

* **😮 What:** To swap debt token with ease
* **🕗 When:** Whenever you want to change debt position, for lower borrow APY or for other purposes.
* 🤔 **How:** Use the flash borrowed tokens to repay the debt, then borrow new debt to pay back the flashloan.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*Za11VHA1MNvv0LGM" alt=""><figcaption><p>Debt swap combo</p></figcaption></figure>

### **3. Collateral swap combo (**[Shortcut](https://furucombo.app/combo/c0gf3l3gbu8c71g6sn80?refreshPrice=1))

* **😮 What:** To swap your collateral with ease
* **🕗 When:** Whenever you want to change the collateral position, for higher lending APY or for other purposes.
* 🤔 **How:** Use the flash borrowed tokens to supply into your smart wallet and further decrease the utilization rate, then withdraw the released collateral to pay back the flashloan.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*Jq7laHASIwfWidom" alt=""><figcaption><p>Collateral swap combo</p></figcaption></figure>

### **4. Self-liquidation combo for the smart wallet position (**[Shortcut](https://furucombo.app/combo/c0gf493gbu8c71g6sn9g?refreshPrice=1))

* **😮 What:** To close Compound debt position without any upfront funds.
* **🕗 When:** When your collateral ratio is in danger.
* 🤔 **How:** It will use your collateral to pay off ALL the debts on Compound powered by flashloan.

<figure><img src="https://cdn-images-1.medium.com/max/1440/0*7ebQl6ZrVzEAJPiP" alt=""><figcaption><p>Self-liquidation combo for the smart wallet position</p></figcaption></figure>

***

**Is this all? Of course not!**

There are so many other combos you can create with the newly released borrow features! For example… you can now borrow money from Compound to join farming, and you can move your collateral-and-debt position between Compound and Maker easily with flashloan.

> **🎉 Bravo! You are the Compound pro now! Go make your own combo to maximize your position with ease! 🎉**

<figure><img src="https://cdn-images-1.medium.com/max/1440/1*BMygie7AS4jRa3CUnJwNlg.gif" alt=""><figcaption></figcaption></figure>

#### Contact us

If you experience issues that are not covered in this guide, please reach out to the team directly on discord.

* Discord: [discord.furucombo.app](https://discord.furucombo.app/)
* Twitter: [@furucombo](https://twitter.com/furucombo)
* Recommend Read: [Beginner’s guide to Furucombo](https://medium.com/furucombo/beginners-guide-to-furucombo-747862e7ef55)\
