                    ELECTROMAGNETISM
Electromagnetism is the branch of physics that studies electric charges, electric and magnetic fields, electric currents, and the interaction between electricity and magnetism.
It forms the foundation of electrical and electronic engineering, electric motors, generators, transformers, communication systems, sensors, and electromagnetic radiation.
 Main topics;
1. Electrostatics: Charges, electric forces and fields.
2. Electric potential and capacitance: Electrical energy storage.
3. Current electricity: Charge flow, resistance and circuits.
4. Magnetostatics: Magnetic fields produced by currents and magnets.
5. Electromagnetic induction: Production of voltage by changing magnetic flux.
6. Electromagnetic waves: Propagation of coupled electric and magnetic fields.
 Fundamental quantities;
Quantity| SI unit| Symbol
Electric charge| coulomb (C)| Q or q
Electric current| ampere (A)| I
Voltage / potential difference| volt (V)| V
Electric field strength| N/C or V/m| E
Resistance| ohm (Ω)| R
Capacitance| farad (F)| C
Magnetic flux| weber (Wb)| Φ
Magnetic flux density| tesla (T)| B
Inductance| henry (H)| L
Electrical power| watt (W)| P
Frequency| hertz (Hz)| f
 Constants;
- Elementary charge: e ≈ 1.602 × 10⁻¹⁹ C.
- Permittivity of free space: ε₀ ≈ 8.854 × 10⁻¹² F/m.
- Permeability of free space: μ₀ ≈ 1.257 × 10⁻⁶ H/m.
- Speed of light in vacuum: c ≈ 3.00 × 10⁸ m/s.

ELECTROSTATICS:
 Electric charge;
Electric charge is a fundamental property of matter responsible for electric interactions.
- Positive charge: associated with protons.
- Negative charge: associated with electrons.
- Like charges repel; unlike charges attract.
- Charge is quantized: Q = ne, where n is an integer for a net isolated charge.
- Charge is conserved: the total charge of an isolated system remains constant.
The SI unit is the coulomb (C).
Coulomb's law; Coulomb's law gives the electrostatic force between two stationary point charges:
    F = (1/4πε) |q₁q₂|/r²
In vacuum:
    F = (1/4πε₀) |q₁q₂|/r²
Where:
- q₁ and q₂ = charges in coulombs.
- r = separation between charges in metres.
- ε = permittivity of the medium.
- 1/(4πε₀) ≈ 8.99 × 10⁹ N·m²/C².
The force acts along the line joining the charges. It is repulsive for like charges and attractive for unlike charges.
For several charges, use the principle of superposition: calculate each force as a vector and add them.
 Electric field;
An electric field describes the force experienced by a positive test charge at a point.
    E = F/q
Therefore:
    F = qE
For a point charge:
    E = (1/4πε) |Q|/r²
The field direction is:
- Away from a positive source charge.
- Toward a negative source charge.
Electric field strength is measured in N/C or V/m.
For multiple source charges:
    E_net = ΣEᵢ
Electric field lines begin on positive charges and end on negative charges, or extend to infinity. They never cross.
 Electric dipole;
An electric dipole consists of two equal and opposite charges separated by a distance.
Dipole moment:
    p = qd
Here d is the displacement vector from the negative charge to the positive charge.
The dipole moment points from negative to positive charge. A dipole in an external electric field experiences torque:
    τ = p × E
Magnitude:
    τ = pE sin θ
Potential energy:
    U = −p · E = −pE cos θ
Dipoles are important in dielectric materials, molecular polarization and capacitive devices.
 Electric flux and Gauss's law; 
 Electric flux measures the electric field passing through a surface.
For a uniform field through a flat surface:
    Φₑ = EA cos θ
More generally:
    Φₑ = ∫ E · dA
Gauss's law:
    ∮ E · dA = Q_enclosed/ε₀
The integral is over a closed surface, and Q_enclosed is the net charge inside it.
Gauss's law is especially useful for highly symmetric charge distributions.
For an isolated point charge, a spherical Gaussian surface gives:
    E = Q/(4πε₀r²)
For an ideal infinitely long line charge with linear charge density λ:
    E = λ/(2πε₀r)
For an ideal infinite nonconducting sheet with surface charge density σ:
    E = σ/(2ε₀)
These results assume the stated ideal geometries and vacuum.
 Conductors in electrostatic equilibrium;
