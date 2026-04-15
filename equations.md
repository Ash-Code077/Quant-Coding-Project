# Model Equations

## 1. Sentiment Signal(WIP_Focus)

S_sentimental represents aggregated market sentiment derived from external sources.

Initial concept:
$S_{sentimental} = \sigma(x)[Z(C_r) + \log(A_w/A_{adj}) + F_m + N_{sold}/\bar{H}]$

Where:
- $\sigma(x)$: risk-adjusted sigmoid function
- $C_r$: geopolitical/conflict factor
- $A_w / A_adj$: normalized rating ratio across sources
- $F_m$: mean sentiment score (NLP-based)
- $N_sold$: insider selling activity
- $\bar{H}$: estimated holdings baseline
- Z: Z score

---

## 2. Structural Volatility Signal(WIP)

Goal: Capture the *shape* of price movement rather than just magnitude.

### Feature 1: Path Complexity

structure_score = path_length / displacement

Where:
- path_length = Σ |returns|
- displacement = |Σ returns|

Interpretation:
- ≈ 1 → smooth trend
- >> 1 → chaotic movement

---

### Feature 2: Directional Instability

sign_changes = number of sign flips in returns

---

### Combined Structural Signal

S_mathematical = w_a * structure_score + w_b * sign_changes

---

## 3. Final Model

S_final = w1 * S_sentimental + w2 * S_mathematical

---

## 4. Regime Hypothesis

If S_mathematical is high (chaotic):
→ sentiment dominates

If S_mathematical is low (trending):
→ momentum/structure dominates

---

## Notes

This framework is iterative and subject to refinement based on empirical results.
