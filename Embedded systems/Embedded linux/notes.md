                EMBEDDED LINUX
Embedded Linux is the use of the Linux operating system in dedicated embedded devices designed to perform specific functions.
It combines the Linux kernel, system libraries, utilities, device drivers and application software to control embedded hardware.
Unlike general-purpose desktop Linux, embedded Linux systems are optimized for specific applications, often with limited memory, processing power, storage and energy resources.
  Examples of embedded Linux devices:
- Smart TVs and set-top boxes.
- Industrial automation controllers.
- Network routers and switches.
- Medical monitoring equipment.
- Automotive infotainment systems.
- Raspberry Pi-based embedded projects.
- Smart cameras and IoT gateways.
- Robotics and autonomous systems.

 Embedded Linux Architecture
An embedded Linux system consists of several interconnected layers.
  Hardware Layer;
Physical components of the embedded system:
- CPU or microprocessor.
- RAM.
- Flash memory.
- Sensors and actuators.
- Communication interfaces.
- GPIO pins and peripheral controllers.
  Bootloader;
Initializes essential hardware and loads the Linux kernel into memory.
Examples:
- U-Boot.
- Barebox.
  Linux Kernel;
The core of the operating system. It manages hardware resources and provides essential operating system services.
Main functions:
- Process scheduling.
- Memory management.
- Device management.
- Interrupt handling.
- File system support.
- Networking.
- Security and access control.
  Device Drivers;
Software components that allow the kernel to communicate with hardware devices.
Examples:
- GPIO drivers.
- UART drivers.
- SPI drivers.
- I²C drivers.
- USB drivers.
- Ethernet drivers.
  Root Filesystem;
Contains the files and directories required by the Linux system.
It includes:
- System libraries.
- Executable programs.
- Configuration files.
- Device files.
- System utilities.
- Application files.
  Application Layer;
Contains programs developed to perform the specific functions of the embedded device.
Examples:
- Sensor monitoring.
- Motor control.
- Data acquisition.
- Network communication.
- AI inference.

 Embedded Linux Boot Process
Booting is the sequence of operations that takes place when an embedded Linux device is powered on.
  Typical boot sequence:
1. Power-on: The processor starts executing instructions from its reset address.
2. Boot ROM: Processor-specific startup code initializes enough hardware to locate the next boot stage.
3. Bootloader: Initializes essential hardware, configures memory and loads the kernel.
4. Kernel initialization: The Linux kernel initializes memory management, drivers, scheduling and other subsystems.
5. Root filesystem mounting: The kernel mounts the root filesystem.
6. Init system: The first userspace process, normally PID 1, starts system services.
7. Application startup: Embedded applications begin executing.
  Common init systems:
- systemd.
- BusyBox init.
- SysVinit.
Important: The exact boot sequence depends on the processor, boot configuration and embedded platform.

 Linux Kernel
The Linux kernel is the central component of the operating system. It acts as an interface between hardware and software.
  Main kernel responsibilities:
Process management:
- Creates and terminates processes.
- Schedules CPU time.
- Supports multitasking.
- Manages inter-process communication.
Memory management:
- Allocates and frees memory.
- Manages virtual memory.
- Handles memory protection.
- Supports memory mapping.
Device management:
- Controls hardware through device drivers.
- Handles device communication.
- Manages hardware resources
File system management:
- Supports file storage and access.
- Manages file permissions.
- Provides access to different filesystem types.
Networking:
- Implements network protocols.
- Manages network interfaces.
- Supports TCP/IP communication.
Interrupt handling:
- Responds to hardware and software interrupts.
- Coordinates events requiring immediate processor attention.

 Device Drivers
A device driver is software that allows the operating system to control and communicate with a hardware component.
Embedded Linux supports several driver types.
  Character Drivers;
Handle data as a stream of characters or bytes.
Examples:
- UART.
- Serial ports.
- Some sensor interfaces.
  Block Drivers;
Handle data in fixed-size blocks.
Examples:
- SD cards.
- eMMC storage.
- Hard drives.
  Network Drivers;
Control network communication hardware.
Examples:
- Ethernet controllers.
- Wi-Fi adapters.
  Common hardware interfaces:
- GPIO: General-purpose digital input/output.
- UART: Asynchronous serial communication.
- SPI: High-speed synchronous serial communication.
- I²C: Two-wire communication commonly used for sensors.
- USB: Universal Serial Bus for connecting peripherals.
- CAN: Controller Area Network, commonly used in automotive and industrial systems.

 Embedded Linux Filesystem Structure