For an ideal conductor in electrostatic equilibrium:
- The electric field inside the conducting material is zero.
- Excess charge resides on its surface.
- The conductor is an equipotential body.
- The electric field just outside the surface is perpendicular to it.
Applications include electrostatic shielding, Faraday cages and protection of sensitive electronics.

ELECTRIC POTENTIAL AND ELECTRICAL ENERGY
 Electric potential
Electric potential is the electric potential energy per unit positive test charge.
    V = U/q
Potential difference is the work done per unit charge by an external agent in moving a test charge slowly between two points, with the sign determined by the direction of transfer.
For a point charge:
    V = (1/4πε)(Q/r)
For several point charges:
    V_net = ΣVᵢ
Electric potential is a scalar quantity, so potentials add algebraically rather than as vectors.
 Relationship between electric field and potential
In one dimension:
    Eₓ = −dV/dx
In three dimensions:
    E = −∇V
For a uniform field along the direction of motion:
    |ΔV| = Ed
The electric field points in the direction of decreasing potential.
 Electric potential energy
For a charge q at potential V:
    U = qV
For two point charges:
    U = (1/4πε)(q₁q₂/r)
The sign of the potential energy depends on the signs of the charges.
Work done by the electric field:
    W_field = −ΔU
For a charge moving through a potential difference:
    ΔU = qΔV
For a charge q moving from an initial potential Vᵢ to a final potential V_f, the work done by the electric field is:
    W_field = q(Vᵢ − V_f)
 Equipotential surfaces;
An equipotential surface has the same electric potential at every point.
- No work is done by the electrostatic field when a charge moves along an equipotential surface.
- Electric field lines are perpendicular to equipotential surfaces.
- Closely spaced equipotential surfaces indicate a strong field.

CAPACITANCE AND DIELECTRICS:
 Capacitance;
A capacitor stores separated electric charge and energy.
    C = Q/V
Where:
- C = capacitance in farads.
- Q = magnitude of charge on either plate.
- V = potential difference between the plates.
Capacitance depends on geometry and the insulating material, not on Q and V independently for an ideal linear capacitor.
 Parallel-plate capacitor;
For ideal parallel plates separated by distance d:
    C = εA/d
In vacuum:
    C = ε₀A/d
Where A is the overlapping plate area and ε = εᵣε₀ for a uniform dielectric filling the gap.
Increasing plate area increases capacitance. Increasing plate separation decreases capacitance. 
 Capacitors in combination;
Parallel combination
    C_eq = C₁ + C₂ + C₃ + ...
- Voltage is the same across each capacitor.
- Total charge is the sum of individual charges.
Series combination
    1/C_eq = 1/C₁ + 1/C₂ + 1/C₃ + ...
- Charge magnitude is the same on each ideal series capacitor.
- Total voltage is the sum of individual voltage drops.
For n identical capacitors, each of capacitance C:
- Parallel: C_eq = nC.
- Series: C_eq = C/n.
Energy stored in a capacitor
    U = ½CV²
Equivalent forms:
    U = ½QV = Q²/(2C)
Energy density in an electric field in a linear dielectric:
    uₑ = ½εE²
Applications include filtering, timing circuits, power electronics, pulse energy storage and signal coupling.

CURRENT ELECTRICITY:
 Electric current;
Electric current is the rate of flow of charge.
    I = dQ/dt
For constant current:
    I = Q/t
Conventional current flows in the direction positive charge would move. 
In metallic conductors, electrons drift in the opposite direction.
Current is measured in amperes:
    1 A = 1 C/s.
 Ohm's law;
For an ohmic conductor under constant physical conditions:
    V = IR
Where:
- V = potential difference.
- I = current.
- R = resistance.
Resistance:
    R = V/I
Resistance of a uniform conductor:
    R = ρL/A
Where:
- ρ = electrical resistivity.
- L = conductor length.
- A = cross-sectional area.
Longer conductors generally have greater resistance; larger cross-sectional area generally reduces resistance.
For many metallic conductors over a limited temperature range:
    R_T ≈ R₀[1 + α(T − T₀)]
Here α is the temperature coefficient of resistance referenced to T₀.
Resistors in combination;
Series
    R_eq = R₁ + R₂ + R₃ + ...
- Same current flows through every resistor.
- Supply voltage is divided across them.
Parallel:
    1/R_eq = 1/R₁ + 1/R₂ + 1/R₃ + ...
- Same voltage appears across each resistor.
- Total current is the sum of branch currents.
For n identical resistors of resistance R:
- Series: R_eq = nR.
- Parallel: R_eq = R/n.
 Kirchhoff's laws;
