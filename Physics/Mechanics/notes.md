            MECHANICS:
    STATICS, KINEMATICS, KINETICS, OSCILLATIONS AND WAVES

        INTRODUCTION TO MECHANICS
Mechanics is the branch of physics concerned with the behaviour of bodies under the action of forces, including bodies at rest, bodies in motion, and systems that oscillate or transmit waves.

Main branches:
- Statics: Study of bodies in equilibrium.
- Kinematics: Description of motion without considering its causes.
- Kinetics: Study of the relationship between forces, mass, and motion.
- Oscillations and waves: Study of repeated motion about equilibrium and the propagation of disturbances through space or a medium.

Fundamental physical quantities:
Quantity| SI unit| Dimension
Length, displacement| metre (m)| [L]
Mass| kilogram (kg)| [M]
Time| second (s)| [T]
Velocity| m/s| [LT⁻¹]
Acceleration| m/s²| [LT⁻²]
Force| newton (N)| [MLT⁻²]
Work and energy| joule (J)| [ML²T⁻²]
Power| watt (W)| [ML²T⁻³]
Pressure and stress| pascal (Pa)| [ML⁻¹T⁻²]
Frequency| hertz (Hz)| [T⁻¹]

Newton's second law defines force:
    F = ma
One newton is the force required to accelerate a 1 kg mass at 1 m/s².

Important vector quantities:
Displacement, velocity, acceleration, force and momentum are vectors: they have both magnitude and direction. Mass, time, energy and speed are scalars.

For a vector A making angle θ with the positive horizontal axis:
- Horizontal component: Aₓ = A cos θ
- Vertical component: Aᵧ = A sin θ
- Magnitude: A = √(Aₓ² + Aᵧ²)
- Direction: θ = tan⁻¹(Aᵧ/Aₓ), with the correct quadrant considered.
Always draw a diagram and define positive directions before resolving vectors.
        
        STATICS
Statics deals with bodies in equilibrium, meaning that their linear and angular accelerations are zero. A body in static equilibrium has no resultant force and no resultant moment.

Newton's laws relevant to statics:
First law: A body remains at rest or moves with constant velocity unless acted upon by a resultant external force.
Second law: The resultant force equals mass multiplied by acceleration. For equilibrium, acceleration is zero.
Third law: Every action force has an equal and opposite reaction force acting on a different body.

Conditions for equilibrium:
    For a coplanar rigid body:
        ΣFₓ = 0
        ΣFᵧ = 0
        ΣM = 0
Where:
- ΣFₓ = sum of horizontal forces.
- ΣFᵧ = sum of vertical forces.
- ΣM = sum of moments about a chosen point.
For three-dimensional equilibrium, all three force components and all three moment components must sum to zero.

Moments and torque:
A moment is the turning effect of a force about a point or axis.
Moment = Force × perpendicular distance
M = Fd⊥
More generally, the moment vector is:
M = r × F
Magnitude:
M = rF sin θ
Where r is the position vector from the pivot to the point of application and θ is the angle between r and F.
SI unit: N·m.
Choose a sign convention, commonly anticlockwise positive and clockwise negative.
Principle of moments: For a body in equilibrium, the sum of clockwise moments equals the sum of anticlockwise moments about any point.
Taking moments about a suitable pivot can eliminate unknown forces whose lines of action pass through that pivot.

Free-body diagrams (FBDs):
A free-body diagram isolates one body and shows every external force and couple acting on it.
Common forces include:
- Weight: W = mg, acting vertically downward through the centre of gravity.
- Normal reaction: Perpendicular to the contact surface.
- Tension: Acts along a taut cable, pulling away from the body.
- Friction: Acts along the contact surface and opposes relative motion or its tendency.
- Applied force: An externally imposed push or pull.
- Spring force: F = −kx for an ideal linear spring.
- Support reactions: Forces and, where applicable, moments exerted by supports.
Typical ideal support reactions in a 2D problem:
- Roller or smooth surface: one reaction normal to the surface.
- Pin or hinge: two force components, usually Rₓ and Rᵧ.
- Fixed support: two force components and a reaction moment.
These idealizations depend on the support model specified in the problem.

