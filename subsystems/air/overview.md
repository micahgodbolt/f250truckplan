# Air Subsystem Overview

Objective: Deliver fast, reliable multi-tire inflation (2–4 tires simultaneously) with future expandability (air bags, lockers) while minimizing heat soak and electrical losses.

## Current State Snapshot
| Aspect            | Status                     | Notes                                         |
|-------------------|----------------------------|-----------------------------------------------|
| Compressor Choice | Pending (ARB Twin favored) | Viair dual alternative still open             |
| Mount Location    | Not Selected               | Need thermal & packaging survey               |
| Manifold Plan     | Defined (6-port)           | Ports reserved for future expansions          |
| 4-Tire Harness    | Concept                    | To be built DIY after compressor install      |
| Tank              | Deferred                   | Add only if air tools / bead seating frequent |

## Option Comparison
| Option                   | CFM @0 / @30 | Duty Cycle | Approx Weight | Est Cost | Pros                   | Cons                     |
|--------------------------|--------------|------------|--------------:|---------:|------------------------|--------------------------|
| ARB Twin CKMTA12         | 6.2 / ~4.7   | 100%       |         16 lb |     $640 | High output, compact   | Cost, heat concentration |
| Dual Viair 485C Kit      | 5.6 / ~4.0   | 100%       |         19 lb |     $520 | Redundancy (two units) | More plumbing, footprint |
| Single Viair 485C + Tank | 2.7 / ~2.0   | 100%       |  11 lb + tank |     $450 | Lower cost start       | Slower, adds tank weight |

## Decision Cross-Ref
| Decision Ref (Date)            | Current Choice   | Revisit Trigger           | Link                      |
|--------------------------------|------------------|---------------------------|---------------------------|
| 2025-09-24 (Onboard air early) | Early deployment | If fill times exceed gate | decisions/decision-log.md |

## Data & Metrics to Log
| Metric                     | Method                    | Gate                    |
|----------------------------|---------------------------|-------------------------|
| 4-tire fill time 18→60 psi | Stopwatch (3 runs)        | >11 min triggers review |
| Head temperature post-fill | IR thermometer            | >220°F add shielding    |
| Voltage drop @ full load   | DMM battery vs compressor | >0.6V re-evaluate gauge |

## Open Questions
| Question                              | Impact            | Next Action                                    |
|---------------------------------------|-------------------|------------------------------------------------|
| Under-hood vs bed mounting            | Thermal & service | Measure clearances, record ambient after drive |
| Need for quick front coupler location | Convenience       | Assess frequency of single-hose use            |

## Revisit Gates
| Gate            | Threshold                              | Action                               |
|-----------------|----------------------------------------|--------------------------------------|
| Add Tank        | Frequent air tool / bead tasks (>3/mo) | Add 1–2 gal aluminum tank            |
| Upgrade Harness | Uneven tire fill >3 psi delta          | Larger trunk hose or stagger lengths |

## Upcoming Files
| File                         | Purpose                                 | Trigger to Create          |
|------------------------------|-----------------------------------------|----------------------------|
| compressor-options-matrix.md | Expanded thermal/CFM vs weight analysis | If Viair remains contender |
| air-install-checklist.md     | Step-by-step install QA                 | Before physical install    |

## Change Log
| Date       | Change                   | Notes                     |
|------------|--------------------------|---------------------------|
| 2025-09-24 | Initial overview created | Baseline options captured |

---
Links: `air-system-spec.md` (spec & BOM).