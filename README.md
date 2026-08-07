# Trending Now A/B Test: Measuring the Impact of a Product Card Callout on Add-to-Cart Rate

## Business Question

An e-commerce retailer has excess inventory for selected products and is evaluating merchandising strategies to increase customer engagement and product movement.

This project evaluates whether adding a **"Trending Now" callout** to a product card increases the likelihood that customers add the product to their cart.

**Business question:**

> Does displaying a "Trending Now" callout on an eligible product card increase customer add-to-cart rate compared with showing the same product without the callout?

---

# Experiment Overview

## Hypothesis

### Null Hypothesis (H₀)

Displaying a "Trending Now" callout has no impact on customer add-to-cart rate.

### Alternative Hypothesis (H₁)

Customers exposed to products with a "Trending Now" callout have a higher add-to-cart rate than customers exposed to products without the callout.

---

# Experiment Design

| Component        | Definition                                         |
| ---------------- | -------------------------------------------------- |
| Product area     | E-commerce product listing/product card            |
| Treatment        | Product card displayed with "Trending Now" callout |
| Control          | Product card displayed without callout             |
| Unit of analysis | Customer-product exposure                          |
| Primary metric   | Add-to-cart rate                                   |
| Guardrail metric | Purchase conversion rate                           |

## Primary Metric

Add-to-cart rate:

```
customers who add product to cart
---------------------------------
customers exposed to product card
```

This metric was selected because it measures customer intent while accounting for differences in product exposure volume.

---

# Data

This project uses a synthetic e-commerce experiment built using an underlying customer, product, campaign, and behavioral dataset.

The original dataset provides realistic:

* customer attributes
* product attributes
* campaign information
* browsing behavior
* add-to-cart events
* purchase events

A synthetic experiment layer is generated to simulate randomized exposure to:

* Treatment: "Trending Now" callout
* Control: No callout

The synthetic experiment design is documented to ensure assumptions are transparent and reproducible.

---

# Analysis Plan

## 1. Data Preparation

* Validate customer, product, and event data
* Identify eligible product exposures
* Construct experiment dataset

## 2. Experiment Design

Define:

* treatment/control assignment
* sample size requirements
* hypothesis
* success metrics

## 3. Power Analysis

Estimate:

* baseline add-to-cart rate
* minimum detectable effect
* required sample size

## 4. Statistical Testing

Primary analysis:

* two-proportion hypothesis test
* confidence intervals
* effect size estimation

## 5. Segment Analysis

Investigate whether results differ by:

* new vs returning customers
* device type
* campaign channel
* product category
* price range

---

# Expected Business Decision

The experiment will inform whether the retailer should:

1. Roll out the "Trending Now" callout broadly.
2. Target the callout to specific customer/product segments.
3. Avoid implementation if the lift is not meaningful.

The final recommendation will consider:

* statistical significance
* practical impact
* segment-level differences
* experiment limitations

---

# Repository Structure

```
data/
notebooks/
src/
outputs/
docs/
```

---

# Key Limitations

* The experiment uses a synthetic treatment assignment rather than a live production A/B test.
* Results demonstrate experimental methodology and decision-making rather than measuring the impact of an actual deployed feature.
* Synthetic assumptions are documented and evaluated for realism.

---

# Tools

Python

Libraries:

* pandas
* numpy
* scipy
* statsmodels
* matplotlib
* seaborn

---

# Author

Rebekah Song

