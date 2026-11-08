            POWER ELECTRONICS
Power electronics is the branch of electronics concerned with the conversion, control and efficient management of electrical power using semiconductor switching devices.
It controls the flow of electrical energy from a source to a load by converting voltage, current and frequency into the required form.
  Main functions;
- AC to DC conversion (Rectification).
- DC to AC conversion (Inversion).
- DC to DC conversion (Chopping).
- AC to AC conversion (AC voltage and frequency control).
- Regulation and control of electrical power supplied to loads.
  Applications;
- Switched-mode power supplies (SMPS).
- Electric vehicles and battery chargers.
- Solar photovoltaic systems and wind energy.
- Industrial motor drives.
- UPS systems.
- Welding equipment.
- Railway traction systems.
- Renewable energy and energy storage.

 POWER ELECTRONICS CONVERSION SYSTEM
A typical power electronic system consists of:
1. Input source: Supplies electrical energy (AC or DC).
2. Power converter: Changes the form of electrical power.
3. Controller: Generates switching signals to regulate output.
4. Gate driver: Provides appropriate switching signals and isolation where necessary.
5. Feedback circuit: Measures output voltage/current and compares it with the reference.
6. Load: Uses the converted electrical energy.
The controller adjusts switching operation to maintain the required output.

 SEMICONDUCTOR POWER SWITCHING DEVICES
Power semiconductor devices control large voltages and currents through switching operations.
  Power diode;
- An uncontrolled semiconductor device.
- Conducts when forward-biased and blocks when reverse-biased.
- Used in rectifiers, freewheeling circuits and protection circuits.
  Silicon Controlled Rectifier (SCR);
- A thyristor with anode, cathode and gate terminals.
- Turns ON when forward-biased and triggered by a gate pulse.
- Remains ON after triggering until current falls below the holding current or another commutation method is used.
- Mainly used in controlled rectifiers and high-power AC control.
Important terms:
- Latching current: Minimum anode current required to maintain conduction immediately after triggering.
- Holding current: Minimum current required to keep an SCR conducting.
- Firing angle (α): Delay angle between the AC supply reference point and the SCR triggering instant.
  Power MOSFET;
- A voltage-controlled device.
- Has gate, drain and source terminals.
- Offers high switching speed and high input impedance.
- Commonly used in high-frequency, low-to-medium-voltage converters.
  Insulated Gate Bipolar Transistor (IGBT);
- Combines MOSFET gate characteristics with bipolar transistor conduction.
- Voltage-controlled and suitable for high-voltage and high-current applications.
- Common in industrial inverters, motor drives and traction systems.
- Generally switches slower than a power MOSFET.
  TRIAC;
- A bidirectional thyristor.
- Conducts current in both directions when triggered.
- Used in AC power control, light dimmers and fan-speed controllers.
Comparison of switching devices
Device| Control| Main application
Diode| Uncontrolled| Rectification
SCR| Gate turn-on| Controlled rectifiers
MOSFET| Voltage-controlled| High-frequency switching
IGBT| Voltage-controlled| High-power switching
TRIAC| Gate-controlled| AC power control

 POWER RECTIFIERS (AC TO DC)
A rectifier converts alternating current (AC) into direct current (DC).
  Half-wave rectifier;
- Uses one diode.
- Allows only one half-cycle of the AC waveform to reach the load.
- Produces pulsating DC.
- Has high ripple and relatively low efficiency.
For an ideal half-wave rectifier with resistive load:
Average DC output voltage:
    Vdc = Vm/π
RMS output voltage:
    Vrms = Vm/2
Maximum rectification efficiency ≈ 40.6%.
  Full-wave rectifier;
Uses both positive and negative half-cycles of AC.
Types:
- Centre-tapped full-wave rectifier.
- Bridge rectifier (four diodes).
For an ideal full-wave rectifier:
Average DC output voltage:
    Vdc = 2Vm/π
RMS output voltage:
    Vrms = Vm/√2
Maximum rectification efficiency ≈ 81.2%.
Ripple frequency = 2f
  Controlled rectifier;
Uses SCRs instead of ordinary diodes to control the average DC output by adjusting the firing angle.
For a single-phase fully controlled bridge with continuous load current:
    Vdc = (2Vm/π)cos α
