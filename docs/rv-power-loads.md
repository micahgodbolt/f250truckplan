# RV 120V Load Worksheet

Purpose: Define which shore/RV AC loads (if any) the truck inverter should support, establish continuous + surge power requirements, daily energy budget, and prioritize loads. Focus is on partial support (no A/C) to keep inverter + battery system weight and cost disciplined.

---

## 1. Methodology

1. Inventory devices that are 120V only (exclude 12V native loads already handled by RV DC system).
2. Record nameplate INPUT watts or amps (NOT just advertised output watts e.g., microwave “1000W” output usually ~1500W input).
3. Measure actual draw with a plug-in watt meter (Kill A Watt or similar) for variable devices (TV, stereo) if possible.
4. Determine typical simultaneous usage groupings (e.g., microwave never with space heater; TV + stereo overlap common).
5. Assign Duty Cycle Pattern:
   - Continuous: runs steadily while on (TV, stereo at low variability)
   - Intermittent: high draw, short duration (microwave)
6. Estimate Daily Runtime (hours) under expected trip pattern (stationary RV stay vs overland transit may differ—capture both if helpful).
7. Calculate Daily Watt-hours = Rated/Measured Watts × Duty Factor × Runtime.
8. Mark Priority Tier:
   - A = Essential / strongly desired off-grid
   - B = Nice to have
   - C = Skip / only on shore power
9. Identify if load will be supported by truck inverter (Y/N) or left to shore/generator only.
10. Sum continuous + surge of all simultaneously expected supported loads to inform inverter sizing margin (aim ≤70% inverter continuous rating for sustained combined draw).

---

## 2. Load Table (Populate & Refine)

| Device / Load                   | Qty | Input Amps @120V | Input Watts (Nameplate) | Surge / Start (W)  | Duty Cycle / Pattern  | Est Daily Runtime (h) | Daily Wh (calc) | Priority (A/B/C) | Support via Truck Inverter? (Y/N) | Notes / Measurement Source  |
|---------------------------------|-----|------------------|-------------------------|--------------------|-----------------------|-----------------------|-----------------|------------------|-----------------------------------|-----------------------------|
| LED TV (assumed 40–50")         | 1   | 0.5–0.8          | 60–95                   | ~120 (turn-on)     | Continuous when on    | 2.0                   | 150 (example)   | A                | Y (candidate)                     | Measure actual draw         |
| Stereo / AV Receiver            | 1   | 0.3–0.6          | 35–70                   | 150 (audio peaks)  | Continuous variable   | 2.0 (overlaps TV)     | 100 (example)   | B                | Y (if modest)                     | Measure average vs peak     |
| Microwave (1000W output)        | 1   | 12.5–13.5        | 1500–1650               | 1700–2000          | Intermittent (bursts) | 0.25 (15 min total)   | 400 (example)   | B                | Y (short use)                     | Verify input label          |
| Roof A/C #1 (13.5k BTU)         | 1   | 12–13            | 1450–1600               | 3000+ (compressor) | Cycling               | 4.0 (hot day)         | 6000 (example)  | C                | N                                 | Generator / shore only      |
| Roof A/C #2 (13.5k BTU)         | 1   | 12–13            | 1450–1600               | 3000+              | Cycling               | 0–4                   | 0–6000          | C                | N                                 | Skip off battery            |
| Converter/Charger (if back-fed) | 1   | 5–12 (variable)  | 600–1400 (bulk)         | 1500               | Tapers after bulk     | 1.0 bulk + 2 float    | 1000 (varies)   | C                | N (avoid loop)                    | Disable when on inverter    |
| Misc Outlets (laptop/phones)    | 2   | 0.3 total        | 35–40                   | 60                 | Continuous when used  | 3.0                   | 120 (example)   | A                | Y                                 | Could charge via DC instead |

Adjust values with actual measurements; replace example daily Wh once measured.

---

## 3. Simultaneous Load Scenarios

| Scenario                          | Included Loads                           | Continuous (W) | Surge (W) | Notes                                         |
|-----------------------------------|------------------------------------------|----------------|-----------|-----------------------------------------------|
| Evening Entertainment             | TV + Stereo + device charging            | ~180           | ~300      | Low demand – easy for 1kW inverter            |
| Meal Prep (Microwave cycle)       | Microwave (active) + small standby loads | 1550–1650      | 1800–2000 | Short duration – ensures need >1500W inverter |
| Mixed (Microwave + Entertainment) | Microwave + TV (audio paused)            | 1600–1700      | 2000      | Manage manually to avoid overload             |

---

## 4. Inverter Sizing Guidance (Preliminary)

1. Base Option (≤1000W): Supports TV, stereo, device charging—NO microwave; simplest wiring & lighter (save ~15–20 lbs vs larger unit + heavier cable).
2. Mid Option (1500–2000W): Enables microwave short bursts + entertainment; requires 2/0 or 1/0 cabling depending on distance, higher cost & weight.
3. Large (3000W): Still cannot realistically support A/C (due to sustained draw + battery capacity limits) and adds significant weight; generally unjustified unless additional high-draw tools planned.

Recommendation (Provisional): Target 1500–2000W pure sine inverter if microwave off-grid use is truly desired. Otherwise stay ≤1000W and rely on propane cooking + shore/generator for microwave & A/C. Confirm actual microwave usage frequency before committing.

---

## 5. Data To Collect (Action List)

- Record exact model numbers for TV, stereo/receiver, microwave, both A/C units.
- Photograph each nameplate (amps, volts, power factor if listed).
- Measure real-time watts of TV and stereo during typical use (Kill A Watt) – capture average and peak.
- Time a typical microwave heating session (minutes/day).
- Decide if off-grid microwave use is a priority (Y/N) and expected daily minutes.
- Confirm if any outlets you want powered are on same circuit as converter/charger (avoid backfeeding a charger from inverter → inefficiency loop).

---

## 6. Next Steps Integration

Once table is populated:

1. Sum Peak Supported Continuous Watts.
2. Choose inverter size with ≥20–30% headroom over that continuous sum.
3. Recalculate battery Ah required: Daily Wh (supported loads) / (System Voltage × Allowable Depth of Discharge). For 12.8V LiFePO4 @ 80% DoD: Required_Ah ≈ Daily_Wh / (12.8 × 0.8).
4. Update `f250-overland-build-plan.md` Electrical section with finalized inverter size and whether microwave included.

---

## 7. Placeholder for Your Measured Values

Add updated rows below once collected (duplicate table if you want a "Measured" version separate from assumptions).

> After populating, ping to generate an inverter cabling gauge & fuse sizing recommendation.
