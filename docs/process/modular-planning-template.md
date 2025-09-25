# Modular Planning Template (Reusable Methodology)

Purpose: Provide a repeatable pattern for shrinking a large, monolithic plan into a lean "authoritative roadmap" + supporting modular artifacts (decisions, gates, data logs, scenarios, tasks) without losing traceability.

---

## 1. Core Principles

- Separation of Concerns: Stable decisions live apart from volatile data & measurements.
- Traceability: Every decision records its rationale + revisit trigger.
- Gating Before Spend: Purchases or irreversible mods require explicit data-backed gates.
- Weight / Cost Discipline: Track cumulative resource usage (mass, dollars, amp-hours, time) against buffers.
- Incremental Validation: Gather real measurements before escalating complexity.

---

## 2. Standard Artifact Set

| Artifact                | Purpose                                                | Update Frequency | Typical Location                                       |
|-------------------------|--------------------------------------------------------|------------------|--------------------------------------------------------|
| Build Plan (overview)   | High-level roadmap + current snapshot table            | Moderate         | `f250-overland-build-plan.md` (or `<project>-plan.md`) |
| Decision Log            | Chronological record (what / why / trigger to revisit) | On change        | `docs/decisions/decision-log.md`                       |
| Gates & Triggers        | Formal criteria to advance phases or add components    | On new gate      | `docs/decisions/gates-and-triggers.md`                 |
| Data Logs               | Raw measurements feeding gates                         | High             | `docs/data/*.md`                                       |
| Scenarios / Models      | Projections (weight, cost, capacity)                   | As inputs shift  | `docs/data/weight-scenarios.md` etc.                   |
| Task / TODO Ledger      | Operational execution list                             | Frequent         | `tasks/todo-ledger.md`                                 |
| Process Template (this) | Pattern reference                                      | Rare             | `docs/process/modular-planning-template.md`            |

Optional Extensions:

- Risk Register (`docs/decisions/risks.md`)
- Change Log (`CHANGELOG.md`) when versioning major phases
- Metrics Dashboard (automated generation script)

---

## 3. File Naming Conventions

- `docs/decisions/*` = reasoning & gating (stable meta-structure)
- `docs/data/*` = volatile measurement inputs
- `tasks/` = actionable execution lists
- `<project>-plan.md` = ONLY: summary, snapshot table, phase map, quick links
- Use kebab-case; prefix with domain when helpful: `suspension-sag-log.md`, `power-consumption-log.md`

---

## 4. Lifecycle Phases

| Phase               | Objective                                            | Key Outputs                      | Exit Criteria                       |
|---------------------|------------------------------------------------------|----------------------------------|-------------------------------------|
| 0 Discovery         | Define mission, constraints, initial assumptions     | Assumptions block, initial tasks | Constraints accepted & documented   |
| 1 Baseline          | Capture real measurements (weights, geometry, usage) | Data logs seeded                 | >=80% baseline metrics filled       |
| 2 Validation        | Run with minimal upgrades, collect deltas            | Updated gates decisions          | At least one feedback loop complete |
| 3 Targeted Upgrades | Add components gated by data                         | Decision log entries             | Buffers maintained post-upgrades    |
| 4 Optimization      | Prune weight / complexity, refine ergonomics         | Optimization list & actions      | Buffers increased or risk reduced   |
| 5 Sustain & Audit   | Periodic review & maintenance                        | Audit log                        | No open critical risks              |

---

## 5. Decision Log Schema

```markdown
### YYYY-MM-DD | Area | Decision Title
Decision: <Concise statement>
Rationale: <Data / constraints driving this>
Alternatives Considered: <Short bullets>
Triggers to Revisit: <Quantitative gates>
Status: Active | Deprecated | Replaced
```

---

## 6. Gate Definition Pattern

```markdown
Gate: <Name>
Purpose: <Why gate exists>
Inputs Required: <Specific measurements>
Thresholds:
- Proceed: ...
- Monitor: ...
- Block / Rework: ...
Action on Breach: <What to do>
Next Review Cadence: <Interval or event>
```

Embed cross-references: "See data source: `docs/data/sag-rake-log.md` rows n..m".

---

## 7. Snapshot Table Pattern (in Main Plan)

A single table summarizing current state + next gate reduces scrolling.

```markdown
| Subsystem | Current Decision | Next Gate / Data Needed | Notes |
|-----------|------------------|-------------------------|-------|
```

Keep row order consistent to avoid diff noise.

---

## 8. Data Log Template Snippets

### Example: Geometry / Sag Log

```markdown
| Date | Config | LF (in) | RF | LR | RR | Front Avg | Rear Avg | Rake (Rear-Front) | Notes |
|------|--------|--------:|---:|---:|---:|----------:|---------:|------------------:|-------|
```

