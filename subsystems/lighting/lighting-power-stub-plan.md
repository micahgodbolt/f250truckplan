# Lighting & Power Stub Plan

**Objective:** Pre-wire scalable, fused circuits for lighting and accessories. Phase 1: Bumper bar + bed area lights. Phase 2: SP integration post-install.

## Finalized Light Layout

### Phase 1 Configuration (Immediate Implementation)
```
                    FRONT OF TRUCK
                         ╔═══╗
                    ┌────╫ C ╫────┐  
              ┌─────┴──[FB]──────┴─────┐  FB = Front Bumper Bar (150W)       
              │                         │  
      [S1]────┤                         ├────[S2] S = Side Scene (20W ea)
              │          BED            │    
      [W1]────┤                         ├────[W2] W = Work Lights (15W ea)
              │     ┌─────────────┐     │    
              │     │ Super Pac.  │     │    R = Rear Scene (20W ea)
              │     │   Wedge     │     │    I = Interior (8W total)
              │     └─────────────┘     │    
              └─────────[R1][R2]────────┘    
```

### Light Specifications
| Position  | Light Type       | Wattage  | Control            | Purpose         | Implementation               |
|-----------|------------------|----------|--------------------|-----------------|------------------------------|
| **FB**    | Front Bumper Bar | 150W     | Aux Switch 5 (40A) | Trail driving   | Phase 1 - Paladin curved bar |
| **S1/S2** | Side Scene       | 20W ea   | Bed Panel          | Camp setup      | Phase 1 - Bed rail mount     |
| **W1/W2** | Work Lights      | 15W ea   | Aux Switch 1 (25A) | Mechanical work | Phase 1 - Bed corner mount   |
| **R1/R2** | Rear Scene       | 20W ea   | SP Remote          | Camp lighting   | Phase 2 - SP integration     |
| **I1-I4** | Interior         | 8W total | SP Remote          | Inside tasks    | Phase 2 - SP integration     |

## Upfitter Switch Assignment (Tremor Factory)

**Confirmed Ratings:**
- Aux 1 & 2: 25A each
- Aux 3: 10A  
- Aux 4: 15A
- Aux 5 & 6: 40A each (continuous "hot switches")

**Phase 1 Assignment:**
- **Aux 5 (40A):** Front bumper bar (150W) - Primary driving light
- **Aux 1 (25A):** Work lights (30W total) - Mechanical tasks
- **Aux 2 (25A):** GMRS radio
- **Aux 3 (10A):** Air compressor trigger
- **Aux 4 (15A):** Spare
- **Aux 6 (40A):** Spare (future ditch lights or secondary driving)

## Control Strategy

**Dashboard Controls (Driving/Work):**
- Immediate access to front driving lights and work lights
- Engine bay to bumper = simple 3-4 foot wire runs

**SP Remote Controls (Camp):**  
- Rear scene lights for cooking/social area
- Interior lights for inside SP tasks
- Side scene lights for camp perimeter (evaluate post-SP install)

**Bed Panel Controls:**
- Power accessories (Starlink, fridge)
- Master disconnect

## Circuit Inventory (Updated with Control Strategy)
| Circuit ID  | Load Group   | Light Position        | Est Continuous (A) | Peak (A) | Wire Gauge | Fuse (A) | Switch Control | Light Specs        |
|-------------|--------------|-----------------------|-------------------:|---------:|------------|----------|----------------|--------------------|
| L1-DITCH    | Ditch Lights | D1, D2 (A-pillar)     |                  4 |        5 | 14 AWG     | 10       | Aux 5 (40A)    | 2×25W, 5000K spot  |
| L2-FRONT    | Front Scene  | G1, G2 (bumper/grill) |                  4 |        5 | 14 AWG     | 10       | Aux 6 (40A)    | 2×25W, 5000K flood |
| L3-SIDE     | Side Scene   | S1, S2 (bed sides)    |                  3 |        4 | 16 AWG     | 5        | Aux 2 + Panel  | 2×20W, 4000K wide  |
| L4-WORK     | Work Lights  | W1, W2 (bed corners)  |                2.5 |        3 | 16 AWG     | 5        | Aux 1 + Panel  | 2×15W, 5000K flood |
| L5-REAR     | Rear Scene   | R1, R2 (tailgate)     |                  3 |        4 | 16 AWG     | 5        | Panel switch   | 2×20W, 3000K warm  |
| L6-INTERIOR | Interior/Bed | I1-I4 (wedge area)    |                  1 |        1 | 18 AWG     | 3        | Panel dimmer   | 4×2W, 2700K warm   |
| P1         | Fridge Feed (future)        |                  5 |        7 | 10 AWG               |       15 | Relay (ignition isolation optional) | Anderson SB50 front of drawer |
| P2         | Starlink                    |                  6 |        7 | 12 AWG               |       10 | Panel switch                        | 12V converter mount roof pass |
| P3         | GMRS Radio                  |       6 (Tx burst) |       10 | 14 AWG               |       15 | Factory Aux Switch + relay          | Separate from L circuits      |
| P4         | Compressor Trigger          |                  1 |        2 | 18 AWG               |        3 | Factory Aux Switch + relay          | Main power via heavy feed     |
| AUX        | Expansion Spare 1           |                TBD |      TBD | 12 AWG               |       15 | None (capped)                       | Future lighting               |
| AUX2       | Expansion Spare 2           |                TBD |      TBD | 12 AWG               |       15 | None (capped)                       | Future water pump             |