Friction:
Friction resists relative motion or impending motion between contacting surfaces.
Static friction:
    0 ≤ fₛ ≤ μₛN
Maximum static friction:
    fₛ,max = μₛN
Kinetic friction:
    fₖ = μₖN
Where:
- N = normal reaction.
- μₛ = coefficient of static friction.
- μₖ = coefficient of kinetic friction.
Usually μₛ ≥ μₖ for the same pair of surfaces.
Friction is not always equal to μN: static friction adjusts to the required value up to its maximum.
For a block on an inclined plane of angle θ:
- Weight component parallel to plane: mg sin θ.
- Weight component perpendicular to plane: mg cos θ.
- If no other perpendicular forces act, N = mg cos θ.
At impending downward slip, the limiting equilibrium condition is:
    mg sin θ = μₛmg cos θ
Therefore, tan θ = μₛ at the limiting angle of repose.

Centre of gravity and centre of mass:
- Centre of mass: The point representing the mass-weighted average position of a body.
- Centre of gravity: The point through which the resultant gravitational force acts.
In a uniform gravitational field, the two points coincide.
For discrete masses:
    x̄ = Σ(mᵢxᵢ)/Σmᵢ
    ȳ = Σ(mᵢyᵢ)/Σmᵢ
For a composite uniform-density body, the same weighted-average principle can be applied using component areas or volumes, with holes treated as negative areas or volumes.

Statics problem-solving procedure:
1. Isolate the body and draw its FBD.
2. Resolve inclined forces into components.
3. Apply ΣFₓ = 0 and ΣFᵧ = 0.
4. Take moments about a point that simplifies the equations.
5. Solve the simultaneous equations.
6. Check units, directions, and whether friction limits are satisfied.

        KINEMATICS
Kinematics describes motion using displacement, velocity, acceleration and time, without considering the forces causing the motion.

Basic quantities:
Distance: Total path length travelled; scalar.
Displacement: Change in position; vector.
Average speed:
    Average speed = Total distance / Total time
Average velocity:
    v̄ = Δx/Δt
Average acceleration:
    ā = Δv/Δt
Instantaneous velocity and acceleration are:
    v = dx/dt
    a = dv/dt = d²x/dt²
In two or three dimensions, these quantities are vector-valued.

Equations of uniformly accelerated motion:
For constant acceleration in one dimension:
    v = u + at
    s = ut + ½at²
    v² = u² + 2as
    s = ½(u + v)t
Where:
- u = initial velocity.
- v = final velocity.
- a = constant acceleration.
- t = elapsed time.
- s = displacement.
These equations apply only when acceleration is constant.
For freely falling objects near Earth's surface, neglecting air resistance:
    a = g ≈ 9.81 m/s² downward.
    If upward is positive, a = −g.

Motion graphs:
Displacement–time graph:
    - Gradient = velocity.
    - A straight line indicates constant velocity.
Velocity–time graph:
    - Gradient = acceleration.
    - Signed area under the graph = displacement.
Speed–time graph:
    - Area under the graph = distance travelled.
    - Gradient represents the rate of change of speed where differentiable.
Acceleration–time graph:
    - Signed area = change in velocity.
Do not confuse the area under a velocity–time graph with distance when velocity changes sign.

Motion in two dimensions:
Projectile motion
For a projectile launched at speed u at angle θ above horizontal, assuming no air resistance and level launch and landing heights:
Horizontal motion:
    x = (u cos θ)t
    vₓ = u cos θ
Vertical motion, taking upward as positive:
    y = (u sin θ)t − ½gt²
    vᵧ = u sin θ − gt
For return to the launch height:
Time of flight:
    T = 2u sin θ/g