### Example: Temperature Log

```markdown
| Date | Ambient°F | Segment | Sustained Temp°F | Peak°F | Load Context | Notes |
|------|-----------|---------|-----------------:|-------:|-------------|-------|
```

---

## 9. Task Ledger Columns

- Category
- Task
- Source (which gate/decision drove it)
- Priority (A/B/C or MoSCoW)
- Status (Pending / In Progress / Blocked / Done / Deferred)
- Notes

Keep the main plan to a trimmed "Top 5" subset referencing full ledger.

---

## 10. Versioning & Change Control

- Increment plan version when: (a) phase boundary crossed, (b) major strategy shift, (c) irreversible component selection.
- Add a `CHANGELOG.md` entry summarizing: Added, Changed, Removed, Deprecated, Fixed, Security (keep Conventional Commits style if desired).
- Reference decision IDs in change log for traceability.

---

## 11. Automation Hooks (Optional Future Enhancements)

- Pre-commit script to validate tables align (column count) and ensure snapshot table present.
- Script to aggregate weights & flag GAWR buffer < threshold.
- Generation of HTML dashboard from markdown via static site generator.

---

## 12. Quick Start Checklist

1. Create skeleton directories: `docs/decisions`, `docs/data`, `tasks`, `docs/process`.
2. Draft `<project>-plan.md` with: Overview, Reference Map, Snapshot Table (initially empty), Phase Outline.
3. Populate initial assumptions → convert each to either a validated fact or a decision entry after data.
4. Add first gates (weight buffer, critical performance metrics).
5. Create empty data logs tied to those gates.
6. Start task ledger linking each task to a gate or decision (no orphan tasks).
7. After first measurement pass, update snapshot & evaluate if any gates triggered.
8. Keep only summary + snapshot in plan; move creeping detail out as new files.

---

## 13. Anti-Pattern Warnings

| Smell                   | Mitigation                                                    |
|-------------------------|---------------------------------------------------------------|
| Plan regains bloat      | Enforce rule: if section > ~30 lines & volatile → externalize |
| Decisions lack triggers | Refuse merge until revisit criteria added                     |
| Data logs stale         | Add review cadence column & schedule                          |
| Weight creep unnoticed  | Automated aggregation script or manual weekly update          |
| Gates too vague         | Force quantitative thresholds (inches, °F, lbs, Ah)           |

---

## 14. Minimal Skeleton (Copy-Paste)

```markdown
# <Project Name> Plan (v0.1.0)

## Overview & References
- Decision Log: docs/decisions/decision-log.md
- Gates & Triggers: docs/decisions/gates-and-triggers.md
- Data Logs: docs/data/*
- Task Ledger: tasks/todo-ledger.md

## Snapshot
| Subsystem | Current Decision | Next Gate / Data Needed | Notes |
|-----------|------------------|-------------------------|-------|

## Phases (Outline)
1. Discovery
2. Baseline Measurements
3. Targeted Upgrades
4. Optimization
5. Sustain

## Top Near-Term Actions
| Priority | Action | Purpose | Gate |
|----------|--------|---------|------|
```

---

## 15. Migration Procedure (Monolith → Modular)

1. Tag current monolith commit.
2. Identify stable vs volatile sections (mark each heading S = Stable, V = Volatile temporarily).
3. Extract volatile to `docs/data` or `docs/decisions` as appropriate.
4. Replace extracted sections with lean reference pointers.
5. Build snapshot table summarizing extracted content.
6. Create decision entries for any implicit choices uncovered.
7. Run diff review ensuring no required data lost (just relocated).

---

## 16. Lightweight Metrics (Optional)

| Metric                   | Source        | Target | Alert Condition |
|--------------------------|---------------|--------|-----------------|
| Payload Buffer (lbs)     | Weight ledger | ≥150   | <150            |
| Avg Daily DoD (%)        | Power log     | <30    | >40 for 5 days  |
| Rear Sag (in)            | Sag log       | <1.5   | ≥1.5            |
| Trans Peak Tow Temp (°F) | Temp log      | <225   | ≥230 sustained  |

---

## 17. Adaptation to Other Domains

- Software Projects: Replace weight with build time / perf budget; sag with latency; trans temp with CPU temps.
- Expedition Logistics: Replace suspension gates with resupply frequency metrics.

---

## 18. License & Attribution

Free to reuse; adapt sections to context. Maintain decision + gate rigor.

---

## 19. Next Improvement Ideas

- Add YAML front-matter for automated parsing
- Introduce simple CLI script to insert decision skeletons
- Add Mermaid diagrams for dependency mapping

---

End of template.