Linux uses a hierarchical filesystem beginning at the root directory (/).
  Important directories:
- /bin — essential user commands.
- /sbin — essential system administration commands.
- /boot — kernel and boot-related files.
- /dev — device files.
- /etc — system configuration files.
- /home — user directories.
- /lib — essential shared libraries and kernel modules, depending on the distribution.
- /proc — virtual filesystem containing process and kernel information.
- /sys — virtual filesystem exposing device and kernel information.
- /tmp — temporary files.
- /usr — user applications, libraries and utilities.
- /var — variable data such as logs.
- /root — home directory of the root user.
Embedded Linux systems may use compact filesystem arrangements to reduce storage requirements.

 Root Filesystem (Rootfs)
The root filesystem contains the essential files required for Linux userspace operation.
  Common components:
- BusyBox utilities.
- C libraries such as glibc or musl.
- Init system.
- Device configuration.
- System applications.
- Configuration files.
  Common embedded filesystem formats:
SquashFS
- Read-only compressed filesystem.
- Saves storage space.
- Common in routers and embedded appliances.
JFFS2
- Flash filesystem designed for raw NAND/NOR flash.
- Supports wear management.
UBIFS
- Flash filesystem commonly used with UBI-managed NAND flash.
- Designed for larger raw flash devices.
ext4
- General-purpose journaling filesystem.
- Common on SD cards and eMMC storage.

 Cross-Compilation
Cross-compilation is the process of compiling software on one computer (host) for execution on another architecture (target).
   Example:
- Host: x86-64 Ubuntu computer.
- Target: ARM-based embedded board.
A cross-compiler produces executable code suitable for the target processor.
  Example toolchains:
- arm-linux-gnueabihf-gcc.
- aarch64-linux-gnu-gcc.
Example command:
    aarch64-linux-gnu-gcc program.c -o program
The resulting executable is intended for a compatible 64-bit ARM Linux environment.
  Important terms:
- Host: Computer used for development.
- Target: Embedded device running the compiled program.
- Toolchain: Compiler, linker, assembler and supporting tools.
- Sysroot: Target system headers and libraries used during compilation.
- ABI: Application Binary Interface defining how compiled programs interact with the system.

 Embedded Linux Build Systems
Build systems automate the creation of customized embedded Linux distributions.
  Buildroot;
A simple and efficient system for generating:
- Cross-compilation toolchains.
- Root filesystems.
- Kernel images.
- Bootloader images.
Suitable for relatively simple embedded Linux systems.
  Yocto Project;
A flexible framework for creating customized Linux distributions.
Important components:
- BitBake: Build execution engine.
- OpenEmbedded: Build infrastructure and metadata.
- Recipes: Instructions for building software packages.
- Layers: Organized collections of metadata and recipes.
- Images: Complete system configurations produced by the build.
Suitable for complex products requiring customization, reproducibility and long-term maintenance.
  OpenWrt;
A Linux distribution and build system commonly used for routers and networking devices.

 Important Embedded Linux Commands
  System information;
uname -a
cat /proc/cpuinfo
cat /proc/meminfo
lsblk
df -h
free -h
  File management;
ls
cd
pwd
mkdir
cp
mv
rm
find
  Process management;
ps aux
top
kill PID
systemctl status
  Hardware and devices
dmesg
lsusb
lspci
ls /dev
ls /sys/class
  Networking
ip addr
ip route
ping 8.8.8.8
ip link
  Storage and filesystems;
mount
umount
blkid
df -h
Note: Some commands may not be installed in minimal embedded distributions. For example, systemctl is used on systemd-based systems, not every embedded Linux system.

 Real-Time Embedded Linux
Standard Linux is designed for general-purpose multitasking and does not automatically guarantee strict real-time response.
Real-time embedded Linux is configured to provide more predictable response times.
The PREEMPT_RT patch improves Linux kernel preemption and reduces scheduling latency.
  Important concepts:
Latency
-The time between an event occurring and the system responding to it.
Jitter
-Variation in response time or execution timing.
Deadline
-The maximum permitted time for completing a task.
Priority Scheduling
-Higher-priority tasks receive preferential CPU scheduling.
Interrupt Handling
-Interrupts allow the processor to respond to hardware events without continuously polling devices.
Applications:
- Industrial automation.
- Robotics.
- Motion control.
- Audio processing.
- Automotive control subsystems.
Important distinction: PREEMPT_RT improves real-time behavior but does not automatically make every Linux application hard-real-time.

 Inter-Process Communication (IPC)
