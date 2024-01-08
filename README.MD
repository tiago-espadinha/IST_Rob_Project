# Scorbot Robot Project

## Team Members

- Diogo Rosa, ist93044
- Tomás Bastos, ist93194
- Tiago Simões, ist96329

## Project Description

This project provides a Python program that interfaces with two Scorbot robots, enabling control through a PS4 controller.
The program is designed to facilitate robot movements and actions using the controller in order to perform an operation,
with a robot holding a camera and the other a surgical scalpel.

## Requirements

- numpy
- opencv-python
- pygame
- pyserial
- time (standard library)

## Installation

1. Install dependencies as specified above:
   ```bash
   pip install numpy opencv-python pygame pyserial
   ```
2. Ensure camera and robots are physically connected to the computer
3. Verify serial port assignments in Config.py match your system

## Usage

### Configuration

Edit `Config.py` to set:

- `scalp_port`: Serial port for scalpel-holding robot
- `cam_port`: Serial port for camera-holding robot
- `cam_usb`: USB port for connected camera

### Running the Program

1. Connect PS4 controller and camera to computer
2. Connect both robots to their respective serial ports (per Config.py)
3. Connect camera to assigned USB port
4. Execute the main script:
   ```bash
   python scorbot_run.py
   ```

### Controls

- Analog sticks: Move selected robot (X/Y/Z or joint axes)
- Buttons: Predefined actions (see help screen)
- Circle: Move to default position (recommended start)
- Options: Display help screen with button mapping
- Mode switching: Toggle between XYZ and joint control modes

## Outputs

- Real-time video feed from camera displayed in OpenCV window
- Graphical overlay showing current mode, robot selection, and speed
- Help screen visualization (via pygame)
- Serial commands sent to robots for movement control
- No file-based outputs generated during normal operation

## Notes

- For smooth initial operation, position both robots at default pose using Circle button
- Debug mode available in Config.py for additional console feedback
- Button mappings defined in CtrlMap.py can be customized if needed
- Robot movement limits configured in Config.py for safety
- Help screen images stored in Images/ directory for reference
