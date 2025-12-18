# Science Olympiad Division B 2026: Solar System B Event
## Comprehensive Study Guide

---

## TABLE OF CONTENTS
1. General Engineering Principles
2. Spacecraft Design & Propulsion Systems
3. Telescope Design & Technology
4. Individual Mission Profiles
5. Key Formulas & Concepts
6. Cheat Sheet Points

---

# PART 1: GENERAL ENGINEERING PRINCIPLES

## 1.1 ORBITAL MECHANICS FUNDAMENTALS

### Kepler's Laws of Planetary Motion

**Kepler's First Law:** The orbit of each planet is an ellipse with the Sun at one focus. An ellipse is defined by two key parameters:
- **Semi-major axis (a):** Half the longest diameter of the ellipse
- **Eccentricity (e):** How stretched the ellipse is (e = 0 for circles, e approaches 1 for highly elongated ellipses)

**Kepler's Second Law:** A line connecting the planet to the Sun sweeps out equal areas in equal times. This means:
- Planets move faster when closer to the Sun (at perihelion)
- Planets move slower when farther from the Sun (at aphelion)
- This is a consequence of conservation of angular momentum

**Kepler's Third Law:** The square of a planet's orbital period is proportional to the cube of its semi-major axis:
\[T^2 \propto a^3\]

Where T is the orbital period and a is the semi-major axis.

### Orbital Parameters

