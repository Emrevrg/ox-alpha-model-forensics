# Methodology

## Objective

Assess the most plausible developer and model family behind OpenRouter's stealth `ox-alpha` listing without treating self-identification or stylistic similarity as conclusive.

## Study design

The reported workflow triangulates across independent evidence classes:

1. **Infrastructure:** service-layer errors, namespaces, response envelopes, and routing behavior.
2. **Fingerprinting:** tokenizer behavior and deliberately selected tokenization probes.
3. **Modal behavior:** image/video token accounting and encoder-side behavior.
4. **Reasoning behavior:** controlled prompts designed to reveal stable behavioral tendencies.
5. **Knowledge boundaries:** time-sensitive and release-sensitive probes.
6. **Self-knowledge asymmetry:** differences between what the model can do and what it claims about itself.
7. **A/B comparison:** matched prompts against candidate reference models.
8. **Evidence aggregation:** explicit updates from a candidate baseline to a final assessment.

## Probe protocol

For each probe, preserve:

- exact prompt and attachments;
- model identifier, route, and timestamp;
- request parameters and client version;
- raw response and error payload;
- token counts and modality metadata;
- repetition count and observed variance;
- equivalent runs against candidate and negative-control models.

A probe should be labeled exploratory until it has a preregistered scoring rule and reproducible raw artifacts.

## Evaluation

Evidence is recorded as an observation before interpretation. Each item receives a strength class, plausible alternative explanations, provenance, and an independence note. Conclusions use cautious terms such as `estimated`, `likely`, and `independent forensic assessment`.

## Research environment

The reports identify OpenCode, LM Arena Agent Mode, Codex, custom behavioral probes, and session JSON analysis as components of the workflow. Automated findings require manual verification before inclusion.
