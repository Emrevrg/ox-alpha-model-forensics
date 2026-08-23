# Ox Alpha Model Forensics

[![Research status](https://img.shields.io/badge/status-independent%20assessment-334155)](#status-and-scope)
[![Confidence](https://img.shields.io/badge/assessment%20confidence-~93%25-7c3aed)](#final-assessment)
[![License: MIT](https://img.shields.io/badge/license-MIT-0f766e.svg)](LICENSE)

Independent model-forensics investigation into the possible identity of OpenRouter's stealth `ox-alpha` model.

[Read the English report](reports/OX_ALPHA_Final_Forensics_Report_EN.pdf) | [Türkçe raporu oku](reports/OX_ALPHA_Final_Forensics_Report_TR.pdf) | [Review the findings](docs/research-findings.md)

> [!IMPORTANT]
> This repository documents an independent attribution assessment. It is not an official confirmation by OpenRouter, Zhipu AI, or any other model provider.

## Final assessment

The report assigns its highest confidence to:

- **Likely developer:** Zhipu AI (Z.ai)
- **Likely model family:** GLM-5.3
- **Variant hypothesis:** probable multimodal variant
- **Assessment confidence:** approximately 93%

The confidence figure is the report's evidence-aggregation result. It is not a benchmark accuracy score, a frequentist confidence interval, or a calibrated posterior validated against a large set of known stealth models.

## Status and scope

This project studies attribution signals across multiple layers rather than treating any single behavioral resemblance as proof. The report describes:

1. Infrastructure forensics
2. Tokenizer fingerprinting
3. Vision and video behavior analysis
4. Knowledge-cutoff probing
5. Self-knowledge asymmetry testing
6. A/B behavioral comparison
7. Bayesian-style evidence aggregation

## Evidence summary

| Layer | Reported observation | Evidentiary role |
| --- | --- | --- |
| Infrastructure | A Java service-layer trace containing `com.wd.paas.api.domain.v4.chat.ChatCompletionRequest` and error-code behavior | Narrows likely serving-stack relationships; not model-weight proof |
| Tokenizer | A reported 30/30 match against the GLM-5.3-family tokenizer probe set | High-value family fingerprint if independently reproduced |
| Vision/video | Similar video-token usage and encoder behavior to GLM-5V-Turbo | Supports a multimodal-family hypothesis |
| Behavioral probes | Sixteen probes covering reasoning, knowledge boundaries, self-knowledge, and response behavior | Supporting attribution evidence |
| A/B comparison | Output-style and behavioral similarities between `ox-alpha` and GLM-family reference models | Corroborative, not decisive on its own |
| Aggregation | An eight-candidate baseline updated across evidence layers to a reported ~93% assessment | Makes judgment assumptions explicit |

The report's update chain is `12.5% -> 42% -> 68% -> 78% -> 83% -> 87% -> 88% -> 93%`. See [Research findings](docs/research-findings.md), [the evidence framework](methodology/evidence-framework.md), and [the Bayesian-style analysis](methodology/bayesian-analysis.md).

## Research methodology

The investigation reports using:

- OpenCode
- LM Arena Agent Mode
- Codex
- Custom behavioral probes
- Session JSON analysis
- Automated analysis combined with manual verification and independent evidence review

The repository separates observations, interpretations, and conclusions. Reproduction claims should be evaluated only against the artifacts actually published here.

## Repository contents

- [`reports/`](reports/) - final English and Turkish reports
- [`methodology/`](methodology/) - research design, evidence framework, and confidence aggregation
- [`evidence/`](evidence/) - evidence categories and artifact manifests
- [`sessions/`](sessions/) - locations for sanitized sessions and analysis notes
- [`tools/`](tools/) - analysis scripts and usage notes
- [`docs/`](docs/) - timeline, FAQ, limitations, and source provenance
- [`CONTRIBUTING.md`](CONTRIBUTING.md) - evidence-submission and review requirements

## Reproduction

1. Record the tested model identifier, provider route, timestamp, parameters, and raw response.
2. Run the same probe set against `ox-alpha` and declared reference models.
3. Preserve tokenizer counts, error payloads, modality metadata, and complete outputs.
4. Sanitize secrets and personal data without changing model-produced content.
5. Score each evidence item under the published framework.
6. Recompute the aggregation with documented assumptions and sensitivity checks.

Raw sessions are not considered available until files are present under `sessions/sanitized-session-data/`. Empty manifests must not be interpreted as evidence.

## Report integrity

Both final reports are preserved byte-for-byte from the supplied source files. Their SHA-256 checksums, page counts, and visual-QA notes are recorded in [`reports/README.md`](reports/README.md).

## Limitations

- No official confirmation from OpenRouter or Zhipu AI is documented in the reports.
- The exact model variant remains unresolved.
- Behavioral similarity is supporting evidence, not standalone proof.
- Shared infrastructure can identify a provider or serving path without identifying the underlying weights.
- A 30/30 probe match is meaningful only to the extent that probe selection, controls, and raw outputs are available for audit.
- The ~93% figure depends on priors, likelihood assignments, and evidence-independence assumptions.

See [Limitations](docs/limitations.md) for the complete discussion and [Sources](docs/sources.md) for provenance.

## Citation

Citation guidance is available in [CITATION.md](CITATION.md) and machine-readable form in [CITATION.cff](CITATION.cff).

## License

Repository text and original code are released under the [MIT License](LICENSE). Third-party material and the included reports may carry separate rights; consult the report files and source notices before redistribution.
