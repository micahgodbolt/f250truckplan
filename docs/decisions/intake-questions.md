# Build Plan Input Questionnaire (Editable by Owner)

Purpose: Central place for you to supply answers that convert provisional assumptions into validated facts. Fill in the `Answer` fields (keep the structure). I will parse and update `assumptions.md`, gates, and the main plan after each batch.

Instructions:

1. Leave the question ID and wording intact.
2. Enter your answer after `Answer:` (one line or short paragraph; multi-line okay beneath).
3. Dates are OPTIONAL. If you leave the `Date Provided:` line blank (or delete it), I'll auto-stamp the processing date when I ingest your answers.
4. Add any clarifying context under `Notes:` if needed.
5. If you don't know yet, leave `Answer:` blank; I'll keep it in the next round.
6. To intentionally defer a question you consider non-essential, set `Answer: Skip` (capital S optional). I will:
   - Mark it as deferred and remove it from the next cycle unless it becomes gating.
   - Re-surface only if later data shows it blocks a decision.
7. New questions? Add them at the bottom under `## Owner Added Questions` with a new ID `U1`, `U2`, etc.

Parsing Rules Summary:

| Answer Field Value | Interpretation  | Next Action                       |
|--------------------|-----------------|-----------------------------------|
| (blank)            | Pending/unknown | Leave in list                     |
| Skip / skip        | User-deferred   | Hide next iteration unless gating |
| Any other text     | Provided fact   | Update assumptions & gates        |


Legend:

- (H) = High priority answer (unlocks multiple downstream decisions)
- (M) = Medium priority
- (L) = Low priority / nice-to-have

---

## Core Vehicle & Capacity (Pending Only)

Only show unanswered items here. All answered questions have moved to Processed Answers.

### Q2 (H) Axle Code (door jamb two-character) & Diff Type

Answer: 

Notes: (Already decoded from sticker as 4M = 4.30 e-locker; fill only if you want it explicitly captured.)

---

## Power & Appliances (Pending Only)

### Q6 (M) Fridge Model (or planned) & Approx Empty Weight

Answer: 

Notes: (Provide make/model when chosen.)

---

## Usage & Terrain Profile (All Answered – reference Processed Answers)

---

## Storage & Layout (All Answered – reference Processed Answers)

---

## Recovery & Air System (All Answered – reference Processed Answers)

---

## Future Upgrades & Constraints (All Answered – reference Processed Answers)

---

## Existing Gear Inventory (Answered – see Processed Answers row 'Gear')

---

## Risk / Constraints (All Answered – reference Processed Answers)

---

## Processed Answers (Locked In)

