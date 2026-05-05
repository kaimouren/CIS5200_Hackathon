# The MJRTY Effect — A Model of Structural Bias in Online Ratings

**CIS 5020: Critical Analysis of Algorithms · Final Hackathon · Spring 2026 · University of Pennsylvania**

🔗 **[Live demo]([https://your-username.github.io/mjrty-yelp/](https://kaimouren.github.io/CIS5200_Hackathon/))** ← replace with your GitHub Pages URL

---

## What this is

A conceptual simulation — not an empirical claim about any specific platform.

This project demonstrates how a seemingly reasonable filtering and aggregation pipeline can produce systematic bias under certain conditions. Using a model inspired by the Boyer–Moore majority vote (MJRTY) algorithm, it shows how minority signals can be gradually suppressed, compounded over time, and compressed into a star rating that appears objective but reflects structure, not quality.

The simulation is motivated by published fairness research on review platforms (Duma et al., ICWSM 2025) and Yelp's publicly documented Elite user system.

---

## The argument in four steps

1. **Filter** — if a quality filter concentrates weight in users with correlated preferences, the reviewer pool becomes demographically skewed
2. **Aggregation** — a skewed pool produces a MJRTY-like cancellation effect: majority votes suppress minority appreciation signals, even when underlying quality is equal
3. **Feedback** — lower ratings reduce visibility, which reduces minority reviews next round, which skews the pool further — the bias compounds without correction
4. **Compression** — all three stages collapse into a single number that circulates as ground truth, with the pipeline invisible

**Core insight:** The system does not need to be malicious. It only needs to be uncorrected.

---

## How to run

**Option A — Open directly**
Download `index.html` and open in any browser. No server, no dependencies.

**Option B — GitHub Pages**
1. Fork or clone this repo
2. Settings → Pages → Source: `main` branch, `/ (root)`
3. Live at `https://your-username.github.io/mjrty-yelp/`

---

## Course connections

| Topic | Lectures |
|---|---|
| Boyer-Moore MJRTY streaming majority | 9–10 |
| Online matching fairness, APB scandal | 22–23 |
| Algorithmic legitimacy — Borges' Lottery in Babylon | 24 |

---

## References

- Duma et al. (2025). *Auditing Yelp's Business Ranking and Review Recommendation Through the Lens of Fairness.* ICWSM 2025. https://arxiv.org/abs/2308.02129
- Yelp Trust & Safety. (2025). *Recommendation software.* https://trust.yelp.com/recommendation-software/
- Misra & Gries (1982). *Finding repeated elements.* Science of Computer Programming. (Boyer-Moore MJRTY)
