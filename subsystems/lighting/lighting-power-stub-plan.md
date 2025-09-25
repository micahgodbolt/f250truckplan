# Lighting & Power Stub Plan

Objective: Pre-wire scalable, fused, labeled circuits for perimeter, work, and accessory loads (Starlink, GMRS, fridge, compressor control) minimizing future rework and preserving modularity within Super Pacific wedge. Interim power: Anker F2000 (portable). Future: Hard-mounted house battery system (timeline TBD).

## Strategy
- Run permanent low-voltage distribution backbone now (fused), even if some loads connect later.
- Keep high-current inverter & battery bank deferred until loads & duty cycle validated.
- Use marine-grade tinned copper; sealed connectors; service loops for panel removal.

## Circuit Inventory (Initial Provision)
| Circuit ID | Load Group                  | Est Continuous (A) | Peak (A) | Wire Gauge (one-way) | Fuse (A) | Switch Type                         | Notes                         |
|------------|-----------------------------|-------------------:|---------:|----------------------|---------:|-------------------------------------|-------------------------------|
| L1         | Front Scene (ditch + grill) |                  8 |       10 | 14 AWG               |       15 | Dash SPST + relay                   | Pair 25W LEDs                 |
| L2         | Side Scene (driver/pass)    |                  6 |        8 | 16 AWG               |       10 | Panel switch (2-pos)                | Shared both sides             |
| L3         | Rear Scene / Camp           |                  5 |        6 | 16 AWG               |       10 | Panel switch                        | Tailgate zone                 |
| L4         | Bed / Interior (SP wedge)   |                  3 |        3 | 18 AWG               |        5 | Dimmer (PWM)                        | Warm + task split later       |
| L5         | Rock / Courtesy (future)    |                  2 |        2 | 18 AWG               |        3 | Panel switch                        | Stub only now                 |
| P1         | Fridge Feed (future)        |                  5 |        7 | 10 AWG               |       15 | Relay (ignition isolation optional) | Anderson SB50 front of drawer |
| P2         | Starlink                    |                  6 |        7 | 12 AWG               |       10 | Panel switch                        | 12V converter mount roof pass |
| P3         | GMRS Radio                  |       6 (Tx burst) |       10 | 14 AWG               |       15 | Ignition-fed relay                  | Separate from L circuits      |
| P4         | Compressor Trigger          |                  1 |        2 | 18 AWG               |        3 | Dash switch to relay coil           | Main power via heavy feed     |
| AUX        | Expansion Spare 1           |                TBD |      TBD | 12 AWG               |       15 | None (capped)                       | Future lighting               |
| AUX2       | Expansion Spare 2           |                TBD |      TBD | 12 AWG               |       15 | None (capped)                       | Future water pump             |

## Distribution Layout
| Element               | Spec                                        | Location                       | Notes                       |
|-----------------------|---------------------------------------------|--------------------------------|-----------------------------|
| Main Feed (temporary) | 4 AWG from starter battery                  | Through firewall grommet       | Sized for future loads      |
| Master Fuse           | 125A MIDI ≤7" from battery                  | Engine bay                     | Protect downstream harness  |
| Bus / Fuse Block      | 12-circuit w/ negative bus (Blue Sea style) | Front bed bulkhead (protected) | Central service point       |
| Ground Reference      | 4 AWG to frame ground stud                  | Same side as feed              | Star washer, anti-corrosion |
| Conduit               | Split loom + PET braid outer                | High abrasion zones            | Label under loom ends       |

