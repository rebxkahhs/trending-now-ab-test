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

