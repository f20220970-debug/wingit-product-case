# Wingit: category teardown and PRD

A product case for **Wingit**, an at-home beauty concierge (try premium beauty at home with an advisor, pay only
for what you keep).

- **[Category teardown](docs/category_teardown.md):** how premium customers buy beauty in India today, where it
  breaks (shade mismatch, counterfeits, refused returns), what an at-home concierge fixes, where the model will
  strain, and the metrics to own.
- **[PRD: pre-visit beauty profile](docs/prd_pre_visit_beauty_profile.md):** a 90-second profile at booking that
  lets the advisor arrive with the right kit, with an AI-assisted kit recommendation, success and counter-metrics,
  a randomised rollout and privacy and bias safeguards.

- **[Unit-economics model](model/at_home_trial_unit_economics.xlsx):** a formula-driven Excel model of an at-home
  try-and-buy visit: revenue, gross profit, advisor, travel, testers and shrinkage per visit → contribution per visit,
  break-even visits per advisor per day, contribution per customer (visits + app reorders), CAC payback, with bear /
  base / bull scenarios and two sensitivity grids.

## What the model shows (illustrative assumptions, not Wingit data)
- In the base case the visit itself only just breaks even: about ₹43 contribution on ₹3,300 revenue per visit,
  with break-even at about 3.6 visits per advisor per day.
- About 92% of a customer's yearly contribution comes from **app reorders** of products discovered on the visit,
  so the visit works best as discovery and acquisition, and visit-free replenishment carries the profit.
- The biggest levers: visits per advisor per day (route density), visit conversion, and items bought per visit;
  the kit-personalisation PRD targets the last two directly.

Built from public sources (funding coverage, a national consumer survey, customer reviews); every figure is cited.