- **Periapsis:** The closest point in an orbit to the central body
- **Apoapsis:** The farthest point in an orbit from the central body
- **Perigee/Apogee:** Specific terms for Earth orbits (periapsis/apoapsis)
- **Polar Orbit:** An orbit passing over both poles (passes over a planet's north and south poles)
- **Equatorial Orbit:** An orbit above the planet's equator

## 1.2 ORBITAL MANEUVERS AND DELTA-V

### What is Delta-V (Δv)?

Delta-v is the change in velocity required to perform a maneuver. It's measured in meters per second (m/s) and represents the spacecraft's "fuel budget."

**Key Concept:** Δv is not the same as actual change in velocity—it's the impulse needed.

### Hohmann Transfer Orbit

The most fuel-efficient way to transfer between two circular orbits:

1. Spacecraft in lower circular orbit fires engines to enter an elliptical transfer orbit
2. At the apoapsis of the transfer orbit, it fires again to enter the higher circular orbit
3. This creates an ellipse tangent to both orbits

**Why it matters:** Used by many space missions to reach their destinations with minimal fuel consumption.

**Formula for total Δv needed:**
\[\Delta v_{total} = \Delta v_1 + \Delta v_2\]

Where:
\[\Delta v_1 = \sqrt{\frac{GM}{r_1}} \left(\sqrt{\frac{2r_2}{r_1 + r_2}} - 1\right)\]

\[\Delta v_2 = \sqrt{\frac{GM}{r_2}} \left(1 - \sqrt{\frac{2r_1}{r_1 + r_2}}\right)\]

### Gravity Assists (Gravity Slingshot)

A spacecraft flies close to a planet to be propelled by its gravity, creating a "slingshot" effect:
- Increases spacecraft velocity without using propellant
- Used by Galileo (Venus and Earth flybys), Voyager 2, and New Horizons
- Critical for reaching distant planets efficiently

---

# PART 2: SPACECRAFT DESIGN & PROPULSION SYSTEMS

## 2.1 PROPULSION SYSTEMS

### Chemical Propulsion

**How it works:** Combustion of fuel and oxidizer creates hot, high-pressure gases expelled through a nozzle to produce thrust.

**Advantages:**
- High thrust for short periods
- Essential for launch and orbit insertion
- Proven, reliable technology

**Disadvantages:**
- Limited total impulse (amount of momentum that can be transferred)
- Heavy propellant requirements for long missions
- Lower specific impulse than ion thrusters

**Specific Impulse (Isp):** Measures propulsion efficiency (seconds of thrust per kg of propellant)
- Chemical rockets: ~300-450 seconds
- Ion thrusters: ~3000+ seconds

### Ion Propulsion (Electric Propulsion)

**How it works:** 
1. Propellant (usually Xenon) is ionized
2. Ions are accelerated through an electric field
3. High-speed ions expelled produce thrust through momentum conservation

**Advantages:**
- Much higher specific impulse (more efficient)
- Can operate for months or years
- Produces sustained, gentle thrust
- Perfect for deep-space missions
- Less propellant needed

**Disadvantages:**
- Very low thrust (about 1/20,000th of a pound force)
- Cannot overcome Earth's gravity for launches
- Requires reliable power source

**Examples:**
- **BepiColombo:** Uses solar electric propulsion with Xenon ion thrusters
- **Dawn:** First NASA mission to use ion propulsion for multi-target exploration

## 2.2 POWER SYSTEMS

### Solar Panels
- Generate electricity from sunlight
- Used on spacecraft near the Sun (Mercury, Venus, Earth, Mars missions)
- Efficiency decreases with distance from Sun
- Used by: Juno, Cassini (also has RTGs)

### Radioisotope Thermoelectric Generators (RTGs)
- Convert heat from radioactive decay into electricity
- Essential for distant missions (Jupiter, Saturn, beyond)
- Provide consistent power for decades
- Used by: Voyager 1 & 2, Cassini, New Horizons

**Example:** Voyager 2 has three RTGs, each providing ~157W at launch (halving every 87.7 years)

## 2.3 ATTITUDE CONTROL AND STABILIZATION

### Three-Axis Stabilization
Most modern spacecraft use three-axis stabilization:
- Maintains specific orientation relative to the Sun and a reference star
- Essential for pointing instruments accurately
- Uses:
  - **Reaction Wheels:** Spinning wheels that create torque
  - **Thrusters:** Small chemical rockets for attitude adjustments
  - **Star Trackers:** Identify guide stars for orientation reference
  - **Sun Sensors:** Maintain Sun-pointing capability

**Square Pyramidal Configuration:** Four reaction wheels in optimal arrangement (used in many modern spacecraft) for redundancy—if one fails, spacecraft can still maneuver.

### Spin Stabilization
Some spacecraft spin around a fixed axis:
- Maintains stability like a gyroscope
- Example: Galileo spacecraft rotated at 3 revolutions per minute
- Simpler than three-axis but less flexible

## 2.4 THERMAL CONTROL SYSTEMS

### Why It Matters
- In space, components face extreme temperatures (extreme heat from the Sun, extreme cold in shadow)
- Electronics and instruments require precise temperature control
- Without thermal control: component failure, degraded performance, mission failure

### Passive Thermal Control
**Multilayer Insulation (MLI) Blankets:**
- Multiple thin layers of material with low emittance
- Acts like thermal blankets
- No power required

**Radiators:**
- Metal surfaces (often flat-plate or structural panels) that emit excess heat as infrared radiation
- Heat radiates to space via infrared emission
- Most common method on spacecraft
- Can be fixed or deployable

**Surface Treatments:**
- **Optical Solar Reflectors (OSR):** Mirror-like surfaces that reflect solar heat
- **Second Surface Mirrors (SSM):** Reflect sunlight while allowing internal heat radiation

### Active Thermal Control
**Fluid Loops:**
- Single-phase loops: Pumped fluid circulates to transfer heat to radiators
- Two-phase loops: Heat pipes that passively move heat via phase change
- Example: International Space Station uses ammonia loops

**Electric Heaters:**
- Thermostatically controlled resistive heaters
- Keep equipment above minimum temperature during cold phases

## 2.5 SPACECRAFT ATTITUDE CONTROL ACTUATORS

### Reaction Wheels
- Spinning wheels mounted to spacecraft
- When wheel spins up, spacecraft rotates opposite direction
- Used for continuous attitude control
- Tetrahedral configuration: four wheels provide redundancy

### Thrusters
Used for:
- Attitude adjustment
- Orbit insertion burns
- Course corrections
- Trajectory modifications

**Types:**
- **Hydrazine thrusters:** Chemical monopropellant (Voyager, Cassini, many others)
- **Ion thrusters:** Electric propulsion (BepiColombo, Dawn)
- **Cold gas thrusters:** Simple pressurized gas systems

### Momentum Wheels and Control Moment Gyroscopes
- Store angular momentum
- Can be "unloaded" using thrusters to reset momentum

---

# PART 3: TELESCOPE DESIGN & TECHNOLOGY

## 3.1 OPTICAL PRINCIPLES

### Mirrors vs Lenses
- **Reflecting Telescopes (Mirrors):** Curved mirrors collect and focus light
  - Advantages: No chromatic aberration, can be larger, can be very precise
  - All large space telescopes use mirrors
  - Examples: Hubble, JWST, ground-based telescopes

- **Refracting Telescopes (Lenses):** Lenses bend light to focus
  - Advantages: Simpler construction
  - Disadvantages: Limited size due to gravity sag, chromatic aberration

### Key Mirror Specifications

**Surface Accuracy:**
- Hubble's primary mirror is so smooth that if expanded to Earth's diameter, bumps would only be 15 cm tall
- Must be polished to within nanometers (nm) accuracy
- 2200 nm error in Hubble's primary mirror caused the spherical aberration problem

**Mirror Coatings:**
- **Aluminum coating:** Provides reflectivity (typically 100 nm thick)
- **Magnesium fluoride coating:** Protects aluminum from oxidation, increases UV reflectivity

### Monolithic vs Segmented Mirrors

**Monolithic (Single-Piece) Mirrors:**
- Maximum practical size: ~8 meters diameter
- Examples: Hubble's primary (2.4m), Large Binocular Telescope (8.4m each)
- Advantages: Simpler construction and alignment
- Disadvantages: Heavy, expensive, structural sag under own weight

**Segmented Mirrors:**
- Array of smaller hexagonal or square mirror segments
- Can be much larger than monolithic mirrors
- Computer-controlled alignment using actuators
- Examples: Keck Observatory (10m segments), planned ELTs (30m+)
- Advantages: 
  - Can be arbitrarily large
  - Easier to fabricate individual segments
  - Lighter weight than monolithic equivalent
  - Easier to transport and install
- Disadvantages: 
  - Complex alignment system required
  - Higher cost due to control systems
  - Thermal environment and launch vibration can cause misalignment

## 3.2 ADAPTIVE OPTICS

### What is Adaptive Optics?

Technique to correct light distortion in real-time:

1. **Problem:** 
   - Atmospheric turbulence distorts starlight (for ground-based telescopes)
   - Thermal variations and launch vibrations cause mirror misalignment (for space telescopes)
   - Results in blurred images

2. **Solution:**
   - Measure wavefront distortion using a guide star (or reference)
   - Use deformable mirror to correct distortion
   - Adjustments made hundreds to thousands of times per second
   - Computer-controlled system maintains alignment

### Deformable Mirrors

**MEMS Deformable Mirrors:**
- Microelectromechanical Systems using tiny actuators
- Can adjust surface to nanometer precision
- Used in modern adaptive optics systems

**Magnetically Controlled Deformable Mirrors:**
- Use magnetic forces to deform mirror surface
- Example: ELT's M4 mirror has 5,000 magnets making adjustments 1,000 times per second to accuracy of tens of nanometers

### Why It Matters for Segmented Mirrors
- Compensates for misalignment of individual segments
- Corrects for wavefront aberrations from launch vibration and thermal effects
- Allows segments to maintain proper focus without complex manual alignment

## 3.3 INFRARED ASTRONOMY

### The Infrared Spectrum
- **Wavelengths:** 0.75 to 300 micrometers (μm)
- **Advantages:** 
  - Passes through dust clouds where visible light is blocked
  - Can observe cooler objects (brown dwarfs, protostars, galaxies)
  - Reveals "hidden" universe of star and planet formation

### Key Challenge: Heat Radiation

**The Problem:**
- Everything emits infrared radiation (thermal energy)
- At room temperature, the telescope itself emits infrared that overwhelms faint astronomical sources
- Solution: Cool the telescope to very low temperatures

### Cooling Strategies

**Passive Cooling:**
- Position telescope in space away from heat sources
- JWST orbits at L2 (Sun-Earth Lagrange Point 2) to get away from Earth and Moon heat

**Sunshield (JWST):**
- Large passive thermal barrier (size of tennis court: 21m × 14m)
- Five layers of Kapton membrane coated with aluminum and silicon
- Protects telescope from sunlight, Earth-light, and Moon-light
- Cools telescope to 40 Kelvin (−233°C)
- One of the most important enabling technologies for JWST

### Infrared Detectors
- Different from visible light detectors
- **HgCdTe arrays:** Common infrared detector material
- Must be kept very cold (liquid nitrogen or colder)
- Sensitive to specific infrared wavelength ranges

## 3.4 SUBMILLIMETER AND RADIO ASTRONOMY

### Radio/Millimeter/Submillimeter Telescopes
- Observe much longer wavelengths than visible light
- Can observe through dust, gas, and distant cosmic objects
- Different technology than optical telescopes

### Interferometry

**Concept:**
- Combine signals from multiple antennas
- Use mathematical analysis to create effective image resolution equivalent to telescope diameter equal to farthest distance between antennas
- Much cheaper than building one giant telescope

**Advantages:**
- Can achieve ultra-high resolution
- More economical than single large dish
- Flexible array configurations

**Example: ALMA (Atacama Large Millimeter/submillimeter Array)**
- 66 antennas working as interferometer
- Can be spaced from 150m to 16km apart
- Effective resolution equivalent to 16km diameter telescope
- Operates at wavelengths 3.6mm to 0.32mm
- Located at 5,000m elevation in Chilean Andes (dry, high location reduces atmospheric absorption)

---

# PART 4: INDIVIDUAL MISSION PROFILES

## SPACECRAFT MISSIONS

### BepiColombo

**Mission Goal:** Study Mercury close to the Sun; test Einstein's theory of general relativity

**Key Technical Features:**
- **Spacecraft Configuration:** Two separate spacecraft (MPO and MMO) each with own propulsion
- **Propulsion:** Solar Electric Propulsion Module (SEPM) with Xenon ion thrusters (290 mN thrust) plus chemical thrusters for orbit insertion
- **Journey:** 6.7-year cruise with 6 gravity assists (Venus twice, Mercury four times)
- **Power:** Solar panels (33 square meters of GaAs cells)
- **Attitude Control:** Four hydrazine thrusters in redundant pairs plus reaction wheels
- **Scientific Objectives:**
  - Study Mercury's interior structure and geology
  - Investigate magnetic field origin
  - Analyze exosphere composition and dynamics
  - Search for asteroids sunward of Earth
  - Test Einstein's theory via gravitational effects

**Cheat Sheet:** BepiColombo = extreme heat management, ion propulsion, multiple gravity assists

---

### Galileo

**Mission Goal:** Explore Jupiter and its moons; first spacecraft to orbit an outer planet

**Key Technical Features:**
- **Spacecraft:** Orbiter + atmospheric entry probe
- **Mass:** 2,562 kg combined at launch
- **Configuration:** Dual-spin stabilization (one section rotated at 3 rpm)
- **Journey:** Used gravity assists from Venus and Earth to reach Jupiter
- **Orbit Insertion:** Fired main engine at Jupiter to brake into orbit
- **Instruments:** 
  - Six instruments on rotating section for all-direction observation
  - Imaging systems
  - Atmospheric probe for direct composition measurement

**Notable Discoveries:**
- First asteroid flyby (951 Gaspra)
- First asteroid moon (Dactyl around 243 Ida)
- Observed Comet Shoemaker-Levy 9 collision with Jupiter
- Evidence for liquid oceans under Europa's ice surface
- Jupiter's dust ring system and magnetosphere mapping

**End of Mission:** Intentionally destroyed in Jupiter's atmosphere to avoid contaminating Europa's subsurface ocean

**Cheat Sheet:** Dual-spin stability, gravity assists, atmospheric probe design

---

### Juno

**Mission Goal:** Study Jupiter's origin, structure, atmosphere, and magnetic field

**Key Technical Features:**
- **Propulsion:** Main engine for 35-minute Jupiter Orbit Insertion burn
- **Orbit:** Polar elliptical orbit (unprecedented for Jupiter)
- **Spin Rate:** Increased to 5 rpm for stability during orbit insertion, reduced to 2 rpm for normal operations
- **Autonomous Operations:** JOI required autonomous sequence due to 48-minute communication delay—no real-time control possible

**Polar Orbit Advantages:**
- Best for mapping and monitoring
- Can observe polar magnetosphere and all latitudes
- Unlike Earth-orbiting satellites, Juno traverses pole-to-pole in north-south direction

**Science Goals:**
- Determine if Jupiter has rocky ice core
- Measure global water and ammonia in atmosphere
- Study convection and wind profiles
- Investigate Jovian magnetic field origin
- Explore polar magnetosphere

**Cheat Sheet:** Polar orbits best for mapping, autonomous spacecraft operations, communication delays

---

### Cassini-Huygens

**Mission Goal:** Explore Saturn system; first spacecraft to orbit Saturn

**Key Technical Features:**
- **Configuration:** Orbiter (Cassini) + Lander (Huygens probe)
- **Power:** Plutonium-powered RTGs (nuclear power)
- **Mission Duration:** 2004-2017 (13 years, 294 Saturn orbits)
- **Orbit Insertion:** Complex Saturn Orbital Insertion maneuver:
  - Oriented High-Gain Antenna away from Earth and along flight path (to shield instruments from ring particles)
  - Rotated again to point engine along flight path
  - Deceleration burn: 622 m/s to allow Saturn capture

**Huygens Probe:**
- First landing on a moon in outer solar system
- Parachuted to Titan surface in January 2005
- Transmitted data for 2.5 hours during descent
- Revealed methane lakes and liquid hydrcarbon surface

**Grand Finale (Final Mission Phase):**
- Executed 22 risky passes through gap between Saturn and inner rings
- Maximized scientific return before mission end
- Intentionally plunged into Saturn's atmosphere to avoid contaminating moons

**Scientific Achievements:**
- Mapped Saturn's rings in unprecedented detail
- Discovered six named moons
- Identified Enceladus and Titan as potentially habitable
- Measured Saturn's magnetosphere and atmosphere
- Determined ring mass

**Cheat Sheet:** Complex orbit insertion, RTG power for outer planets, atmospheric entry probes

---

### Voyager 2

**Mission Goal:** Explore outer planets; only spacecraft to visit ice giants (Uranus and Neptune)

**Key Technical Features:**
- **Power:** Three Multihundred-Watt RTGs (each ~157W at launch)
- **Propulsion:** 16 Hydrazine thrusters, later supplemented with 8 backup thrusters
- **Attitude Control:** Three-axis stabilization with:
  - Sun sensor for orientation reference
  - Canopus star tracker (maintains high-gain antenna pointing to Earth)
  - Gyroscopes for pitch and yaw control
- **Spacecraft Bus:** Decagonal prism shape
- **Journey:** Used gravity assists at each planet to reach next destination

**Propulsion Details:**
- Solid rocket motor (1,123 kg) + 8 hydrazine monopropellant engines (jettisoned after Jupiter burn)
- Four pitch/yaw engines, four roll engines
- Remaining 16 MR-103 thrusters for attitude control and trajectory corrections

**Scientific Achievements:**
- First and only close encounters with Uranus and Neptune
- Discovered 13 new moons
- Revealed ring systems of Uranus and Neptune
- Captured detailed images of Great Dark Spot on Neptune
- Currently in interstellar space (beyond solar system)

**Still Operating:** Still transmitting data after 47+ years using original power systems

**Cheat Sheet:** RTG power essential for deep space, multiple gravity assists, decades-long mission viability

---

### New Horizons

**Mission Goal:** First close exploration of Pluto; explore Kuiper Belt objects

**Key Technical Features:**
- **Design Lineage:** Based on CONTOUR and TIMED spacecraft from Johns Hopkins Applied Physics Lab
- **Propulsion System:** 
  - Used for course corrections only (not primary acceleration)
  - Jupiter gravity assist provided acceleration to Pluto
  - 93-second thruster burn to adjust trajectory (March 2010)
  - Final 23-second burn to fine-tune approach (June 2015)
  - 15-minute series of status burns to confirm successful flyby

**Hibernation Mode:**
- Spent most of journey in hibernation to preserve systems
- Annual brief checkups
- Revived for last time December 6, 2014

**Communication Delays:**
- At Pluto approach: 4 hours 25 minutes one-way delay
- Autonomous encounter sequence required (no real-time ground control)

**Pluto Flyby (July 14, 2015):**
- Closest approach: 4,800 miles (7,800 km) above surface
- Revealed diverse geologic features
- Images started showing Pluto details a month before encounter

**Extended Mission:**
- Redirected to Arrokoth (former KBO 2014 MU69) using trajectory adjustments
- Continues exploring Kuiper Belt objects

**Cheat Sheet:** Hibernation for long missions, autonomous autonomous sequences, Jupiter assists for deep space

---

### Dawn

**Mission Goal:** Explore two protoplanets of asteroid belt: Vesta and Ceres

**Key Technical Features:**
- **Historic Significance:** First NASA mission to use ion propulsion for primary propulsion
- **Propulsion:** Ion thrusters (not just for station-keeping)
- **Multi-Target Capability:** First spacecraft to orbit two separate celestial bodies
  - Previous multi-target missions (Voyager) could only do flybys due to chemical propulsion limitations
  - Ion propulsion allows entering and leaving orbits

**Trajectory:**
- Launched September 2007
- Entered Vesta orbit July 16, 2011 (14-month survey)
- Left Vesta late 2012 for Ceres
- Entered Ceres orbit March 6, 2015

**End of Mission:**
- Hydrazine fuel depleted November 1, 2018
- Remains in stable orbit around Ceres (derelict but harmless)

**Scientific Achievements:**
- First spacecraft to visit either Vesta or Ceres
- First to orbit dwarf planet
- Studied protoplanet geology and composition
- Mapped surface features

**International Collaboration:** NASA, ESA, Italian, German, French, and Dutch components

**Cheat Sheet:** Ion propulsion enables multi-target missions, asteroid science, can enter/leave orbits

---

### Lunar Reconnaissance Orbiter (LRO)

**Mission Goal:** Comprehensive lunar reconnaissance; prepare for future human missions

**Key Technical Features:**
- **Launch Mass:** ~1,480 kg (Delta II launch vehicle)
- **Orbit Transfer:** Direct lunar transfer (minimum energy trajectory, ~4 days)
- **Orbit Insertion:** 4 maneuvers over 2-4 days using onboard propulsion
- **Operational Orbit:** Circular polar mapping orbit at 50 km altitude
  - Nominal: 50 ± 20 km altitude
  - Quasi-frozen orbit to maintain consistent geometry

**Commissioning Process:**
- Initial orbit: 30 km × 216 km (elliptical)
- Series of maneuvers to circularize at 50 km
- Commissioning phase: up to 60 days in circular orbit before nominal operations

**Scientific Instruments:**
- Multiple cameras and spectrometers for detailed lunar mapping
- Thermal imaging (Diviner) to measure surface temperature
- Radar for subsurface composition

**Station-Keeping:**
- Periodic maneuvers to maintain orbit against perturbations
- Momentum management to prevent reaction wheel saturation

**Cheat Sheet:** Polar lunar orbits, station-keeping requirements, direct transfer trajectories

---

### Hayabusa

**Mission Goal:** First asteroid sample return mission

**Key Technical Features:**
- **Propulsion:** Ion engines with four thruster heads on two-axis gimbal plate
- **Target:** Asteroid 25143 Itokawa (550m × 180m)
- **Sample Collection:** Autonomous sampling horn deployment
  - Expected collection: <1 gram of material
  - Used particles kicked up by impact rather than explosives

**Landing Challenge:**
- Controlled landing on asteroid (first ever)
- Extremely low surface gravity required precise navigation
- Spacecraft reduced descent to 3 cm/sec near surface
- Released target marker 40 meters above surface
- First touchdown: ~10 cm/sec, bounced multiple times
- Settled within 30m of target marker

**Problems Encountered:**
- Ion engine failures (lost three of four neutralizers)
- Sample collector failure
- Spacecraft became lost after second touchdown
- Spacecraft bounced several times, settled at polar region
- Waited nearly 30 minutes for emergency lift command

**Successful Return:**
- June 13, 2010: Returned to Earth over Australian desert
- Sample capsule recovered ~500m from predicted location
- Contained thousands of small particles from asteroid
- Confirmed very primitive carbonaceous asteroid composition

**Legacy:**
- Demonstrated asteroid sample return is possible
- Paved way for Hayabusa2 (improved design, successful sample return)
- Proved ion propulsion viability for asteroid missions

**Cheat Sheet:** Low-gravity landing challenges, sample return capsules, ion propulsion for asteroids

---

### Deep Impact

**Mission Goal:** Probe interior composition of comet Tempel 1

**Key Technical Features:**
- **Unique Design:** Two-section spacecraft
  - **Flyby spacecraft:** 601 kg section for remote observations
  - **Smart Impactor:** 372 kg copper-core projectile that hit the comet

**Impactor Design:**
- **Cratering Mass:** 100 kg of pure copper (NOT explosive)
- Material composition: 49% copper, 24% aluminum
- Copper chosen because:
  - Not expected on comet (won't interfere with spectroscopy)
  - Cheaper than explosives for creating impact
  - Creates distinctive signature in post-impact analysis

**Trajectory Corrections:**
- Up to 4 trajectory adjustments between release and impact
- Final targeting maneuver: 6 m/s velocity change (June 23, 2005)
- Impactor aimed for ~100 km-wide window in space

**Instruments:**
- High Resolution Imager (HRI): Visible camera + infrared spectrometer (1.05-4.8 μm)
- Medium Resolution Imager (MRI): Backup imager for navigation
- Impactor Targeting Sensor (ITS): Identical to MRI but without filter wheel

**Impact (July 4, 2005):**
- Released impactor to strike comet
- Flyby spacecraft observed impact from safe distance
- Collected data on interior composition, dust ejection, heat generation

**Extended Mission:**
- Later extended mission planned to do flyby of Comet Boethin (at $40 million cost, reduced mission)
- Would use spectrometer to study comet composition and surface features

**Cheat Sheet:** Impact missions for scientific study, autonomous navigation required, composition analysis via spectroscopy

---

## TELESCOPE MISSIONS

### Hubble Space Telescope (HST)

**Mission Goal:** Observe universe at visible and ultraviolet wavelengths from space

**Key Technical Features:**
- **Primary Mirror:** 2.4 meters diameter, monolithic glass
- **Mirror Coating:**
  - Aluminum layer: 3/1,000,000th inch thick (provides reflectivity)
  - Magnesium fluoride layer: coated on top (protects from oxidation, enhances UV reflectivity)
- **Mirror Smoothness:** So smooth that if expanded to Earth's diameter, largest bumps would be 6 inches (15 cm) tall

**The Spherical Aberration Problem:**
- **The Error:** Outer edge of primary mirror polished too flat by ~2,200 nm (1/450 mm)
- **Cause:** Incorrect assembly of custom reflective null corrector during polishing
- **Impact:** Severe spherical aberration—light from mirror edge focused at different point than light from center
- **Solution:** Correction optics (essentially "spectacles") installed via Hubble Servicing Mission 1 (1993) to compensate
- **Design Innovation:** Corrective optics built with same error in opposite direction

**Testing Problem that Went Unnoticed:**
- Some conventional null correctors gave correct readings indicating spherical aberration
- But results were dismissed because reflective null corrector (thought more accurate) disagreed
- Missed opportunity to catch error before launch

**Optical Configuration:**
- Primary mirror: Curved reflector
- Secondary mirror: Smaller reflector to direct light to instruments
- Instruments positioned at focal plane

**Operational Aspects:**
- Multiple servicing missions to repair, upgrade, and maintain
- Attitude control for precise pointing
- Thermal management in space environment

**Scientific Impact:**
- Revolutionized astronomy by providing high-resolution visible and UV observations
- Discovered evidence for supermassive black holes
- Measured expansion rate of universe
- Captured iconic images transforming public understanding of cosmos

**Cheat Sheet:** Monolithic mirror, Spherical aberration correction, visible+UV observations, servicing capabilities

---

### James Webb Space Telescope (JWST)

**Mission Goal:** Observe infrared universe; study star/galaxy formation, exoplanet atmospheres, early universe

**Key Technical Features:**

**Sunshield (Critical Innovation):**
- **Size:** 21m × 14m (size of tennis court, too big for any existing rocket)
- **Structure:** Five layers of ultra-thin Kapton membrane
  - Layer 1 (Sun-facing): 50 μm thick
  - Layers 2-5: 25 μm thick each
- **Coatings:**
  - All layers: 100 nm aluminum on both sides (reflectivity)
  - Outer two layers: Additional 50 nm doped silicon coating (purple color, toughens shield, enhances heat reflection)
- **Function:** Blocks heat from Sun, Earth, and Moon; allows telescope to cool passively to 40K (−233°C)
- **Deployment:** Folded to fit rocket fairing, deployed post-launch after 10 days in space

**Mirror System:**
- **Primary Mirror:** 6.5 meters diameter
- **Configuration:** 18 hexagonal beryllium segments coated with gold
  - Gold chosen because: excellent infrared reflector, durable
  - Segments allow larger effective aperture than monolithic mirror
- **Segmented Mirror Advantages:**
  - Can be arbitrarily large (impossible with monolithic beyond ~8m)
  - Lighter weight than equivalent monolithic mirror
  - Each segment can be individually crafted and transported

**Operational Position:**
- Orbits at Sun-Earth L2 (Lagrange Point 2)
- L2 location: ~1 million km from Earth, on far side of Earth from Sun
- Halo orbit around L2 keeps Sun, Earth, Moon on same side of spacecraft
- Maintains consistent thermal environment for sunshield

**Infrared Capability:**
- **Wavelength Range:** Near-infrared to mid-infrared
- **Observation Goal:** Observe cooler objects and earlier universe
- **Challenge:** Infrared from telescope itself can overwhelm faint sources
- **Solution:** Ultra-cold telescope (40K) prevents self-generated infrared interference

**Deployment and Testing Challenges:**
- One of most complex engineering achievements
- Thousands of potential failure points during deployment
- Multiple deployment mechanisms had to work perfectly
- Successful initial deployment after 25+ years of development

**Scientific Objectives:**
- Study first galaxies after Big Bang
- Examine star formation in nebulae
- Analyze exoplanet atmospheres
- Study galaxy evolution
- Investigate origins of life chemistry

**Cheat Sheet:** Segmented mirror, sunshield cooling, infrared detection, L2 orbit, folding deployment

---

### Hubble vs. JWST Comparison

| Feature | Hubble | JWST |
|---------|--------|------|
| **Primary Mirror** | 2.4m monolithic | 6.5m segmented (18 hexagons) |
| **Wavelength** | Visible + UV | Near-infrared + mid-infrared |
| **Thermal Environment** | Ambient space (~280K) | Ultra-cold (~40K at L2) |
| **Cooling** | Not required | Passive via massive sunshield |
| **Location** | Low Earth orbit (600 km) | Sun-Earth L2 (~1 million km) |
| **Mirror Material** | Glass with aluminum coat | Beryllium with gold coat |
| **Servicing** | Regular Shuttle missions | Impossible to service |
| **Design Flexibility** | Fixed after launch | Segmented allows correction |

---

### ALMA (Atacama Large Millimeter/Submillimeter Array)

**Mission Goal:** Study star/planet formation, distant galaxies, cold dust, molecular lines in electromagnetic spectrum

**Key Technical Features:**

**Interferometry:**
- 66 individual antennas working together as single telescope
- Can be moved to different positions for variable "zoom"
- **Configuration Range:** 150m to 16km maximum separation
- **Effective Resolution:** Equal to single telescope with diameter = maximum antenna separation (16km!)
- **Much Cheaper Than:** Building single 16km-diameter antenna

**Antenna Specifications:**
- Main array: 54 twelve-meter diameter antennas
- Compact array: 4 twelve-meter + 12 seven-meter antennas
- **Frequency Range:** 31 to 1000 GHz (millimeter to submillimeter wavelengths)
- **Wavelength Range:** 3.6mm to 0.32mm

**Location & Advantages:**
- **Site:** Chajnantor plateau, Atacama Desert, northern Chile
- **Elevation:** 5,000 meters (16,000 feet)
- **Why This Location:**
  - High elevation above 60% of Earth's atmosphere
  - Dry desert minimizes water vapor (absorbs millimeter/submillimeter radiation)
  - Reduces noise and signal attenuation
  - Critical for observing at these wavelengths

**Technical Challenge - Synchronization:**
- Main technical challenge: Simultaneously point all 66 antennas at same target
- Capture astronomic signal at each antenna
- Convert to digital format
- Transmit signals to main building
- Supercomputer correlates signals and generates scientific data
- Requires incredibly precise timing and coordination

**Cost:** ~$1.4 billion (most expensive ground-based telescope)

**Scientific Capabilities:**
- Unprecedented sensitivity and resolution at millimeter/submillimeter wavelengths
- Resolution 10x sharper than Hubble (for its wavelength range)
- Reveals cold dust and gas (not visible in optical light)
- Studies star-forming regions obscured by dust
- Observes distant early galaxies
- Analyzes molecular composition of nebulae and exoplanet-forming disks

**Cheat Sheet:** Interferometry principle, atmospheric opacity at high wavelengths, signal correlation, array configuration

---

# PART 5: KEY FORMULAS & CONCEPTS

## 5.1 ORBITAL MECHANICS FORMULAS

### Vis-Viva Equation
\[v^2 = GM\left(\frac{2}{r} - \frac{1}{a}\right)\]

Where:
- v = orbital velocity
- G = gravitational constant
- M = mass of central body
- r = current distance from central body
- a = semi-major axis of orbit

### Kepler's Third Law
\[T^2 = \frac{4\pi^2}{GM} a^3\]

Or simplified form:
\[T^2 \propto a^3\]

### Hohmann Transfer Delta-V
\[\Delta v_1 = \sqrt{\frac{GM}{r_1}} \left(\sqrt{\frac{2r_2}{r_1 + r_2}} - 1\right)\]

\[\Delta v_2 = \sqrt{\frac{GM}{r_2}} \left(1 - \sqrt{\frac{2r_1}{r_1 + r_2}}\right)\]

\[\Delta v_{total} = \Delta v_1 + \Delta v_2\]

## 5.2 ROCKET EQUATION

### Tsiolkovsky Rocket Equation
\[\Delta v = v_e \ln\left(\frac{m_0}{m_f}\right)\]

Where:
- Δv = change in velocity
- v_e = effective exhaust velocity
- m_0 = initial mass (with propellant)
- m_f = final mass (without propellant)

### Specific Impulse (Isp)
\[I_{sp} = \frac{v_e}{g_0}\]

Where:
- I_sp = specific impulse (in seconds)
- v_e = exhaust velocity
- g_0 = Earth's gravitational acceleration (9.81 m/s²)

## 5.3 TELESCOPE RESOLUTION

### Rayleigh Criterion (Angular Resolution)
\[\theta = 1.22 \frac{\lambda}{D}\]

Where:
- θ = minimum angular resolution (in radians)
- λ = wavelength of light
- D = diameter of telescope aperture

**What it means:** Larger telescopes (larger D) and shorter wavelengths (smaller λ) = better resolution (smaller θ)

### Magnification
\[M = -\frac{f_o}{f_e}\]

Where:
- M = magnification
- f_o = focal length of objective (primary mirror)
- f_e = focal length of eyepiece

---

# PART 6: CHEAT SHEET ESSENTIAL POINTS

**Students: Use these bullet points for quick review before the exam!**

## Mission Summary Quick Reference

### SPACECRAFT

1. **BepiColombo**
   - Mercury orbiter with ion propulsion
   - Tests Einstein's general relativity
   - Uses solar electric propulsion (ion thrusters)
   - Multiple Venus and Mercury gravity assists
   - Extreme thermal management for Mercury proximity

2. **Galileo**
   - Jupiter orbiter with atmospheric probe
   - Gravity assists from Venus and Earth
   - Dual-spin stabilized (3 rpm rotating section)
   - First outer planet orbiter
   - Intentionally destroyed in Jupiter atmosphere

3. **Juno**
   - Jupiter's atmospheric scientist
   - Polar elliptical orbit (unprecedented)
   - Autonomous Jupiter Orbit Insertion (48-minute delay)
   - Spin-up to 5 rpm for stability during maneuver
   - Studies composition, atmosphere, magnetosphere

4. **Cassini-Huygens**
   - Saturn orbiter with Titan lander (Huygens)
   - 294 Saturn orbits over 13 years
   - RTG power (plutonium)
   - Landed Huygens on Titan (outer solar system first)
   - Grand Finale through Saturn's rings

5. **Voyager 2**
   - Only spacecraft to visit Uranus and Neptune
   - RTG power enabling 47+ year mission
   - 16 hydrazine thrusters
   - Gravity assists at each planet
   - Still transmitting from interstellar space

6. **New Horizons**
   - Pluto/Kuiper Belt explorer
   - Hibernation mode for long cruise
   - Autonomous encounter sequences
   - Jupiter gravity assist for acceleration
   - Course corrections for KBO flybys

7. **Dawn**
   - First ion propulsion multi-target mission
   - Orbited Vesta then Ceres
   - Proves ion engines enable orbit entry/exit
   - Derelict in Ceres orbit after fuel depletion
   - International collaboration (NASA, ESA, Italy, Germany, France, Netherlands)

8. **Lunar Reconnaissance Orbiter (LRO)**
   - Lunar polar mapping orbiter
   - 50 km altitude circular orbit
   - Quasi-frozen orbit for stable geometry
   - Direct lunar transfer (~4 days)
   - Supports future lunar missions

9. **Hayabusa**
   - First asteroid sample return
   - Landed on asteroid Itokawa
   - Ion propulsion
   - <1 gram sample successfully returned
   - Overcome landing challenges, component failures

10. **Deep Impact**
    - Comet impact mission (not destruction!)
    - Smart Impactor + Flyby spacecraft design
    - 372 kg copper impactor (cheaper than explosives)
    - Analyzed interior composition via spectroscopy
    - Extended mission planned for comet comparison

### TELESCOPES

1. **Hubble Space Telescope**
   - 2.4m monolithic mirror
   - Visible + ultraviolet observations
   - Sphere aberration corrected with "spectacles"
   - Serviceable via Space Shuttle
   - Revolutionized astronomy

2. **JWST**
   - 6.5m segmented mirror (18 hexagons)
   - Infrared observations (studying early universe)
   - Massive sunshield (21m × 14m, five layers)
   - L2 orbit (1 million km from Earth)
   - Ultra-cold operation (40K)

3. **ALMA**
   - 66-antenna millimeter/submillimeter interferometer
   - 150m to 16km configuration (effective 16km resolution)
   - Atacama Desert location (5000m elevation)
   - Wavelengths 3.6mm to 0.32mm
   - Most expensive ground-based telescope ($1.4B)

## Engineering Principles Quick Summary

### Propulsion Systems
- **Chemical:** High thrust, short duration, essential for launch, heavy
- **Ion:** Low thrust, high efficiency, long duration, ~3000+ Isp seconds

### Power Systems
- **Solar Panels:** Used near Sun (Mercury to Mars), lighter
- **RTGs:** Essential beyond Mars, provide consistent power for decades

### Attitude Control
- **Three-axis:** Precise pointing, uses reaction wheels + thrusters + star trackers
- **Spin-stabilized:** Simple, less flexible
- **Reaction Wheels:** Create torque without propellant consumption

### Thermal Management
- **Passive:** Radiators, MLI blankets, reflective surfaces
- **Active:** Fluid loops, electric heaters, deployable radiators

### Orbital Mechanics
- **Kepler's Laws:** Elliptical orbits, equal area in equal time, T² ∝ a³
- **Hohmann Transfer:** Most fuel-efficient transfer between circular orbits
- **Gravity Assists:** Free acceleration using planetary gravity

### Mirror Technology
- **Monolithic:** Single glass, limited to ~8m, cheaper for small telescopes
- **Segmented:** Multiple mirrors, arbitrarily large, requires active alignment
- **Coatings:** Aluminum for reflectivity, other materials for specific properties

### Telescope Capabilities
- **Resolution:** Better with larger diameter and shorter wavelengths (Rayleigh criterion)
- **Infrared:** Reveals dust-obscured star formation, requires extreme cooling
- **Interferometry:** Multiple small telescopes act as one large telescope, cheaper than monolithic

## Common Exam Question Types

### You might be asked about:

1. **Why certain propulsion systems for specific missions**
   - Ion for multi-target missions (Dawn)
   - Chemical for orbit insertion burns
   - RTGs for distant missions (Voyager, Cassini)

2. **Orbital mechanics calculations**
   - Hohmann transfer Δv calculations
   - Orbital period relationships
   - Gravity assist trajectories

3. **Engineering tradeoffs**
   - Monolithic vs. segmented mirrors
   - Thermal control passive vs. active
   - Spin vs. three-axis stabilization

4. **Mission-specific challenges and solutions**
   - Hubble spherical aberration and correction
   - JWST sunshield design and cooling
   - Hayabusa landing and sample collection
   - Deep Impact impact observation

5. **Scientific objectives and how engineering enables them**
   - Why JWST needs infrared capability and cooling
   - Why ALMA located at high, dry location
   - Why ion propulsion enables multi-target missions
   - Why segmented mirrors allow large telescopes

6. **Comparison questions**
   - Hubble vs. JWST differences
   - Chemical vs. ion propulsion
   - Ground-based vs. space telescopes
   - Monolithic vs. segmented mirrors

---

## FINAL EXAM PREPARATION CHECKLIST

Before the exam, make sure you understand:

✓ All 13 missions: names, purposes, key features
✓ Difference between chemical and ion propulsion
✓ Kepler's Laws and their applications
✓ Hohmann transfer concept
✓ Three-axis attitude control components
✓ Thermal control systems (passive vs. active)
✓ Monolithic vs. segmented mirror design
✓ Why infrared telescopes need cooling
✓ Interferometry concept for ALMA
✓ Space telescope advantages over ground-based
✓ Why certain missions use certain power systems (solar vs. RTG)
✓ Gravity assists and how they save fuel
✓ Autonomous operations and communication delays
✓ Sample return missions challenges
✓ L2 Lagrange point and JWST positioning

---

**GOOD LUCK ON YOUR EXAM!**
*Remember: Understand the principles, not just memorize facts. Questions test your comprehension of WHY spacecraft and telescopes are designed the way they are.*