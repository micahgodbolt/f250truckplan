# Subsystems Documentation Hub

Purpose: Provide a consistent, navigable structure for each build subsystem (Recovery, Air, Suspension, Storage, Lighting, Electrical Power, Protection, Tires, Water, Communications, Safety/Medical) capturing:

- Overview & mission
- Current state snapshot
- Option set (pros/cons, weight, cost, complexity)
- Decision status & revisit gates
- Key metrics to log (data needed to advance)
- Links to detailed spec/BOM files & logs

## Structure Pattern (Per Subfolder)

```text
/subsystems/<domain>/
  overview.md             (high-level goals, decision matrix, open questions)
  <domain>-spec.md        (detailed design / architecture) *optional if merged with overview*
  <domain>-bom.md         (BOM or kit list if distinct)
  CHANGELOG.md            (only if frequent iteration justified)
```

Cross-domain measurement & weight logs remain in `docs/data/` to avoid duplication.

## Current Domains & Status

| Domain             | Folder Path              | Key Files                            | Next Additions / Enhancements                                     | Key Pending Data / Gate Inputs               |
|--------------------|--------------------------|--------------------------------------|-------------------------------------------------------------------|----------------------------------------------|
| Recovery           | `/subsystems/recovery`   | `overview.md`, `recovery-kit-bom.md` | Add decision matrix (hitch block vs receiver shackle arsenal)     | Item scale weights; recovery event log start |
| Air                | `/subsystems/air`        | `overview.md`, `air-system-spec.md`  | Add compressor option matrix (Twin vs Dual Viair vs Single+Tank)  | Fill time, voltage drop, head temps          |
| Suspension         | `/subsystems/suspension` | `shock-package-matrix.md`            | Create `overview.md` (ride log template, sag capture protocol)    | Baseline ride heights; oscillation counts    |
| Storage            | `/subsystems/storage`    | `storage-organization-gate.md`       | Create `overview.md` (bin audit + retrieval time test procedure)  | Retrieval time trials; bin weight audit      |
| Lighting           | `/subsystems/lighting`   | `lighting-power-stub-plan.md`        | Create `overview.md` (scene output targets, harness gauge matrix) | Night-use gap log; circuit current measures  |
| Electrical (House) | (Future)                 | (planned inverter / battery spec)    | Create folder once fridge model + Ah profile captured             | Fridge Ah/day; inverter run length, surge    |
| Protection         | (Future)                 | (armor selection matrix)             | Create folder after underbody photo survey                        | Strike evidence photos                       |
| Tires/Wheels       | (Future)                 | (37" feasibility worksheet)          | Create worksheet after towing temp & weight data                  | Towing trans temps; scale weights            |
| Water              | (Future)                 | (capacity & treatment plan)          | Add when sustained >2-night trips frequent                        | Daily consumption log                        |
| Comms              | (Future)                 | (GMRS / satellite integration plan)  | Add after antenna + mount locations defined                       | Mounting locations; coverage gaps            |

## Rationale for Hub Approach

| Benefit           | Explanation                                                                                |
|-------------------|--------------------------------------------------------------------------------------------|
| Traceability      | Option matrices live beside finalized specs; decision log can deep link.                   |
| Weight Discipline | Each subsystem frontloads weight & cost impact before purchase.                            |
| Gating Clarity    | Gates summarized per domain, even if canonical definitions are in `gates-and-triggers.md`. |
| Reuse             | Template pattern lets you spin up new domains quickly with consistent sections.            |

## When to Create a New Domain Folder

Create once BOTH apply:

1. You have ≥2 meaningful option paths to compare OR a spec needing iteration.
2. There are distinct gating measurements not yet satisfied.

Else keep notes in main plan until promotion warranted.

## Immediate Additions (Action Queue)

1. Create `suspension/overview.md` (include ride log template: surface type, speed, oscillation count, subjective NVH notes).
2. Create `storage/overview.md` (current bin inventory table + retrieval time test protocol).
3. Create `lighting/overview.md` (stage goals, lumen targets, harness gauge & fuse matrix, mounting interference notes).
4. Expand `air/overview.md` with compressor option matrix (CFM @ 0 & 30 PSI, duty cycle %, weight, current draw, cost, redundancy notes).
5. Add decision matrix section to `recovery/overview.md` (soft gear sequencing, hitch hardware ecosystem, winch gate triggers).

## Cross-Referencing Decisions

Each overview should include a small table:

```markdown
| Decision Ref | Current Choice | Revisit Trigger | Link |
|--------------|----------------|-----------------|------|
```

Ref numbers map to `decision-log.md` date entries.

## Naming Conventions

- Use kebab-case for multiword filenames (`lighting-power-stub-plan.md`).
- Keep overview filenames exactly `overview.md` for uniform linking.
- Option matrices: `<domain>-matrix.md` (e.g., `shock-package-matrix.md`).

## Next Action

Generate missing overviews (Suspension, Storage, Lighting) then link this hub in the main build plan. Defer creation of future domain folders until their gating data is available to avoid placeholder churn.

---
Change Log:

- 2025-09-24: Migrated from `docs/subsystems/` to root `subsystems/`; updated paths & current domain status table; pruned duplicate heading.
