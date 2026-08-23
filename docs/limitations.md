# Limitations

## Attribution boundary

- A serving-stack trace can identify infrastructure without identifying the underlying model weights.
- A tokenizer match can indicate shared lineage or implementation but may not resolve a fine-tune or variant.
- Multimodal token accounting can reflect shared preprocessing rather than a shared base model.
- Behavioral similarity is sensitive to system prompts, decoding parameters, safety layers, and routing.

## Data boundary

- Raw session evidence must be sanitized and published before third parties can audit individual claims.
- Probe selection can introduce confirmation bias if candidate-specific probes are chosen after observing results.
- Small or single-run samples do not establish stable behavior.
- Public discussion and media reports are contextual sources, not primary technical evidence.

## Confidence boundary

- The reported ~93% is conditional on priors, likelihood assignments, evidence selection, and independence assumptions.
- Equal priors across eight named labs omit uncertainty about unknown providers unless an explicit `other` hypothesis is included.
- Correlated evidence can inflate a naive Bayesian chain.
- No calibration set of known stealth-model cases is currently documented.

## Confirmation boundary

No official confirmation from OpenRouter or Zhipu AI is documented. The exact variant remains unresolved. Future disclosures or reproducible counter-evidence may materially change the conclusion.