| QID  | Topic / Short Label   | Answer (User)                                   | Status     | Notes / Interpretation                        | Next Action                |
|------|-----------------------|-------------------------------------------------|------------|-----------------------------------------------|----------------------------|
| Q1   | Payload Sticker       | 3030 lb (F60/R65/S65)                           | Fact       | Confirms payload buffer; assumption validated | None                       |
| Q3   | Height & Limits       | 84" no limits                                   | Fact       | Headroom for roof & 37"                       | None                       |
| Q4   | Budget                | $20k; ~$500/mo + fall lump                      | Fact       | Drives phased purchases                       | Integrate budget table     |
| Q5   | Occupants             | 2 adults, 2 teens, 2x~60 lb dogs                | Fact       | Max payload scenario logged                   | Weight ledger placeholder  |
| Q7   | Microwave Watts       | Skip                                            | Deferred   | Not gating inverter                           | Revisit if microwave added |
| Q8   | Keurig Wattage        | 1500 W                                          | Fact       | Confirms inverter continuous sizing           | Add to load calc           |
| Q9   | Other High AC Loads   | None                                            | Fact       | Simplifies surge planning                     | None                       |
| Q10  | Longest Engine-Off    | Skip                                            | Deferred   | Use DoD data instead                          | If >2 day stationary trend |
| Q11  | Temp Extremes         | Skip                                            | Deferred   | Using moderate baseline                       | If <20°F or >95°F trips    |
| Q12  | Trail Mix             | FS + mud/ruts + snow                            | Fact       | Guides shock/traction choices                 | Tire shortlist matrix      |
| Q13  | Hwy vs Dirt           | “Lots highway; enough dirt”                     | Fact       | Balanced AT needed                            | Tire scoring               |
| Q14  | Tire Noise Tolerance  | Medium                                          | Fact       | Avoid loud MT patterns                        | Tire shortlist             |
| Q15  | Fuel Range Attitude   | “Not worried; larger tank nice”                 | Fact       | Aux tank low priority                         | Remove early gate          |
| Q16  | Storage Philosophy    | Bins + molle; drawers later                     | Fact       | Drawer weight deferred                        | Drawer gate note           |
| Q17  | Roof Additions        | SP wedge + solar + awning/privacy               | Fact       | Plan wiring stubs                             | Solar & awning mounts      |
| Q18  | Roof Height Tolerance | Not worried                                     | Fact       | Height not constraint                         | None                       |
| Q19  | Recovery Gear         | None yet                                        | Fact       | Need BOM                                      | Generate BOM               |
| Q20  | Compressor Need       | Multi-tire fill; future airbags                 | Fact       | Suggest twin high-flow                        | Air system spec            |
| Q21  | Air-Up Preference     | 2–4 tires simultaneously                        | Preference | Requires manifold & hoses                     | Air system spec            |
| Q22  | Trailer Air-Up        | No                                              | Fact       | Volume calc simpler                           | None                       |
| Q23  | 37" Interest          | Medium                                          | Fact       | Keep evaluation open                          | Build impact worksheet     |
| Q24  | 37" Constraints       | Must not degrade drivability                    | Constraint | Comfort & trans temp gate                     | Add to gate criteria       |
| Q25  | MPG Floor             | Skip                                            | Deferred   | Not gating now                                | If economy concern later   |
| Q26  | Year1 Comfort Targets | Lights, privacy, power, suspension, SP interior | Fact       | Phase plan inputs                             | Map to phases              |
| Q27  | Specialized Equip     | Starlink, GMRS                                  | Fact       | Provide power & mount                         | Add 12V feed stub          |
| Q28  | Reliability Focus     | Better towing ride; solo confidence             | Focus      | Prioritize suspension + recovery              | Shock matrix & BOM         |
| Q29  | Fatigue Factors       | Organization & quick setup                      | Focus      | Emphasize modular storage & lighting          | Storage gate doc           |
| Q30  | Corrosion Concern     | Low                                             | Fact       | Minimal rust treatment                        | Basic hardware coating     |
| Gear | Existing Power/Med    | Anker F2000 + extra; basic med; GMRS handhelds  | Fact       | Interim power defers battery bank             | Define switchover trigger  |

### Deferred (Skip) Summary

| QID | Topic                | Revisit Trigger                         |
|-----|----------------------|-----------------------------------------|
| Q7  | Microwave Watts      | If microwave added / surge margin tight |
| Q10 | Engine-Off Duration  | >2 stationary days common               |
| Q11 | Temperature Extremes | Planned trips outside 20–95°F           |
| Q25 | MPG Floor            | If 37" or heavy armor impacts economy   |

### Open (Pending) Questions

| QID | Topic                       | What’s Needed                  | Why It Matters                |
|-----|-----------------------------|--------------------------------|-------------------------------|
| Q2  | Axle Code (already decoded) | Optional explicit confirmation | Pure provenance; not blocking |
| Q6  | Fridge Model                | Make/model & empty weight      | Mounting, amp draw modeling   |

### Next Auto-Generation Candidates

1. Recovery Kit BOM
2. Air System Specification
3. 37" Impact Worksheet
4. Shock Package Comparison Matrix
5. Storage & Organization Gate Outline
6. Lighting & Power Stub Plan

Reply with any combination of numbers (e.g., 1 2 4) or "all" to generate.

---

## Owner Added Questions

(Add any new Q with ID U1, U2, etc.)

### U1 (example placeholder)

Answer: 
Date Provided: 
Notes:

---

## Change Log (Auto-Maintained When Parsed)

### 2025-09-24 Intake Consolidation

- Collapsed answered Q1–Q30 into Processed Answers table.
- Moved skip items into Deferred Summary with revisit triggers.
- Reduced active questionnaire to pending Q2 & Q6 only.
- Added Next Auto-Generation Candidates list.

---
End of questionnaire.