Maximum height:
    H = u²sin²θ/(2g)
Horizontal range:
    R = u²sin 2θ/g
Maximum range occurs at θ = 45° under these assumptions.
If the landing height differs from the launch height, solve the vertical displacement equation for the appropriate flight time before calculating horizontal range.

Circular motion:
For an object moving in a circle of radius r:
Angular displacement: θ (radians)
Angular velocity:
    ω = dθ/dt  
Angular acceleration:
    α = dω/dt
Linear speed:
    v = rω
Tangential acceleration:
    aₜ = rα
Centripetal acceleration:
    a꜀ = v²/r = rω²
Centripetal acceleration always points toward the centre of the circular path. It changes the direction of velocity, even when speed is constant.
For uniform circular motion:
    ω = 2π/T = 2πf 
    v = 2πr/T
Where T is the period and f is the frequency.

Relative velocity:
Velocity of A relative to B:
    vₐᵦ = vₐ − vᵦ
The equation is vector-based. For motion along a straight line, assign consistent positive directions before subtracting.

Kinematics problem-solving tips
- Identify known and unknown quantities before choosing equations.
- Use consistent signs for displacement, velocity and acceleration.
- Convert all quantities to SI units.
- Use calculus for variable acceleration: a = dv/dt and v = dx/dt.
- Draw the trajectory for projectile and circular-motion problems.---

        KINETICS (DYNAMICS)
Kinetics studies the motion of bodies and the forces responsible for that motion.

Newton's laws of motion:
First law: A body remains at rest or in uniform straight-line motion if the resultant external force is zero.
Second law:
    ΣF = dp/dt
For constant mass:
    ΣF = ma
Third law: Forces between two interacting bodies are equal in magnitude, opposite in direction, and act on different bodies.
The third-law pair must not be placed on the same body's FBD.

Common forces and applications:
Weight:
    W = mg
Hooke's law for a linear spring:
    Fₛ = −kx
The negative sign indicates that the spring force opposes displacement from equilibrium.
Newton's law of universal gravitation:
    F = Gm₁m₂/r²
Where G is the gravitational constant and r is the distance between the centres of the two masses.
Near Earth's surface, weight is approximated by mg.

Work, energy and power:
Work
For a constant force:
    W = F s cos θ
Where θ is the angle between the force and displacement.
For a variable force in one dimension:
    W = ∫F(x) dx
Work is positive when the force has a component along displacement, negative when it opposes displacement, and zero when it is perpendicular to displacement.
Kinetic energy
    KE = ½mv²
Gravitational potential energy
Near Earth's surface:
    PE = mgh
Elastic potential energy
For an ideal spring:
    Eₛ = ½kx²
Work–energy theorem
Net work done on a body equals its change in kinetic energy:
    Wₙₑₜ = ΔKE = ½mv² − ½mu²
Conservation of mechanical energy
If only conservative forces do work:
    KE₁ + PE₁ = KE₂ + PE₂
If friction or other non-conservative forces do work, their work must be included in the energy balance.
Power
Average power:
    P = W/t
Instantaneous power:    
    P = dW/dt = F · v
For a constant force parallel to velocity:
    P = Fv
SI unit: watt (W).

Momentum and impulse:
Linear momentum:
    p = mv
Impulse:
    J = ∫F dt = Δp
For a constant force:
    J = FΔt
The impulse equals the change in momentum.
For an isolated system with negligible external resultant impulse:
Total momentum before interaction = Total momentum after interaction.

Collisions:
Elastic collision: Both momentum and total kinetic energy are conserved.
Inelastic collision: Momentum is conserved for an isolated system, but kinetic energy is not conserved.
Perfectly inelastic collision: Bodies stick together after impact.
For two bodies sticking together in one dimension:
    m₁u₁ + m₂u₂ = (m₁ + m₂)v
Therefore:
    v = (m₁u₁ + m₂u₂)/(m₁ + m₂)
Use signed velocities to represent directions.

