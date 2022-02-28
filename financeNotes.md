# HFT - High Frequency Trading

## What the hell is high frequency trading anyways?

    High Frequency Trading - A method of trading that uses powerful computer programs to transact a large number of orders in fractions of a second.

Instead of people making trades within the market, financial firms are taking advantage of a computer's processing capabilities. These clusters of computers are making multiple trades per second. Due to sheer speed of these trades, these firms are able to capitalize on profit-making-opportunities in the market that only last fractions of a second.

---

### **Types of HFT bots:**

***News Bots:***

- These computer trading bots make trades based on the information they gather from the news / online articles / social media posts. 

- These bots will scan the words off these reports, and generate an idea of whether the news is positive or negative. Based off that data the bot will automatically decide on how to trade different types of stock almost instantly before other people have time to react.

***Quant Bots:***

- These bots will consume multiple data points from the stock market and be able to make real-time analysis of the state of the market. The bots will then be able to make multiple small-profit trades that accumulate into massive profit gains per day.

- These bots are the most popular among trading firms.



***Quant-Predator Bots: (Illegal by the way cause stock manipulation, but still interesting regardless)***

- The name is exactly how it sounds... these bots prey on the other quant bots. 

- These bots will try and identify the data points that quant bots are obtaining for their algorithm, and they will send out garbage data<sub>*1*</sub> that will throw off their trades, making them sell/buy and an unprofitable margin. And then these bots will capitalize on their mistakes and profit.

- Example attack algorithms
  - Spoofing: Creating false orders in the market to make a false impression of demand and canceling them a billionth of a second later before they are filled

  - Quote Stuffing: Creating multiple bogus offers that will never get filled, they are just stuffing the market with terrible values to slow down other trading algorithms.

## Downsides of HFT

- The largest downsides I've seen when it comes to HFT is how these bots can negatively impact the actual financial market through technological drawbacks.

Ex: Recursion.

Lets say there's one bot that is purposely selling stocks to drive the price down on stocks that are already within a downtrend. It will eventually buy back in at a lower price and let the price rise up again before profiting.

Now imagine if one bot also managed to see the same opportunity as the other bot, and did the exact same thing it did. It will drive the stock down in price and eventually buy back in at a lower price and let the price rise up again before profiting.

However... these bots would never profit. It would ultimately keep on driving this stock price down unless someone turned these bots off, or there was code to make the bots stop if they realize they are in a recursive loop.

Now these things don't really happen, but it is a warning to show how destructive these bots can be if they happen to malfunction.


        Footnote:

        1 - Y'know fud, but its for robots. 

---

## So you wanna get into HFT's (AKA: Becoming a Quant Developer)

- Develop in C++/Python
- Begin to understand Finance stuff
- Start to understand opportunities in the market, and study what is happening
- Just start trying to make some bots while working on all this

Plus heres some helpful books:

- Option Volatility and Pricing by Sheldon Natenberg

- Dynamic Hedging

- Frequently Asked Questions in Quantitative Finance (Second Edition) by Paul Wilmott

- Python for Data Analysis

- Introduction to Linear Algebra

- Advances in Active Portfolio Management

- Technical Analysis is Mostly Bullshit