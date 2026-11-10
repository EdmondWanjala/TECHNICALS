            REAL-TIME SYSTEMS (RTS)
A real-time system is a computer system that must produce correct results within specified time constraints.
  In real-time computing, correctness depends on two factors:
1. Logical correctness: Producing the correct output.
2. Temporal correctness: Producing the output within the required time.
A system may produce the correct result but still fail if the result arrives too late.
  Examples;
- Automotive airbag control systems.
- Aircraft flight-control systems.
- Industrial automation.
- Medical monitoring equipment.
- Robotics.
- Traffic control systems.
- Embedded communication systems.
  Characteristics of real-time systems;
- Predictable response time.
- Deterministic or bounded execution behaviour.
- Task scheduling.
- Time-constrained operations.
- Interrupt handling.
- Efficient resource management.
- Reliable operation.

 CLASSIFICATION OF REAL-TIME SYSTEMS
Real-time systems are classified according to how strictly they must meet deadlines.
  Hard real-time systems;
A hard real-time system must always meet its specified deadlines. Missing a critical deadline is considered a system failure.
  Examples:
- Aircraft flight control.
- Airbag deployment.
- Pacemakers.
- Critical industrial protection systems.
  Characteristics:
- Strict deadlines.
- Highly predictable response.
- High reliability.
- Failure may cause serious damage or loss of life.
  Firm real-time systems;
A firm real-time system can tolerate occasional missed deadlines, but a result produced after its deadline has no value.
  Examples:
- Certain industrial inspection systems.
- Time-limited automated measurement systems.
  Characteristics:
- Late results are useless.
- Occasional deadline misses may be tolerated.
- Correct timing remains important.
  Soft real-time systems;
A soft real-time system can tolerate occasional deadline misses, although performance or quality decreases.
  Examples:
- Video streaming.
- Online gaming.
- Audio processing.
- Multimedia applications.
  Characteristics:
- Deadlines are important but not absolute.
- Late results may still be useful.
- Performance degrades rather than causing complete system failure.

 REAL-TIME SYSTEM ARCHITECTURE
A typical real-time embedded system contains:
1. Sensors: Collect physical measurements.
2. Input interfaces: Receive sensor data.
3. Processor/microcontroller: Executes instructions.
4. Real-Time Operating System (RTOS): Manages tasks and system resources where used.
5. Memory: Stores programs, data and task information.
6. Communication interfaces: Exchange data with other devices.
7. Actuators: Execute physical actions.
8. Clock/timer: Provides timing information and generates interrupts.
  Basic operation;
Physical environment → Sensors → Input processing → Real-time controller → Actuators → Physical response.
Example: In an anti-lock braking system (ABS), wheel-speed sensors continuously measure wheel rotation. The controller processes the measurements and adjusts brake pressure within strict timing constraints to prevent wheel lockup.

 TASKS IN REAL-TIME SYSTEMS
A task is an independent unit of work executed by a processor.
  Examples:
- Reading a temperature sensor.
- Updating a display.
- Controlling a motor.
- Sending communication data.
- Monitoring system faults.
  Task classifications;
Periodic tasks
- Execute repeatedly at regular intervals.
- Example: Reading a temperature sensor every 100 ms.
Aperiodic tasks
- Occur irregularly and do not have a fixed repetition interval.
- Example: Processing a user button press.
Sporadic tasks
- Occur irregularly but have a known minimum interval between successive arrivals.
- Example: Processing emergency events that cannot occur more frequently than a specified interval.
  Task parameters;
Important task parameters include:
- Arrival time (r): Time when a task becomes ready.
- Execution time (C): Processor time required to complete the task.
- Deadline (D): Time by which the task must finish.
- Period (T): Time between successive releases of a periodic task.
- Response time (R): Time from task release until completion.
- Blocking time (B): Time a task waits because of resource access restrictions or lower-priority task activity.
For a periodic task, a common utilization measure is:
    U = C/T
Where:
- C = execution time.
- T = task period.
For multiple independent tasks:
    Utotal = Σ(Ci/Ti)

 REAL-TIME SCHEDULING
Scheduling determines which task executes and when.
The scheduler allocates processor time to tasks according to their priorities, deadlines and scheduling policies.
  First Come, First Served (FCFS);
Tasks execute in the order they arrive.
Characteristics:
- Simple scheduling.
- Non-preemptive in its basic form.
- Earlier arriving tasks execute first.
- Can cause long waiting times.
  Round Robin (RR);
