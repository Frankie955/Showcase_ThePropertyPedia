# ThePropertyPedia

**Live: [www.thepropertypedia.com](https://www.thepropertypedia.com)**

A property calculator that answers two questions about a purchase:

1. **Is the property itself worth owning?** Net cash and real IRR over your holding period.
2. **Is that better than the alternative?** The same money invested elsewhere, compared at the sale date.

It reports what the numbers do. It does not tell anyone what to buy.
Illustrative only, not financial advice.

**See it move**: Choose **How It Works** for an animated walkthrough.

![ThePropertyPedia: does it generate a positive return, and is that return better than the alternative? Two questions, one calculator.](docs/share-card.png)

## What it does

- Four calculators: **live in it**, **rent it out**, **rent it out then live in it**, **live in it then rent it out**
- Inputs for price, deposit, mortgage, running costs, rent, growth rates, inflation, tax and exit costs
- Results in nominal and real (today's money) terms
- Stress test, break-even holding period, cumulative chart and sensitivity tool
- Save and compare scenarios, shareable links, PDF export

## How it is built

- **React (Create React App), no backend.** Every calculation runs in the browser.
- **All financial logic is pure functions**, separate from the UI.
- **One definition per concept.** Each figure has a single source and every screen reads it, so a chart cannot contradict the card beside it.
- Deployed on Vercel.

## Quality and testing

Quality assurance was carried out by Claude (Anthropic's AI assistant) under my direction. Claude audited the calculation engine, the figures shown on screen, the wording and the design, using independent re-derivations, large simulations and adversarial reviews. These found real defects, which were fixed or logged.

A sample of the larger checks:

- **Nearly 15 million** field checks across 80,000 generated scenarios
- **843,286** differential assertions against an independent reference model
- **416,000** metamorphic relation checks
- **52,000** scenarios re-derived as net present value
- **153,144** on-screen figures checked against the reference
- **2,222** regression assertions, run on each change
- **47** findings confirmed in an adversarial review by five independent reviewers; 45 fixed, 2 deferred
- Findings logged and numbered **F1 to F210**, each with a severity and a status

## Source code

The source is kept private. 
