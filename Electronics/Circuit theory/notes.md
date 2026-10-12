                    CIRCUIT THEORY
Circuit theory is the study of electrical circuits, their components, and the relationships between voltage, current, resistance, power, and energy.

Basic Electrical Quantities:
- Electric charge (Q): Quantity of electricity, measured in coulombs (C).
- Current (I): Rate of flow of electric charge, measured in amperes (A).
    I = Q/t, I = dQ/dt.
- Voltage (V): Electrical potential difference; work done per unit charge.
    V = W/Q
- Resistance (R): Opposition to current flow, measured in ohms (Ω).
- Power (P): Rate of electrical energy transfer, measured in watts (W).
    P = VI
- Energy (W or E): Electrical work done, measured in joules (J).
    E = Pt = VIt
        Where Q = charge, t = time, and W = work or energy.

Circuit Elements:
Passive elements
    - Resistor: dissipates electrical energy.
    - Capacitor: stores energy in an electric field.
    - Inductor: stores energy in a magnetic field.
Active elements
    - Independent voltage source: maintains a specified voltage.
    - Independent current source: maintains a specified current.
    - Dependent source: output depends on another voltage or current in the circuit.
Ideal circuit assumptions
    - Ideal wires have zero resistance.
    - Ideal voltage sources maintain constant voltage.
    - Ideal current sources maintain constant current.
    - Ideal components have no unintended losses or parasitic effects.

Ohm’s Law:
For a linear resistor at constant physical conditions:
    V = IR
Therefore:
    - I = V/R
    - R = V/I
Power in a Resistor
    P = VI = I²R = V²/R
Energy dissipated over time t:
    E = Pt
Important: A resistor converts electrical energy into heat. Always check that its power rating is sufficient for the expected dissipation.

Series and Parallel Circuits:
Series Circuits
  Components are connected along a single current path.
    - Current is the same through every component.
    - Supply voltage equals the sum of voltage drops.
    - Equivalent resistance:
        R_eq = R₁ + R₂ + ... + Rₙ
  Voltage divider rule:
    Vₖ = V_s × Rₖ/(R₁ + R₂ + ... + Rₙ)
  For a series circuit, the larger resistor receives the larger voltage drop when the current is the same.

Parallel Circuits:
  Components share the same two nodes.
    - Voltage is the same across every branch.
    - Total current is the sum of branch currents.
    - Equivalent resistance:
        1/R_eq = 1/R₁ + 1/R₂ + ... + 1/Rₙ
  For two resistors:
    R_eq = (R₁R₂)/(R₁ + R₂)
  Current divider rule for two parallel resistors:
    I₁ = I_T × R₂/(R₁ + R₂)
    I₂ = I_T × R₁/(R₁ + R₂)
    The branch with lower resistance carries more current.
Key checks
- Series equivalent resistance exceeds every individual positive resistance.
- Parallel equivalent resistance is less than the smallest branch resistance.

Kirchhoff’s Laws:
  Kirchhoff’s Current Law (KCL)
    At any circuit node, total current entering equals total current leaving.
    ΣI = 0, using consistent current signs.
    This follows from conservation of electric charge.
  Kirchhoff’s Voltage Law (KVL)
    Around any closed loop, the algebraic sum of voltages is zero.
    ΣV = 0
    This follows from conservation of energy for the lumped-circuit model.
    Sign convention: A voltage rise is positive and a voltage drop is negative, or vice versa, provided the convention is used consistently.

Circuit Analysis Methods:
  Nodal Analysis
    Used to determine unknown node voltages.
      Procedure:
    1. Select a reference node (ground).
    2. Assign voltages to the remaining nodes.
    3. Apply KCL at each non-reference node.
    4. Express branch currents using Ohm’s law.
    5. Solve the simultaneous equations.
    For a resistor between nodes a and b:
    I_ab = (V_a − V_b)/R
  Mesh Analysis
    Used to determine currents in independent meshes of a planar circuit.
        Procedure:
    1. Assign a mesh current to each independent mesh.
    2. Apply KVL around each mesh.
    3. Express shared-branch currents as differences of mesh currents.
    4. Solve the resulting equations.
    For a resistor shared by meshes 1 and 2, its voltage drop in mesh 1 is R(I₁ − I₂), assuming both mesh currents are clockwise.

