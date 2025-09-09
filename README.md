# Introduction
This repository provides comprehensive engineering documentation and design specifications for an autonomous vehicle prototype, developed for the 2025 WRO Open Championship Asia &amp; Pacific – Philippines, under the Future Engineers Challenge category.

## Content
* `schemes` folder includes one or more JPEG, PNG, or PDF schematic diagrams of the electromechanical components that show all of the parts (motors and electrical components) utilized in the car and their connections.
* `src`  folder includes all of the programming flowcharts and code needed to compete in WRO 2025 Open Championship Asia &amp; Pacific - Philippines, under the Future Engineers Challenge category. 
* `photos - team & vehicle` folder contains photographs of the team members and vehicles from all angles, including top and bottom views, as well as the photo that was included in the documentation.
* `video` folder contains video.md file that demonstrates how to robot funtions to solve both tasks (Open Challenge & Obstacle Challenge).
* `models` folder contains the 3D design of the vehicle in .lxf and the rendered model of the vehicle.
* `others` folder contains additional files that can be utilized to learn how to understand the car set up for the competition.

# NovaTech Team, Malaysia
We are Team NovaTech from Malaysia, proudly representing our country in the Future Engineers category of the World Robot Olympiad (WRO) Open Championship (Asia & Pacific) 2025. Our team consists of three passionate and dedicated members:
* Lai Chaun Choy
* Adam Syahmi Bin Mohd Syahrizal
* Muhammad Hakim Bin Khairul Azam

