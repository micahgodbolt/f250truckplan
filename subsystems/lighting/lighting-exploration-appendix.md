# Lighting System Exploration & Analysis

> Appendix document containing detailed analysis, alternative approaches, and exploratory content removed from main lighting plan to maintain focus on actionable decisions.

## Control Strategy Explorations

### Upfitter Switch Integration Complexity Analysis

**Challenge:** Engine bay upfitter switches → SP wedge lights = ~12 feet wiring

#### Wiring Route Options Explored
| Route                | Path Description                                                    | Pros                        | Cons                             | Difficulty  |
|----------------------|---------------------------------------------------------------------|-----------------------------|----------------------------------|-------------|
| **Interior**         | Engine bay → firewall grommet → under dash → behind rear seat → bed | Protected from elements     | Dash removal, interior panels    | Hard        |
| **Frame Rail**       | Engine bay → along frame rail → up to bed                           | Shorter distance, protected | Frame drilling, underbody work   | Medium      |
| **Existing Harness** | Piggyback on existing trailer/upfitter harness routes               | May exist already           | Limited capacity, shared routing | Easy-Medium |

#### Wire Specifications for Long Runs
| Load             | Distance | Voltage Drop Target | Recommended Gauge | Fuse Rating |
|------------------|----------|---------------------|-------------------|-------------|
| 50W Front Lights | ~12 feet | <3% (0.36V)         | 12 AWG            | 10A         |
| 25W Single Light | ~12 feet | <3% (0.36V)         | 14 AWG            | 5A          |

### Control Philosophy Options Considered

#### Option A: Direct Upfitter Switch Control
- **Wiring:** Run 12AWG from engine bay → through cab → to bed fuse block → to SP lights
- **Pros:** Simple switching, uses full aux switch capacity
- **Cons:** Long wire runs (~12 feet), larger gauge wire needed, harder to troubleshoot
- **Cost:** ~$60 in additional heavy gauge wire

#### Option B: Relay-Based Control
- **Trigger wiring:** Run small 18AWG from engine bay → bed area relay box  
- **Power wiring:** Heavy gauge from bed fuse block → relays → SP lights (short runs)
- **Pros:** Shorter heavy wire runs, easier troubleshooting, protects factory wiring
- **Cons:** Additional relay complexity, more components
- **Cost:** ~$40 in relays + $30 in wire

#### Option C: Hybrid Approach
- **High-power SP lights:** Bed panel control only (no aux switch connection)
- **Aux switches:** Control other bed-area lights via relays (shorter runs to side/rear lights)
- **Pros:** Reduces complex wiring, still uses aux switches meaningfully
- **Cons:** SP lights not controllable from dash

## SP Remote Integration Research

### SP Wedge Remote Capability Analysis
- **Question:** Max switching capacity of SP remote outputs?
- **Question:** Can SP outputs handle 20W scene lights directly?
- **Question:** Is there SP-compatible relay module for higher loads?
- **Question:** What's practical remote range for camp use?

### Power Integration Options Evaluated
| Option          | Description                                                 | Pros                                    | Cons                                  |
|-----------------|-------------------------------------------------------------|-----------------------------------------|---------------------------------------|
| **SP Direct**   | Camp lights powered through SP's switched outputs           | Simple wiring, integrated remote        | Limited by SP's switching capacity    |
| **SP + Relays** | SP triggers external relays for high-power camp lights      | Full remote capability, higher capacity | More complex, additional components   |
| **Hybrid**      | Low-power lights direct, high-power via SP-triggered relays | Optimized complexity vs capability      | Need to determine SP switching limits |

## Detailed Operational Scenarios (Pre-Decision)

### Scenario Analysis: SP Remote Integration
**Scenario 1: Night Trail Driving**
- Aux 5 (Front Driving): ON - Primary forward illumination
- Aux 6 (Ditch/Spot): ON - Long-range supplementation  
- All camp lights: OFF
- **Result:** Maximum forward visibility, no distracting camp lighting

**Scenario 2: Camp Arrival (Remote Setup)**
- **SP Remote:** Side scene (S1/S2) ON - Perimeter illumination from outside truck
- Aux 1 (Work Lights): ON if mechanical setup needed
- **Result:** Safe camp setup without entering cab to control lights

**Scenario 3: Camp Living (Evening)**
- **SP Remote:** Rear scene (R1/R2) ON - Warm cooking/social lighting
- **SP Remote:** Interior (I1-I4) dimmed - Subtle inside lighting
- All driving lights: OFF
- **Result:** Perfect camp ambiance, controlled remotely while outside

**Scenario 4: Mechanical Work (Day/Night)**
- Aux 1 (Work Lights): ON - Focused task lighting from dash
- **SP Remote:** Side scene ON if additional perimeter light needed
- **Result:** Bright work lighting, supplemented by remote camp lights

**Scenario 5: Security Check (Remote)**
- **SP Remote:** All perimeter lights (S1/S2, R1/R2) ON briefly
- Check camp area from distance
- **SP Remote:** Return to desired lighting level
- **Result:** Remote situational awareness without approaching truck

## Alternative Mounting Strategies Considered

### SP Wedge vs Bumper Integration
**SP Wedge Advantages:**
- Integrated with existing equipment
- Cleaner aesthetic than bumper add-ons
- Easier wiring runs (shorter distances to bed fuse block)

**Bumper Integration Advantages:**
- Simple wiring (3-4 foot runs from engine bay)
- Direct upfitter switch control
- No complex routing through cab/frame

## Decision Archive

**Key Decision:** Prioritize bumper-mounted solution for Phase 1 due to SP installation timing and wiring complexity unknowns.

**Rationale:** 
- Immediate implementation capability
- Known wiring routes and complexity
- Preserve options for SP integration post-installation
- Avoid engineering around unknown hardware configuration