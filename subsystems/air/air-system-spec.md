# Onboard Air System Specification

## Project Summary

| Aspect                | Details                                                                |
|-----------------------|------------------------------------------------------------------------|
| **Total Cost Est**    | **$1,135 - $1,355** (depending on bracket source)                      |
| **Added Weight**      | **~28 lbs** (forward-biased, engine bay mount)                         |
| **Install Time**      | **12-16 hours** (2-3 weekends: electrical + pneumatic + commissioning) |
| **Build Phase**       | **Phase 1 (Foundation)** - Early implementation recommended            |
| **Dependencies**      | Aux fuse block install, basic electrical skills or shop assistance     |
| **Skill Level**       | **Intermediate** (12V wiring, basic pneumatic fittings, drilling)      |
| **Professional Work** | **Optional**: Main power wiring if uncomfortable with 100A circuits    |
| **Commissioning**     | **2-3 trail sessions** to validate performance & tune system           |

### Phasing Rationale
**Install Early (Phase 1)** because:
- Enables tire pressure tuning from Day 1 (immediate trail benefit)
- Foundation for future air bags & pneumatic tools
- No dependencies on other major systems
- Learning curve best tackled before more complex builds
- Electrical backbone useful for subsequent electrical phases

---

## Objective
Enable simultaneous 2–4 tire inflation with future compatibility for rear helper air bags and light pneumatic tools while controlling weight and electrical load. Target fill: 37" (future) or current Tremor-sized tires from trail (~18 psi) to road (~65 psi rear / 60 psi front) in ≤ 10 minutes total (4-tire manifold) under moderate ambient (60–80°F).

## Architecture Summary