Rotational dynamics:
Angular motion has direct parallels with linear motion.
Linear quantity| Rotational quantity
Displacement, s| Angular displacement, θ
Velocity, v| Angular velocity, ω
Acceleration, a| Angular acceleration, α
Mass, m| Moment of inertia, I
Force, F| Torque, τ
Momentum, p| Angular momentum, L
Torque:
    τ = r × F
For a rigid body rotating about a fixed axis with constant moment of inertia:
    Στ = Iα
Rotational kinetic energy:
    KEᵣ = ½Iω²
Angular momentum for rotation about a fixed principal axis:
    L = Iω
Moment of inertia:
    I = Σmᵢrᵢ²
For a continuous body:
    I = ∫r² dm
Parallel-axis theorem:
    I = I꜀ₘ + Md²
Where I꜀ₘ is the moment of inertia about a parallel axis through the centre of mass, M is total mass and d is the distance between the axes.
Common moments of inertia;
- Point mass at radius r: I = mr².
- Thin hoop about its central axis: I = MR².
- Solid disc or cylinder about its central axis: I = ½MR².
- Solid sphere about a diameter: I = ⅖MR².
- Uniform slender rod about its centre, perpendicular to its length: I = ¹⁄₁₂ML².
- Uniform slender rod about one end, perpendicular to its length: I = ⅓ML².
These expressions depend on the stated geometry and rotation axis.

Dynamics problem-solving procedure:
1. Draw an FBD.
2. Choose coordinate axes along convenient directions.
3. Apply ΣF = ma to translational motion.
4. Apply Στ = Iα if rotational motion is involved.
5. Alternatively, use energy or momentum when the conditions permit.
6. Check units, signs and whether the assumptions apply.

        OSCILLATIONS
An oscillation is repeated motion about an equilibrium position. Periodic oscillations repeat after equal intervals of time.
Examples include vibrating machine components, pendulums, springs, vehicle suspension systems and electrical-mechanical analogies.

Basic quantities:
- Amplitude, A: Maximum displacement from equilibrium.
- Period, T: Time for one complete cycle, measured in seconds.
- Frequency, f: Number of cycles per second, measured in hertz.
- Angular frequency, ω: Rate of change of phase, measured in rad/s.
- Phase: Describes the state of the oscillator within its cycle.
Relationships:
    f = 1/T
    ω = 2πf = 2π/T

Simple harmonic motion (SHM):
SHM occurs when the restoring acceleration is directly proportional to displacement from equilibrium and directed toward equilibrium.
    a = −ω²x
Restoring force:
    F = −kx
For a mass–spring system:  
    ω = √(k/m)
Period:
    T = 2π√(m/k)
Frequency:
    f = (1/2π)√(k/m)
Displacement:
    x(t) = A cos(ωt + φ)
Velocity:
    v(t) = −Aω sin(ωt + φ)
Acceleration:
    a(t) = −Aω² cos(ωt + φ) = −ω²x
Maximum speed:
    vₘₐₓ = Aω
Maximum acceleration:
    aₘₐₓ = Aω²
For ideal SHM, speed is maximum at equilibrium and zero at the turning points. The magnitude of acceleration is zero at equilibrium and maximum at the turning points.

Energy in SHM:
For an ideal mass–spring oscillator:
Total energy:
    E = ½kA² = ½mω²A²
Potential energy:
    PE = ½kx²
Kinetic energy:
    KE = ½mv² = ½k(A² − x²)
Total mechanical energy remains constant when damping and external energy losses are absent.
At equilibrium, kinetic energy is maximum. At maximum displacement, potential energy is maximum.

Simple pendulum:
For a point mass suspended by a light, inextensible string of length L, with small angular oscillations:
    T = 2π√(L/g)
    f = (1/2π)√(g/L)
The period is independent of the bob's mass and approximately independent of amplitude only for small oscillations.
For large angular displacements, the small-angle approximation sin θ ≈ θ is no longer sufficiently accurate.