Each task receives a fixed time slice called a time quantum.
When its time expires, the task is moved to the end of the ready queue if it has not completed.
Characteristics:
- Time-sharing approach.
- Provides fair processor allocation.
- Commonly used in general-purpose systems.
- Not inherently deadline-aware.
  Priority-based scheduling
Tasks are assigned priorities, and the highest-priority ready task is selected.
Characteristics:
- Critical tasks can execute before less important tasks.
- Commonly used in RTOS environments.
- May be preemptive or non-preemptive.
  Rate Monotonic Scheduling (RMS);
A fixed-priority scheduling algorithm that assigns higher priority to tasks with shorter periods.
Rule:
- Shorter task period = Higher priority.
- Longer task period = Lower priority.
For n independent periodic tasks with deadlines equal to their periods, a sufficient schedulability condition is:
    U ≤ n(2^(1/n) − 1)
As n approaches infinity, the utilization bound approaches:
    U ≤ ln(2) ≈ 0.693
This is a sufficient worst-case bound, not a necessary condition. Some task sets with utilization above this bound can still be schedulable.
  Earliest Deadline First (EDF);
A dynamic-priority scheduling algorithm that assigns the highest priority to the task with the earliest absolute deadline.
Characteristics:
- Priorities change during execution.
- Tasks with closer deadlines execute first.
- Under ideal uniprocessor assumptions, independent preemptible periodic tasks with deadlines equal to periods are schedulable when total utilization is at most 100%.
For such task sets:
    Utotal ≤ 1

 PREEMPTIVE AND NON-PREEMPTIVE SCHEDULING
  Preemptive scheduling;
A running task can be interrupted so that another higher-priority task can execute.
Advantages:
- Faster response to critical events.
- Suitable for priority-based real-time systems.
- Supports urgent task execution.
Disadvantages:
- More complex.
- Requires context switching.
- Can introduce synchronization problems.
  Non-preemptive scheduling;
Once a task begins execution, it continues until it finishes or voluntarily yields the processor.
Advantages:
- Simpler implementation.
- Lower context-switching overhead.
- Easier task interaction in some designs.
Disadvantages:
- High-priority tasks may wait for lower-priority tasks to finish.
- Response time may increase.

 REAL-TIME OPERATING SYSTEM (RTOS)
An RTOS is an operating system designed to manage tasks and system resources while providing predictable timing behaviour.
Unlike a general-purpose operating system, an RTOS emphasizes meeting timing constraints.
  Functions of an RTOS;
1. Task scheduling.
2. Task creation and termination.
3. Interrupt management.
4. Memory management.
5. Inter-task communication.
6. Resource sharing.
7. Synchronization.
8. Timer management.
9. Priority management.
10. Real-time event handling.
 Examples of RTOS;
- FreeRTOS.
- Zephyr.
- VxWorks.
- QNX Neutrino.
- ThreadX.
- RTEMS.
- embOS.
  RTOS kernel;
The kernel is the central component responsible for managing system execution.
It typically handles:
- Scheduling.
- Task switching.
- Interrupt handling.
- Synchronization.
- Resource management.
  Tasks and threads;
A task is an independently schedulable unit of execution.
An RTOS task commonly has:
- Task function.
- Stack.
- Priority.
- State.
- Task control information.
  Task states;
Common task states include:
1. Running: Currently executing on the processor.
2. Ready: Prepared to execute but waiting for processor time.
3. Blocked: Waiting for an event, delay or resource.
4. Suspended: Temporarily removed from scheduling until resumed.
5. Terminated: No longer executing.

 TASK SYNCHRONIZATION AND COMMUNICATION
Multiple tasks may need to share information or coordinate their execution.
  Semaphore;
A semaphore is a synchronization mechanism used to control access to shared resources or signal events between tasks.
Types:
- Binary semaphore: Has two states, available or unavailable; commonly used for event signaling.
- Counting semaphore: Maintains a count of available resources or pending events.
  Mutex;
A mutex (mutual exclusion) ensures that only one task accesses a protected shared resource at a time.
Important distinction:
- A mutex provides ownership and mutual exclusion.
- A semaphore is commonly used for signaling or resource counting.
  Queue;
A queue allows tasks to exchange data in an organized first-in, first-out manner.
Example:
A sensor-reading task sends measurements to a processing task through a queue.
  Event flags;
Event flags allow tasks to wait for one or more specific events or conditions.
  Race condition;