Kirchhoff's current law (KCL):
    ΣI_in = ΣI_out
Conservation of charge at a circuit junction.
Kirchhoff's voltage law (KVL):
    ΣΔV = 0
The algebraic sum of voltage changes around a closed loop is zero for a lumped circuit model.
When using KVL, choose a loop direction and apply consistent signs to voltage rises and drops.
 Electrical power and energy;
Power
    P = VI
Using Ohm's law:
    P = I²R
    P = V²/R
Electrical energy transferred:
    E = Pt
For a resistor, electrical energy is dissipated mainly as heat.
Commercial electrical energy is commonly measured in kilowatt-hours:
    1 kWh = 3.6 × 10⁶ J.
 Electromotive force and internal resistance;
Electromotive force (emf), ε, is the energy supplied per unit charge by a source.
For a source with emf ε and internal resistance r supplying current I:
    V_terminal = ε − Ir
When charging a source, the terminal voltage may instead be V_terminal = ε + Ir under the usual sign convention.
For a simple closed circuit with external resistance R:
    I = ε/(R + r)
The source's internal resistance causes voltage drop and power loss.
 Direct current and alternating current;
Direct current (DC): Current maintains one direction, though its magnitude may vary.
Alternating current (AC): Current periodically reverses direction.
For sinusoidal AC:
    v(t) = Vₘ sin(ωt)
    i(t) = Iₘ sin(ωt + φ)
Where Vₘ and Iₘ are peak values and φ is the phase difference.
For a sinusoidal waveform:
    V_rms = Vₘ/√2
    I_rms = Iₘ/√2
For a pure resistor:
    P_average = V_rms I_rms = I_rms²R
For general sinusoidal AC:
    P_average = V_rms I_rms cos φ
Here cos φ is the power factor for the sinusoidal voltage-current pair.

MAGNETIC FIELD:
A magnetic field describes magnetic effects produced by moving charges, electric currents and magnetic materials.
Magnetic flux density is represented by B and measured in tesla (T).
Magnetic field lines form closed loops. Outside a bar magnet they run from north to south, and inside the magnet they return from south to north.
 Magnetic force on a moving charge;
Lorentz magnetic force:
    F = q(v × B)
Magnitude:
    F = |q|vB sin θ
Where θ is the angle between velocity and magnetic field.
The force is perpendicular to both velocity and magnetic field. Its direction depends on the charge sign.
The complete Lorentz force, including an electric field, is:
    F = q(E + v × B)
A magnetic field alone does no work on a point charge because its force is perpendicular to the particle's instantaneous velocity.
 Motion of a charged particle in a magnetic field;
If velocity is perpendicular to a uniform magnetic field, the particle moves in a circle:
    |q|vB = mv²/r
Therefore:
    r = mv/(|q|B)
Cyclotron angular frequency for non-relativistic motion:
    ω = |q|B/m
Period:
    T = 2πm/(|q|B)
If velocity has a component parallel to the field, the particle follows a helical path.
Applications include mass spectrometers, charged-particle beam control and cyclotrons.
 Magnetic force on a current-carrying conductor;
    F = I(L × B)
Magnitude:
    F = BIL sin θ
Where L is a vector in the direction of conventional current with magnitude equal to the conductor length inside the field.
The direction can be determined using the right-hand rule for conventional current and the magnetic field.
This principle is used in electric motors, loudspeakers and electromagnetic actuators.
 Magnetic field produced by currents;
Long straight wire:
    B = μI/(2πr)
Centre of a circular coil of N turns, radius R:
    B = μNI/(2R)
Ideal long solenoid:
    B = μnI
Where n = N/L is the number of turns per unit length.
Here μ is the permeability of the surrounding medium. For vacuum, μ = μ₀. Material properties and geometry affect the field in real systems.
 Ampère's law;
For steady currents in magnetostatics:
    ∮ B · dl = μ₀I_enclosed
For a linear uniform medium, the corresponding idealized relation uses the appropriate permeability.
Ampère's law is especially useful for highly symmetric current distributions, such as long straight wires and ideal solenoids.
 Magnetic flux;
Magnetic flux through a flat surface in a uniform field:
    Φ_B = BA cos θ
More generally:
    Φ_B = ∫ B · dA
Where θ is the angle between the magnetic field and the surface normal.
SI unit: weber (Wb).
Magnetic flux depends on field strength, surface area and orientation.