Damped and forced oscillations:
Damped oscillation: Energy is lost through effects such as friction or air resistance, so amplitude decreases with time.
Underdamped system: Oscillates while its amplitude decays.
Critically damped system: Returns to equilibrium as quickly as possible without oscillating, for the ideal linear model.
Overdamped system: Returns to equilibrium without oscillation but more slowly than the critically damped case.
Forced oscillation: A system is driven by an external periodic force.
Resonance: Large response occurs when the driving frequency is near a system's natural frequency. Damping limits the response.
Engineering examples include bridges, rotating machinery, vehicle suspension, turbines and vibration isolation systems.

        WAVES
A wave is a travelling disturbance that transfers energy and momentum without requiring net transport of matter over the entire medium.
Mechanical waves: Require a material medium, e.g. sound and water waves.
Electromagnetic waves: Do not require a material medium, e.g. light.
Transverse waves: Oscillation is perpendicular to the direction of propagation.
Longitudinal waves: Oscillation is parallel to the direction of propagation.

Wave quantities:
- Amplitude, A: Maximum disturbance from equilibrium.
- Wavelength, λ: Distance between successive points in the same phase.
- Frequency, f: Oscillations per second.
- Period, T: Time for one complete oscillation.
- Wave speed, v: Speed at which the wave pattern propagates.
Fundamental relationship:
    v = fλ
Also:
    f = 1/T
Angular frequency:
    ω = 2πf
Wave number:
    k = 2π/λ
Do not confuse wave speed with the oscillatory speed of individual particles in a mechanical medium.
Progressive sinusoidal wave
For a wave travelling in the positive x-direction:
    y(x,t) = A sin(kx − ωt + φ)
For a wave travelling in the negative x-direction:
    y(x,t) = A sin(kx + ωt + φ)
Here φ is the phase constant.
The wave equation for an ideal one-dimensional wave is:
    ∂²y/∂t² = v² ∂²y/∂x²
with wave speed v for the relevant medium and wave type.

Wave speed in common engineering applications:
Transverse wave on a stretched string:
    v = √(Fₜ/μ)
Where Fₜ is the string tension and μ is mass per unit length.
Sound in an ideal fluid:
    v = √(B/ρ)
Where B is the bulk modulus and ρ is density.
The sound speed depends on the medium's properties and, in gases, on temperature and thermodynamic conditions.

Superposition and interference:
When waves overlap in a linear medium, the resultant displacement is the algebraic sum of their individual displacements.
Constructive interference: Waves combine to produce a larger amplitude when they arrive in phase.
Destructive interference: Waves reduce or cancel one another when they arrive out of phase.
Path-difference conditions for ideal coherent waves:
    Constructive: Δr = nλ
    Destructive: Δr = (n + ½)λ
    where n = 0, 1, 2, … for the usual two-wave case.

Standing waves and resonance:
Standing waves arise from the superposition of waves travelling in opposite directions with the same frequency.
    - Nodes: Points of zero displacement.
    - Antinodes: Points of maximum oscillation amplitude.
For a string fixed at both ends, or an ideal open-open air column:
    fₙ = nv/(2L), n = 1, 2, 3, …
For an ideal pipe closed at one end and open at the other:
    fₙ = nv/(4L), n = 1, 3, 5, …
Here L is the vibrating length, and v is wave speed. Real air columns may require end corrections.
Resonance occurs when a system is driven at or near one of its natural frequencies. It is important in musical instruments, acoustic systems and vibration control.

Doppler effect:
The Doppler effect is the apparent change in observed frequency caused by relative motion between a wave source and an observer.
For sound in a stationary medium:
    f′ = f(v ± vₒ)/(v ∓ vₛ)
