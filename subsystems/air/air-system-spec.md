# Onboard Air System Specification

Objective: Enable simultaneous 2–4 tire inflation with future compatibility for rear helper air bags and light pneumatic tools while controlling weight and electrical load. Target fill: 37" (future) or current Tremor-sized tires from trail (~18 psi) to road (~65 psi rear / 60 psi front) in ≤ 10 minutes total (4-tire manifold) under moderate ambient (60–80°F).

## Architecture Summary

| Component             | Spec                                                                 | Rationale                       | Notes                                 |
|-----------------------|----------------------------------------------------------------------|---------------------------------|---------------------------------------|
| Compressor            | Twin motor 100% duty (e.g., ARB Twin CKMTA12) OR Dual Viair 485C kit | High CFM for parallel inflation | ARB: ~6.2 CFM @ 0 psi, ~4.7 @ 29 psi  |
| Mount Location        | Under hood (passenger fender) preferred                              | Short cable run, airflow        | Validate heat soak after trail climbs |
| Air Manifold          | 6-port aluminum block w/ 1/4" NPT                                    | Future lockers / bags reserved  | Cap unused with thread seal           |
| Hose Routing          | Removable 4-tire whip manifold (¼" ID)                               | Even pressure equalization      | Bleed valve built-in                  |
| Quick Couplers        | Industrial (Type M) front & rear bulkheads                           | No hood opening needed          | Stainless for corrosion resistance    |
| Pressure Switch       | 150 psi on / 180 psi off                                             | Standard for compressor kits    | Matched to safety valve               |
| Safety Relief         | 175–180 psi                                                          | Overpressure protection         | Mount directly on manifold            |
| Air Filter Relocation | Snorkel-style remote filter                                          | Cleaner intake                  | Serviceable element                   |
| Electrical Feed       | 6 AWG pos/neg to future aux fuse block                               | Min voltage drop                | 100A fuse @ battery                   |
| Control               | Dash switch (sealed) via relay                                       | Operator convenience            | Add secondary kill near compressor    |

## Performance Estimates (ARB Twin Baseline)

Assumptions: 35–37" LT tires ~6,000–6,500 in^3 internal volume each at 65 psi (rough estimate). Practical flow at mid-pressure ~4.5 CFM combined.

| Method          | Tires at Once | Est Total Time 18→60 psi | Notes                           |
|-----------------|---------------|--------------------------|---------------------------------|
| Single hose     | 1             | ~14–16 min               | Sequential; baseline reference  |
| Dual whip (Y)   | 2             | ~9–10 min                | Pressure equalization mid cycle |
| 4-tire manifold | 4             | ~8–9 min                 | Balanced; minimal reconnection  |

(Refine with real timing; log first three sessions.)

## Electrical Design

| Aspect      | Spec                                   | Detail                           |
|-------------|----------------------------------------|----------------------------------|
| Max Draw    | ~56A continuous (ARB Twin)             | Inrush slightly higher           |
| Wire Gauge  | 6 AWG OFC tinned                       | Run length ≤6 ft battery → relay |
| Fuse        | 100A MIDI or ANL within 7" of battery  | Protects wiring not device       |
| Relay       | 100A continuous rated                  | Switch low-current dash circuit  |
| Dash Switch | LED backlit (water-resistant)          | Label "AIR"                      |
| Ground      | Direct to chassis ground + star washer | Avoid paint resistance           |

## Pneumatic Layout

1. Compressor discharge → vibration isolator hose → check valve (if not integrated) → manifold.
2. Manifold ports:
   - Port 1: Pressure switch (150/180)
   - Port 2: Safety relief 175 psi
   - Port 3: Front bulkhead coupler
   - Port 4: Rear bulkhead coupler
   - Port 5: Future air bags regulator (capped)
   - Port 6: Future locker solenoid (capped)

## 4-Tire Inflation Harness

| Component         | Spec                                    | Notes                      |
|-------------------|-----------------------------------------|----------------------------|
| Main Trunk        | 3/8" lightweight hybrid hose            | Reduce pressure drop       |
| Branch Lines (x4) | 1/4" coil or fabric hose 10–12 ft       | Reach each corner w/ slack |
| Chucks            | Locking air chucks (straight)           | Uniform clamp force        |
| Center Block      | Bleed + gauge (liquid filled 0–100 psi) | Group equalization         |

Log gauge vs TPMS variance on first use; adjust calibration table.

## Mounting & Heat Considerations

- Maintain ≥1" clearance from exhaust components.
- Add reflective barrier if radiant temp > 180°F at compressor intake after grade climb test.
- Verify duty cycle at end of 4-tire fill: surface temp < 220°F (IR thermometer).

## Moisture & Corrosion (PNW)

| Risk                | Mitigation                                           |
|---------------------|------------------------------------------------------|
| Moist air ingestion | Remote filter, drain manifold quarterly              |
| Coupler corrosion   | Stainless quick connects, silicone grease light film |
| Hose mildew         | Dry harness fully before storage, breathable bag     |

## Future-Proofing for Air Bags

| Item                | Placeholder              | Notes                        |
|---------------------|--------------------------|------------------------------|
| Regulator           | 0–100 psi mini w/ gauge  | Inline before bag lines      |
| Lines               | 1/4" DOT push-to-connect | Reuse existing manifold port |
| Solenoid (optional) | 12V for cab control      | Add fused trigger            |

## Bill of Materials (Initial)

| Category   | Item                             | Qty   | Est Weight | Est Cost | Notes               |
|------------|----------------------------------|-------|-----------:|---------:|---------------------|
| Compressor | ARB Twin CKMTA12                 | 1     |      16 lb |     $640 | Includes harness    |
| Mount      | Bracket (laser cut)              | 1     |       3 lb |     $120 | Under-hood kit      |
| Electrical | 6 AWG cable (red/black)          | 12 ft |       2 lb |      $45 | Oversize slightly   |
| Electrical | Fuse + holder 100A               | 1     |     0.2 lb |      $25 | Class at source     |
| Electrical | Relay 100A + socket              | 1     |     0.3 lb |      $30 | Weatherproof        |
| Pneumatic  | Manifold 6-port                  | 1     |     0.5 lb |      $30 | Aluminum            |
| Pneumatic  | Pressure switch 150/180          | 1     |     0.1 lb |      $30 | ARB std             |
| Pneumatic  | Safety relief 175 psi            | 1     |     0.1 lb |      $15 | Brass               |
| Couplers   | Stainless quick connect          | 2     |     0.3 lb |      $30 | M-style             |
| Harness    | 4-tire inflation kit (DIY parts) | 1     |       4 lb |     $140 | Build custom        |
| Filter     | Remote filter kit                | 1     |     0.4 lb |      $40 | Serviceable         |
| Misc       | Loom, clamps, heat shield        | 1 set |       1 lb |      $35 | Install consumables |

Initial Added Weight ≈ 28 lb (forward-biased). Track under Air category.

## Commissioning Checklist

| Step                     | Verification                     |
|--------------------------|----------------------------------|
| Torque manifold fittings | Leak-free (soapy water)          |
| Voltage drop @ full load | <0.6V battery→compressor         |
| Fill time test (4 tires) | Log stopwatch result             |
| Thermal check            | Surface temp < limit             |
| Noise assessment cab     | Acceptable (note dB if possible) |

## Gates & Triggers

| Gate            | Threshold              | Action                                   |
|-----------------|------------------------|------------------------------------------|
| Fill time gate  | >11 min for 4 tires    | Investigate leaks or upgrade tank assist |
| Heat soak gate  | >220°F compressor head | Add heat shield / cooldown cycle         |
| Electrical gate | Fuse trips             | Inspect inrush, cable sizing             |

## Open Decisions

| Decision                 | Options                           | Criteria                 | Status             |
|--------------------------|-----------------------------------|--------------------------|--------------------|
| ARB Twin vs Dual Viair   | Single unit vs modular redundancy | CFM sustained, packaging | Pending (lean ARB) |
| Under-hood vs Frame Rail | Access vs debris exposure         | Serviceability, cooling  | Pending            |

## Next Steps

1. Confirm compressor model (log in decision file).
2. Acquire BOM components.
3. Bench pre-assemble manifold; leak test before truck install.
4. Log first three fill cycles; append data to sag/usage logs.

Assumptions: Tire volume estimates; refine with actual size & pressure curve. Adjust wiring if run >8 ft (consider 4 AWG).
