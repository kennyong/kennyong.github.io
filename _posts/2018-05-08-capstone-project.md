---
layout: post
categories: posts
title: Trading Cryptocurrencies with Time Series and Prophet
tags: [#crypto]
date-string: May 8, 2018
---

Disclaimer:
The following content is intended for educational purpose only. Please check with your authorised broker for advice.
Cryptos speculation is also not advised.

# Trading Cryptocurrencies with Correlation, Time Series and Prophet

### Problem Statement

Can we make money from trading cryptocurrencies with Time Series and Prophet?

### Success Metrics

* Quickly predict trends
* Predict possible entry price and exit price

### Battle Of The Cryptos With Two Trading Strategies

* To apply a **"Hedging Strategy"** (for risk adverse investors), using **Correlation**.
This strategy involves buying a pair of cryptos: the first crypto at larger proportion which is going in an upward direction, and a second crypto at a lower proportion which is going in an opposite direction. The rationale for this strategy, though not intuitive, is used to hedge against a sudden correction. In a rare event of a drop of 40% in value in a single day trade, which was recorded, the second crypto should be moving in the opposite ie, upward, direction in order to reduce the losses in the first crypto. Therefore, such a strategy might appeal to a risk adverse investor.

* To apply a **"Buy Low Sell High"** strategy using **Prophet**.
The most straightforward strategy in trading.

### Cryptocurrencies Used for Comparison

* Bitcoin (BTC)
* Ethereum (ETH)
* Bitcoin Cash (BCH)
* Ripple (XRP)
* Stella (STRC)
* Litecoin (LTC)
* Ethereum  Classic (ETC)
* Dash (Dash)

#### Source of Data: 
https//poloniex.com

#### Firstly, some basic EDA on the various cryptocurrencies for our first trading strategy: **Hedging**

![crypto-price-image](/images/Image/Cryptocurrencies Price (2-hours) without Normalization.png){:class="img-responsive"}

As can be seen, the various cryptocurrencies are trading at different price range.

#### Normalising Price

We can see the fluctuations of the prices at the same scale after they are normalised, using MinMax Scaler.

![crypto-price-normalised-image](/images/Image/Cryptocurrencies Price (2-hours) after Normalization.png){:class="img-responsive"}

#### Heatmap to find Correlation of the various Cryptos

From the normalised prices, the prices of the various cryptos seem to be moving in a correlated manner. However, a correlated strategy 
would not work for a "Hedging Strategy". To prove that the cryptos are indeed correlated, we will use the heatmap.

#### Pointers

* Correlation can range between -1 to 1
* Correlation > 0 indicates that the cryptos used in comparison are positively correlated, and vice versa if correlation < 0.
* If a pair of cryptos have the same magnitude of value but in opposite signs, the net effect becomes 0 (which is as good as not investing)
* For "Hedging Strategy" to work sufficiently, I will set the first crypto (main crypto which we want to make money with, in my example, Ethereum (ETH). The correlation of the second crypto, as compared to ETH, should be within the range between -0.5 to 0, so that the opposite movements of this pair of cryptos will not be cancelled fully.

![crypto-heatmap-image](/images/Image/Correlation of ETH and other Crypto.png){:class="img-responsive"}

#### Conclusion in using Heatmap to see the effectiveness of a "Hedging Strategy"

From the heatmap, we can see that the correlation of the the cryptos (against ETH), ranges between 0.68 to 0.96. This means that none of the cryptos are moving in the opposite direction of ETH. We can also deduce that the cryptos are highly correlated (positively) to ETH since that they are more than 0.5.

My first conclusion is, "Hedging Strategy" is not recommended for cryptocurrencies in general. 

My second conclusion is, instead of diversifying the investment among the various cryptos, we might want to focus only on one which yields the highest return (in other words, it is a very high risk investment).