Where:
- f′ = observed frequency.
- f = emitted frequency.
- v = sound speed in the medium.
- vₒ = observer speed relative to the medium.
- vₛ = source speed relative to the medium.
Choose signs so that motion of the observer toward the source increases the numerator, and motion of the source toward the observer decreases the denominator. The formula assumes speeds below the sound speed and uses velocities along the line of sight.

        ESSENTIAL ENGINEERING APPLICATIONS
Mechanics supports the design and analysis of:
- Structures: equilibrium, forces, moments and load distribution.
- Machines: rotational dynamics, torque, power and efficiency.
- Vehicles: acceleration, braking, momentum and suspension.
- Robotics: kinematics, dynamics and actuator requirements.
- Mechanical components: vibration, fatigue-related loading and resonance.
- Acoustics: wave propagation, sound transmission and vibration isolation.
- Civil and structural engineering: stability, friction, equilibrium and dynamic loading.
- Manufacturing: motion control, rotating systems and material handling.

        QUICK FORMULA REFERENCE:
Statics
    ΣFₓ = 0; ΣFᵧ = 0; ΣM = 0
    M = Fd⊥
    fₛ ≤ μₛN; fₖ = μₖN
Kinematics
    v = u + at
    s = ut + ½at²
    v² = u² + 2as
    a = dv/dt; v = dx/dt
    a꜀ = v²/r = rω²
Kinetics
    ΣF = ma
    W = Fs cos θ
    KE = ½mv²
    PE = mgh
    Eₛ = ½kx²
    Wₙₑₜ = ΔKE
    p = mv; J = Δp
    Στ = Iα
    KEᵣ = ½Iω²
    P = F · v
Oscillations
    f = 1/T; ω = 2πf
    a = −ω²x
    Tₛₚᵣᵢₙg = 2π√(m/k)
    Tₚₑₙdᵤₗᵤₘ = 2π√(L/g), for small oscillations
Waves
    v = fλ
    k = 2π/λ
    ω = 2πf
    vₛₜᵣᵢₙg = √(Fₜ/μ)
    fₙ = nv/(2L), for a string fixed at both ends.

        EXAM AND PROBLEM-SOLVING TIPS:
1. Start with a diagram. Use a free-body diagram for forces and a motion diagram for kinematics.
2. State assumptions. Examples: negligible air resistance, constant acceleration, ideal spring, small pendulum oscillations, or no energy loss.
3. Choose the correct method. Use equilibrium for statics, motion equations for constant-acceleration kinematics, Newton's laws for force-based dynamics, energy for speed and height relationships, momentum for collisions, and SHM or wave equations for oscillatory systems.
4. Resolve vectors correctly. Check whether angles are measured from the horizontal or vertical.
5. Use SI units throughout. Convert kilometres per hour to metres per second by dividing by 3.6.
6. Check dimensions. Both sides of a physical equation must have compatible dimensions.
7. Distinguish scalar and vector quantities. Speed is not velocity; distance is not displacement.
8. Check limiting cases. A calculated acceleration should approach zero when the resultant force approaches zero.
9. Use signs consistently. Negative acceleration does not automatically mean slowing down; compare acceleration and velocity directions.
10. Give final answers with units and sensible significant figures.

        FINAL CONCEPTUAL DISTINCTIONS:
- Statics vs dynamics: Equilibrium versus motion with nonzero acceleration.
- Kinematics vs kinetics: Description of motion versus forces causing motion.
- Mass vs weight: Mass measures inertia in kilograms; weight is gravitational force in newtons.
- Centripetal force: Not a separate type of force; it is the net inward force required for circular motion.
- Work vs power: Work is energy transferred; power is the rate of energy transfer.
- Momentum vs kinetic energy: Momentum is conserved in an isolated system; kinetic energy is conserved in elastic collisions but not generally in inelastic collisions.
- Oscillation vs wave: Oscillation is repeated motion about equilibrium; a wave propagates a disturbance through space or a medium.
- Frequency vs wave speed: Frequency is determined by the source; wave speed depends on the medium and wave type. Since v = fλ, changing the medium can change wavelength.