## Labeling & Documentation
| ID   | Label Text | Color Heatshrink | Documentation Ref   |
|------|------------|------------------|---------------------|
| L1   | FRONT-SCN  | White/Black      | Lighting Plan Table |
| L2   | SIDE-SCN   | White/Green      | Lighting Plan Table |
| L3   | REAR-SCN   | White/Yellow     | Lighting Plan Table |
| L4   | BED-INT    | White/Blue       | Lighting Plan Table |
| L5   | ROCK       | White/Violet     | Lighting Plan Table |
| P1   | FRIDGE     | White/Red        | Power Stub Table    |
| P2   | STARLINK   | White/Orange     | Power Stub Table    |
| P3   | GMRS       | White/Grey       | Power Stub Table    |
| P4   | AIR-TRIG   | White/Brown      | Air Spec            |
| AUX  | SPARE1     | White            | Expansion           |
| AUX2 | SPARE2     | White            | Expansion           |

## Roof / Pass-Through Planning
| Pass-Through | Loads                               | Seal Method           | Gauge       | Notes                         |
|--------------|-------------------------------------|-----------------------|-------------|-------------------------------|
| Roof Gland 1 | Starlink power, future solar input  | Marine gland + butyl  | 12 & 10 AWG | Separate solar positive route |
| Roof Gland 2 | Scene light harness (front & sides) | Adhesive base + gland | 14 AWG      | Keep slack loop               |

## Grounding Strategy
- Single primary chassis ground bonded to distribution negative bus; avoid multiple random grounds.
- Future house battery negative bonds at single point to avoid ground loops with inverter.

## Interim Power Integration (Anker F2000)
| Approach | Action |
|----------|--------|
| Fridge Early Use | Run via Anker 12V output → temporary 10 AWG lead; later migrate to P1 | Avoid double wiring |
| Lighting During Interim | Power block fed from battery (engine) not Anker | Maintain isolation |
| Transition Trigger | When >48h engine-off runtime becomes requirement | Initiate house battery project |

## Moisture & Corrosion
| Risk | Mitigation |
|------|------------|
| Condensation in canopy | Drip loops + sealed heatshrink ends | Prevent wicking |
| Salt mist (ferries) | Dielectric grease on exposed terminals | Annual inspection |

## Wire Gauge Justification
Using <3% voltage drop target at full load for longest run (~15 ft one-way P1 fridge feed). 10 AWG meets drop constraint at 7A continuous.

## Installation Sequence
1. Route main feed + ground; install master fuse (leave disconnected at battery until final test).
2. Mount fuse block; terminate feed & ground.
3. Pull individual circuits (leave +3 ft service loop at load zones) and label both ends.
4. Terminate low current circuits (lighting) with weather-pack connectors; cap unused spares.
5. Continuity & polarity test each circuit; then connect master fuse.
6. Functional test loads (where present); document initial amp draw.

## Commissioning Checklist
| Step                                           | Result |
|------------------------------------------------|--------|
| All labels legible & heatshrink recovered      |        |
| Voltage drop test P1 (simulated 7A)            | <0.5V  |
| Fuse value match table                         |        |
| No abrasion points (visual)                    |        |
| Moisture ingress check roof glands (hose test) |        |

## Expansion Reserve
Spare circuits sized to handle future water pump (~8A) or rear inverter control. Additional high-current (≥150A) inverter feed will bypass current block and use separate Class-T fuse & 4/0 cable (deferred).

## Open Decisions
| Decision              | Options                            | Criteria                     | Status  |
|-----------------------|------------------------------------|------------------------------|---------|
| Scene Light Brand     | Diode Dynamics vs Baja Designs     | Lumens/W, beam pattern, cost | Pending |
| Fridge Connector Type | Anderson SB50 vs SB30              | Current rating, form factor  | Pending |
| Roof Harness Path     | Exterior channel vs interior chase | UV exposure, serviceability  | Pending |

## Next Steps
1. Confirm final fridge location footprint (tie into storage gate doc).
2. Choose scene light brand; update BOM & decision log.
3. Procure wire, block, connectors; begin install with feed & block only.
4. Log actual current draws post-install; update table if variance >15%.

Assumptions: Ambient moderate; adjust fuse sizing if continuous ambient > 100°F (derate). Final inverter system deferred pending load modeling.
