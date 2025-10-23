# TG-51 Protocol Study Notes
## What is TG-51?

- Clinical reference dosimetry protocol for external beam radiation therapy
- Replacement for the older TG-21 protocol
- **Much simpler** than previous methods

## Beam Types Covered

- **Photon beams:** ⁶⁰Co to 50 MV
- **Electron beams:** 4 to 50 MeV

## Key Equipment

- **Ion chambers** with water calibration factors
- **Water phantom** (required for all measurements)

## Main Formula

**D^Q_w = MkQN^60Co_D,w**

Where:

- **D^Q_w** = absorbed dose to water
- **M** = corrected ion chamber reading
- **kQ** = beam quality correction factor
- **N^60Co_D,w** = calibration factor for ⁶⁰Co

## Ion Chamber Corrections

**M = P_ion P_TP P_elec P_pol M_raw**

- **P_ion** = ion recombination
- **P_TP** = temperature/pressure
- **P_elec** = electrometer accuracy
- **P_pol** = polarity effects
- **M_raw** = raw reading

## Beam Quality Specifications

### Photon Beams

- Use **%dd(10)_x** (percentage depth dose at 10 cm)
- Reference depth: **10 cm**

### Electron Beams

- Use **R_50** (50% dose depth)
- Reference depth: **0.6R_50 - 0.1 cm**
- **R_50** comes from measured **I_50**

## Setup Requirements

- **Field size:** ≥10×10 cm² (≥20×20 cm² for high energy electrons)
- **SSD:** 100 cm (90-110 cm for electrons)
- **Water phantom only**

## Why TG-51 is Better

- **No complex tables** of stopping powers
- **No mass-energy absorption coefficients**
- **Direct water calibration**
- **Simpler calculations**
- **Worksheets provided**




Perfect — thanks for pasting your baseline notes. I now see the structure you want: **Markdown bullets with inline LaTeX**, equations called out at the top, followed by organized sections (Primary dose equation variables, Beam quality correction factor variables, etc.). No bold inside LaTeX.

Here’s the **final comprehensive set**, combining what was in your notes with all the missing definitions from the TG-51 images you shared. I kept your exact style and ordering, just expanded it.

---

# TG-51 Notes (Comprehensive)

$D_w^Q = M \cdot N_{D,w}^{60Co} \cdot k_Q$

- $D_w^Q$ = absorbed dose to water at beam quality $Q$
    
- $M$ = ion meter reading (charge collected), corrected for $P_{TP}$, $P_{pol}$, $P_{ion}$, and $P_{cel}$
    
- $N_{D,w}^{60Co}$ = absorbed dose to water calibration factor for the chamber in $^{60}Co$
    
- $k_Q$ = beam quality correction factor
    

$k_Q = \frac{(S_w/S_{air})_Q \cdot (W/e)_{air}^Q}{(S_w/S_{air})_{60Co} \cdot (W/e)_{air}^{60Co}} \cdot \frac{(L/\rho)_w^{air}}{(L/\rho)_w^{air}} \cdot P_{wall} \cdot P_{cel}$

$k_Q = k_{Q,Q_0} \cdot \frac{N_{D,w}^{Q_0}}{N_{D,w}^{60Co}}$

$%dd(10)_x = 100 \cdot \frac{D(10cm)}{D(d_{max})}$

$P_{pol} = \frac{|M_+| + |M_-|}{2M}$

$P_{TP} = \frac{(273.2 + T) \cdot P_0}{(273.2 + T_0) \cdot P}$

$D_w^{E_0} = M \cdot N_{D,w}^{60Co} \cdot k_{R_{50}}$

---

## Primary Dose Equation Variables

- $M_{raw}(d)$ = uncorrected chamber reading at depth $d$
    
- $M$ = corrected chamber reading (includes $P_{TP}$, $P_{pol}$, $P_{ion}$, $P_{cel}$, $P_{gr}$)
    
- $MU$ = monitor units (or minutes for $^{60}Co$)
    
- $rdg$ = electrometer reading in arbitrary units
    
- $N_{D,w}^Q$ = absorbed dose to water calibration factor at beam quality $Q$ (Gy/C or Gy/rdg)
    
