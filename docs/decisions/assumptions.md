# Assumptions Register (Provisional – Awaiting Field Data)

Purpose: Explicitly list the temporary stand‑ins we are using so we can keep designing the overland build before scale / sag / temp measurements are available. Each assumption has: Rationale, Risk if Wrong, Validation Method, Target Date.

 Update cadence: Review whenever a new real measurement is captured or before committing a purchase > $500 or >40 lb.

| ID  | Domain                | Assumption (Provisional Fact)                                                                                   | Rationale / Source                                                              | Risk If Wrong                                | Validation Method                     | Priority to Validate (H/M/L) | Status    |
|-----|-----------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------|------------------------------|-----------|
| A1  | Platform              | Axle ratio 4.30 w/ rear e-locker (FACT)                                                                         | Door sticker axle code 4M = 4.30 electronic locking rear (Ford axle code chart) | (Risk retired)                               | Visual verification complete          | —                            | Validated |
| A2  | Payload               | Payload sticker 3,030 lb (FACT)                                                                                 | User-provided sticker value                                                     | (Risk retired)                               | Visual confirmation (photo logged)    | —                            | Validated |
| A3  | Camper                | Super Pacific shell = 390 lb installed (net over bare bed)                                                      | Provided earlier                                                                | Real weight ±25 lb affects rear %            | Scale delta front/rear after install  | M                            | Active    |
| A4  | Constant Rear Load    | Steady expedition load (fridge + gear excl. passengers) 250–300 lb now; grows to 450–500 lb w/ recovery + power | Typical minimal kit path                                                        | Leaf pack timing misjudged                   | Cumulative ledger once gear purchased | M                            | Active    |
| A5  | Tongue Weight         | Travel trailer loaded tongue 850–900 lb (11–12%)                                                                | Target distribution for stability                                               | WDH tuning or payload buffer off             | 3‑pass scale sequence                 | H                            | Active    |
| A6  | Electrical Daily Draw | 45–55 Ah / 24h (fridge 2.0A avg + misc small loads) initial                                                     | Common 50L fridge + devices                                                     | Battery expansion decision delayed/early     | 48h shunt log                         | M                            | Active    |
| A7  | Inverter Need         | Keurig 1,500 W confirmed; microwave spec skipped; no simultaneous high draws                                    | User Keurig data; microwave answer = Skip                                       | Possible microwave surge under/over-sized    | Capture microwave nameplate later     | L                            | Partial   |
| A8  | Tire Use Profile      | 70% highway, 20% forest service washboard, 10% technical slow                                                   | Typical PNW weekend + trips                                                     | Shock valving choice mismatch                | Trip log categorization (3 trips)     | M                            | Active    |
| A9  | Garage / Height Limit | Actual current height 84"; within limit (FACT)                                                                  | User measurement; below 8'4" target                                             | (Risk retired)                               | Measurement provided                  | —                            | Validated |
| A10 | Winch Timing          | Winch deferred ≥ Phase 2 (after bumper choice)                                                                  | Weight-first discipline                                                         | Early front axle weight penalty              | Needs case analysis before purchase   | L                            | Active    |
| A11 | Rear Sag Behavior     | Camper + baseline gear < 1" added rear sag (no trailer)                                                         | Light initial load expectation                                                  | Underestimates need for spring solution      | Measure hub→fender set                | H                            | Active    |
| A12 | Transmission Temps    | Peak towing ATF < 215°F on representative grade with 35"                                                        | Normal for gas SD                                                               | 37" evaluation inaccurate                    | Temp log w/ OBD reader                | H                            | Active    |
| A13 | Budget Flow           | Year 1 discretionary: $20k; baseline ~$500/mo + larger fall lump (FACT)                                         | User input                                                                      | (Risk retired)                               | Budget review updates                 | —                            | Validated |
| A14 | Passenger Load        | Typical: 2 adults; Max: 2 adults + 2 teens + 2 dogs (~120 lb dogs) (UPDATED)                                    | User input expands occupancy range                                              | Max load reduces payload buffer for gear     | Track actual max trip occupancy       | M                            | Active    |
| A15 | Water Carry           | Start with 10–14 gal (84–117 lb) only on longer trips                                                           | Conservative initial approach                                                   | Underestimates need → extra fuel stops       | Track actual consumption trip logs    | L                            | Active    |
| A16 | Armor Scope           | Only trans, transfer, steering vulnerable early                                                                 | Risk probability moderate                                                       | Under-protect critical component             | Photo survey & trail type mapping     | M                            | Active    |
| A17 | Air System            | Dual compressor no tank adequate (8 tires cycle tolerance)                                                      | Prior builds & CFM estimates                                                    | Underestimates refill time frustration       | Time a full cycle after install       | L                            | Active    |
| A18 | Lighting Need         | Reverse/work + cargo lights yield 80% functional benefit                                                        | Prior experience                                                                | Future rework if forward throw needed sooner | Usage log (night tasks unlit)         | L                            | Active    |
| A19 | Fridge Size           | 45–50L adequate for 2–3 day runs (model TBD)                                                                    | Typical consumption; model not chosen                                           | Outgrows quickly for >5 day trips            | Select model & log power use          | L                            | Active    |
| A20 | Future Solar          | Portable 200W covers deficit until ≥3 stationary days appear                                                    | Alternator driving pattern                                                      | Over/under invest early                      | Energy balance after 3 trips          | M                            | Active    |
| A21 | Interim Power Source  | Anker Solix F2000 + extra 2048Wh pack will bridge initial season (FACT)                                         | Existing gear inventory (user)                                                  | Delays permanent 12V bank integration timing | Define switchover DoD / trip criteria | L                            | Validated |

