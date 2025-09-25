# F250 Overland Build Plan

> Action-focused plan. Background rationale moved to `docs/overland-context.md`.

## 1. Over## 11. Open Questions / Parking Lot

- Scale-confirm camper axle impact & final mounting hardware mass (Pending scale data).
- Keurig exact wattage (assumed 1500W) – verify for surge margin logging.
- **Storage decision**: DECKED D4 + Super Pacific integration vs custom half-width fabrication.
- Winch line speed vs weight preference (shortlist once bumper ordered).
- Air system mount location (engine bay vs frame rail vs under-bed).
- Corrosion mitigation schedule (decide annual vs semi-annual after first winter exposure).

## 12. Phase 0 & Phase 1 Detailferences

This file now stays lean: focuses on upgrade decisions, phase sequencing, costs, and active gates. All supporting context & raw data moved to modular docs.

Reference Map:

- Subsystems Hub: `subsystems/README.md`
- Context & philosophy: `docs/overland-context.md`
- Detailed weight tables & scenarios: `docs/data/weight-scenarios.md`
- Sag / rake measurements: `docs/data/sag-rake-log.md`
- Towing transmission temps: `docs/data/towing-trans-temp-log.md`
- Hitch / WDH scaling: `docs/data/hitch-setup-log.md`
- Decisions archive: `docs/decisions/decision-log.md`
- Gates & detailed triggers: `docs/decisions/gates-and-triggers.md`
- Full TODO ledger: `docs/tasks/todo-ledger.md`

Baseline vehicle, use profile, constraints, and full subsystem rationales were relocated (see context + decisions). This plan shows WHAT will be done, WHEN, and high-level WHY.

## 5. Phased Roadmap

| Phase                               | Objective                          | Key Deliverables                                    | Exit Criteria                       |
|-------------------------------------|------------------------------------|-----------------------------------------------------|-------------------------------------|
| 0 Assessment                        | Baseline data & priorities         | Scale weight, measurements, use refinement          | Payload & use profile locked        |
| 1 Foundation (Safety & Reliability) | Protection, recovery basics, tires | Tires, basic recovery kit, comms baseline           | Field test weekend                  |
| 2 Suspension & Handling             | Payload-ready, ride quality        | Tuned shocks, springs/leaf pack, steering tightness | Washboard test acceptable           |
| 3 Power & Electrical                | House power & redundancy           | Dual/aux battery, DC-DC, wiring backbone            | 48h fridge runtime proven           |
| 4 Storage & Organization            | Efficient secure cargo             | Drawer / modular bins, tie-down grid                | Rapid camp deployment               |
| 5 Living Systems                    | Comfort & sustainment              | Fridge, water, cooking, shade/shelter               | 4-day trip without resupply         |
| 6 Advanced Recovery & Comms         | Remote reliability                 | Winch, upgraded comms, traction aids                | Self-recovery drill success         |
| 7 Optimization                      | Weight & refinement                | Component audits, reduce redundancies               | Net weight reduction / improved MPG |

## 6. Subsystem Status Snapshot

| Subsystem       | Current Decision                          | Next Gate / Data Needed              | Notes                                                        |
|-----------------|-------------------------------------------|--------------------------------------|--------------------------------------------------------------|
| Tires           | Retain 35" Year 1                         | Towing trans temps; payload buffer   | 37" deferred until data margin proven                        |
| Suspension      | **SELECTED: Carli Backcountry 2.0**       | Phase 2 implementation timing        | Decision final; $3,200 system ready for Phase 2 procurement  |
| Towing / WDH    | ReCurve R3 planned                        | Three-pass scale; front axle restore | Tune bar tension before considering bags                     |
| Armor           | Selective (trans + transfer + steering)   | Underbody photo survey               | Add plates only on evidence                                  |
| Recovery        | **SELECTED: ARB TRED Pro + Yankum rope**  | Ready for Phase 1 procurement        | $615 Phase 1 cost; winch deferred to Phase 2                 |
| Electrical      | 12V 2.2–3.0 kW inverter-charger + 150Ah   | Cable run length; appliance wattage  | Second battery only if DoD >30% sustained                    |
| Air System      | **SELECTED: ARB Twin CKMTA12**            | Ready for Phase 1 implementation     | $1,135-1,355 system; mount location TBD                      |
| Storage         | **Research: DECKED vs half-width custom** | Super Pacific integration testing    | DECKED D4 pragmatic choice vs custom fabrication             |
| Living Systems  | 50L fridge + modular water                | 48h Ah consumption log               | Water plumbing deferred                                      |
| Lighting        | **SELECTED: F150LEDs Paladin Phase 1**    | Bumper mount + upfitter switches     | $200 Phase 1; SP integration Phase 2                         |
| Weight Mgmt     | Track cumulative; validate as we go       | Scale tickets; ledger updates        | Progressive validation approach - optimize if buffer <200 lb |
| Future Trim Aid | Rear air bags deferred                    | Rake & towing sag data               | Trim aid only; not spring substitute                         |

## 7. Immediate Action Items

Immediate (Pre-Phase 1):

