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
The mobility management section should provide a comprehensive analysis of the vehicle’s locomotion system, detailing how movement is achieved and regulated. This includes the specification and justification of motor types selected, along with the integration process and control mechanisms implemented. A technical overview of the vehicle chassis also had been included, covering either custom fabrication or off-the-shelf selection, as well as the structural layout and component mounting strategy. Key mechanical and electrical engineering parameters such as torque, rotational speed (RPM), gear ratios, and power requirements had been addressed to demonstrate performance optimization.
## 1.1 Self-Driving Car Design

## 1.2 Chassis of Self-Driving Car
Our self-driving car uses a strong and lightweight chassis built with LEGO Technic parts. The main structure is based on the LEGO 32019 rim, which provides a solid base to attach motors, sensors, and other components. We use a differential gear system to help the car turn smoothly and maintain balance when moving. The tyres used are LEGO 86652, chosen for their good grip and stability on different surfaces. This chassis design is easy to modify and allows us to test and improve the car during development. It also keeps the weight evenly distributed, which helps the car move more accurately during autonomous tasks.
### 1.2.1 Self-Driving Car's Tyre
For our self-driving car, we selected the LEGO 86652 tyres due to their excellent grip and compatibility with our wheel and axle setup. These tyres offer reliable traction on various surfaces, which is essential for accurate movement and stability during autonomous navigation. Their size and tread pattern help maintain balance and reduce slipping, especially when the car is turning or adjusting its path. The tyres also support the differential gear system effectively, allowing smooth power distribution between the left and right wheels. Overall, the LEGO 86652 tyres contribute to better control, performance, and safety of the vehicle throughout its operation.
### 1.2.2 Differential Gear
Our self-driving car uses a differential gear system to improve its turning performance and overall movement control. The differential allows the left and right wheels to rotate at different speeds when the car is turning, which helps prevent wheel skidding and improves stability. This is especially important during autonomous navigation, where precise movement is required. By evenly distributing torque between the wheels, the differential gear also helps maintain balance and smooth transitions when changing direction. Using LEGO Technic components, the differential is integrated into the drivetrain in a compact and efficient layout, ensuring both functionality and ease of maintenance.

### 1.2.3 Selection of Motor and Its Engineering Principle

### 1.2.4 Connection of Motor the Chassis
The WHEELTEC MG310P20 7.4V DC motors are mounted to the chassis using adapted LEGO Mindstorms structural elements. The LEGO beams and frames serve as a modular mounting system, allowing precise positioning of the motors without the need for custom-machined brackets. This modular design also enables quick adjustments or replacements during testing and competition.
The motor shafts are connected to the LEGO axle system, which is integrated into the differential gear mechanism. The LEGO connectors ensure that torque from the motors is effectively transferred to the drivetrain while keeping alignment consistent. Since LEGO parts are manufactured to tight tolerances, the fit between the motor mounts and chassis is secure, minimizing vibration and preventing misalignment during operation.
The use of LEGO components also allows for non-permanent but rigid connections, which is advantageous for prototyping. Motors can be detached easily for inspection or modification, while still maintaining structural integrity during runs. Wiring from the motors to the TB6612FNG motor driver is routed along the LEGO beams, secured with clips to avoid interference with the wheels or moving parts.
By integrating LEGO Mindstorms parts into the chassis design, the team achieves a balance between structural stability, ease of modification, and alignment accuracy—key factors for consistent performance in the self-driving car challenge.

## 1.3 Steering
Our self-driving car implements an Ackermann steering system, which is designed to mimic the natural turning geometry used in real-world vehicles. This system ensures that the inner and outer front wheels turn at different angles during a curve, allowing for smoother and more accurate cornering. By minimizing tyre slip and mechanical strain, Ackermann steering improves the car’s handling and reduces energy loss during turns. We built the steering mechanism using LEGO Technic components, carefully aligning the pivot points to approximate true Ackermann geometry. This setup is mechanically efficient and integrates well with our differential gear system, resulting in precise directional control and crucial for autonomous path following tasks.

# 2.0 Power and Sense Management

## 2.1 Power Source

## 2.2 Sensor

**Front view of the robot**

**Back view of the robot**

**(i) Main Controller**
ESP32-S3-DevKitC-1

The ESP32-S3-DevKitC-1 serves as the primary control unit of our self-driving car. Powered by the ESP32-S3 microcontroller, it features a dual-core Xtensa® 32-bit LX7 processor with integrated Wi-Fi and Bluetooth Low Energy (BLE), allowing for wireless debugging, data transmission, and potential remote control functions. The ESP32-S3 offers high processing power and AI acceleration instructions, making it ideal for handling real-time sensor inputs, executing navigation algorithms, and controlling actuators. In our robot, it processes data from the camera, color sensor, and distance sensors to make immediate driving decisions. Its compact size, multiple GPIO pins, and low power consumption make it a versatile choice for embedded robotics applications.'

**(ii) Power Regulator**
Mini MP1584EN DC-DC Buck Converter

