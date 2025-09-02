# Acquired-Stock-Tracker
An in depth look at the companies covered by Acquired, a podcast by Ben Gilbert and David Rosenthal, https://www.acquired.fm/

Objective:
I want to look at the standalone companies traded on public exchanges that have been covered in an acquired episode. I have two focal points in mind:
How good is Acquired as a stock picker
Total lifetime return if bought and held on episode release date
Comparison to common indexes
Best and worst performers
Does an episode release have an effect on a companies trading
Change in stock price 1,5,30 days post episode release
Account for change in indexes as well to standardize

Data:
Using https://www.acquired.fm/episodes to find the companies, and release date. Ticker for each company found online.

Using googlefinance() to pull current and historical stock data.

Metrics:
For company/index:
Stock Price
At release
+1 day
+5 days
+30 days
Current
Change in price
Release to +1
Release to +5
Release to +30
Release to Current
Current value of $100 invested at release date

For Acquired:
Top 3 performers
Bottom 3 performers
Total value of $100 invested in every stock
Lifetime return





Summary:

Objective:
My objective for this project was to investigate the stock prices of the companies covered in Acquired, one of my favorite podcasts that goes in-depth into the history and strategy of companies. I have always wondered if, considering their pension for covering successful companies and their now sizable audience (currently 3rd on Spotify’s Technology Podcast chart), the release of an episode had any effect on the stock price of the company. To answer this and a few other more general questions I began to dig into the data.

Methodology:
Initially I had to compile a list of the companies I should and could include. I only included standalone companies trading on public exchanges both today and near the episode’s release date. Additionally I decided to only look at companies whose episodes were about the company’s story from founding, their public listing event, or a merger that defines the current business. Once I had this list compiled, and the associated ticker symbols, I began to list the metrics I wanted to compute.

My main focus was on the statistical significance of a stock’s abnormal returns vs the S&P 500 after the release of an episode, but additionally I wanted to take a look at the portfolio as a whole and some general trends.

Abnormal Returns Significance:
To determine the statistical significance of the abnormal returns I looked at the stock price 1, 5, and 30 days post-release as well as the current stock price. I then compared these values to the price of the S&P during the same windows of time.

Results:
+1 day: Mean abnormal +0.21% (SD 2.60%), t = 0.57, p = 0.57, 95% CI [−0.52%, +0.94%] →These results indicate no evidence of a next-day effect.


+5 days: Mean abnormal ≈ 0.00% (SD 5.91%), t ≈ 0.00, p ≈ 0.997, 95% CI [−1.66%, +1.67%] → These results indicate there is essentially no 5-day effect.


+30 days: Mean abnormal −2.15% (SD 11.75%), t = −1.31, p = 0.20, 95% CI [−5.45%, +1.16%] → These results indicate the 30-day change is directionally negative but not statistically significant.


Release-to-date vs S&P: Mean abnormal +12.65% with very high dispersion (SD 236%), t = 0.38, p = 0.70, CI [−53.76%, +79.06%] →These results are not distinguishable from zero; outcomes are dominated by a few outsized winners.

After digging into the data, it is apparent that the release of an Acquired episode has no statistically significant effect on the company’s stock price. This result is far from surprising given the astronomically complex relationships that govern stock prices.

General Trends in Portfolio:
While the results of the abnormal returns analysis provide us with no strong correlation to hang out hat on, I was still interested in which companies performed the best, which performed the worst, and how well your portfolio would have done if you had invested in each company post-release vs the S&P post-release.

Results:
Top short-term movers:
 +1d: Meituan, Dropbox, Virgin Galactic.
 +5d: Virgin Galactic, Pinterest, Shopify.
 +30d: Bitcoin, Shopify, Novo Nordisk.


Bottom short-term movers:
 +1d: Peloton, Ethereum, Stitch Fix.
 +5d: Doordash, Airbnb, Peloton.
 +30d: Peloton, Nvidia, Sonos.

Long-run since release:
 Leaders: Tesla, Nvidia, Facebook.
 Laggards: Virgin Galactic, Peloton, Lyft.

Investing $1000 into each company at episode release grows $51,000 → $155,254 (+204% total, +$104,255 profit)
Investing $1000 into the S&P at each episode release grows $51,000 → $148,801 (+192% total, +$97,801 profit)

Again, these results are in no way statistically significant, but they provide an interesting narrative. The top short-term movers include none of the long-run leaders, but they do include Virgin Galactic, the overall largest laggard with a price decrease of 99.34% from episode release to current day ($466.2 to $3.11). Of the lowest short-term movers Peloton is a constant, even ending as the second worst performing stock, only behind Virgin Galactic. Lastly, the thought experiment of investing in each episode concludes in a slightly more positive total than if you were to invest solely in the S&P, but again these results show the lack of significance the release of an episode has on a stock’s performance.

Overall, while the results lacked any statistical significance, it has been interesting to take a deeper look into the history of such an entertaining and educating podcast and the companies I have learned so much about.
