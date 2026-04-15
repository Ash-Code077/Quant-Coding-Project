# Model Equations

## 1. Sentiment Signal(WIP_Focus)

S_sentimental represents aggregated market sentiment derived from external sources.

Initial concept:
$S_{sentimental} = \sigma(x)[Z(C_r) + \log(A_w/A_{adj}) + F_m + N_{sold}/\bar{H}]$

Where:
- $\sigma(x)$: risk-adjusted sigmoid function
- $C_r$: geopolitical/conflict factor
- $A_w / A_{adj}$: normalized rating ratio across sources
- $F_m$: mean sentiment score (NLP-based)
- $N_{sold}$: insider selling activity
- $\bar{H}$: estimated holdings baseline
- Z: Z score

---

## 2. Structural Volatility Signal(WIP)

Goal: Capture the *shape* of price movement rather than just magnitude.

### Feature 1: Path Complexity

$structure_{score} = path_{length} / displacement$

Where:
- $path_{length}$ = Σ |returns|
- displacement = |Σ returns|

Interpretation:
- ≈ 1 → smooth trend
- \>\> 1 → chaotic movement

---

### Feature 2: Directional Instability

$sign_{changes}$ = number of sign flips in returns

---

### Combined Structural Signal

$$
S_{mathematical} = w_a * structure_{score} + w_b * sign_{changes}
$$
---

## 3. Final Model

$S_{final} = w1 * S_{sentimental} + w2 * S_{mathematical}$

---

## 4. Regime Hypothesis

If $S_mathematical$ is high (chaotic):
→ sentiment dominates

If $S_mathematical$ is low (trending):
→ momentum/structure dominates

---

## Notes

This framework is iterative and subject to refinement based on empirical results.