1. Obtain certified scale weight (full fuel + driver) – record axle splits if possible.
2. Confirm axle ratio & rear locker via door sticker (axle code) & window sticker.
3. Record actual Super Pacific scale delta after install (front & rear axle change) & center of gravity info if available.
4. Measure current rear ride height (hub center to fender) unloaded for future sag comparison.
5. Scale hitch hardware weight (ReCurve R3 components) separately if possible; document brake controller gain baseline.
6. Finalize inverter spec (brand/model, continuous & surge ratings >2kW) & mounting run length (cab passthrough zone).
7. Prioritize post-camper sequence: recovery kit vs onboard air vs power core (rank 1–3).
8. Perform three-pass axle weight sequence (unhitched / hitched no bars / hitched bars engaged) and log results.
9. Capture Keurig model & nameplate watt rating (photo or manual) – verify surge headroom (assume 1500W OK).

## 8. Risks

| Risk                | Mitigation                                                |
|---------------------|-----------------------------------------------------------|
| Overloading GVWR    | Weight tracking sheet; weigh after each major phase       |
| Electrical faults   | Proper gauge, fusing at source, marine-grade terminations |
| Tire failure remote | Full-size spare, plug kit, sidewall patch, onboard air    |
| Fuel contamination  | Keep spare filter, carry funnel + water-separating filter |
| Navigation loss     | Redundant offline maps + satellite messenger              |
| Winch misuse injury | Formal training / practice session                        |

## 9. Budget Tracking (To Populate)

| Phase | Item                                  | Option (Chosen)           | Est Cost (USD) |  Weight (lbs) | Priority | Selected?    |
|-------|---------------------------------------|---------------------------|---------------:|--------------:|----------|--------------|
| 0     | Scale tickets (multiple passes)       | Local CAT scales          |             40 |             0 | A        | Pending      |
| 0     | Tire tools (gauge, chalk, IR)         | Mid                       |             85 |             3 | A        | Pending      |
| 1     | Recovery core kit                     | **ARB TRED Pro + Yankum** |            615 |            75 | A        | **SELECTED** |
| 1     | Onboard air (dual compressor)         | **ARB Twin CKMTA12**      |          1,245 |            28 | B        | **SELECTED** |
| 1     | L-track & anchors                     | Aluminum track + fittings |            250 |            15 | A        | Pending      |
| 1     | Fridge 50L + wiring (temp)            | Efficient mid             |            900 |            60 | A        | Pending      |
| 2     | Suspension upgrade                    | **Carli Backcountry 2.0** |          3,200 |             6 | A        | **SELECTED** |
| 2     | Front bumper (aluminum hybrid)        | Mid                       |          1,400 |           110 | A        | Planned      |
| 2     | Winch 12k synthetic                   | Mid (waterproof)          |          1,000 |            75 | A        | Planned      |
| 2     | Skid package (selective)              | Mid                       |            800 |            90 | B        | Planned      |
| 2     | Steering brace / components           | Mid                       |            300 |             5 | B        | Planned      |
| 3     | 150Ah LiFePO4 battery                 | Quality mid               |            900 |            42 | A        | Planned      |
| 3     | 60A DC-DC charger + cabling           | Mid                       |            500 |            10 | A        | Planned      |
| 3     | 2.5–3.0 kW inverter-charger           | Mid                       |          1,600 |            50 | A        | Planned      |
| 3     | 4/0 cabling + lugs + fuse (Class-T)   | Quality copper            |            450 |            12 | A        | Planned      |
| 3     | Monitoring (shunt + display)          | Mid                       |            200 |             1 | A        | Planned      |
| 3     | Portable solar 200W                   | Folding panel             |            350 |            18 | B        | Deferred     |
| 2     | Storage system                        | **DECKED D4 or custom**   |          1,500 |           180 | A        | Research     |
| 2     | Lighting Phase 1                      | **F150LEDs Paladin**      |            200 |             8 | A        | **SELECTED** |
| 5     | Water containers (2x5–7 gal)          | Mid                       |            120 |        83–116 | A        | Pending      |
| 5     | Shade awning (lightweight)            | Light mid                 |            600 |            25 | B        | Deferred     |
| 6     | Winch accessories (line dampers, etc) | Mid                       |            250 |            10 | B        | Deferred     |
| 6     | Comms (GMRS mobile + antenna)         | Mid                       |            350 |             5 | A        | Planned      |
| 6     | Satellite messenger                   | Existing? (assume buy)    |            400 |           0.5 | A        | Pending      |
| 7     | Weight optimization swaps (est)       | TBD                       |            500 | -30 (savings) | B        | Future       |
| ALL   | Corrosion protection materials        | Fluid film / brushes      |            120 |             3 | A        | Pending      |

Budget Notes: Costs are planning estimates (mid options). Contingency reserve 10–15% recommended. Mark actuals upon purchase.

## 10. Recent Decisions Summary

### Phase 1 - Ready for Procurement
- **Recovery System**: ARB TRED Pro 45" + Yankum 7/8" x 30' rope ($615 total)
- **Air System**: ARB Twin CKMTA12 compressor system ($1,245 average)
- **Lighting Phase 1**: F150LEDs Paladin 150W curved bar + upfitter switches ($200)

