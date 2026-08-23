# Contributing

Contributions are welcome when they improve reproducibility, correct factual errors, or add auditable evidence.

## Before opening an issue

- Check whether the point is already covered by the reports or limitations.
- Distinguish direct observation, interpretation, and speculation.
- Do not submit private session exports, credentials, personal data, or copyrighted material without redistribution rights.

## Evidence submissions

Include:

1. exact model identifier, provider route, timestamp, and client version;
2. complete prompt, attachments, parameters, and raw response;
3. repeat count and observed variance;
4. equivalent candidate-model and negative-control runs;
5. a checksum for every artifact;
6. redaction notes;
7. alternative explanations and evidence dependencies.

Place proposed artifacts in the matching `evidence/` category. Sanitized sessions belong in `sessions/sanitized-session-data/`.

## Language and claims

Use `estimated`, `likely`, and `independent forensic assessment`. Do not replace probabilistic attribution with terms such as `proved`, `confirmed`, or `definitive` unless an authoritative primary source supports the change.

## Pull requests

- Keep each pull request focused.
- Explain what changed and why.
- Link every new claim to a primary artifact or authoritative source.
- Run `git diff --check` and verify all local Markdown links.
- Do not modify the two source PDFs; add a new version with a clear provenance record if a revised report is authorized.