Where:
- Vm = peak AC input voltage.
- α = SCR firing angle.
Increasing α reduces the average DC output voltage.

 DC–DC CONVERTERS (CHOPPERS)
A DC–DC converter changes one DC voltage level into another using high-speed semiconductor switching.
  Buck converter (Step-down);
Reduces the input DC voltage.
Ideal continuous-conduction-mode relationship:
    Vout = D × Vin
Where D is the duty cycle.
    D = Ton/Ts
  Boost converter (Step-up);
Increases the input DC voltage.
Ideal continuous-conduction-mode relationship:
    Vout = Vin/(1 − D)
The output voltage is greater than the input voltage for 0 < D < 1.
  Buck-boost converter;
Can produce an output voltage magnitude either higher or lower than the input, with reversed polarity in the basic inverting topology.
    Vout = −[D/(1 − D)]Vin
Important switching terms
- Switching frequency (fs): Number of switching cycles per second.
- Switching period (Ts): Time taken for one complete switching cycle.
- Duty cycle (D): Fraction of the switching period during which the switch is ON.
- Ripple: Periodic variation in output voltage or current.
- Continuous conduction mode (CCM): Inductor current never falls to zero.
- Discontinuous conduction mode (DCM): Inductor current reaches zero during part of the switching cycle.

 DC–AC CONVERTERS (INVERTERS)
An inverter converts DC electrical power into AC electrical power.
  Types;
1. Voltage Source Inverter (VSI): Uses a relatively stiff DC voltage source.
2. Current Source Inverter (CSI): Uses a relatively stiff DC current source.
3. Single-phase inverter.
4. Three-phase inverter.
5. PWM inverter.
  Single-phase bridge inverter;
- Uses four controlled switches.
- Alternately switches diagonal pairs to generate an AC output.
- Produces a square-wave output unless modulation techniques are applied.
  Three-phase inverter;
- Uses six main power switches arranged in three legs.
- Generates three-phase AC output.
- Used in industrial motor drives and renewable energy systems.
  Pulse Width Modulation (PWM);
PWM controls the average output voltage by varying the width of switching pulses.
Advantages:
- Controls output voltage.
- Improves waveform quality.
- Reduces certain harmonic components.
- Enables efficient motor-speed control.

 AC–AC CONVERTERS
AC–AC converters modify AC voltage, frequency or both.
  AC voltage controller;
- Controls the RMS value of AC voltage without necessarily changing its frequency.
- Commonly uses SCRs or TRIACs.
- Applications include heater control and light dimming.
  Cycloconverter;
- Converts AC power at one frequency directly into AC power at another frequency.
- Commonly used for high-power, low-speed motor drives.
  Matrix converter;
- Converts AC directly to AC without an intermediate DC link.
- Uses controlled bidirectional switches.
- Can provide variable output voltage and frequency.

 GATE DRIVING AND SWITCHING CONTROL
Power semiconductor devices require appropriate gate-drive circuits for reliable switching.
Functions of a gate driver:
- Supplies suitable gate voltage/current.
- Provides fast and controlled switching.
- Provides electrical isolation where required.
- Prevents simultaneous conduction of switches in the same inverter leg.
- Protects against excessive gate voltage and switching disturbances.
  Dead time;
A short delay inserted between turning OFF one switch and turning ON its complementary switch.
Purpose:
- Prevents shoot-through.
- Avoids direct short-circuiting of the DC supply through the inverter leg.

 FILTERS AND RIPPLE REDUCTION
Filters smooth converter output and reduce unwanted AC components.
 Capacitor filter;
- Connected across the load.
- Stores energy and reduces output voltage ripple.
- Commonly used in rectifier circuits.
 Inductor filter;
- Connected in series with the load.
- Opposes rapid changes in current.
- Reduces current ripple.
 LC filter;
Combines an inductor and capacitor to provide improved smoothing.
For an ideal LC resonant frequency:
    f₀ = 1/(2π√LC)
Where L is inductance and C is capacitance.

 POWER ELECTRONICS PERFORMANCE PARAMETERS
  Efficiency;
η = (Pout/Pin) × 100%
High efficiency means less power is lost during conversion.
  Power loss;