## Pending User Inputs (What You Can Give Without a Scale Right Now)

Provide these and we can harden choices / pre-build wiring & mounting:

1. Payload sticker text (photograph / transcribe all lines including tire pressures).
2. Axle code from door jamb (two-character code) – unlocks exact ratio & diff type.
3. Current overall vehicle height (ground to tallest point) with camper installed.
4. Garage / ferry / parking height limit (if any different from assumption A9).
5. Annual budget & approximate monthly mod cashflow (fill A13 X value; list any earmarked big purchases already planned).
6. Appliance specifics: Fridge model, Keurig model, microwave nameplate watts (continuous + if surge given).
7. Typical max occupants & pet weight confirmation (validate A14 or adjust).
8. Trip profile details: Longest planned single remote stint (days) this year; coldest overnight °F; hottest expected cabin interior °F.
9. Trail difficulty intent (pick dominant two): Graded FS roads / Mild ruts / Moderate rock / Deep mud / Snow travel.
10. Noise tolerance for tires & suspension (Low / Medium / Don’t care) – influences shock valving aggressiveness.
11. Storage philosophy preference: Keep open bed modular (bins + L-track) vs commit to drawer system after Phase 1 (confirm).
12. Any must-integrate existing gear (compressor brand, recovery boards, radios, fridge you already own, etc.).
13. Acceptable maximum continuous air-up time for all truck tires (minutes) – will verify A17.
14. Fuel range goal between fill-ups while towing & while solo (miles target) – informs possible auxiliary fuel later.

## How We’ll Use These Inputs Immediately

| Input →            | Impacts                                | Decisions Unlocked                                 |
|--------------------|----------------------------------------|----------------------------------------------------|
| Payload sticker    | Accurate buffer math                   | Confidence in early armor & power weight allowance |
| Axle code          | Gear ratio confirmation                | 37" tire gearing viability pre-check               |
| Height & limits    | Rack / antenna / light bar constraints | Prevents accidental over-height planning           |
| Budget numbers     | Phase spend cadence                    | Which subsystem advances first if simultaneous     |
| Appliance specs    | Inverter continuous/surge confirmation | Lock wire gauge & fuse rating                      |
| Occupants          | Payload calc & seating storage trade   | Rear spring & drawer decisions                     |
| Climate extremes   | Battery sizing & insulation strategy   | Cold-weather power contingency                     |
| Trail intent       | Armor & suspension priority            | Choose shock package path early                    |
| Noise tolerance    | Tire model short list & shock valving  | Avoid regret re: aggressive patterns               |
| Storage philosophy | Delay or advance drawer engineering    | Weight & cost deferral plan                        |
| Existing gear      | Prevent duplicate purchases            | Update weight ledger placeholders                  |
| Air-up time target | Compressor CFM / dual vs single        | Electrical load planning                           |
| Range goal         | Optional jerry / aux tank gating       | Route planning support                             |

## Interim Design Actions We Can Proceed With (Even Before Data)

- Pre-draft inverter/charger wiring diagram using assumed 4/0 & Class-T 300A (will only adjust length-based voltage drop calc later).
- Shortlist 2–3 fridge mounting approaches (L-track brackets vs light frame) once model known.
- Create recovery kit BOM with weight placeholders (swap actual weights later).
- Prepare dual-compressor mounting mock layout (need only rough engine bay / frame rail measurement & photo later).
- Draft lighting harness plan (reverse/work circuits + future stubs) independent of exact light brand.
- Shock package comparison matrix (OEM vs Carli Backcountry vs Carli Pintop) using assumed loads to narrow valving direction.

## Validation Queue (Next Five Highest Priority Measurements When Possible)

1. Axle split baseline (scale) – unlocks true rear percentage & leaves spring path clarity.
2. Hub→fender unladen vs camper – validates A11 & front rake for any future front coil change.
3. Tongue weight actual – refine payload remaining & confirm WDH sizing.
4. Towing transmission sustained / peak temps – gating 37" tire feasibility.
5. 48h fridge + accessory Ah draw – confirms battery expansion threshold.

---

### Deferred / Skipped Inputs (Will Re-surface If They Become Gating)

| Related Q | Topic                        | Current Status | Reason Skipped / Impact                              | Revisit Trigger                              |
|-----------|------------------------------|----------------|------------------------------------------------------|----------------------------------------------|
| Q7        | Microwave nameplate watts    | Skip           | Inverter sizing still OK with Keurig 1500W alone     | If microwave added or inverter surge close   |
| Q10       | Longest engine-off camp days | Skip           | Solar / battery expansion uses DoD log later instead | If repeated >2 day stationary trips planned  |
| Q11       | Coldest / hottest temps      | Skip           | Default moderate climate assumptions retained        | If cold <20°F or hot >95°F trip scheduled    |
| Q25       | MPG floor                    | Skip           | Fuel economy not gating early component choices      | If considering 37" or armor weight tradeoffs |


When you provide any of the Pending Inputs, I'll replace the corresponding assumption row with an explicit fact and (if thresholds change) generate updated gating or priority shifts. Use the structured Q/A intake file: `docs/decisions/intake-questions.md` (created separately) for easy editing—just fill the Answer fields.

Feel free to just paste raw answers in a reply; exact formatting not required.
