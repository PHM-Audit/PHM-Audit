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

## The standard-proposal campaign — 18 touchpoints × 12 vendors

The same deterministic pre-execution verification interface, proposed in
vendor ecosystems with reproducible gate tests (benign FP=0, injected caught,
published npm smoke):

| Vendor | Entry point | Artifacts |
|---|---|---|
| OpenAI | #5351 (closed, maintainer-confirmed) + #5330 thread | [agent-action-verifier](https://github.com/PHM-Audit/agent-action-verifier) — AgentDojo real-LLM runs, FP fix-cycle 16→1→0 |
| Google ADK | #7520 + #6099 | adk_evidence/ in agent-action-verifier |
| DeepSeek | SDK 51-case contract + harness plugin | [phm-deepseek-guardrail](https://github.com/PHM-Audit/phm-deepseek-guardrail) · [dsh-action-guard](https://github.com/PHM-Audit/dsh-action-guard) (Show Your Plugins! #9614) |
| Tencent | Hy3 template-injection #236 + youtu-agent #300 | evidence in-repo |
| Alibaba | agentscope #1509 (implementation response) | artifacts in thread |
| Tesla | vehicle-command #517 | [phm-tesla-guardrail](https://github.com/PHM-Audit/phm-tesla-guardrail) |
| Unitree | go2-robotics issue #187 | [phm-unitree-guardrail](https://github.com/PHM-Audit/phm-unitree-guardrail) — official-URDF gate |
| DJI | Cloud API #112 + drone audit cloud | [phm-drone-audit-cloud](https://github.com/PHM-Audit/phm-drone-audit-cloud) — NGSIM 845,100 frames |
| Microsoft | agents-sdk-models proposal | artifacts in thread |

## Method in one line

Deterministic, operator-declared, pre-execution adjudication with an audit
ledger — gate-first (benign FP=0), evidence-first (every number recomputable),
closed engines with open metrics.

*Scripts are closed-source core assets; metrics, logs, and gates are open.*
