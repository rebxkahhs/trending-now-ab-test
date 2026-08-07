# Project Limitations

## 1. Synthetic Experiment Data

This project uses a synthetic A/B testing layer built on top of an e-commerce behavioral dataset.

The underlying dataset provides realistic customer, product, campaign, and interaction data. However, the "Trending Now" treatment assignment is simulated to represent how a real product-card experiment could be designed.

Because the treatment was not deployed on a live website, the estimated impact should be interpreted as an experimental simulation rather than a measured business outcome.

---

## 2. Synthetic Treatment Assignment Assumptions

In a real A/B test, treatment assignment would occur through an experimentation platform that randomly assigns eligible users to treatment and control groups.

This project simulates randomized assignment to create a controlled comparison.

The validity of the experiment depends on the assumption that:

- Treatment assignment is independent of customer characteristics
- Treatment and control groups are comparable
- The simulated treatment effect represents a realistic business scenario

---

## 3. Simulated Treatment Effect

The synthetic data generation process includes assumptions about the expected impact of the "Trending Now" callout.

These assumptions are documented separately in:
data/synthetic/generation_parameters.yaml

The purpose of these assumptions is not to prove that the callout works, but to create a realistic environment for demonstrating experiment design, statistical testing, and business decision-making.

---

## 4. External Validity

Results from this analysis should not be directly interpreted as the expected impact of implementing a "Trending Now" callout in a real production environment.

Actual results may differ due to:

- Brand awareness
- Customer demographics
- Competitive environment
- Product assortment
- Website design
- Seasonality
- Pricing strategy
- Marketing campaigns

A real business implementation would require a live controlled experiment.

---

## 5. Product Selection Bias

Products eligible for a "Trending Now" designation may differ systematically from other products.

For example:

- Higher popularity products may already receive more engagement
- Certain categories may naturally have higher conversion rates
- Inventory levels may influence merchandising decisions

The experiment design attempts to isolate the effect of the callout itself by assigning treatment at the exposure level.

---

## 6. Segment Analysis Limitations

Segment-level analysis is useful for identifying differences in treatment effects, but smaller segments may not have enough observations to produce reliable conclusions.

Segment findings should be interpreted carefully, especially when:

- Sample sizes are small
- Multiple segments are evaluated
- Results are exploratory rather than pre-specified

---

## 7. Business Decision Limitations

A statistically significant result does not automatically guarantee business value.

A final rollout decision should also consider:

- Incremental revenue impact
- Implementation cost
- Customer experience impact
- Long-term purchasing behavior
- Potential effects on other products

This analysis focuses primarily on customer engagement and conversion behavior.

