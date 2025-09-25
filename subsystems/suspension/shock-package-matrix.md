# Shock Package Comparison Matrix

Objective: Compare candidate shock systems for the F-250 Tremor (stock leafs initially) to improve towing ride quality, washboard control, and future readiness for moderate added constant rear load (camper + gear est 600–800 lb). Keep lift ≤2" to avoid driveline complexity and maintain garage/ferry flexibility.

## Candidate Packages

| ID | Package                       | Front/Rear Shock Type           |                     Lift (in) | Service Interval           | Est System Cost (Installed) | Added Unsprung Wt (per corner) | Notes                                   |
|----|-------------------------------|---------------------------------|------------------------------:|----------------------------|----------------------------:|-------------------------------:|-----------------------------------------|
| S0 | Stock Tremor                  | OEM twin-tube                   |                             0 | N/A                        |                          $0 |                              0 | Baseline harsh high-speed washboard     |
| S1 | Fox 2.0 Performance (bolt-on) | 2.0 IFP                         |                             0 | 40–50k mi (inspect)        |                        $950 |                        +1.5 lb | Mild improvement; limited heat capacity |
| S2 | Carli Commuter 2.0            | 2.0 IFP tuned                   | ~2" front / 0–0.5" rear block | 30–40k mi                  |                      $2,400 |                          +2 lb | Comfort-focused; good small-bump        |
| S3 | Carli Backcountry 2.0         | 2.0 Remote (front) / IFP (rear) |                  ~2" / 0–0.5" | 20–30k mi (rebuild fronts) |                      $3,200 |                          +3 lb | Better heat & chatter control front     |
| S4 | Carli Pintop 2.5              | 2.5 Remote (King)               |                  ~2.5" / 0–1" | 15–25k mi                  |                      $4,800 |                          +6 lb | Large performance jump; more weight     |
| S5 | King 2.5 Custom (base valve)  | 2.5 Remote                      |               Variable 0–2.5" | 15–25k mi                  |                      $5,200 |                          +6 lb | Custom valving; requires tuning passes  |

## Evaluation Criteria Weights

| Criterion                           | Weight (1–5) | Rationale                    |
|-------------------------------------|--------------|------------------------------|
| Unladen Washboard Compliance        | 5            | Wife carsick risk mitigation |
| Towing Stability (Porpoise Control) | 5            | Priority ride outcome        |
| Service Interval / Maintenance Load | 4            | Min downtime                 |
| Cost vs Benefit                     | 4            | Budget disciplined           |
| Future Load Headroom                | 3            | Camper + gear growth         |
| Install Complexity                  | 2            | DIY vs shop time             |
| Added Unsprung Weight               | 2            | Steering & ride penalty      |

## Qualitative Scoring (1 Poor – 5 Excellent)

| Package            | Washboard | Towing Stability | Maintenance Burden (inverse) | Cost Efficiency | Load Headroom | Complexity (inverse) | Unsprung Weight (inverse) | Weighted Score* |
|--------------------|-----------|------------------|------------------------------|-----------------|---------------|----------------------|---------------------------|-----------------|
| S0 Stock           | 1         | 2                | 5                            | 5               | 2             | 5                    | 5                         | 2.9             |
| S1 Fox 2.0         | 2         | 2                | 4                            | 4               | 2             | 4                    | 4                         | 2.9             |
| S2 Commuter 2.0    | 4         | 3                | 4                            | 3               | 3             | 4                    | 4                         | 3.8             |
| S3 Backcountry 2.0 | 4         | 4                | 3                            | 3               | 3             | 3                    | 3                         | 3.9             |
| S4 Pintop 2.5      | 5         | 5                | 2                            | 2               | 5             | 2                    | 2                         | 4.0             |
| S5 King 2.5 Custom | 5         | 5                | 2                            | 2               | 5             | 1                    | 2                         | 3.8             |

*Illustrative—refine after empirical ride logging.

## Package Summaries

### S2 Carli Commuter 2.0

- Strength: Material comfort gain unladen; minimal unsprung weight increase.
- Limitation: Heat capacity limited in sustained corrugations vs remote res.
- Fit With Goals: Good first upgrade if sag data shows stock leafs acceptable.

### S3 Carli Backcountry 2.0

- Strength: Remote front improves high-speed chatter & heat; retains moderate cost.
- Limitation: Rear still IFP; towing porpoise improvement moderate.

### S4 Carli Pintop 2.5

- Strength: Broad performance envelope; strong towing and washboard control.
- Limitation: Cost + weight; faster rebuild cadence (revalve potential).

### S5 King 2.5 Custom

- Strength: Tailored valving for your weight curve & ride preference.
- Limitation: Requires tuning cycles; risk of ‘chasing setup’. Higher downtime.

## Gating Measurements Needed

| Measurement                                                 | Purpose                              | Gate Threshold                             |
|-------------------------------------------------------------|--------------------------------------|--------------------------------------------|
| Baseline front/rear unladen ride height                     | Track rake & spring pre-load         | Input to sag calc                          |
| Rear sag with camper typical load                           | Determine need for leaf pack vs bags | >1.5" sag triggers leaf/assist             |
| Towing pitch oscillation count (50–60 mph expansion joints) | Evaluate damping adequacy            | >3 oscillations post-bump triggers upgrade |
| Transmission temp towing (baseline)                         | 37" decision synergy                 | <215–225°F acceptable                      |

## Decision Flow

1. Collect baseline ride data (3 varied surfaces, notes of harshness, oscillations).
2. If unladen harshness primary & towing oscillation moderate → S2 or S3.
3. If towing oscillation severe & future 800 lb constant load probable → S4.
4. Defer S5 custom until stable constant load defined for at least 3 months.

## Maintenance & Rebuild Planning

| Package | Rebuild Interval (mi / hrs corrugation) | Typical Cost (pair)            | Downtime Mitigation        |
|---------|-----------------------------------------|--------------------------------|----------------------------|
| S2      | 40k–50k / low                           | Replace when performance fades | Keep stock as spare        |
| S3      | 25k–35k / moderate                      | $300–350                       | Stagger front pair service |
| S4      | 20k–25k / moderate-high                 | $400–500                       | Plan winter service window |
| S5      | 15k–25k / high                          | $450–550                       | Local tuner relationship   |

## Risk Notes

| Risk                                     | Mitigation                              |
|------------------------------------------|-----------------------------------------|
| Over-lifting front (>2.5")               | Choose springs matched to target height |
| Added unsprung weight reduces small bump | Balanced valving / tire pressure tuning |
| Premature shock fade on long washboard   | Remote reservoir & cooldown stops       |

## Next Data Actions

1. Populate ride log template (create if absent) with subjective 1–5 comfort scores.
2. Record towing oscillation metric on next trailer run.
3. Enter rear sag under load into `sag-rake-log.md`.

---
Assumptions: Future constant load 600–800 lb; confirm after camper + drawer decisions. Adjust scoring if load deviates >15%.
