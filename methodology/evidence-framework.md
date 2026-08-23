# Evidence framework

## Evidence classes

| Class | Examples | Typical strength | Principal caveat |
| --- | --- | --- | --- |
| Infrastructure | stack traces, namespaces, gateway errors | Moderate to strong for provider/stack attribution | Shared gateways do not prove model weights |
| Fingerprinting | tokenizer counts, rare-token behavior | Strong for model-family narrowing when controls are public | Probe leakage and shared tokenizers |
| Modal | image/video token accounting, encoder behavior | Moderate | Common preprocessing stacks can converge |
| Behavioral | reasoning patterns, refusals, knowledge probes | Weak to moderate | Prompt sensitivity and sampling variance |
| A/B testing | matched prompts against reference models | Moderate with blinded scoring and repeats | Style is not identity |

## Evidence record

Every published item should include:

- stable identifier;
- raw artifact path;
- collection time;
- tested endpoint and parameters;
- observation;
- interpretation;
- alternative explanations;
- reproducibility status;
- strength rating;
- dependencies on other evidence.

## Strength scale

- **S1 - Contextual:** useful background, little attribution power.
- **S2 - Supporting:** shifts the hypothesis modestly.
- **S3 - Discriminative:** rules out meaningful alternatives under documented controls.
- **S4 - Near-direct:** difficult to explain without a close provider or model-family relationship.

No behavioral item should receive S4 on its own.

## Independence rule

Correlated signals must not be multiplied as though independent. For example, response style, reasoning format, and refusal behavior may share the same instruction-tuning cause. Group them or apply a dependence discount before aggregation.
