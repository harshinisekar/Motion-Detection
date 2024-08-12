# Motion-Detection
 This Python project uses OpenCV to capture live video from a webcam and detect motion in real-time. It records the start and end times of detected motion and saves them in a CSV file. The project is ideal for basic security systems or monitoring activities, providing a simple yet effective motion detection solution.

# Motion Detection with OpenCV

## Overview
This project is a Python application that uses OpenCV to capture live video from a webcam and detect motion. The program records the start and end times of detected motion and saves them in a CSV file. The application also displays several frames to visualize the motion detection process.

## Features
- Captures live video from a webcam.
- Detects motion by comparing current frames with a static background.
- Records the start and end times of motion in a Pandas DataFrame.
- Saves the recorded motion times to a CSV file.
- Displays the captured frames in real-time, including grayscale, difference, threshold, and color frames.

## Prerequisites
- Python 3.x
- OpenCV library (`cv2`)
- Pandas library (`pandas`)

## Installation
1. Clone the repository or download the script.
2. Install the required libraries:
    ```sh
    pip install opencv-python pandas
    ```

## Usage
1. Run the script:
    ```sh
    python motion_detection.py
    ```
2. The application will start capturing video from your webcam and display various frames on the screen:
   - **Gray Frame**: Displays the grayscale version of the current frame.
   - **Difference Frame**: Shows the difference between the current frame and the static background.
   - **Threshold Frame**: Highlights the areas where motion is detected.
   - **Color Frame**: Draws a green rectangle around the detected moving object.

3. Press the `m` key to stop the motion detection and save the recorded times to a CSV file named `MovementsTimeFile.csv`.

## How It Works
- **Static Background**: The application initializes a static background frame from the first few frames captured.
- **Motion Detection**: Each new frame is compared with the static background to identify any changes. If a change is detected, the motion is recorded.
- **Time Recording**: The start and end times of the detected motion are stored in a list and later saved in a Pandas DataFrame.
- **CSV File**: The recorded motion times are saved in a CSV file for later analysis.

## Output
![output 1](https://github.com/user-attachments/assets/6be285ad-7c36-4809-a232-395cc1b2e793)
![output 2](https://github.com/user-attachments/assets/de62c825-a05d-4c4b-98f5-1b6c12355af5)
![output 3](https://github.com/user-attachments/assets/e805939c-4bbc-4bc4-bd0d-46c47f634953)
![output 4](https://github.com/user-attachments/assets/78fccc95-f0f9-482f-92c2-4925f7bad16d)

## Notes
- Ensure your webcam is properly connected to your system.
- The application uses a threshold value to detect motion. You can adjust this value to fine-tune the motion detection sensitivity.
- The system stops capturing video and recording motion when the `m` key is pressed.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