The Mini MP1584EN is a high-efficiency step-down (buck) DC-DC converter used to regulate voltage for the robot’s components. It can convert higher input voltages from the battery to stable, lower voltages suitable for sensitive electronics. In our robot, the MP1584EN is configured to provide a regulated 5V supply for sensors, the main controller, and other modules. Its adjustable output voltage, compact size, and high conversion efficiency help maintain consistent performance while minimizing power losses and heat buildup. This ensures that all components receive clean and stable power, which is crucial for preventing malfunctions during operation.

**(iii) Motor Control**
TB6612FNG DC Motor Driver

The TB6612FNG DC Motor Driver is responsible for controlling the rotational direction and speed of the robot’s DC motors. It can drive two DC motors independently, with forward, reverse, brake, and stop control functions. The driver supports a wide operating voltage range and provides up to 1.2A continuous current per channel, with a peak output of 3.2A. In our self-driving car, the TB6612FNG receives Pulse Width Modulation (PWM) signals from the main controller to precisely adjust motor speed, enabling smooth acceleration, deceleration, and turning. Its dual H-bridge design ensures efficient power transfer and low heat generation, which is essential for reliable performance during long runs.

**(v) Color Sensor**
TCS3472 RGB Color Sensor

Our self-driving car integrates the TCS3472 RGB Color Sensor to enhance its ability to detect and respond to specific colors in the competition environment. The TCS3472 is an advanced color recognition module that combines a red, green, and blue (RGB) sensing element with a clear photodiode, along with an IR blocking filter to improve color accuracy under different lighting conditions. It also features an integrated ADC (Analog-to-Digital Converter) that outputs digital values for each color channel, 

**(vi) Laser Sensor**
VL53L0X Time-of-Flight Sensor

The VL53L0X is a laser-based Time-of-Flight (ToF) distance sensor used in our self-driving car for precise obstacle detection. It emits an invisible infrared laser and measures the time it takes for the light to bounce back from an object, calculating distances with millimeter-level accuracy. The sensor has a range of up to 2 meters in optimal conditions and is unaffected by object color or reflectivity, making it more reliable than traditional IR proximity sensors. In our application, the VL53L0X is used for detecting nearby obstacles and assisting in parking maneuvers. By providing real-time distance data to the main controller, it allows the car to slow down, stop, or navigate around objects with high precision.

**(iv) Camera Sensor**
Pixy2 CMUcam5 Smart Vision Sensor

In our self-driving car, the Pixy2 Camera is used exclusively for object and colour signature recognition, which plays a crucial role in the vehicle's ability to navigate the environment. We trained the Pixy2 to detect specific colour markers placed on objects such as pillars and parking boundaries. These colour signatures act as visual cues that allow the robot to identify obstacles and make appropriate navigation decisions. For example, the car uses the Pixy2 to recognize coloured pillars and determine whether to steer left or right to avoid collisions. Additionally, the camera helps the vehicle detect designated parking zones and execute precise movements when entering or exiting these areas.

The following figures shows a close-up view of the Pixy2 Camera: 
(JPG)

The Pixy2 is mounted at the top of the chassis with a clear line of vision toward the forward surroundings. It is calibrated using PixyMon v2 software, where we fine-tuned the camera’s brightness, colour threshold, and exposure settings to ensure consistent object detection under different lighting conditions. By offloading the visual processing to the camera's onboard system, we reduce the processing burden on the main controller, allowing for quicker reactions and smoother movements.

**(vii) Orientaion and Motion Sensing**
GY-BNO08X Gyro

Our self-driving car is equipped with the GY-BNO08X 9-axis absolute orientation sensor, which plays a role in maintaining accurate navigation and stability during autonomous operation. The GY-BNO08X integrates a 3-axis gyroscope, a 3-axis accelerometer, and a 3-axis magnetometer, along with the Bosch BNO080/BNO085 sensor fusion chip. This combination allows it to provide highly accurate orientation data, including quaternion, Euler angles, and linear acceleration, without the need for complex calculations on the main controller.

In our design, the GY-BNO08X is used to monitor the car’s heading, measure changes in orientation, and correct drift during navigation. This is especially important in scenarios such as the Open Challenge, where the car must maintain straight paths, execute precise turns, and recover its correct heading after obstacle avoidance maneuvers. The sensor enables the robot to adjust steering in real time, ensuring smooth and stable movement, even over longer distances where accumulated error from wheel encoders or motor control alone would become significant.

**(viii) Audible Feedback** 
MH-FMD Active Buzzer

The MH-FMD Active Buzzer is used in our self-driving car to provide audible signals for status indication and debugging purposes. Unlike passive buzzers, the active buzzer contains an internal oscillator, allowing it to generate sound simply by supplying power. In our design, it is triggered by the controller to produce beeps that signal events such as successful start-up, obstacle detection, or completion of a parking maneuver. This feature assists in both competition runs and testing phases, giving operators a quick, non-visual method of understanding the robot’s current status.


## 2.3 Build of Materials
## Wiring Diagram
**(i) Open Challenge**
**(ii) Obstacle Challenge**
# 3.0 Obstacle Management
## 3.1 Open Challenge
## 3.2 Obstacle Challenge

# 4.0 Engineering Factors
# 5.0 Improvements and Enhancements
# ** Credits** 

