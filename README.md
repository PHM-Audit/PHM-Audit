# PHM-Audit — deterministic verification, evidence-first

Physics-grounded deterministic verification layer for AI agents, robots,
vehicles, drones — and the SDKs that drive them. Every claim ships with an
on-disk artifact; every aggregate recomputes from open metric files.

## Headline: 5,000,086,001 (≈5B) measurement units

Four layers, closing state 2026-10-09 — full ledger with verbatim metrics,
audit logs, closing marks and SHA-256 manifest:
**[phm-evidence-ledger](https://github.com/PHM-Audit/phm-evidence-ledger)**

## Benchmark: DPC-Bench v0.2

**[dpc-bench](https://github.com/PHM-Audit/dpc-bench)** — paired clean/corrupted
benchmark for physical-consistency defect detection (7 task families, ~10.2K records,
three-caliber labels L1/L2/L3). Six synthetic families each modeled on a real, publicly
documented defect (AgiBot-World #164, PaXini data-kit #3, GalaxeaLeRobotToolkit #5, NGSIM
unit semantics, DJI log frame losses, UZH-FPV kinematic violations); one real-data family
derived from NGSIM I-80 (USDOT public domain). Zero-false-positive-on-clean is reported
separately. Open board — submissions welcome.

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
- **microsoft/PyRIT — under review** ([PR #3507](https://github.com/microsoft/PyRIT/pull/3507), 2026-11): deterministic physics-consistency scorer built on this package. Six first-round correctness issues fixed same-day; PyRIT's creator then pushed four follow-up commits, verified 356 scoped tests, and approved ("no blocking concerns"). Merge pending separate maintainer decision — not yet merged.
- **MCP official Registry** — `io.github.PHM-Audit/phm-lite-check@1.0.1` listed at registry.modelcontextprotocol.io (verified 2026-11-06); listing = metadata publication, not endorsement.
- **MedCheck (in development)** — deterministic medical-advice boundary checker (dosage bounds, symptom-conclusion consistency, supervision-evasion detection) with three-state verdicts. Case replay on public litigation records: 9/9 internal, 6/8 cross-case, control-group zero false positives (v0.2.1, SHA-256-anchored artifact).
- **Independent physical audits (open data)** — all-clean passes over 2,241 Sentry objects, 381 active-spacecraft TLEs, and lunar-sample metadata (263 samples / 3,300 records); 5 Earth mini-moon objects flagged for NaN-semantics defects; C-MAPSS README-vs-paper metric mismatch documented (0.001% vs 73.6%).


## Method in one line

Deterministic, operator-declared, pre-execution adjudication with an audit
ledger — gate-first (benign FP=0), evidence-first (every number recomputable),
closed engines with open metrics.

*Scripts are closed-source core assets; metrics, logs, and gates are open.*
