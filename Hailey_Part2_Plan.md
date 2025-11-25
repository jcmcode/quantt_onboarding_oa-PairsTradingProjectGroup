## 1. Define the Stock Universe
Select a broad but manageable set of tickers.
- Compile 200–500 symbols from major indices (e.g., S&P 500), sector ETFs, commodities, and thematic areas (EVs, semiconductors, renewable energy).
- Ensure variety to allow discovery of non-obvious relationships.

---

## 2. Generate Candidate Pairs
Use methods to narrow down which pairs are worth testing.
- Apply clustering (K-Means or hierarchical) to group related stocks.
- Use PCA to compare stocks based on factor exposures.
- Optionally apply simple filters such as sector grouping or correlation thresholds.
- This results in a candidate list of ticker pairs for detailed analysis.

---

## 3. Run Statistical Tests
Evaluate which candidate pairs have characteristics suitable for pairs trading.
- Test cointegration (Engle–Granger or Johansen).
- Apply our existing algorithm from Part 1 to compute hedge ratio, spread, and z-scores.
- Apply volatility adjustments based on feedback (e.g., normalize each leg by volatility or ATR).
- Check for structural breaks or regime shifts to ensure the relationship is persistent over time.
- Should be left with a validated set of pairs that are both statistically sound and compatible with our trading logic.

---

## 4. Historical Validation
Ensure the pair relationship is not recent or unstable.
- Test selected pairs using data going back to the early 2000s.
- Check whether the relationship persists across different market regimes.
- Prioritize pairs with long-term consistency.

---

## 5. Scoring Framework
Develop a method to rank pairs.
- Cointegration test results.
- Half-life of mean reversion.
- Spread volatility.
- Stability of hedge ratio.
- Basic profitability based on a simple spread-based trading rule.
- Should be left with a ranked list of pairs selected for further testing.