IPC allows different processes to exchange information and coordinate operations.
  Common mechanisms:
- Pipes: Transfer data between related processes.
- Named pipes (FIFOs): Allow communication through a filesystem entry.
- Message queues: Exchange structured messages.
- Shared memory: Allow processes to access a common memory region.
- Semaphores: Coordinate access to shared resources.
- Sockets: Support local or network communication.
Applications:
- Sensor data transfer.
- Communication between control applications.
- Robotics software modules.
- Industrial monitoring systems.

 Embedded Linux Security
Embedded devices frequently operate in connected environments, making security important.
  Important security practices:
1. Secure boot: Verify trusted boot software and system images.
2. User authentication: Use strong passwords and appropriate access controls.
3. File permissions: Restrict unauthorized access.
4. Firewall configuration: Control incoming and outgoing network traffic.
5. Software updates: Patch known vulnerabilities.
6. Encryption: Protect sensitive information.
7. Minimal software: Remove unnecessary packages and services.
8. Secure communication: Use protocols such as SSH and TLS.
9. Hardware security: Protect debug interfaces and sensitive keys.

 Embedded Linux Applications
  IoT Systems;
- Sensor data collection.
- Gateway communication.
- MQTT-based messaging.
- Remote monitoring.
  Robotics;
- Motor control coordination.
- Sensor fusion.
- Computer vision.
- Navigation and mapping.
  Industrial Automation;
- Machine monitoring.
- Process control.
- Data acquisition.
- Industrial communication.
  Networking;
- Routers.
- Firewalls.
- Network gateways.
- Wireless access points.
  Artificial Intelligence;
- Image classification.
- Object detection.
- Speech recognition.
- Edge AI inference.

 Embedded Linux vs Microcontroller-Based Systems
  Embedded Linux:
- Usually runs on an MPU or application processor.
- Supports multitasking.
- Provides memory protection and virtual memory.
- Supports complex applications.
- Can run networking stacks and databases.
- Requires more RAM and storage.
- Has a more complex boot process.
Bare-metal or RTOS-based systems:
- Commonly run on microcontrollers.
- Have smaller memory requirements.
- Offer more direct hardware control.
- Can provide predictable real-time behavior.
- Often have simpler startup procedures.
- Are suitable for dedicated control applications.
Example:
A Raspberry Pi running Linux can handle image processing, databases and network communication, while an STM32 microcontroller can handle precise motor-control operations.
The two can work together in one embedded system.

 Practical Embedded Linux Project
  Project: Linux-Based IoT Environmental Monitoring System
Objective: Build an embedded Linux device that collects environmental sensor data and transmits it to a remote monitoring platform.
Required components:
- Raspberry Pi or another Linux-capable embedded board.
- Temperature and humidity sensor.
- ADC module if using an analog sensor.
- Internet connection.
- Python.
- MQTT broker or IoT platform.
Working principle:
1. The Linux device boots and initializes its hardware.
2. A sensor interface reads temperature and humidity.
3. A Python application processes the measurements.
4. The application publishes the data through MQTT.
5. A remote platform receives and stores the data.
6. Users monitor environmental conditions through a dashboard.
Skills developed:
- Linux system administration.
- GPIO and sensor interfacing.
- Python programming.
- Networking.
- MQTT communication.
- Embedded application development.

 Important Examination and Practical Tips
- Understand the architecture and layers of Embedded Linux.
- Know the functions of the bootloader, kernel, drivers and root filesystem.
- Memorize the Linux boot sequence.
- Understand character, block and network device drivers.
- Distinguish Buildroot, Yocto and OpenWrt.
- Understand cross-compilation and toolchains.
- Know important Linux filesystem directories.
- Understand IPC mechanisms.
- Distinguish standard Linux from real-time Linux.
- Understand the difference between embedded Linux and microcontroller-based systems.
- Practise Linux terminal commands on Ubuntu or a Raspberry Pi.
- Remember that embedded Linux is highly customizable for specific hardware and applications.

KEY TAKEAWAY:
Embedded Linux is a customized Linux-based operating system used to develop sophisticated embedded devices. 
Its architecture combines a bootloader, Linux kernel, device drivers, root filesystem and application software to provide hardware control, multitasking, networking and advanced computing capabilities.