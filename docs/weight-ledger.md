# Weight Ledger

Purpose: Maintain accurate running weight and axle distribution after each modification. Update after every major add/remove. Use scale tickets whenever possible.

---

## 1. Columns

- Date: Measurement or change date
- Item / Change: Component added/removed
- Front Delta (lbs): Change in front axle weight
- Rear Delta (lbs): Change in rear axle weight
- Item Weight (lbs): Standalone component weight (if known)
- Running Front (lbs): Updated front axle actual
- Running Rear (lbs): Updated rear axle actual
- Running Total (lbs): Sum (front + rear)
- Payload Used (lbs): Running Total – (Curb + driver) OR direct from sticker baseline
- Notes: Source (scale, mfr spec, estimate) / actions

---

## 2. Baseline Section (Populate Once)

| Date | Configuration                   | Front Axle (lbs) | Rear Axle (lbs) | Total (lbs) | Notes               |
|------|---------------------------------|------------------|-----------------|-------------|---------------------|
| TBD  | Bone stock (full fuel + driver) |                  |                 |             | Scale ticket CAT #1 |

Action: Add passenger baseline if frequently traveling with >1 person.

## 3. Change Log Table

| Date | Item / Change                    | Front Delta (lbs) | Rear Delta (lbs) | Item Weight (lbs)  | Running Front (lbs) | Running Rear (lbs) | Running Total (lbs) | Payload Used (lbs) | Notes                  |
|------|----------------------------------|-------------------|------------------|--------------------|---------------------|--------------------|---------------------|--------------------|------------------------|
| TBD  | Super Pacific Camper Install     | +?                | +?               | 390 (spec)         |                     |                    |                     |                    | Record axle shift      |
| TBD  | ReCurve R3 Hitch Hardware        | +?                | +?               | 100 est            |                     |                    |                     |                    | Weigh assembled        |
| TBD  | Front Bumper + Winch             | +?                | +?               | 185 est            |                     |                    |                     |                    | After install scale    |
| TBD  | Selective Skids                  | +?                | +?               | 90 est             |                     |                    |                     |                    | Transmission+Tcase     |
| TBD  | Fridge + Mount                   | 0                 | +60              | 60 est             |                     |                    |                     |                    | Center if possible     |
| TBD  | 150Ah Battery + DC-DC + Inverter | 0                 | +102             | 102 (42+50+10 est) |                     |                    |                     |                    | Consolidate components |
| TBD  | Recovery Core Kit                | +5                | +70              | 75 est             |                     |                    |                     |                    | Distributed low        |
| TBD  | L-track & Anchors                | 0                 | +15              | 15 est             |                     |                    |                     |                    |                        |
| TBD  | Portable Solar (stowed)          | 0                 | +18              | 18 est             |                     |                    |                     |                    | Only when carried      |
| TBD  | Water (10 gal)                   | 0                 | +83              | 83                 |                     |                    |                     |                    | Variable load          |

## 4. Derived Metrics (Manual or Spreadsheet)

- % Front vs Rear distribution
- Remaining payload margin = Payload Sticker – Payload Used
- Front & Rear vs GAWR (need GAWR values from door sticker)
- Center of gravity shift approximation (optional for advanced analysis)

## 5. Procedure Notes

1. Always weigh with consistent fuel state (full tank preferred) or record fuel percentage.
2. When adding/removing multiple items at once, list each line; if only combined scale data is available, apportion by spec weights.
3. For tongue weight validation: record truck axles unhitched vs hitched (no bars) vs hitched (bars engaged) to compute actual tongue & redistribution.
4. Keep photographic record of scale tickets; reference ticket ID in Notes.
5. If payload margin < 200 lbs: initiate Phase 7 optimization early (audit for heavier-than-planned substitutions).

## 6. Next Steps

- Populate Baseline scale row ASAP.
- After camper install, re-scale before adding other major components.
- Maintain this ledger in parallel with Budget Tracking for cost-weight correlation.

> Option: Export to CSV or spreadsheet later for auto-calculations.
