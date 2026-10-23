# PRD: Pre-visit beauty profile, so the advisor arrives with the right kit

**Problem.** A Wingit visit only works if the advisor brings products that suit this customer. Today the kit is
decided with little information about the customer's skin, tone, concerns and budget, so some of every kit is
wasted, visits convert less than they could, and advisors spend time on products the customer would never buy.
Every low-converting visit costs advisor time, travel and kit.

**Evidence.**
- Category pain: customers can't judge shade online and can't return opened products (category teardown).
- Wingit's own promise is personalised discovery (Peak XV Surge profile); the visit is where that promise is kept.

**Users.**
- Customers booking their first visit (main focus), and returning customers booking again.
- Advisors preparing a kit before each visit.

**Solution (v1).**
1. **Profile at booking (under 90 seconds):** skin type, skin concerns, undertone (with a simple visual guide),
   favourite products today, occasion (everyday, office, wedding), budget range. Optional: one natural-light selfie.
2. **Kit recommendation for the advisor:** rules plus an LLM rank products from current stock into a 12-15 item
   kit with a one-line reason each ("dry skin + warm undertone: hydrating foundation in shades 3-4").
   The advisor can edit the kit; the recommendation is a starting point, not a decision.
3. **After the visit:** the advisor logs what was tried, kept and rejected (with reason). This builds each
   customer's beauty profile for reorders and trains better kit recommendations.

*Out of scope for v1:* automatic shade matching from the selfie, customer-facing recommendations in the app,
virtual try-on.

**Success metric.** Revenue per visit.
**Supporting metrics.** Kit hit rate (items bought ÷ items tried); first-visit conversion; repeat booking within 60 days.
**Counter-metrics.** Booking completion rate (the profile must not scare customers off); advisor prep time;
stock tied up in kits; customer complaints about recommendations.

**Experiment and rollout.**
- Randomise by booking for 4-6 weeks in Gurugram: half of advisors' visits use the profile and recommended kit,
  half use the current process. Balance by advisor so advisor skill doesn't decide the result.
- Decision rule: ship if revenue per visit rises meaningfully with booking completion down by no more than
  2 points. Set the exact thresholds once the current revenue per visit and its variability are known.

**Risks and open questions.**
- **Privacy:** selfies and skin data are personal data; collect only with clear consent, keep them optional,
  and follow India's data protection law (DPDP Act).
- **Bias:** shade and undertone guidance must work across Indian skin tones; validate with advisors on a
  diverse set of customers before trusting any automated suggestion.
- **Cold start:** with little purchase history at launch, start with advisor-written rules and add the LLM
  ranking as visit data accumulates.
- Baselines needed: current revenue per visit, kit size, and share of kit items that get tried and bought.