![image](https://github.com/user-attachments/assets/ae78726b-bb93-4ce8-8b34-3485730f5529) 

Each member brings a unique set of skills and perspectives to the team—ranging from hardware engineering and programming to system design and project management. Together, we share a common interest in robotics and innovation, and through this project, we aim to explore real-world applications of autonomous vehicle technology while enhancing our collaboration, critical thinking, and engineering skills.

## Performance Video
To demonstrate the functionality and the capabilities of our self-driving car prototype, we have recorded a performance video showcasing its navigation, obstacle avoidance, and autonomous decision-making in a simulated environment. The video highlights key features such as wall tracking, sensor-based movement, and system stability under various conditions. This visual documentation provides evidence of our vehicle's real-time performance and serves as a practical validation of our design and programming approach.
The video can be accessed via the following link or by scanning the attached QR code.

(QR CODE)

# 1.0 Mobility Management

The mobility management section should provide a comprehensive analysis of the car’s locomotion system, detailing how movement is achieved and regulated. This includes the specification and justification of motor types selected, along with the integration process and control mechanisms implemented. A technical overview of the car chassis also had been included, covering either custom fabrication or off-the-shelf selection, as well as the structural layout and component mounting strategy. Key mechanical and electrical engineering parameters such as torque, rotational speed (RPM), gear ratios, and power requirements had been addressed to demonstrate performance optimization.

## 1.1 Self-Driving Car Design

The self-driving car was designed with an emphasis on modularity, stability, and functional integration to meet the requirements of the Future Engineers Challenge. The chassis was constructed using a combination of LEGO® Mindstorms® Education Core Set (45544), Education Expansion Set (45560), and LEGO® Spike® Prime Education elements, creating a lightweight yet durable frame that supports efficient weight distribution and secure component placement. For propulsion, the WHEELTEC MG310P20 7.4V L motors with encoders were selected to deliver consistent torque and precise speed control. Steering is managed by a light DS-E001D micro servo motor, which provides quick and accurate angular adjustments while minimizing additional weight on the front axle. The integration of the Pixy2 vision camera and auxiliary digital modules enhances the vehicle’s ability to perform autonomous navigation and obstacle detection. This design highlights the synergy of lightweight steering control, robust propulsion, and structural stability, resulting in an effective engineering solution for autonomous driving in a competitive robotics environment.

|![Image](https://github.com/user-attachments/assets/0450d784-8dff-496e-90d7-f4238744cb3d) Front View|![Image](https://github.com/user-attachments/assets/0c5133b3-e71c-4c82-ab42-77784d581a45) Rear View| 
| ----------- | ----------- |
|![Image](https://github.com/user-attachments/assets/c1bba12d-1e39-47ab-a7f2-abb3f0b542cd)Left View|![Image](https://github.com/user-attachments/assets/2c8916ed-96d0-4b80-bfd8-33060fa7d230)Right View|
|![Image](https://github.com/user-attachments/assets/6f88da07-31ea-4bda-971b-134a84c220f6) Top View | ![Image](https://github.com/user-attachments/assets/40e6f9e2-84d8-4c12-9df2-fb3b502153dd) Bottom View|


## 1.2 Chassis of Self-Driving Car

The self-driving car prototype was constructed using the LEGO® Mindstorms® Education Core Set (45544) in combination with the Education Expansion Set (45560) and  LEGO® Spike Prime Education Set, which together provided a versatile and modular chassis framework. The structural components from the Expansion Set were utilized to reinforce the base and create a stable platform capable of supporting additional electronics, while the Core Set contributed essential mechanical elements such as beams, axles, and connectors for precise assembly. The Spike Prime set supplied modern elements with improved versatility and modularity, enhancing the structural rigidity and enabling compact mounting of electronic components such as sensors and controllers. This ®-based chassis was selected due to its lightweight yet durable properties, allowing for easy modification during the design iteration process

### 1.2.1 Self-Driving Car's Tyre

The LEGO® TYRE NORMAL WIDE Ø43,2 X 22 44309 and RIM WIDE W.CROSS 30x20 56145 were selected as the front tyres of the self-driving car. Their medium size provides an optimal contact surface with the competition field, reducing slippage while ensuring smooth steering response. When paired with the DS-E001D micro servo motor for directional control, these tyres enable precise angular adjustments, which are critical for autonomous navigation tasks.
 We selected the LEGO® 44771 tyres and RIM Ø 56 X 34 15038 as the rear tyres due to their excellent grip and compatibility with our wheel and axle setup. These tyres offer reliable traction on various surfaces, which is essential for accurate movement and stability during autonomous navigation. Their size and tread pattern help maintain balance and reduce slipping, especially when the car is turning or adjusting its path.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/22f59c8e-0994-465b-8f58-ac4e499d2df7" />

### 1.2.2 Gear System of Self Driving Car

Our self-driving car uses a differential gear system to improve its turning performance and overall movement control. The differential allows the left and right wheels to rotate at different speeds when the car is turning, which helps prevent wheel skidding and improves stability. This is especially important during autonomous navigation, where precise movement is required. By evenly distributing torque between the wheels, the differential gear also helps maintain balance and smooth transitions when changing direction. Using LEGO® Technic components, the differential is integrated into the drivetrain in a compact and efficient layout, ensuring both functionality and ease of maintenance.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/20cc6de7-0ba1-4c0a-98ec-97d99a59d0b9" />

### 1.2.3 Selection of Motor and Its Engineering Principle

(i)	Main Motor: WHEELTEC MG310P20 7.4V L

For the main propulsion system, the WHEELTEC MG310P20 7.4V L DC motor with integrated encoder was selected due to its balance of torque, speed, and precise feedback control. The encoder provides real-time rotational data, enabling closed-loop control that is essential for accurate navigation and maintaining consistent velocity during autonomous tasks. 

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a5ae5be9-0228-4e45-b409-f1a83c3b270a" />

(ii) Steering Motor : DS-E001D Micro Servo Motor 

The DS-E001D micro servo motor is a compact and lightweight actuator used for small, precise movements on our car. It operates at low voltage, making it compatible with thepower source from the LJ501855 battery and the ESP32 control system. This servo is ideal for tasks such as steering mechanisms, sensor alignment, or activating small attachments. Its design allows easy integration with LEGO®-compatible mounting points, enabling flexible positioning on the chassis. With its quick response time and accurate angle control, the DS-E001D enhances the car’s ability to perform controlled, repeatable actions during autonomous navigation.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/52ecd8c5-3ca7-45e3-8a03-53d54eafd9e0" />

### 1.2.4 Connection of Motor the Chassis

he WHEELTEC MG310P20 7.4V DC motors are mounted to the chassis using adapted LEGO® Mindstorms structural elements. The LEGO® beams and frames serve as a modular mounting system, allowing precise positioning of the motors without the need for 3D custom-machined brackets. This modular design also enables quick adjustments or replacements during testing and competition.
The motor shafts are connected to the LEGO® axle system, which is integrated into the differential gear mechanism. The LEGO® connectors ensure that torque from the motors is effectively transferred to the drivetrain while keeping alignment consistent. Since LEGO® parts are manufactured to tight tolerances, the fit between the motor mounts and chassis is secure, minimizing vibration and preventing misalignment during operation.
The use of LEGO® components also allows for non-permanent but rigid connections, which is advantageous for prototyping. Motors can be detached easily for inspection or modification, while still maintaining structural integrity during runs. Wiring from the motors to the TB6612FNG motor driver is routed along the LEGO® beams, secured with clips to avoid interference with the wheels or moving parts.

## 1.3 Steering

Our self-driving car implements an Ackermann steering system, which is designed to mimic the natural turning geometry used in real-world vehicles. This system ensures that the inner and outer front wheels turn at different angles during a curve, allowing for smoother and more accurate cornering. By minimizing tyre slip and mechanical strain, Ackermann steering improves the car’s handling and reduces energy loss during turns. We built the steering mechanism using LEGO Technic components, carefully aligning the pivot points to approximate true Ackermann geometry. This setup is mechanically efficient and integrates well with our differential gear system, resulting in precise directional control and crucial for autonomous path following tasks.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2ecc3480-f90d-45dd-b2cf-88664e73e11f" />

# 2.0 Power Source, Sense and Control Panel Management

The Power Source, Sense, and Control Board Management section outlines the essential subsystems that ensure reliable operation and intelligent performance of the self-driving car. A stable and efficient power source is crucial for supporting motors, sensors, and processing units, while proper management prevents voltage fluctuations that may compromise system performance. The sensing components, including vision and environmental detectors, act as the vehicle’s perception system, enabling it to interpret surroundings and respond accurately to dynamic conditions. Meanwhile, the control board integrates hardware and software coordination, serving as the central hub for decision-making, signal processing, and command execution. 

Together, these three subsystems form the backbone of the autonomous vehicle, ensuring seamless interaction between energy supply, environmental awareness, and computational control.


## 2.1 Power Source

The LJ501855 Battery provides 7.4 V and 1400 mAh. The battery acts as the energy for all the car’s electronic components and motors. It delivers stable voltage output, ensuring that the sensors, control board, and motor driver function without interruptions. Its capacity allows for extended operation, reducing the need for frequent charging during development and competition. The compact design fits neatly within the LEGO® chassis, keeping the weight balanced for better stability.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/16dcc6ad-eb38-4a4c-9059-128d13882532" />

## 2.2 Sensor and Control Panel

| Control Board | Control Board (Closed-Up) |
| ----------- | ----------- |
| ![Image](https://github.com/user-attachments/assets/a421cb90-f355-4308-b93c-6a0d18a976ab) | ![Image](https://github.com/user-attachments/assets/dcfa7f53-67e3-44d7-818e-919a234d5cbe) | 



**(i) Main Controller**
ESP32-S3-DevKitC-1

The ESP32-S3-DevKitC-1 serves as the primary control unit of our self-driving car. Powered by the ESP32-S3 microcontroller, it features a dual-core Xtensa® 32-bit LX7 processor with integrated Wi-Fi and Bluetooth Low Energy (BLE), allowing for wireless debugging, data transmission, and potential remote control functions. The ESP32-S3 offers high processing power and AI acceleration instructions, making it ideal for handling real-time sensor inputs, executing navigation algorithms, and controlling actuators. In our robot, it processes data from the camera, color sensor, and distance sensors to make immediate driving decisions. Its compact size, multiple GPIO pins, and low power consumption make it a versatile choice for embedded vehicle applications.'

**(ii) Power Regulator**
Mini MP1584EN DC-DC Buck Converter

The Mini MP1584EN is a high-efficiency step-down (buck) DC-DC converter used to regulate voltage for the robot’s components. It can convert higher input voltages from the battery to stable, lower voltages suitable for sensitive electronics. In our robot, the MP1584EN is configured to provide a regulated 5V supply for sensors, the main controller, and other modules. Its adjustable output voltage, compact size, and high conversion efficiency help maintain consistent performance while minimizing power losses and heat buildup. This ensures that all components receive clean and stable power, which is crucial for preventing malfunctions during operation.

**(iii) Motor Control**
TB6612FNG DC Motor Driver

The TB6612FNG DC Motor Driver is responsible for controlling the rotational direction and speed of the robot’s DC motors. It can drive two DC motors independently, with forward, reverse, brake, and stop control functions. The driver supports a wide operating voltage range and provides up to 1.2A continuous current per channel, with a peak output of 3.2A. In our self-driving car, the TB6612FNG receives Pulse Width Modulation (PWM) signals from the main controller to precisely adjust motor speed, enabling smooth acceleration, deceleration, and turning. Its dual H-bridge design ensures efficient power transfer and low heat generation, which is essential for reliable performance during long runs.

**(iv) Color Detection System**
TCS3472 RGB Color Sensor

Our self-driving car integrates the TCS3472 RGB Color Sensor to enhance its ability to detect and respond to specific colors in the competition environment. The TCS3472 is an advanced color recognition module that combines a red, green, and blue (RGB) sensing element with a clear photodiode, along with an IR blocking filter to improve color accuracy under different lighting conditions. It also features an integrated ADC (Analog-to-Digital Converter) that outputs digital values for each color channel, making it easy to process data on the main controller without additional signal conditioning.

In our application, the TCS3472 is primarily used to identify colored markers on the track, which serve as navigation and control signals for the car. This direct color recognition capability is essential for obstacle avoidance and ensures that the car responds to visual cues without relying solely on shape detection from the camera

**(v) Laser Sensor**
VL53L0X Time-of-Flight Sensor

The VL53L0X is a laser-based Time-of-Flight (ToF) distance sensor used in our self-driving car for precise obstacle detection. It emits an invisible infrared laser and measures the time it takes for the light to bounce back from an object, calculating distances with millimeter-level accuracy. The sensor has a range of up to 2 meters in optimal conditions and is unaffected by object color or reflectivity, making it more reliable than traditional IR proximity sensors. In our application, the VL53L0X is used for detecting nearby obstacles and assisting in parking maneuvers. By providing real-time distance data to the main controller, it allows the car to slow down, stop, or navigate around objects with high precision.

**(vi) Camera Sensor**
Pixy2 CMUcam5 Smart Vision Sensor

In our self-driving car, the Pixy2 Camera is used exclusively for object and colour signature recognition, which plays a crucial role in the vehicle's ability to navigate the environment. We trained the Pixy2 to detect specific colour markers placed on objects such as pillars and parking boundaries. These colour signatures act as visual cues that allow the robot to identify obstacles and make appropriate navigation decisions. For example, the car uses the Pixy2 to recognize coloured pillars and determine whether to steer left or right to avoid collisions. Additionally, the camera helps the vehicle detect designated parking zones and execute precise movements when entering or exiting these areas.

The Pixy2 is mounted at the top of the chassis with a clear line of vision toward the forward surroundings. It is calibrated using PixyMon v2 software, where we fine-tuned the camera’s brightness, colour threshold, and exposure settings to ensure consistent object detection under different lighting conditions. By offloading the visual processing to the camera's onboard system, we reduce the processing burden on the main controller, allowing for quicker reactions and smoother movements.

**(vii) Orientaion and Motion Sensing**
GY-BNO08X Gyro

In our design, the GY-BNO08X is used to monitor the car’s heading, measure changes in orientation, and correct drift during navigation. This is especially important in scenarios such as the Open Challenge, where the car must maintain straight paths, execute precise turns, and recover its correct heading after obstacle avoidance maneuvers. The sensor enables the car to adjust steering in real time, ensuring smooth and stable movement, even over longer distances where accumulated error from wheel encoders or motor control alone would become significant The stability and precision provided by the GY-BNO08X directly improve our self-driving car’s ability to handle parking maneuvers, obstacle avoidance, and straight-line navigation with minimal deviation.

**(viii) Audible Feedback** 
MH-FMD Active Buzzer

The MH-FMD Active Buzzer is used in our self-driving car to provide audible signals for status indication and debugging purposes. Unlike passive buzzers, the active buzzer contains an internal oscillator, allowing it to generate sound simply by supplying power. In our design, it is triggered by the controller to produce beeps that signal events such as successful start-up, obstacle detection, or completion of a parking maneuver. This feature assists in both competition runs and testing phases, giving operators a quick, non-visual method of understanding the robot’s current status.
 
**(ix) Button: PCB Mounted Circuit Button** 

a PCB mounted circuit button was integrated as a user-interface component to provide manual control and initialization functions. The button allows the team to safely start and stop the autonomous program and reset calibration routines such as sensor alignment before a trial. Its direct placement on the PCB ensures durability, compact wiring, and ease of accessibility, which reduces the likelihood of connection errors during competition.


## 2.3 Build of Materials
List below shows the record of all the components, materials and parts used in the construction of the self-driving car. It serves as a structured inventory that details the specifications, quantities, and sources of each item, ensuring clarity and accuracy in the design process.

<img width="470" height="689" alt="Image" src="https://github.com/user-attachments/assets/460d8bb4-73ce-47d1-bbd2-afd3187cd65f" />
<img width="470" height="689" alt="Image" src="https://github.com/user-attachments/assets/3fee17a6-239f-40ae-a14b-62ee9bbf9e7a" />
<img width="470" height="689" alt="Image" src="https://github.com/user-attachments/assets/48d63e07-5e11-409a-9711-80e596f310ba" />
<img width="470" height="689" alt="Image" src="https://github.com/user-attachments/assets/fc0a2b3a-737c-42b2-bade-8b12cb38e5eb" />
<img width="470" height="689" alt="Image" src="https://github.com/user-attachments/assets/85f19cf6-c20b-429d-9a60-17248c07fc93" />

## Wiring Diagram
The wiring schematic illustrates the electrical connections between the power source, control board, sensors and actuators, providing a clear reference for assembly, troubleshooting, and system maintenance.

The following diagram illustrates the both wiring connections for the Open Challenge and Obstacle Challenge:

![Image](https://github.com/user-attachments/assets/13d69007-0f13-4c8a-b260-f4b65a1331a0)

# 3.0 Obstacle Management
## 3.1 Open Challenge
In the Future Engineers Open Challenge, both time-of-flight (ToF) sensors can be used to detect the distance between inner and outer walls. An exact distance is coded into the program to maintain its distance between the walls and ensure accurate alignment between the walls. These sensors are also used to determine the direction of its path during the round; if the right side of the wall is bigger than the left, it will go clockwise and vice versa. The gyro ensures that the vehicle stays on a straight path.

The following diagram presents the flowchart for the Open Challenge:

<img width="1067" height="2194" alt="Image" src="https://github.com/user-attachments/assets/65d61b2d-adfd-4412-b42b-54570752431f" />

## 3.2 Obstacle Challenge
By using a time-of-flight (ToF) sensor, the vehicle can measure the relative distance to surrounding walls or obstacles and then decide whether to navigate clockwise or counterclockwise based on which direction provides a clearer, shorter or safer path. After the vehicle finishes its 3 laps of round, the vehicle is doing its parallel parking. The ToF sensor is used to measure the distance between two parking blocks for the vehicle park inside the area. The Pixy2 camera can be used in the Future Engineers Obstacle Challenge to detect red and green traffic signs, helping the car decide the correct side to pass before completing the parallel parking task. The parking area is also determined by the detection of its colour. To ensure the vehicle moves in the correct orientation and angular velocity, the gyro allows it to maintain a stable heading, detect turns and decide whether to steer clockwise or counterclockwise during obstacle navigation.

The following diagram presents the flowchart for the Obstacle Challenge:

<img width="3034" height="2498" alt="Image" src="https://github.com/user-attachments/assets/8a806c63-5430-4c09-811d-400db80cd3c6" />

# 4.0 Engineering Factors
Most of the parts on our robot are designed to be modular and easy to replace. This makes it very convenient for us during testing and competition because if any component breaks or stops working, we don’t need to rebuild the whole system from scratch. Instead, we can simply unplug the damaged part and quickly plug in a new one. This not only saves us time but also makes troubleshooting much less stressful. Using LEGO-based structures and standardized electronic modules also helps keep everything organized and ensures that replacements can be done smoothly without affecting the overall design of the robot.

### 4.1	Ackermann Steering
We used Ackermann steering for the steering system of our robot. This type of steering mechanism allows the wheels to turn at different angles when making a corner, which makes the movement smoother and more efficient. By using Ackermann steering, our robot can achieve a larger turning angle while reducing friction between the wheels and the ground. This not only improves the accuracy of our turns but also reduces wear on the tyres and helps the vehicle maintain better stability during navigation. It is especially useful in tight spaces on the competition field where precise and controlled turning is important.

### 4.2	Differential Gear
We also applied a differential gear system to our driving motor. The purpose of using a differential is to allow the left and right wheels to rotate at different speeds, especially when the robot is making a turn. Without a differential, both wheels would be forced to spin at the same speed, which could cause skidding, higher friction, and unstable movement. By having this system in place, our robot is able to turn more smoothly and efficiently while maintaining better balance. This setup improves overall handling and makes the driving motion more natural, similar to how real cars function on the road.

### 4.3	Special angle and placement of the PixyMonV2 Camera
We tested the PixyMon V2 camera at different angles to find the most suitable placement for our robot. After several trials, we discovered that positioning the camera at a 20° angle provided the best field of view between the robot and the obstacles on the track. With this setup, the Pixy2 Camera is able to detect obstacles from a greater distance and give the robot enough time to respond. As a result, our robot can avoid obstacles more efficiently and move around them in a smoother and more controlled manner.

# 5.0 Improvements and Enhancements
We have changed our camera from an OpenMV H7 camera to Pixy Mon V2 Camera. This is because PixyMonV2 has a wider lens view compared to the open MV H7 Camera. This can help our robot to scan a wider view and have a better vision when avoiding obstacles. This may prevent our robot from missing the obstacles on the field and go in the wrong direction. This also helps our robot to avoid turning back too soon after passing an obstacle.

# ** Credits** 