| Component             | Spec                                       | Est Cost | Rationale                       | Notes                                 |
|-----------------------|--------------------------------------------|----------|---------------------------------|---------------------------------------|
| Compressor            | ARB Twin CKMTA12 (locked choice)           | **$640** | High CFM for parallel inflation | ~6.2 CFM @ 0 psi, ~4.7 @ 29 psi       |
| Mount Location        | Under hood (passenger fender) preferred    | $80-200  | Short cable run, airflow        | Validate heat soak after trail climbs |
| Air Manifold          | 6-port aluminum block w/ 1/4" NPT          | **$30**  | Future lockers / bags reserved  | Cap unused with thread seal           |
| Hose Routing          | Removable 4-tire whip manifold (¼" ID)     | **$140** | Even pressure equalization      | Bleed valve built-in                  |
| Quick Couplers        | Industrial (Type M) front & rear bulkheads | **$30**  | No hood opening needed          | Stainless for corrosion resistance    |
| Pressure Switch       | 150 psi on / 180 psi off                   | **$30**  | Standard for compressor kits    | Matched to safety valve               |
| Safety Relief         | 175–180 psi                                | **$15**  | Overpressure protection         | Mount directly on manifold            |
| Air Filter Relocation | Snorkel-style remote filter                | **$40**  | Cleaner intake                  | Serviceable element                   |
| Electrical Feed       | 6 AWG pos/neg + 100A fuse/relay            | **$100** | Min voltage drop                | 100A fuse @ battery                   |
| Control               | Dash switch (sealed) via relay             | **$30**  | Operator convenience            | Add secondary kill near compressor    |

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

## Bulkhead Coupler System Design

### Front Bulkhead Location Options
| Location                    | Pros                  | Cons                    | F-250 Specific Notes             |
|-----------------------------|-----------------------|-------------------------|----------------------------------|
| Behind grille (center-low)  | Protected, clean look | Requires grille removal | Good access, avoid crash sensors |
| Front bumper side           | Easy access, visible  | Exposed to debris       | Consider bumper upgrade path     |
| Inner fender (pass through) | Very protected        | Harder to locate/access | Tremor skid may interfere        |

**Recommendation**: Behind grille, passenger side of center - balances protection with access.

### Rear Bulkhead Location Options  
| Location               | Pros                       | Cons                        | F-250 Specific Notes         |
|------------------------|----------------------------|-----------------------------|------------------------------|
| Bed side (driver rear) | Easy truck-side access     | Exposed, bed liner issues   | Clear of spare tire mount    |
| Tailgate (center)      | Central, protected when up | Tailgate removal complexity | Wiring harness consideration |
| Under bed rail         | Very protected             | Harder access, dirt buildup | Good for permanent install   |

**Recommendation**: Bed side driver rear - easiest access for solo operation, clear sight lines.

### Bulkhead Components & Installation

| Component            | Spec                             | Installation Notes                    |
|----------------------|----------------------------------|---------------------------------------|
| Quick Coupler (male) | Stainless M-type bulkhead mount  | Through-hole with backing plate       |
| Air Line             | 3/8" push-to-connect to 1/4" NPT | Use thread sealant + backup wrench    |
| Backing Plate        | 2" x 2" stainless or aluminum    | Distribute load, prevent pull-through |
| Dust Cap             | Threaded or snap-on cover        | Keep debris out when not in use       |
| Routing Protection   | Split loom + P-clamps every 18"  | Protect from abrasion & heat          |

### Air Line Routing Strategy

**Engine Bay → Front Bulkhead** (Short Run ~3 ft)
- Route along passenger fender inner
- Avoid exhaust heat zones
- Secure with existing mounting points
- Use vibration damping grommets

**Engine Bay → Rear Bulkhead** (Long Run ~12 ft)  
- Follow existing harness routing under truck
- Cross frame at transmission crossmember area
- Avoid exhaust, driveshaft clearance
- Protect with abrasion sleeve in critical areas
- Consider stainless brake line if stone damage risk high

### Usage Workflow
1. **Connect harness** to convenient bulkhead (front for front work, rear for camp/trailer)
2. **Deploy 4-tire manifold** from either connection point
3. **Equalize pressure** across all tires simultaneously  
4. **Disconnect & store** - no hood access needed

## 4-Tire Inflation Harness

| Component         | Spec                                    | Notes                      |
|-------------------|-----------------------------------------|----------------------------|
| Main Trunk        | 3/8" lightweight hybrid hose            | Reduce pressure drop       |
| Branch Lines (x4) | 1/4" coil or fabric hose 10–12 ft       | Reach each corner w/ slack |
| Chucks            | Locking air chucks (straight)           | Uniform clamp force        |
| Center Block      | Bleed + gauge (liquid filled 0–100 psi) | Group equalization         |

Log gauge vs TPMS variance on first use; adjust calibration table.

## Mounting Options & Brackets

### ARB Twin Mounting Solutions for F-250

| Option                    | Source                         | Est Cost | Pros                            | Cons                       |
|---------------------------|--------------------------------|----------|---------------------------------|----------------------------|
| ARB OEM bracket           | ARB dealers                    | $80-120  | Direct fit, warranty support    | Limited F-250 availability |
| Off-road fab shops        | Local 4x4 shops                | $120-200 | Custom F-250 fit, local support | Varies by shop quality     |
| Online custom fabricators | Rago Fabrication, etc.         | $150-250 | Precision fit, proven designs   | Shipping time, no test fit |
| Universal + modification  | Amazon/eBay universal brackets | $40-80   | Cheap, available                | Requires welding/drilling  |
| DIY fabrication           | Steel supplier + welding       | $30-60   | Custom fit, learning experience | Requires welding skills    |

**Recommended Path**: Start with **ARB dealer inquiry** for F-250 Tremor-specific bracket. If unavailable, contact **local off-road fabrication shops** - they often have patterns for Super Duty engine bay mounts.

### Key Bracket Requirements
- **Load capacity**: 25+ lb static (ARB Twin + vibration)
- **Vibration isolation**: Rubber bushings or pads
- **Access clearance**: Service filter without removal
- **Heat zone**: Keep compressor >1" from exhaust components
- **Electrical routing**: Clean path for 6 AWG cables

### Popular F-250 Mounting Locations
1. **Passenger inner fender** - most common, good access
2. **Firewall area** - compact, but harder service access  
3. **Frame rail forward** - very solid, may require longer electrical run

## Heat Considerations

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

| Category   | Item                               | Qty   | Est Weight | Est Cost | Notes                  |
|------------|------------------------------------|-------|-----------:|---------:|------------------------|
| Compressor | ARB Twin CKMTA12                   | 1     |      16 lb |     $640 | Includes harness       |
| Mount      | Bracket (see mount options below)  | 1     |       3 lb |  $80-200 | F-250 engine bay fit   |
| Electrical | 6 AWG cable (red/black)            | 12 ft |       2 lb |      $45 | Oversize slightly      |
| Electrical | Fuse + holder 100A                 | 1     |     0.2 lb |      $25 | Class at source        |
| Electrical | Relay 100A + socket                | 1     |     0.3 lb |      $30 | Weatherproof           |
| Pneumatic  | Manifold 6-port                    | 1     |     0.5 lb |      $30 | Aluminum               |
| Pneumatic  | Pressure switch 150/180            | 1     |     0.1 lb |      $30 | ARB std                |
| Pneumatic  | Safety relief 175 psi              | 1     |     0.1 lb |      $15 | Brass                  |
| Couplers   | Stainless quick connect (bulkhead) | 2     |     0.3 lb |      $30 | M-style through-hole   |
| Couplers   | Backing plates & hardware          | 2     |     0.2 lb |      $15 | Stainless distribution |
| Air Lines  | 3/8" hose engine→bulkheads         | 15 ft |     1.5 lb |      $45 | Front 3ft + rear 12ft  |
| Protection | Split loom & P-clamps              | 1 set |     0.5 lb |      $25 | Line protection        |
| Harness    | 4-tire inflation kit (DIY parts)   | 1     |       4 lb |     $140 | Build custom           |
| Filter     | Remote filter kit                  | 1     |     0.4 lb |      $40 | Serviceable            |
| Misc       | Thread sealant, grommets           | 1 set |     0.5 lb |      $20 | Install consumables    |

**BOM Totals:**
- **Total Weight:** ~28 lbs (forward-biased, engine bay mount)
- **Total Cost:** $1,135 - $1,355 (depending on bracket source)
- **Core System:** $1,055 (excluding mount bracket)
- **Bracket Range:** $80 (ARB dealer) - $200 (custom fab) - $300 (premium)

Track under Air category in weight ledger.

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

| Decision                 | Options                           | Criteria                 | Status                 |
|--------------------------|-----------------------------------|--------------------------|------------------------|
| ARB Twin vs Dual Viair   | Single unit vs modular redundancy | CFM sustained, packaging | **Locked: ARB Twin**   |
| Under-hood vs Frame Rail | Access vs debris exposure         | Serviceability, cooling  | **Locked: Engine Bay** |
| Bracket Source           | ARB OEM vs Fab Shop vs DIY        | Cost vs fit vs timing    | Pending procurement    |

## Next Steps

1. Confirm compressor model (log in decision file).
2. Acquire BOM components.
3. Bench pre-assemble manifold; leak test before truck install.
4. Log first three fill cycles; append data to sag/usage logs.

Assumptions: Tire volume estimates; refine with actual size & pressure curve. Adjust wiring if run >8 ft (consider 4 AWG).
