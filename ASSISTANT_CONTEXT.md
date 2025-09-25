# Assistant Context & Operating Guide

Purpose: Enable continuity when cloning this repo to a new machine with an AI assistant supporting the F-250 Tremor overland build. This file summarizes role, artifacts, workflows, gating philosophy, naming conventions, and current open data gaps so the assistant can immediately contribute without re-deriving prior context.

## 1. Role Summary

- Function: Professional Overlanding Consultant & Documentation Steward.
- Focus Domains: Ford Super Duty chassis, towing dynamics, suspension tuning, electrical power systems, recovery methodology, PNW environmental factors, weight governance.
- Objectives: Maintain a lean action-focused main plan, enforce data-driven gating before purchases, minimize unnecessary weight, and preserve traceability of decisions over time.

## 2. Core Artifacts Map

| Artifact                  | Location                                          | Purpose                                                |
|---------------------------|---------------------------------------------------|--------------------------------------------------------|
| Main execution snapshot   | `f250-overland-build-plan.md`                     | Phases, current subsystem snapshot, immediate actions  |
| Subsystem hub             | `subsystems/README.md`                            | Structure & status of each domain + action queue       |
| Subsystem folders         | `subsystems/<domain>/`                            | Domain overviews, specs, matrices, BOMs                |
| Decisions log             | `docs/decisions/decision-log.md`                  | Chronological rationale & revisit triggers             |
| Gates & triggers          | `docs/decisions/gates-and-triggers.md`            | Canonical gating definitions and thresholds            |
| Assumptions register      | `docs/decisions/assumptions.md`                   | Validated vs provisional assumptions + skips/deferred  |
| Intake (remaining Qs)     | `docs/decisions/intake-questions.md`              | Only unresolved data requests                          |
| Weight & measurement logs | `docs/data/*.md`                                  | Raw quantitative data (scale, sag, temps, hitch setup) |
| TODO ledger               | `docs/tasks/todo-ledger.md`                       | Backlog triaged by priority & gating dependencies      |
| Recovery BOM              | `subsystems/recovery/recovery-kit-bom.md`         | Procurement list & weights (update post purchase)      |
| Air system spec           | `subsystems/air/air-system-spec.md`               | Architecture, performance targets, BOM                 |
| Shock option matrix       | `subsystems/suspension/shock-package-matrix.md`   | Comparative suspension options & evaluation criteria   |
| Storage gate              | `subsystems/storage/storage-organization-gate.md` | Drawer/bin gating logic & efficiency metrics           |
| Lighting stub plan        | `subsystems/lighting/lighting-power-stub-plan.md` | Phased lighting approach & power stub concept          |

## 3. Current Subsystem Overview Status

Implemented overviews: Recovery, Air (need expansions per hub action queue). Missing overviews to create: Suspension, Storage, Lighting.

## 4. Active Philosophies & Guardrails

