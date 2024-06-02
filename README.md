# Robot Control with SLAM and Speech Recognition

![Robot](https://your_image_url_here.jpg)

## Overview

This project combines Simultaneous Localization and Mapping (SLAM) with speech recognition to control a robot's movements. SLAM is used to map the environment and localize the robot within it, while speech recognition allows users to give commands to the robot verbally.

The system integrates the following components:

- **SLAM (Simultaneous Localization and Mapping)**: Implemented using an Extended Kalman Filter (EKF), the SLAM algorithm allows the robot to build a map of its environment and estimate its own position within that map using sensor data.

- **Camera Detection**: Utilizing a camera mounted on the robot, ArUco marker detection is employed to identify landmarks in the environment, aiding in localization and mapping.

- **Speech Recognition**: An activation phrase triggers the system to listen for commands. Upon recognition of a command, the robot executes the corresponding action, such as moving forward, backward, turning left, or turning right.

- **Arduino Control**: Commands generated from speech recognition are translated into motor control signals and sent to an Arduino board, which controls the robot's actuators to perform the desired actions.

## Features

- **SLAM Mapping**: Real-time mapping of the robot's environment using EKF-SLAM.
- **ArUco Marker Detection**: Detection and localization of ArUco markers for precise mapping and localization.
- **Speech-Activated Control**: Activation phrase triggers the system to listen for commands, allowing users to control the robot via voice commands.
- **Dynamic Movement**: The robot dynamically adjusts its movement based on the detected landmarks and current map.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your_username/robot-control.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Connect the Arduino board and configure the serial port settings in the `main.py` file.

4. Run the `main.py` script:

   ```bash
   python main.py
   ```

## Usage

1. Ensure that the robot's camera has a clear view of the environment and that ArUco markers are placed within the robot's operating area.

2. Speak the activation phrase to activate the system.

3. Issue voice commands such as "move forward", "move backward", "turn left", or "turn right" to control the robot's movements.

4. Monitor the SLAM mapping progress and the robot's position on the graphical user interface.

## Contributing

Contributions are welcome! If you have any suggestions, feature requests, or bug reports, please open an issue or submit a pull request.

## Acknowledgements

- [EkfSLAM](https://github.com/your_username/ekf-slam): Library for EKF-SLAM implementation.
- [Vosk](https://github.com/your_username/vosk): Library for speech recognition.
- [OpenCV](https://github.com/opencv/opencv): Library for computer vision tasks.
