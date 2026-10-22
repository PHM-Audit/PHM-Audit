# PHM-Audit — deterministic verification, evidence-first

Physics-grounded deterministic verification layer for AI agents, robots,
vehicles, drones — and the SDKs that drive them. Every claim ships with an
on-disk artifact; every aggregate recomputes from open metric files.

## Headline: 5,000,086,001 (≈5B) measurement units

Four layers, closing state 2026-10-09 — full ledger with verbatim metrics,
audit logs, closing marks and SHA-256 manifest:
**[phm-evidence-ledger](https://github.com/PHM-Audit/phm-evidence-ledger)**

| Layer | Count | Unit | Headline result |
|---|---|---|---|
| Physics-engine gate (Master 2B) | 1,900,000,000 +100M baseline | program executions | FP=0 / FN=0 observed, 10 classes, `REACHED_2B` mark |
| Verifier validation scenes | 1,000,000,000 | scene executions | per-class n/ok recorded verbatim |
| Robotics stream gate | 1,000,086,001 | data frames | collision class: 43,440,642/43,482,000 actively BLOCKed |
| SCL fuzzing | 1,000,000,000 | program executions | no crash observed; 3,226,364,783 rule hits; 2.41 ms/program |

Caliber: three layers count executions, one counts frames — mixed by design,
stated per line. Zero-valued results mean "not observed in this test set",
not absolute guarantees.

## Shipped

- **Dify Official Marketplace** — PHM Physics Check merged into the official plugin registry ([langgenius/dify-plugins#3445](https://github.com/langgenius/dify-plugins/pull/3445), 2026-10-22): deterministic physics checking for agent platforms. Zero network calls, verdicts recomputable by anyone.

## Method in one line

Deterministic, operator-declared, pre-execution adjudication with an audit
ledger — gate-first (benign FP=0), evidence-first (every number recomputable),
closed engines with open metrics.

*Scripts are closed-source core assets; metrics, logs, and gates are open.*