- $N_{D,w}^{60Co}$ = calibration factor in $^{60}Co$ reference beam (Gy/C or Gy/rdg)
    

---

## Beam Quality Correction Factor Variables

- $S_w/S_{air}$ = water-to-air mass collision stopping power ratio
    
- $(W/e)_{air}$ = mean energy required to produce an ion pair in air
    
- $L/\rho$ = mass energy absorption coefficient ratio (water to air)
    
- $P_{wall}$ = chamber wall correction factor
    
- $P_{cel}$ = central electrode correction factor
    
- $P_{gr}^Q$ = gradient correction factor (depends on cavity radius $r_{cav}$ and local dose gradient; = 1 for plane-parallel chambers)
    
- $k_{Q,Q_0}$ = beam quality correction factor from reference quality $Q_0$ to user quality $Q$
    
- $k_{R_{50}}^Q$ = electron beam quality conversion factor specified by $R_{50}$
    
- $k_{ecal}$ = electron conversion factor from calibration quality $Q_{ecal}$ to another electron quality $Q$
    
- $k_{R_{50}}'$ = auxiliary factor used with $k_{ecal}$ in electron beams
    

---

## Correction Factor Variables

- $P_{ion}$ = ion recombination correction factor
    
    - $V_1, V_2$ = applied voltages
        
    - $M_1, M_2$ = readings at those voltages
        
- $P_{pol}$ = polarity correction factor
    
    - $M_+, M_-$ = readings at positive and negative polarity
        
    - $M$ = reading at normal polarity
        
- $P_{TP}$ = temperature–pressure correction factor
    
    - $T$ = temperature at measurement (°C)
        
    - $T_0$ = reference temperature (22 °C)
        
    - $P$ = pressure at measurement
        
    - $P_0$ = reference pressure (760 mmHg or 101.325 kPa)
        
- $P_{cel}$ = electrometer correction factor (unity if chamber + electrometer calibrated together)
    

---

## Beam Quality Specifiers

- $\%dd(10)_x$ = photon percent depth dose at 10 cm, contamination removed
    
- $\%dd(10)$ = measured depth dose at 10 cm, includes contamination
    
- $\%dd(10)_{Pb}$ = measured with 1 mm Pb foil to filter out head scatter contamination
    
- $D(10cm)$ = absorbed dose at 10 cm depth
    
- $D(d_{max})$ = absorbed dose at depth of maximum dose
    
- $TPR_{20,10}$ = tissue phantom ratio, 20 cm to 10 cm depth
    
- $R_{50}$ = electron depth where absorbed dose falls to 50% of maximum
    
- $I_{50}$ = electron depth where ionization (gradient corrected) falls to 50% of maximum
    

---

## Electron Beam Variables

- $E_0$ = most probable electron energy at phantom surface
    
- $d_{ref} = 0.6 R_{50} - 0.1$ = electron reference depth (cm)
    
- $Q_{ecal}$ = arbitrary electron reference quality, defined as $R_{50} = 7.5$ cm
    
- $d_{max}$ = depth of maximum absorbed dose for given beam
    

---

## General Subscripts / Superscripts

- $Q$ = beam quality of interest
    
- $Q_0$ = reference quality (often $^{60}Co$ or high-energy photons)
    
- $w$ = water
    
- $air$ = air
    
- $^{60}Co$ = cobalt-60 reference beam
    
- $r_{cav}$ = cavity radius of cylindrical chamber (cm)
    
- $SSD/SAD$ = source-to-surface or source-to-axis distance (cm)
    
- point of measurement = location in chamber cavity considered as measurement depth (upstream shift for cylindrical, entrance window for plane-parallel)
    
- reference depth = depth at which chamber is placed to measure absorbed dose
    

---

## Environmental Conditions

- $P$ = air pressure inside chamber (kPa)
    
- $T$ = air temperature inside chamber (°C)
    
- standard reference conditions: $T_0 = 22^\circ \text{C}, , P_0 = 101.33 ,\text{kPa}, , 20$–$80\%$ relative humidity
    
