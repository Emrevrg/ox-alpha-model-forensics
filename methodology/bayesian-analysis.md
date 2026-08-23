# Bayesian-style analysis

## Reported framing

The reports describe an initial candidate set of eight labs with equal starting weights of 12.5%, followed by sequential evidence updates that lead to an approximately 93% assessment for the Zhipu AI / GLM-5.3-family hypothesis.

## Published update chain

| Step | Evidence | Reported LR | Cumulative assessment |
| ---: | --- | ---: | ---: |
| 0 | Equal prior across eight candidate labs | 1.0 | 12.5% |
| 1 | Server-layer forensics | 5.0 | 42% |
| 2 | 30/30 tokenizer fingerprint | 3.0 | 68% |
| 3 | Video-encoder fingerprint | 1.7 | 78% |
| 4 | Knowledge-cutoff measurement | 1.35 | 83% |
| 5 | Zhipu self-knowledge asymmetry | 1.35 | 87% |
| 6 | International censorship posture | 1.1 | 88% |
| 7 | A/B style isomorphism | 1.7 | 93% |

These are report-assigned likelihood ratios. They are included for transparency and have not been independently calibrated against a benchmark set of known stealth models.

## Interpretation

This value should be read as a structured confidence assignment under the report's assumptions. It is not automatically a statistically calibrated posterior. A defensible calculation must publish:

- the eight hypotheses;
- prior rationale;
- likelihood ratio or update assigned to each evidence item;
- evidence-dependence adjustments;
- sensitivity to alternative priors and likelihoods;
- treatment of an `unknown/other` hypothesis.

## Recommended computation

For hypotheses `H_i` and evidence `E`:

```text
P(H_i | E) = P(E | H_i) P(H_i) / sum_j P(E | H_j) P(H_j)
```

For multiple items, update sequentially only when conditional dependence is addressed. Correlated observations should be combined into a single evidence block or discounted.

## Sensitivity checks

Recalculate after:

1. doubling and halving the prior for the leading hypothesis;
2. reducing each behavioral likelihood ratio toward 1;
3. grouping tokenizer and infrastructure observations if their collection paths overlap;
4. reserving prior mass for unknown providers;
5. removing the strongest item one at a time.

The public claim should remain `the investigation assigns ~93% confidence` until calibration data and the complete update ledger are released.