A race condition occurs when multiple tasks access shared data concurrently and the final result depends on the timing or order of execution.
Prevention:
- Mutexes.
- Semaphores.
- Atomic operations.
- Critical sections.

 INTERRUPTS AND INTERRUPT SERVICE ROUTINES (ISR)
An interrupt is a signal that temporarily causes the processor to suspend its current execution and respond to an event.
Examples:
- Timer expiration.
- Sensor data arrival.
- UART communication.
- External button press.
- Hardware fault.
  Interrupt Service Routine (ISR);
An ISR is a special function executed in response to an interrupt.
Functions:
- Identify the event.
- Capture important data.
- Clear the interrupt condition where required.
- Signal an RTOS task if further processing is needed.
  Interrupt handling sequence;
1. An interrupt event occurs.
2. The processor saves the necessary execution context.
3. The ISR executes.
4. The interrupt condition is handled.
5. The processor restores execution context or performs a task switch.
6. Normal execution continues.
  Important ISR design principles;
- Keep ISRs short.
- Avoid unnecessary delays.
- Avoid blocking operations.
- Avoid lengthy calculations.
- Use ISR-safe RTOS functions.
- Transfer lengthy processing to an RTOS task.

 TIMERS AND CLOCK MANAGEMENT
Timers are essential for maintaining accurate timing in real-time systems.
  Types:
1. Hardware timers: Dedicated hardware counters used for timing and event generation.
2. Software timers: Managed by software or an RTOS.
3. Watchdog timers: Detect system failures by requiring periodic servicing.
4. Real-time clocks (RTC): Maintain time and date information.
  Timer calculation;
For a basic timer counter:
    T = (Prescaler × Counter period)/fclk
For an up-counter with N counts:
    T = (Prescaler × N)/fclk
Where:
- T = timer interval (s).
- Prescaler = clock division factor.
- N = number of timer counts.
- fclk = timer input clock frequency (Hz).
The exact formula depends on timer architecture and whether counting is inclusive.
  Watchdog timer;
A watchdog timer resets or triggers recovery when the software fails to service it within a specified period.
Applications:
- Fault recovery.
- Embedded system reliability.
- Industrial control.
- Remote monitoring equipment.

 DEADLINES, LATENCY AND JITTER
  Deadline;
The latest time by which a task must complete.
  Latency;
The delay between an event occurring and the system responding to it.
Examples:
- Interrupt latency.
- Communication latency.
- Task response latency.
  Jitter;
Variation in the timing of repeated events or task execution.
Example:
A task intended to execute every 10 ms may execute at intervals of 9.8 ms, 10.2 ms and 10.1 ms.
Low jitter is important in:
- Motor control.
- Digital signal processing.
- Communication systems.
- Robotics.
Response time
Response time is the interval from task release until completion.
    R = Waiting time + Execution time
For a task to meet its deadline:
    R ≤ D
Where D is the relative deadline measured from task release.

 PRIORITY INVERSION
Priority inversion occurs when a high-priority task is forced to wait for a resource held by a lower-priority task.
Example:
1. A low-priority task acquires a shared resource.
2. A high-priority task needs the same resource and becomes blocked.
3. A medium-priority task executes and prevents the low-priority task from releasing the resource.
4. The high-priority task experiences unexpected delay.
Solutions:
- Priority inheritance: Temporarily raises the priority of the lower-priority task holding the resource.
- Priority ceiling protocol: Assigns resource-related priority ceilings to prevent certain forms of priority inversion and deadlock.
- Proper resource management.
- Minimizing critical-section duration.

 RTOS MEMORY MANAGEMENT
RTOS memory management allocates and manages memory for tasks and system operations.
  Important concepts:
Stack: Stores local variables, function call information and execution context.
Heap: Memory area used for dynamic allocation.
Static allocation: Memory is reserved at compile time or system initialization.
Dynamic allocation: Memory is allocated and released during execution.
  Memory management considerations;
- Avoid stack overflow.
- Monitor task stack usage.
- Minimize unnecessary dynamic allocation.
- Avoid memory leaks.
- Prevent memory fragmentation.
- Use static allocation where predictable memory usage is important.

 REAL-TIME SYSTEM PERFORMANCE AND RELIABILITY
  Important performance measures:
1. Response time.
2. Deadline miss ratio.
3. CPU utilization.
4. Scheduling overhead.
5. Interrupt latency.
6. Jitter.
7. Throughput.
8. Reliability.
9. Availability.
  CPU utilization;
