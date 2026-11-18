---
title: Game Licensing Hedge Brief
scenario: game-licensing
llm_used: Claude
type: brief
engagement: fx-hedging
capability: fx-hedging
date: 2026-10-23
revised: 2026-11-18
status: committed
hypothesis: "We expect the forward to leave us with the most dollars if the euro ends below 1.1705, because the forward rate gives us a better rate than the market."
---

## The Exposure

Our company expects to receive 2,600,000 euros in 182 days from a French publisher for game licensing royalties. Since we budget in dollars, what matters is how many USD those euros are worth. The euro amount is fixed, but the dollar amount is not because the dollar exchange rate will fluctuate between now and then.
## What a Bad Move Costs
If the euro falls from $1.12 to $1.07 over the 182 days, we would receive $2,782,000 instead of $2,912,000, leaving us $130,000 short of our budget, which could mean underfunding for necessary company resources, downsizing, or layoffs.
## The Three Hedge Tools
A forward is a contract today where we know exactly what we will get because it locks in the exchange rate for our euros in about 6 months, but the downside is that if the euro gets stronger over that time period, we will not benefit. Our scenario's indicative forward is EURUSD 1.1705, so we would receive $3,043,300 no matter what happens to the euro. 

A money-market hedge lets us borrow euros and convert them to dollars. After the conversion we can then use the dollars to invest at the U.S. rate. When the publisher pays EUR 2,600,000, we use it to repay the euro loan plus interest. The benefit is that it gives the same certainty as a forward. The downside is it is complex and uses up our ability to borrow.

A put option protects us by giving us insurance. The benefit is protection from a fall while we still keep any gain if the euro rises, but the downside is we pay about $50,440 up front regardless.
## What We Are Assuming
We assume a bank will give us a forward or option at a fair price. We assume the French publisher pays in full. We assume that the euros arrive on time in six months. If we had more time, we would test that the French publisher pays in full first. 
## Hypothesis 
We expect the forward to leave us with the most dollars if the euro ends below about 1.1705, because the bank still pays us the higher rate we agreed on. We expect unhedged to win if the euro rises above that, because the forward makes us give up the gain. Today’s spot rate is about 1.12 and the forward is 1.1705, so the forward starts out about 5 cents above spot. The spot rate was from Google, on Oct 30.
## How We Would Know We Were Wrong 
We would be wrong if the model, using the real USD and EUR interest rates, returns either of these results at any end rate between 1.07 and 1.1705:
- the money-market hedge returns more than $3,048,300 (the forward's $3,043,300 plus a $5,000 tolerance), or
- the put option returns more than $3,043,300 after subtracting the $50,440 premium.

Either result would show the forward was not the best choice for EUR 2,600,000 over 182 days.

## Next Steps

Before we recommend anything, we will work through four stages:

- **Stage 2, Specification:** We plan the workbook: inputs (EUR 2,600,000, 182 days, spot, forward, put strike at spot and premium of $0.0194 per EUR, and the USD and EUR interest rates, which we must find), outputs, and the results that would prove us wrong. *Delivers:* a written specification.
- **Stage 3, Build:** We ask an AI to build the workbook, then check every formula ourselves. *Delivers:* a working workbook.
- **Stage 4, Market data:** We replace the scenario numbers with real spot and interest rates. *Delivers:* the model running on real data.
- **Stage 5, Validation:** We check the workbook against our hand calculations ($3,043,300 for the forward, $2,912,000 and $2,782,000 for the unhedged cases, and $50,440 for the put premium) and confirm the money-market result is within $5,000 of the forward. *Delivers:* a reconciliation, then our recommendation.
