A real-time system (RTS) is a computing environment that must process inputs and produce outputs within strict, predictable time constraints. 
Correctness depends not only on the logical result of the computation, but also on the exact physical instant (deadline) when that result is delivered.

Overview
Unlike general-purpose operating systems (like Windows or macOS) that prioritize average throughput or user experience, real-time systems prioritize determinism and low latency.

Classification of Real-Time Systems:
• Hard Real-Time Systems: Missing a single deadline causes total system failure, catastrophic physical damage, or loss of life (e.g., flight control, automotive airbags, pacemakers).
• Firm Real-Time Systems: Missing a deadline results in a significant drop in quality or utility, though it may not cause total failure (e.g., live video streaming or financial trading feeds).
• Soft Real-Time Systems: Missing a deadline degrades performance, but the system continues to function normally (e.g., video game frame rates or telecommunication audio routing).

Key Topics & Core Concepts:
• Determinism: The ability of the system to execute tasks in a predictable, repeatable amount of time every single run.
• Interrupt Latency: The time interval between an external event occurring and the system starting its response to that event.
• Jitter: The unwanted variation in task execution time or delay.
• Task Scheduling Algorithms:
	• Rate Monotonic Scheduling (RMS): A static (fixed) priority algorithm where tasks with shorter periods get higher priority.
	• Earliest Deadline-First (EDF): A dynamic priority algorithm where the task with the closest upcoming deadline is prioritized first.
• Real-Time Operating Systems (RTOS): Specialized kernels—such as FreeRTOS, VxWorks, or Zephyr—designed with fast context-switching, pre-emptive scheduling, and minimal resource overhead.

Applications:
• Automotive: Anti-lock braking systems (ABS), electronic stability control, engine fuel injection, and airbag deployment.
• Avionics & Aerospace: Flight control software, satellite attitude control, and radar navigation systems.
• Medical Devices: Implanted cardiac pacemakers, insulin delivery pumps, and hospital patient life-support monitors.
• Industrial Automation: Robotic assembly lines, chemical plant safety valves, and high-precision CNC machinery.
• Telecommunications: High-speed data routing, packet switching, and mobile network base-station management.