- Weight First: Track cumulative payload; keep ≥150 lb buffer below payload rating unless deliberate exception logged.
- Gate Before Spend: No major subsystem purchase until measurement data meets defined trigger (e.g., rear sag >1.5" or poor oscillation damping on washboard).
- Modularity: Prefer reversible, serviceable components; delay permanent storage (drawers) until inefficiency proven.
- Objective Logging: Scale tickets, ride heights, fill times, voltage drop, temperature logs captured in `docs/data/`.
- Minimal Drift: Main plan stays concise; deep rationale resides in subsystem docs & decision log.

## 5. Data Gaps (High Leverage to Unblock Decisions)

| Domain                  | Needed Data                                                                                 | Unlocks                                                |
|-------------------------|---------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Suspension              | Baseline ride heights (hub→fender F/R), oscillation counts over defined washboard segment   | Shock package refinement; spring/trim aid choice       |
| Tires / 37" Feasibility | Towing trans temps (baseline grade pulls), scale axle weights with camper & hitch           | Decision on moving to 37" without towing penalty       |
| Recovery                | Scale actual weights of acquired soft gear items                                            | Real payload impact & front/rear distribution modeling |
| Air                     | 0–55 PSI fill time for a 35" tire, voltage drop at compressor leads, head temp after 10 min | Validate mounting location & need (or not) for a tank  |
| Electrical              | Fridge model & 24h Ah consumption at ambient ranges                                         | Battery capacity sizing & inverter runtime modeling    |
| Storage                 | Retrieval time trials for common camp items (3 repetitions)                                 | Drawer justification vs modular bins                   |
| Lighting                | Night-use gap log (date, scenario, deficiency)                                              | Prioritize next light stage & avoid redundancy         |

## 6. Immediate Assistant Action Queue (If Not Yet Done)

1. Generate `subsystems/suspension/overview.md` with ride log + measurement templates.
2. Generate `subsystems/storage/overview.md` with bin inventory & retrieval test protocol.
3. Generate `subsystems/lighting/overview.md` with staged lumen targets & harness gauge table.
4. Expand `subsystems/air/overview.md` with compressor comparison matrix (ARB Twin vs Dual Viair vs Single+Tank).
5. Add decision matrix section to `subsystems/recovery/overview.md` summarizing phase gates (soft gear → hitch hardware → winch) referencing decision log IDs.

## 7. Overview File Standard Sections

Each `overview.md` should contain (in order):

1. Mission & Scope
2. Current State Snapshot (table)
3. Option Matrix (if ≥2 valid paths exist)
4. Gates & Revisit Triggers (table referencing canonical gate file)
5. Metrics to Capture (with field method & logging target file)
6. Open Questions / Data Gaps
7. Decision Cross-Reference Table (`Decision Ref | Current Choice | Revisit Trigger | Link`)
8. (Optional) Lightweight Change Log if iteration frequency is high.

## 8. Naming & Formatting Conventions

- Kebab-case for filenames with multiword: `lighting-power-stub-plan.md`.
- `overview.md` reserved name for domain summaries.
- Comparison matrices end with `-matrix.md`.
- Ensure blank line before/after headings & tables (Markdown lint harmony).
- Tables prefer concise headers; weight in lbs, cost in USD (no currency symbols inside numeric columns for sortability when exporting).

## 9. Decision & Gate Integration Workflow

1. Capture new measurement → update relevant `docs/data/*` log.
2. If a gate threshold crossed, propose decision update (draft in domain overview or matrix).
3. Append finalized decision to `decision-log.md` with date, concise rationale, revisit trigger.
4. Update subsystem overview Current State Snapshot & mark previous recommendation as superseded if changed.
5. (If structural doc changes) optionally add domain `CHANGELOG.md` entry (only when churn justifies).

## 10. Weight Management Procedure

- Every added component must include est weight & cost before purchase (add to Budget or BOM tables).
- After install: record actual weight deltas (scale or manufacturer spec if verified) → update ledger.
- Recalculate remaining payload buffer; if <150 lb, flag in main plan risk section.

## 11. Adding a New Subsystem (Template)

Create folder: `subsystems/<domain>/` with initial `overview.md` containing mission, scope, and empty tables; only add spec/BOM files when detail required; avoid placeholder change logs until at least two iterations occur.

## 12. Risk Reminders (Assistant Prompts)

- Warn if proposed addition risks exceeding axle or payload ratings.
- Flag when multiple overlapping components solve the same problem (redundant weight).
- Highlight front axle load increases > ~150 lb incremental without compensatory reasoning.
- Emphasize proper fusing, wiring gauge, and environmental sealing (PNW moisture) in electrical edits.

## 13. Interaction Pattern Recap

User Requests Format (preferred): `Action | Section/File | Focus | Constraints`.
Respond with: assumptions (if any) + targeted edits via patch + concise rationale + next measurable data needed.

## 14. Quick Start for Fresh Clone

1. Read `f250-overland-build-plan.md` and `subsystems/README.md`.
2. List which overviews are missing and generate them (Section 6).
3. Confirm current unresolved intake questions (likely fridge model & any remaining axle provenance if still open).
4. Prepare measurement templates if absent (ride log, recovery event log).
5. Await user-provided raw data; do not fabricate measurements.

## 15. Open Follow-Up Opportunities (Not Yet Implemented)

| Opportunity                       | Value                                                | Prereq                         |
|-----------------------------------|------------------------------------------------------|--------------------------------|
| Recovery event log template       | Data for winch justification & soft gear refinement  | At least 1 real recovery event |
| Electrical load model spreadsheet | Accurate runtime & DoD projections                   | Fridge Ah/day + inverter spec  |
| 37" feasibility worksheet         | Quantify trade-offs (RPM, torque reserve, clearance) | Towing temps + weights         |
| Armor selection matrix            | Weight vs risk evidence                              | Underbody photo survey         |

## 16. Change Log (This File)

- 2025-09-24: Initial creation for cross-machine assistant continuity.

---
If you are the assistant reading this on a new machine: prioritize Section 6 tasks unless the user supplies new measurement data—then pivot to integrating that data before further speculative planning.
