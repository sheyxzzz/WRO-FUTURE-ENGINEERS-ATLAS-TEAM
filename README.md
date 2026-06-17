TEAM ATLAS FUTURE ENGINEERS 2026
====
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/ea5d485b-9a20-4710-9be6-f97996d91661" />

An autonomous vehicle prototype developed for the WRO Future Engineers category, which integrates a vision system powered by the Pixy smart camera. By leveraging real-time image processing and data fusion, the robot is capable of dynamic navigation, adapting to complex environments and avoiding obstacles with high precision.


## Content

* `t-photos` This section has 2 cool photos of us as a team so you can get to know us✨🌀
* `v-photos` This section has 6 photos of the vehicle covering every single angle (front, back, sides, top, and bottom)🚙📸
* `video`  markdown file with the link to a video showing the robot in action, tearing up the track💨
* `schemes`One or more schematics (JPEG, PNG, or PDF) showing all the electromechanical components: motors, sensors, and electronics, and exactly how they connect to each other⚡️
* `src` All the code used to control every single component and make the robot race-ready🧠.
* `models`The source files for 3D printers, laser cutters, or CNC machines used to custom-make the vehicle's parts🧩
* `other` Anything else needed to understand how to get the robot ready for the track. This includes datasets, hardware specs, communication protocol breakdowns, and assembly guides📑

## Overview🚨

The prototype is a fully autonomous mobile robot built with an integrated mechatronics setup, designed to crush the tracks in the World Robot Olympiad’s Future Engineers category. At the heart of it all is an Arduino control unit running the main control loop, handling peripheral signals, and managing the power stage via PWM (Pulse Width Modulation). For track-following and sign recognition, we hooked up a Pixy2 PixyCam. It processes images locally using color segmentation algorithms and feeds the target position vectors straight to the microcontroller via an SPI or I2C serial interface. To spot unexpected obstacles and avoid close-range crashes, the car uses an array of time-of-flight ultrasonic sensors spaced out around the chassis, which calculate distance by measuring high-frequency pulse returns.
Instead of a basic, conventional setup, the locomotion relies on a single-motor drivetrain. A single DC motor drives the wheels to set the car’s linear speed, working hand-in-hand with a steering mechanism to control the turning angle. To lock in precise speed control and track our path, we integrated just one quadrature encoder coupled directly to the drive motor shaft. This rotary sensor generates electrical pulses that the Arduino decodes using hardware interrupts, letting us calculate the actual linear speed in real time and estimate the total distance covered via odometry. This actively compensates for torque loss from friction or battery voltage drops.

## Cómo preparar el repositorio en función de la plantilla

_Elimine esta sección antes de la primera confirmación en el repositorio_

1. Clone este repositorio utilizando la funcionalidad `git clone`.
2. Elimine el directorio `.git`
3. [Inicialice un nuevo repositorio público en GitHub](https://github.com/new) siguiendo las instrucciones de la sección "Crear un nuevo repositorio en la línea de comandos" (que aparece después de presionar el botón "Crear repositorio").



_Remove this section before the first commit to the repository_

1. Clone this repo by using the `git clone` functionality.
2. Remove `.git` directory
3. [Initialize a new public repository on GitHub](https://github.com/new) by following instructions from "create a new repository on the command line" section (appeared after pressing "Create repository" button).