Network Theorems:
  Superposition Theorem
    In a linear circuit with multiple independent sources, the voltage or current in any element equals the algebraic sum of the individual contributions from each independent source acting alone.
    When considering one source at a time:
    - Replace ideal independent voltage sources by short circuits.
    - Replace ideal independent current sources by open circuits.
    - Keep dependent sources active.
    Note: Superposition applies to voltages and currents, not directly to power. Calculate power from the final total voltage or current.
  Thévenin’s Theorem
    Any linear two-terminal network can be represented by an equivalent voltage source V_th in series with a resistance R_th (or impedance Z_th for AC analysis).
    - V_th = open-circuit terminal voltage.
    - R_th = resistance seen looking into the network with independent sources deactivated.
    - With dependent sources present, use a test source or another valid method to determine R_th.
  Norton’s Theorem
    A linear two-terminal network can be represented by a current source I_N in parallel with R_N.
    - I_N = short-circuit terminal current.
    - R_N = R_th.
    - V_th = I_N R_N.
  Maximum Power Transfer
    For a DC resistive network, maximum power is delivered to the load when:
    R_L = R_th
    The maximum load power is:
        P_max = V_th²/(4R_th)
    For AC networks with complex impedance, maximum average power transfer occurs when:
        Z_L = Z_th*
        where * denotes complex conjugation, assuming the usual linear Thévenin model and a conjugate-matched load.

Capacitors and Inductors:
  Capacitor
    A capacitor stores energy in an electric field.
    - Charge: Q = CV
    - Current-voltage relation: i = C(dv/dt)
    - Energy stored: E = ½CV²
    For ideal capacitors:
    - Series: 1/C_eq = Σ(1/Cᵢ)
    - Parallel: C_eq = ΣCᵢ
    A capacitor’s voltage cannot change instantaneously under finite current.
  Inductor
    An inductor stores energy in a magnetic field.
    - Voltage-current relation: v = L(di/dt)
    - Energy stored: E = ½LI²
    For ideal inductors:
    - Series: L_eq = ΣLᵢ
    - Parallel: 1/L_eq = Σ(1/Lᵢ), when mutual coupling is negligible.
    An inductor’s current cannot change instantaneously under finite voltage.
  DC Steady-State Behaviour
    After a sufficiently long time under constant DC conditions:
    - An ideal capacitor behaves as an open circuit.
    - An ideal inductor behaves as a short circuit.
    During switching, both components may have transient responses.

RC and RL Transient Circuits
First-order circuits typically exhibit exponential responses.
General form:
    x(t) = x(∞) + [x(0⁺) − x(∞)]e^(−t/τ)
  Where:
    - x(0⁺) = value immediately after switching.
    - x(∞) = final steady-state value.
    - τ = time constant.
RC Circuit     
    τ = RC seconds
    For capacitor charging from zero toward V_s:
        v_C(t) = V_s(1 − e^(−t/RC))
    For discharging from initial voltage V₀:
        v_C(t) = V₀e^(−t/RC)
RL Circuit
    τ = L/R seconds, where R is the effective resistance seen by the inductor.
    For current rising from zero toward I_∞:
        i_L(t) = I_∞(1 − e^(−tR/L))
    After one time constant, a rising response reaches about 63.2% of its total change; a decaying response retains about 36.8% of its initial value. After approximately 5τ, the response is effectively settled for most practical calculations.

Alternating Current (AC) Circuit Theory
AC voltage and current vary with time, often sinusoidally.
    v(t) = V_m sin(ωt + φ)
        - V_m = peak voltage.
    - ω = angular frequency in rad/s.
    - f = frequency in hertz (Hz).
    - T = period in seconds.
    - φ = phase angle.
  Relations:
    f = 1/T
    ω = 2πf
    For a sinusoidal waveform:
        V_rms = V_m/√2
        I_rms = I_m/√2
    RMS values are used for average power calculations in standard AC circuits.