## Essential Infrastructure

**Power Distribution:**
- 4 AWG main feed from starter battery through firewall grommet
- 125A master fuse in engine bay (≤7" from battery)
- 12-circuit fuse block at front bed bulkhead
- Single point chassis ground with star washer

**Wire Protection:**
- Marine-grade tinned copper throughout
- Split loom + PET braid in high-abrasion areas  
- Sealed connectors and service loops for component removal

## Tremor Factory Upfitter Switch Integration

The F-250 Tremor includes 6 factory upfitter switches providing a clean, integrated solution for controlling driving-related lights and accessories. These switches are located in the dash and connect to pre-wired circuits in the engine bay, making them ideal for triggering relays that control high-power loads from your house electrical system.

### Factory Upfitter Switch Specifications (Verified)
- **Quantity:** 6 switches (Aux 1-6)
- **Location:** Dashboard switch bank
- **Wire termination:** Engine bay junction box
- **Control capability:** Momentary or latching (programmable via FORScan)
- **Current ratings (factory):**
  - Aux 1: 25A
  - Aux 2: 25A  
  - Aux 3: 10A
  - Aux 4: 15A
  - Aux 5: 40A (continuous "hot switch")
  - Aux 6: 40A (continuous "hot switch")

### Optimized Aux Switch Assignment Plan

| Switch No. | Factory Rating | Priority Load             | Control Method     | Rationale                              |
|------------|----------------|---------------------------|--------------------|----------------------------------------|
| Aux 5      | 40A (hot)      | High-Power Driving Lights | Direct Control     | Utilize highest capacity for light bar |
| Aux 6      | 40A (hot)      | Front Scene Lights (L1)   | Direct Control     | Continuous operation capability        |
| Aux 1      | 25A            | Auxiliary Driving Lights  | Relay Trigger      | Good capacity for secondary lights     |
| Aux 2      | 25A            | Work Light Control        | Relay Trigger      | Camp setup lighting                    |
| Aux 4      | 15A            | GMRS Radio (P3)           | Ignition-fed Relay | Adequate for radio + antenna tuner     |
| Aux 3      | 10A            | Compressor Trigger (P4)   | Relay Trigger      | Lowest load - just trigger signal      |

### Control Strategy Options
**Option A: Direct Control (High-Power Lights)**
- Use Aux 5 & 6 (40A hot switches) to directly power light circuits
- Benefit: Eliminates relay complexity for primary driving lights
- Risk: Factory wiring carries full load current

**Option B: Relay Trigger Only (Recommended)**
- Use all aux switches as low-current relay triggers (~200mA)
- Benefit: Protects factory wiring, enables future expansion
- All high-power loads fed through bed-area fuse block

### Wiring Integration Strategy & Complexity Analysis

**Challenge:** Upfitter switches terminate in engine bay, but SP wedge lights are ~8 feet away in bed area.

#### Option A: Direct Upfitter Switch Control (Simplest)
- **Wiring:** Run 12AWG from engine bay → through cab → to bed fuse block → to SP lights
- **Pros:** Simple switching, uses full aux switch capacity
- **Cons:** Long wire runs (~12 feet), larger gauge wire needed, harder to troubleshoot
- **Cost:** ~$60 in additional heavy gauge wire

#### Option B: Relay-Based Control (Recommended)
- **Trigger wiring:** Run small 18AWG from engine bay → bed area relay box  
- **Power wiring:** Heavy gauge from bed fuse block → relays → SP lights (short runs)
- **Pros:** Shorter heavy wire runs, easier troubleshooting, protects factory wiring
- **Cons:** Additional relay complexity, more components
- **Cost:** ~$40 in relays + $30 in wire

#### Option C: Hybrid Approach (Compromise)
- **High-power SP lights:** Bed panel control only (no aux switch connection)
- **Aux switches:** Control other bed-area lights via relays (shorter runs to side/rear lights)
- **Pros:** Reduces complex wiring, still uses aux switches meaningfully
- **Cons:** SP lights not controllable from dash

### Practical Wiring Route Analysis

**Engine Bay → Bed Area Path Options:**

| Route                | Path Description                                                    | Pros                        | Cons                             | Difficulty  |
|----------------------|---------------------------------------------------------------------|-----------------------------|----------------------------------|-------------|
| **Interior**         | Engine bay → firewall grommet → under dash → behind rear seat → bed | Protected from elements     | Dash removal, interior panels    | Hard        |
| **Frame Rail**       | Engine bay → along frame rail → up to bed                           | Shorter distance, protected | Frame drilling, underbody work   | Medium      |
| **Existing Harness** | Piggyback on existing trailer/upfitter harness routes               | May exist already           | Limited capacity, shared routing | Easy-Medium |

**Recommended Approach:** Use existing trailer wiring harness route if available, otherwise interior route with proper grommets and protection.

### Optimized Control Strategy (SP Remote Integration)

**Dashboard Upfitter Switches → Driving/Work Lights**
- Aux 5 (40A): Front driving lights (F1/F2) - primary trail illumination
- Aux 6 (40A): Ditch/spot lights (D1/D2) - supplemental driving  
- Aux 1 (25A): Work lights (W1/W2) - mechanical tasks, setup
- Aux 2-4: Radio, compressor, other accessories

**SP Remote Control → Camp/Scene Lights**
- Side scene lights (S1/S2): Remote controlled for camp perimeter
- Rear scene lights (R1/R2): Remote controlled for cooking/social area
- Interior lights (I1-I4): Remote controlled for inside tasks

**Key Benefits of This Separation:**
- **Driving lights:** Instant dash access while driving (critical for safety)
- **Camp lights:** Remote control from outside truck during setup/use
- **No complex cab routing** for camp lights (SP handles the remote switching)
- **Logical use patterns:** Drive lights when driving, camp lights when camping
- **SP integration:** Leverages existing remote capability you already have

**Wiring Simplification:**
- **Short runs:** Engine bay → bed area for driving/work lights only
- **SP integration:** Camp lights connect to SP's remote-capable outputs
- **No interior routing** needed for remotely controlled camp lights

### Control Philosophy
- **Driving Lights:** Factory dash switches for immediate driver access (Aux 1-3)
- **Camp Lighting:** Bed-area panel switches for setup convenience (L2-L5 circuits)  
- **Hybrid Loads:** Radio/compressor benefit from both dash control and bed-area master disconnect
- **Safety:** All switches return to OFF when ignition cycled (prevents battery drain)

### Programming Notes (FORScan)
- Configure aux switches as latching (not momentary) for lighting loads
- Enable "Memory" function to retain switch states during engine restart
- Disable aux switch operation when truck is off (prevent battery drain)
- Test switch operation before finalizing relay assignments

### Design Decision: Direct vs Relay Control

**Key Finding:** Aux 5 & 6 are 40A "hot switches" with continuous operation capability - significantly higher than typical aux switch ratings.

**Option A: Hybrid Approach**
- Direct control high-power driving lights via Aux 5 & 6 (40A)
- Relay control for all other loads via Aux 1-4
- Pro: Maximum simplicity for primary driving lights
- Con: Factory wiring carries full current, less future flexibility

**Option B: Full Relay Control (Recommended)**  
- All aux switches as relay triggers only
- Pro: Protects factory wiring, maximum expansion capability
- Con: Slightly more complex wiring, additional relays required

## Implementation Plan

### Phase 1 Priorities (Immediate)
1. **Front bumper bar installation** (F150LEDs Paladin 150W)
   - Direct connection to Aux 5 (40A)
   - Simple 3-4 foot wire run from engine bay
   - Immediate driving light capability

2. **Work light installation** 
   - Mount at bed front corners
   - Connect to Aux 1 (25A) via relay
   - Engine bay tasks and camp setup

3. **Bed area fuse block setup**
   - Central distribution point for all bed lighting
   - Future-ready for SP integration

### Phase 2 Gates (Post-SP Install)
1. **Assess SP remote capabilities**
   - Determine switching capacity for camp lights
   - Evaluate remote control integration options

2. **Install remaining camp lights**
   - Side scene lights (evaluate: upfitter vs SP control)
   - Rear scene lights (SP remote control)
   - Interior lights (SP remote control)

### Installation Sequence
1. Install bed area fuse block and main power feed
2. Install front bumper bar with upfitter switch connection  
3. Install work lights with upfitter switch connection
4. Test and document Phase 1 functionality
5. **Phase 2 Gate:** SP installation and capability assessment
6. Complete camp lighting integration based on SP capabilities

## Next Steps
1. **Procure Phase 1 components:** Paladin bumper bar, work lights, fuse block
2. **Install Phase 1 lighting** (bumper bar + work lights)
3. **Test upfitter switch operation** and document current draws
4. **Schedule SP installation** and lighting integration assessment

> **Detailed explorations and alternative approaches moved to:** `lighting-exploration-appendix.md`