ELECTROMAGNETIC INDUCTION:
 Faraday's law;
Electromagnetic induction occurs when magnetic flux linked with a circuit changes, producing an induced emf.
For a coil of N turns:
    ε = −N dΦ_B/dt
For a finite change:
    ε_average = −NΔΦ_B/Δt
The negative sign represents Lenz's law.
Induced emf can result from:
- Changing magnetic field strength.
- Changing the area of a circuit in a field.
- Rotating a circuit relative to a magnetic field.
- Relative motion between a conductor and a magnetic field.
 Lenz's law;
The induced current flows in a direction that opposes the change in magnetic flux that produces it.
It does not necessarily oppose the original magnetic field; it opposes the change in flux.
Lenz's law expresses conservation of energy and is essential when determining induced-current directions.
 Motional emf;
For a straight conductor of length L moving at speed v perpendicular to a uniform magnetic field, with the conductor, velocity and field mutually perpendicular:
    ε = BLv
For other geometries, determine the induced emf using the magnetic flux rule or the motional-emf integral.
Applications include generators, dynamic microphones, speed sensors and electromagnetic braking.
 Self-inductance;
Self-inductance occurs when changing current in a circuit changes its own magnetic flux linkage.
Flux linkage:
    NΦ_B = LI
For a linear inductor with constant L:
    ε_L = −L dI/dt
Inductance is measured in henries (H).
An inductor opposes changes in current, not current itself.
Energy stored in an inductor;
    U = ½LI²
Energy density in a linear magnetic field:
    u_B = B²/(2μ)
This expression applies to a linear, isotropic medium; more general materials require the appropriate field-energy relation.
Inductors are used in filters, transformers, switching power supplies, motors and energy-storage circuits.
 Transformers;
An ideal transformer transfers AC electrical energy between circuits through mutual electromagnetic induction.
Voltage ratio:
    Vₛ/Vₚ = Nₛ/Nₚ
Current ratio for an ideal transformer:
    Iₛ/Iₚ = Nₚ/Nₛ
Power conservation for an ideal transformer:
    VₚIₚ = VₛIₛ
Where p denotes primary and s denotes secondary.
A step-up transformer has more secondary turns than primary turns. A step-down transformer has fewer secondary turns.
Real transformers have copper losses, core losses, leakage flux and finite efficiency.
Transformers require changing magnetic flux and therefore operate with AC or another time-varying excitation, not steady DC after the transient.

ELECTROMAGNETIC WAVES:
Electromagnetic waves are propagating disturbances consisting of coupled electric and magnetic fields. 
They can travel through a vacuum and carry energy and momentum.
In a plane electromagnetic wave in vacuum:
- Electric and magnetic fields are perpendicular to each other.
- Both fields are perpendicular to the direction of propagation.
- The electric and magnetic fields are in phase.
- Their magnitudes satisfy E = cB.
 Wave speed;
In vacuum:
    c = 1/√(μ₀ε₀)
Also:
    c = fλ
In a material medium, wave speed depends on the medium's electromagnetic properties and frequency-dependent response.
For a simple, linear, homogeneous, nondispersive medium:
    v = 1/√(με)
This is an idealized relationship; real materials may exhibit dispersion and losses.
 Electromagnetic spectrum;
From lowest frequency to highest frequency:
1. Radio waves — communication and broadcasting.
2. Microwaves — radar, wireless communication and heating.
3. Infrared — thermal imaging and remote controls.
4. Visible light — vision, illumination and optical systems.
5. Ultraviolet — sterilization and material processing.
6. X-rays — medical imaging and inspection.
7. Gamma rays — nuclear processes and specialized medical applications.
As frequency increases:
- Wavelength decreases in a given propagation medium.
- Photon energy increases.
Photon energy:
    E_photon = hf
Where h ≈ 6.626 × 10⁻³⁴ J·s is Planck's constant.
 Maxwell's equations;
Maxwell's equations unify electricity and magnetism.
Gauss's law for electricity:
    ∇ · E = ρ/ε₀
Electric charge acts as a source of electric fields.
Gauss's law for magnetism:  
    ∇ · B = 0
There are no experimentally established isolated magnetic monopoles in classical electromagnetism; magnetic field lines form closed loops.
Faraday's law:
    ∇ × E = −∂B/∂t
A changing magnetic field produces a circulating electric field.
Ampère–Maxwell law:
    ∇ × B = μ₀J + μ₀ε₀ ∂E/∂t