For n periodic tasks:
    U = Σ(Ci/Ti)
Where:
- Ci = Worst-case execution time of task i.
- Ti = Period of task i.
CPU utilization indicates the fraction of processor time required by the tasks, excluding additional overhead unless explicitly included.
Deadline miss ratio
    Deadline miss ratio = Number of missed deadlines / Total deadlines
A lower ratio generally indicates better deadline performance.

 PRACTICAL IMPLEMENTATION USING FREERTOS
FreeRTOS is a widely used real-time operating system for microcontrollers.
  Common functions include:
- xTaskCreate(): Creates a task.
- vTaskDelay(): Delays a task for a specified number of ticks.
- vTaskDelayUntil(): Supports periodic task execution.
- vTaskStartScheduler(): Starts the scheduler.
- xQueueCreate(): Creates a queue.
- xQueueSend(): Sends data to a queue.
- xQueueReceive(): Receives data from a queue.
- xSemaphoreCreateMutex(): Creates a mutex.
Example: Two-task embedded system
Task 1: Reads a sensor periodically.
Task 2: Processes sensor data and controls an actuator.

#include <Arduino.h>
// Task 1: Read sensor periodically
void SensorTask(void *parameter) {
    while (1) {
        int sensorValue = analogRead(34);
        Serial.print("Sensor: ");
        Serial.println(sensorValue);
        vTaskDelay(pdMS_TO_TICKS(1000));
    }
}
// Task 2: Control an LED
void ControlTask(void *parameter) {
    pinMode(2, OUTPUT);
    while (1) {
        digitalWrite(2, HIGH);
        vTaskDelay(pdMS_TO_TICKS(500));
        digitalWrite(2, LOW);
        vTaskDelay(pdMS_TO_TICKS(500));
    }
}
void setup() {
    Serial.begin(115200);
    // Create sensor task
    xTaskCreate(
        SensorTask,
        "Sensor",
        2048,
        NULL,
        2,
        NULL
    );
    // Create control task
    xTaskCreate(
        ControlTask,
        "Control",
        2048,
        NULL,
        1,
        NULL
    );
}
void loop() {
    // Tasks are managed by FreeRTOS.
}
Explanation:
- Two independent tasks execute under FreeRTOS.
- SensorTask reads an analog input every second.
- ControlTask blinks an LED.
- The scheduler allocates processor time to the tasks.
- Task priorities determine which ready task is selected first.
Note: This example is intended for an ESP32 Arduino environment with the relevant FreeRTOS APIs available. It demonstrates task creation and delays, not a certified hard real-time design.

 APPLICATIONS OF REAL-TIME SYSTEMS
   Application| Real-time operation
Robotics| Motor control and movement coordination
Automotive| Airbag and braking control
Aviation| Flight-control processing
Healthcare| Patient monitoring and device control
Industrial automation| Machine and process control
Telecommunications| Time-sensitive signal processing
Smart grids| Power monitoring and protection
Drones| Flight stabilization and navigation
Embedded IoT| Timely sensor processing and device response

 IMPORTANT FORMULAS SUMMARY
1. Task utilization:   
   U = C/T
2. Total CPU utilization:   
   Utotal = Σ(Ci/Ti)
3. Response time:   
   R = Waiting time + Execution time
4. Deadline condition:   
   R ≤ D
5. Rate Monotonic sufficient utilization bound:   
   U ≤ n(2^(1/n) − 1)
6. EDF utilization condition (ideal uniprocessor, D = T):   
   Utotal ≤ 1
7. Timer interval:   
   T = (Prescaler × N)/fclk
8. Deadline miss ratio:   
   DMR = Missed deadlines/Total deadlines
9. Sampling period:   
   Ts = 1/fs

 KEY TAKEAWAYS
- Real-time systems must produce correct results within specified time constraints.
- Hard, firm and soft real-time systems differ in their tolerance of missed deadlines.
- Tasks are the basic units of execution.
- Scheduling determines the order and timing of task execution.
- RMS uses fixed priorities based on task periods.
- EDF uses dynamic priorities based on absolute deadlines.
- An RTOS manages tasks, interrupts, resources and timing.
- Semaphores, mutexes and queues support task synchronization and communication.
- Interrupts allow processors to respond to important hardware events.
- Priority inversion can delay critical tasks.
- Watchdog timers improve fault recovery.
- Predictability, reliability and deadline compliance are central to real-time system design.

Remember: In real-time systems, producing the correct result is not enough; the result must also be delivered at the correct time.