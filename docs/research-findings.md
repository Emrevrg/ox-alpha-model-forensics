# Research findings

This document is a navigable summary of the two final reports. It distinguishes report-stated observations from interpretation and does not replace the source PDFs.

## Assessment

| Level | Reported conclusion | Certainty in the report |
| --- | --- | --- |
| Company | Zhipu AI (Z.ai) | Very strong |
| Model family | GLM-5.3 | Strong |
| Exact variant | GLM-5.3, GLM-5.3V, or a sibling variant | Uncertain |

The report assigns approximately 93% assessment confidence to the company/family hypothesis. Its lower-confidence variant split is described as indicative only.

## Four evidence layers

### 1. Infrastructure forensics

The report cites a malformed-request response containing the Java namespace `com.wd.paas.api.domain.v4.chat.ChatCompletionRequest` and error code `1214`. It treats this as evidence of a Z.ai-related serving layer while explicitly preserving the alternative that a wrapper may serve different underlying weights.

### 2. Tokenizer and modality fingerprints

The report attributes a 30/30 tokenizer-probe match to community testing and reports a four-video token-usage curve matching GLM-5V-Turbo. Both are third-party measurements in the report and require the original probe definitions and outputs for independent audit.

### 3. Sixteen behavioral probes

The probe program covers masked identity, multilingual pressure, political questions, knowledge cutoff, contamination traps, planning behavior, tokenizer/riddle/spec questions, self-knowledge asymmetry, system-prompt resistance, and frontier-vision behavior. The strongest report-selected observations are:

- a late-November-2025 knowledge boundary;
- deeper and fresher Zhipu ecosystem knowledge than comparison topics;
- behavior consistent with an international rather than domestic endpoint;
- a reasoning fragment instructing the model to identify itself as `ox-alpha`;
- detailed vision analysis of a web-application screenshot.

### 4. Controlled A/B comparison

The same control image and prompt were compared against `ox-alpha` and GLM-5V-Turbo. The report identifies matching inventory order, OCR results, closing pattern, outline emphasis, and Markdown structure. It classifies this as supporting and mimicable evidence, not standalone identity proof.

## Rival hypotheses considered

The report discusses Xiaomi MiMo, Alibaba/Qwen, GLM-5.2, GLM-4.6V, DeepSeek-style domestic RLHF, and US-lab candidates. The eliminations rely on tokenizer differences, error-dialect differences, vision signatures, behavior, and serving-stack patterns.

## Required caution

- Infrastructure attribution is not weight attribution.
- The tokenizer and video findings are community measurements.
- Behavioral similarity can be induced by prompts, fine-tuning, or wrappers.
- OpenCode image normalization prevented clean absolute image-token measurement.
- The likelihood ratios and ~93% result are judgment-based and assumption-dependent.
- No official provider confirmation is documented in the reports.

For the complete wording, quotations, tables, images, and sources, use the [English](../reports/OX_ALPHA_Final_Forensics_Report_EN.pdf) or [Turkish](../reports/OX_ALPHA_Final_Forensics_Report_TR.pdf) report.