Ploss = Pin − Pout
Major losses:
- Conduction losses.
- Switching losses.
- Gate-drive losses.
- Magnetic component losses.
- Diode reverse-recovery losses.
 Power factor;
PF = P/S
Where:
- P = real power (W).
- S = apparent power (VA).
Power factor is affected by phase displacement and waveform distortion.
  Total Harmonic Distortion (THD);
THD = √(V₂² + V₃² + V₄² + ...)/V₁ × 100%
Where V₁ is the RMS fundamental voltage and V₂, V₃, etc. are harmonic RMS voltages.
Lower THD generally indicates a waveform closer to a pure sinusoid.
 Ripple factor;
For a rectifier output:
    Ripple factor (r) = √[(Vrms/Vdc)² − 1]
Where Vrms is the total RMS output voltage and Vdc is its average value.

 PROTECTION AND THERMAL MANAGEMENT
Power electronic devices can be damaged by excessive voltage, current and temperature.
Important protection methods:
- Fuse and circuit breaker protection.
- Overcurrent and short-circuit protection.
- Overvoltage protection using suitable clamping circuits.
- Snubber circuits to control switching transients.
- Heat sinks and cooling fans.
- Thermal monitoring and shutdown.
- Proper insulation and electrical isolation.
- Reverse-polarity and surge protection where required.
  Snubber circuits;
Used to control voltage/current transients during switching.
An RC snubber is commonly used to limit rapid voltage changes (dv/dt) and reduce switching disturbances.

 ELECTRICAL AND MAGNETIC COMPONENTS
Important passive components:
- Inductor: Stores energy in a magnetic field and opposes changes in current.
- Capacitor: Stores energy in an electric field and opposes changes in voltage.
- Transformer: Transfers AC energy between circuits and provides voltage conversion and isolation.
- Resistor: Limits current, divides voltage and dissipates energy.
Energy stored:
    Inductor: EL = ½LI²
    Capacitor: EC = ½CV²

 APPLICATIONS OF POWER ELECTRONICS
1. Renewable energy: Solar inverters and wind turbine converters.
2. Electric vehicles: Motor drives, DC–DC converters and battery chargers.
3. Industrial automation: Variable-frequency drives (VFDs).
4. Telecommunications: Regulated DC power supplies.
5. Domestic appliances: Washing machines, refrigerators and induction cookers.
6. Power systems: HVDC transmission and reactive power compensation.
7. UPS: Converts DC battery power into AC during supply failure.
8. Battery energy storage: Controls charging and discharging.

 IMPORTANT FORMULAS SUMMARY
Quantity| Formula
Duty cycle| D = Ton/Ts
Switching frequency| fs = 1/Ts
Buck converter| Vout = DVin
Boost converter| Vout = Vin/(1−D)
Inverting buck-boost| Vout = −DVin/(1−D)
Half-wave average voltage| Vdc = Vm/π
Full-wave average voltage| Vdc = 2Vm/π
SCR full bridge (continuous current)| Vdc = (2Vm/π)cos α
Efficiency| η = Pout/Pin × 100%
Power loss| Ploss = Pin−Pout
Power factor| PF = P/S
LC resonant frequency| f₀ = 1/(2π√LC)
Inductor energy| EL = ½LI²
Capacitor energy| EC = ½CV²

 IMPORTANT STUDY AND EXAM TIPS
1. Understand the four main conversion processes: AC–DC, DC–DC, DC–AC and AC–AC.
2. Always identify the switching device and its operating principle.
3. Draw circuit diagrams and output waveforms when explaining converters.
4. Distinguish between average voltage and RMS voltage.
5. Remember that peak voltage Vm = √2 × Vrms for a sinusoidal supply.
6. For converter calculations, identify the conduction mode and assumptions before applying formulas.
7. For PWM converters, understand the relationship between duty cycle and output voltage.
8. In SCR circuits, distinguish firing angle, latching current and holding current.
9. Consider switching losses, conduction losses and thermal effects in practical designs.
10. Always include correct SI units in numerical calculations.

KEY IDEA: Power electronics achieves efficient electrical power conversion by controlling semiconductor devices as electronic switches. 
Its central objective is to deliver the required voltage, current and frequency to a load with minimum power loss and acceptable waveform quality.