### Phase 2 - Decisions Locked
- **Suspension**: Carli Backcountry 2.0 system ($3,200 installed)
- **Storage**: Research DECKED D4 vs custom half-width (Super Pacific integration TBD)

### Total Phase 1 Committed Cost: ~$2,060
### Total Phase 2 Locked Decisions: ~$4,900+ (suspension + storage + lighting Phase 2)

## 11. Open Questions / Parking Lot

- Scale-confirm camper axle impact & final mounting hardware mass (Pending scale data).
- Keurig exact wattage (assumed 1500W) – verify for surge margin logging.
- Drawer system necessity after 3 shakedowns (retain modular if efficiency adequate).
- Winch line speed vs weight preference (shortlist once bumper ordered).
- Corrosion mitigation schedule (decide annual vs semi-annual after first winter exposure).

## 11. Phase 0 & Phase 1 Detail

| Phase | Step                                      | Purpose                       | Notes                                      |
|-------|-------------------------------------------|-------------------------------|--------------------------------------------|
| 0     | Scale weight (axle splits)                | Payload & suspension baseline | Use CAT or local feed scale                |
| 0     | Record ride heights (F/R both sides)      | Future sag comparison         | Hub center to fender lip                   |
| 0     | Tire pressure & chalk test                | Optimize contact patch        | Document baseline PSI set                  |
| 0     | Inventory required recovery & safety gaps | Prevent impulse buys          | Build prioritized list                     |
| 0     | Corrosion baseline (photos)               | Track wear in PNW             | Helps future inspections                   |
| 1     | **Acquire ARB TRED Pro + Yankum rope**    | Solo safety baseline          | $615 total; 45" boards + 30' kinetic rope  |
| 1     | **Install ARB Twin air system**           | Air down flexibility & tools  | Mount location TBD; $1,245 system          |
| 1     | **Install F150LEDs Paladin bar**          | Basic lighting upgrade        | Bumper mount + upfitter switch integration |
| 1     | Camper install & re-scale                 | Update constant load          | Capture new axle splits                    |
| 1     | L-track / anchor points install           | Modular cargo retention       | Prepare for storage decision               |
| 1     | Weight audit & adjust plan                | Prevent payload creep         | Compare against 3100 lb limit              |

Exit Criteria Phase 1: Reliable solo weekend trip executed with camper + recovery + fridge powered 48h from temporary battery (or starting battery draw test) without voltage issues; accurate revised weight log; prioritized list for Phase 2 suspension decision.

## 12. Top Near-Term Actions (Full list in `tasks/todo-ledger.md`)

| Priority | Action                                             | Purpose                           | Gate                   |
|----------|----------------------------------------------------|-----------------------------------|------------------------|
| A        | Baseline scale weight (axle splits)                | Payload math & sag gating         | Access to scale        |
| A        | Unladen ride heights (hub→fender)                  | Establish rake baseline           | Level surface          |
| A        | Hitch 3-pass weight (truck / hitch no bars / bars) | Validate WDH setup                | Trailer loaded         |
| A        | Inverter run length & mount distance               | Confirm cable gauge & fuse        | Mount point identified |
| B        | Keurig nameplate & microwave input                 | Surge & load profile verification | Appliance access       |

## 13. Priority Decision Matrix & Gates

### 13.1 Summary Matrix

| Topic                           | Objective                                  | Data Gate(s)                                                     | Risks If Premature                              | Current Recommendation               |
|---------------------------------|--------------------------------------------|------------------------------------------------------------------|-------------------------------------------------|--------------------------------------|
| Onboard Air Integration         | Fast air down/up + trailer & load support  | Final chosen compressor location; amperage wiring path length    | Heat soak, wasted weight (oversize)             | Proceed soon (post location measure) |
| 37" Tires Feasibility           | Increased ground clearance / footprint     | Baseline towing trans temps; scale weights; gearing confirmation | Towing performance loss; higher rotational mass | Defer until data captured            |
| Carli Backcountry Suspension    | Improved washboard control & loaded ride   | Rear sag >1.0–1.5" confirmation; ride log unladen vs loaded      | Over-sprung unladen, unnecessary cost           | Prepare worksheet; wait for sag data |
| Incremental Protection Strategy | Only add skids where real exposure risk    | Underbody inspection photos; trail type frequency analysis       | Excess weight forward; service complexity       | Inspect first, add selective plates  |
| Lighting Integration Approach   | Functional, low-drag lighting upgrade path | Real world night driving gaps; mounting interference check       | Redundant lights, aero/noise penalty            | Stage: reverse/work → scene → ditch  |

See `docs/decisions/gates-and-triggers.md` for full gating logic (suspension, 37" tires, air bags, armor, lighting, electrical expansion).


Legend: Pending = next actionable when prereqs available; Deferred = intentionally paused awaiting external condition/data.

---
Next Step: Provide the action item data in Section 9 (scale weight, axle ratio confirmation, camper weight, RV load list, priority ranking) so we can lock Phase 1 procurement list.
