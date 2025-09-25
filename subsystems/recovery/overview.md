# Recovery Subsystem Overview

Objective: Establish a lightweight, modular recovery capability that scales from core soft gear to winch integration without unnecessary early weight.

## Current State Snapshot
| Aspect              | Status                     | Notes                                    |
|---------------------|----------------------------|------------------------------------------|
| Core Soft Gear      | Planned (Phase 1)          | BOM defined; procurement next            |
| Rear Recovery Point | Pending 2.5" shackle block | Direct-fit chosen over reducer           |
| Traction Boards     | Planned                    | Brand TBD (Maxtrax vs ARB TRED)          |
| Winch               | Deferred                   | Await bumper & weight gate               |
| Ground Anchor       | Deferred                   | Only if routine solo off-tree recoveries |

## Option Set (Phase 1 Core)
| Component          | Option A (Chosen)   | Option B           | Pros (Chosen)                    | Trade-offs                    |
|--------------------|---------------------|--------------------|----------------------------------|-------------------------------|
| Rear Point         | 2.5" shackle block  | 2" block + reducer | Eliminates slop, higher rating   | +~3 lb weight                 |
| Primary Extraction | Yankum 7/8" kinetic | 3/4" rope          | Higher energy, margin, regional  | Slightly heavier, higher cost |
| Shackle Type       | Soft shackles       | Steel bow shackles | Safer failure, lighter           | Inspect abrasion more often   |
| Boards             | ARB TRED Pro        | Budget generic     | Strength, cold impact resilience | Higher cost                   |
| Shovel             | Folding steel       | Full-length        | Compact storage                  | Less leverage                 |

## Phase Roadmap
| Phase       | Capability Added                             | Gate to Advance                               |
|-------------|----------------------------------------------|-----------------------------------------------|
| 1 Core      | Kinetic recovery, boards, shovel, rear point | None (baseline safety)                        |
| 2 Expansion | Additional rigging (pulley), ground anchor   | ≥3 recoveries needing mechanical advantage    |
| 3 Winch     | Powered extraction                           | Bumper selected + scale weight margin ≥200 lb |

## Decision Cross-Ref
| Decision Ref (Date)         | Current Choice  | Revisit Trigger                       | Link                      |
|-----------------------------|-----------------|---------------------------------------|---------------------------|
| 2025-09-24 (2.5" hardware)  | 2.5" direct-fit | Ecosystem forces 2" only use          | decisions/decision-log.md |
| 2025-09-24 (Winch deferred) | Delay winch     | Bumper finalized + recovery frequency | decisions/decision-log.md |

## Data & Metrics to Log
| Metric                     | Method                      | Use                  |
|----------------------------|-----------------------------|----------------------|
| Event count & type         | recovery-event-log (future) | Justify Phase 2 gear |
| Soft shackle wear          | Visual after each use       | Replacement planning |
| Kinetic rope contamination | Post-use inspection         | Cleaning cadence     |

## Open Questions
| Question                | Block Type | Next Action                           |
|-------------------------|------------|---------------------------------------|
| Ground anchor necessity | Deferred   | Log recoveries lacking natural anchor |

**Core decisions complete** ✅ - Ready for Phase 1 procurement!

## Upcoming Files
| File                     | Purpose                              | Trigger to Create                |
|--------------------------|--------------------------------------|----------------------------------|
| recovery-event-log.md    | Chronicle actual recoveries          | After first real recovery        |
| anchor-options-matrix.md | Compare ground anchor vs added ropes | If solo forest recoveries common |
| rigging-cheatsheet.md    | Rapid reference WLL, angles          | Before winch phase               |

## Revisit Gates
| Gate              | Threshold                                                     | Action                  |
|-------------------|---------------------------------------------------------------|-------------------------|
| Add Winch         | >2 stuck events where kinetic insufficient OR bumper selected | Draft winch spec        |
| Add Ground Anchor | >1 recovery w/out usable natural anchor                       | Evaluate anchor options |

## Change Log
| Date       | Change                   | Notes                      |
|------------|--------------------------|----------------------------|
| 2025-09-24 | Initial overview created | Core structure established |

---
Links: `recovery-kit-bom.md` (BOM details).