Magnetic fields are produced by electric current and changing electric fields.
Here:
- ρ = electric charge density.
- J = current density.
- E = electric field.
- B = magnetic flux density.
These differential equations apply in vacuum with the usual SI conventions. Material media require appropriate constitutive relations and macroscopic forms.

ELECTROMAGNETIC APPLICATIONS IN ENGINEERING:
- Electric motors: Magnetic forces produce torque and mechanical motion.
- Generators: Mechanical motion changes magnetic flux and induces emf.
- Transformers: Mutual induction changes AC voltage and current.
- Electronics: Resistors, capacitors and inductors control circuit behaviour.
- Telecommunications: Electromagnetic waves transmit information wirelessly.
- Sensors: Hall-effect, inductive and capacitive sensors measure physical quantities.
- Medical engineering: MRI uses strong magnetic fields and radio-frequency excitation; X-rays support imaging.
- Power systems: Electromagnetism governs transmission, switching and energy conversion.
- Robotics: Motors, encoders, solenoids and electromagnetic actuators control movement.
- Industrial systems: Induction heating, magnetic levitation and electromagnetic braking.

QUICK FORMULA REFERENCE:
Electrostatics
    F = (1/4πε₀)|q₁q₂|/r²
    E = F/q
    E_point = (1/4πε₀)|Q|/r²
    Φₑ = EA cos θ
    ∮E · dA = Q_enclosed/ε₀
Potential and capacitance
    V_point = Q/(4πε₀r)
    U = qV
    C = Q/V
    C_parallel-plate = εA/d
    U_capacitor = ½CV²
Current electricity
    I = dQ/dt
    V = IR
    R = ρL/A
    P = VI = I²R = V²/R 
    ΣI_in = ΣI_out
    ΣΔV = 0
Magnetism
    F = q(v × B)
    F_wire = I(L × B)
    B_wire = μ₀I/(2πr), for a long straight wire in vacuum.
    Φ_B = BA cos θ
Induction   
    ε = −N dΦ_B/dt
    ε_motional = BLv, for mutually perpendicular geometry.
    ε_L = −L dI/dt
    U_inductor = ½LI²
    Vₛ/Vₚ = Nₛ/Nₚ, for an ideal transformer.
Electromagnetic waves
    c = 1/√(μ₀ε₀)
    c = fλ, in vacuum.
    E = cB, for a plane electromagnetic wave in vacuum.
    E_photon = hf

EXAM AND PROBLEM-SOLVING TIPS:
1. Draw a diagram showing charges, field directions, circuit connections or magnetic-field orientation.
2. Identify whether a problem involves electrostatics, current electricity, magnetism or induction.
3. Use vectors for electric and magnetic forces; scalar addition is sufficient for electric potential.
4. Convert all values to SI units before substituting into equations.
5. For circuit analysis, mark current directions and voltage polarities consistently. A negative answer means the actual direction is opposite to the assumed direction.
6. In induction questions, calculate the change in flux, not just the initial or final flux.
7. In magnetic-force questions, identify the angle between the relevant vectors. Force is zero for parallel velocity and magnetic field.
8. Check limiting cases: a stationary charge experiences no magnetic force, and constant magnetic flux produces no induced emf in a fixed circuit.
9. Distinguish emf from terminal voltage, and peak AC values from RMS values.
10. Check dimensions: voltage is J/C, electric field is N/C, magnetic flux is Wb, and inductance is H.
11. State assumptions explicitly: point charges, ideal wires, negligible resistance, uniform fields, or ideal transformers.
12. When a formula contains a negative sign, interpret its physical meaning rather than dropping it automatically.

FINAL CONCEPTUAL DISTINCTIONS:
- Electric field describes force per unit charge; electric potential describes potential energy per unit charge.
- Electric force can do work; magnetic force on a point charge alone does no work.
- Current is the rate of charge flow; voltage is energy transferred per unit charge.
- Resistance dissipates electrical energy; ideal capacitance and inductance store energy in electric and magnetic fields, respectively.
- Magnetic flux is the field integrated over an area; magnetic flux density B is measured in tesla.
- Faraday's law predicts the magnitude and sign of induced emf; Lenz's law explains the opposing direction.
- A transformer changes AC voltage through mutual induction; it does not continuously transform steady DC.
- Electromagnetic waves can propagate through a vacuum, unlike mechanical waves that require a medium.