Reactance:
Inductive reactance:
    X_L = ωL = 2πfL
Capacitive reactance:
    X_C = 1/(ωC) = 1/(2πfC)
    - Inductive reactance increases with frequency.
    - Capacitive reactance decreases with frequency.
Impedance
    Impedance is the total opposition to sinusoidal current, including resistance and reactance, measured in ohms.
    - Resistor: Z_R = R
    - Inductor: Z_L = jωL
    - Capacitor: Z_C = 1/(jωC) = −j/(ωC)
        Here j = √(−1).
    For a series RLC circuit:
    Z = R + j(X_L − X_C)
    |Z| = √[R² + (X_L − X_C)²]
    I = V/Z, using RMS phasors.
AC Power
    For sinusoidal voltage and current:
    - Apparent power: S = V_rms I_rms, measured in volt-amperes (VA).
    - Real power: P = V_rms I_rms cosφ, measured in watts (W).
    - Reactive power: Q = V_rms I_rms sinφ, measured in volt-amperes reactive (var).
    - Power factor: PF = cosφ = P/S.
    For ideal resistors, voltage and current are in phase. In ideal inductors, current lags voltage by 90°. In ideal capacitors, current leads voltage by 90°.

Series RLC Resonance:
Resonance occurs when inductive and capacitive reactances are equal:
    X_L = X_C
Resonant angular frequency:
    ω₀ = 1/√(LC)
Resonant frequency:
    f₀ = 1/(2π√(LC))
At series resonance:
    - Net reactance is zero.
    - Impedance is minimum and equals R.
    - Current is maximum for a fixed applied voltage.
    - Voltage and current are in phase.
For an ideal series RLC circuit, quality factor:
    Q_factor = ω₀L/R = 1/(ω₀CR)
Do not confuse the quality factor symbol with electric charge or reactive power; context determines its meaning.

Electrical Measurements and Instrumentation:
- Ammeter: Measures current; connect in series. An ideal ammeter has zero resistance.
- Voltmeter: Measures voltage; connect in parallel. An ideal voltmeter has infinite resistance.
- Ohmmeter: Measures resistance; test an isolated, unpowered circuit.
- Multimeter: Can measure voltage, current, resistance, and other quantities depending on the model.
Safety: Never connect a current-measurement input directly across a voltage source. Observe the instrument's rating, terminal selection, and measurement category.

Essential Circuit-Theory Tips:
1. Convert all quantities to consistent SI units before calculating.
2. Label nodes, component polarities, current directions, and reference voltages.
3. An assumed current direction may be chosen arbitrarily; a negative answer means the actual direction is opposite.
4. Use KCL at nodes and KVL around loops to verify solutions.
5. Check units: V = AΩ, W = VA, and τ is measured in seconds.
6. Distinguish instantaneous, peak, peak-to-peak, and RMS AC values.
7. Use resistance for DC resistive networks and impedance for sinusoidal AC analysis.
8. Account for initial capacitor voltage and inductor current when analysing switching circuits.
9. Ideal circuit models are approximations; real components have tolerances, parasitic effects, and power limits.
10. Verify whether the circuit is linear before applying linear network theorems.

Quick Formula Summary:
Quantity| Formula
Current| I = Q/t
Ohm’s law| V = IR
Power| P = VI = I²R = V²/R
Series resistance| R_eq = ΣR
Parallel resistance| 1/R_eq = Σ(1/R)
Capacitor current| i = C(dv/dt)
Inductor voltage| v = L(di/dt)
RC time constant| τ = RC
RL time constant| τ = L/R
Angular frequency| ω = 2πf
Inductive reactance| X_L = ωL
Capacitive reactance| X_C = 1/(ωC)
Resonant frequency| f₀ = 1/(2π√LC)
AC real power| P = VI cosφ
Thévenin–Norton relation| V_th = I_N R_th
