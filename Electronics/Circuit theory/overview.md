Circuit theory is the foundational branch of electrical engineering that uses mathematical models to predict, analyze, and design the behavior of interconnected electrical components and networks.

Overview
• Definition: It studies how electrical energy, charge, current, and voltage flow through a closed path or network of components.
• Lumped-Parameter System: Most basic circuit theory assumes physical dimensions are much smaller than the signal wavelength, allowing components to be treated as discrete ("lumped") elements.
• Analysis vs. Synthesis: Analysis involves finding voltages and currents in a known circuit, while synthesis involves designing a circuit to achieve a specific target response.
• Core Variables:
	• Current (I): The time rate of change of electric charge (dQ/dt), measured in amperes (A).
	• Voltage (V): The potential difference or work needed to move a unit charge between two points, measured in volts (V).
	• Power (P): The rate of energy transfer, calculated as P = VI, measured in watts (W).

Key Topics
• Basic Circuit Elements:
	• Active Elements: Components that supply or generate energy (e.g., batteries, independent/dependent voltage and current sources).
	• Passive Elements: Components that consume or store energy—resistors (R, energy-converting), inductors (L, magnetic energy-storage), and capacitors (C, electric field energy-storage).
• Fundamental Laws:
	• Ohm's Law: Relates voltage, current, and resistance in a linear element (V = IR).
	• Kirchhoff's Current Law (KCL): The total current entering a node must equal the total current leaving it (\(\sum I_{\text{in}} = \sum I_{\text{out}}\)).
	• Kirchhoff's Voltage Law (KVL): The directed sum of all electrical potential differences (voltages) around any closed loop is zero (\(\sum V = 0\)).
• Analysis Techniques:
	• Nodal Analysis: Uses KCL to solve for unknown node voltages.
	• Mesh/Loop Analysis: Uses KVL to solve for unknown mesh currents in planar circuits.
	• Network Theorems: Superposition, Thevenin’s equivalent, Norton’s equivalent, and Maximum Power Transfer.
• AC and Dynamic Circuits:
	• Sinusoidal Steady-State: Using complex numbers and phasor notation for Alternating Current (AC) analysis.
	• Transients: First-order (RC and RL) and second-order (RLC) differential equations describing time-domain energy responses.

Applications
• Power Systems: Designing and stabilizing electrical grid distribution, transformers, and load management.
• Analog & Digital Electronics: Building signal amplifiers with operational amplifiers (op-amps), logic gates, microcontrollers, and integrated circuits.
• Signal Processing & Communications: Using low-pass, high-pass, and band-pass RLC filters to shape frequencies.
• Control Systems: Modeling feedback loops and actuator responses in robotics and automation.
• Biomedical Engineering: Designing bioinstrumentation devices like ECG monitors, EEG readers, and cardiac pacemakers.
• Renewable Energy Grids: Optimizing power conversion in solar photovoltaic systems and wind turbine inverters.