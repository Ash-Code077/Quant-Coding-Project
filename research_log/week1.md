# Week 1 Research Log

## Hypothesis

Negative price movements are more strongly influenced by sentiment than by structural variables such as volume or short interest.

---

## Problem

Initial formulation using derivatives (dP/dS) is difficult to implement with discrete data.

---

## Refinement

Reframed into testable hypothesis:

Sentiment should have stronger predictive power for short-term negative returns than structural variables.

---

## New Direction

Instead of comparing sentiment vs structure directly, explore:

Market behavior depends on regime:
- Chaotic → sentiment-driven
- Trending → structure-driven

---

## Key Insight

Structural volatility may determine *when* sentiment matters.

---

## Next Steps

- Define structural volatility metric
- Implement in Python
- Test against future returns
- Implement ML into factors such as $C_r$ for faster and more general application
- TBD
