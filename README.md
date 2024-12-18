# Fishing Macro - README

## Overview
This fishing macro script is designed to assist in a fishing minigame by dynamically tracking the position of the fish and the progress bar on the screen. It uses OpenCV for image recognition and PyAutoGUI for mouse control to keep the fish within the progress bar's bounds efficiently and precisely.

## Features

### Dynamic Fish Tracking
- Tracks the fish using two different fish templates (`fish_template.png` and `new_fish_template.png`).
- Dynamically adjusts click and hold behavior based on the fish's position relative to the progress bar.

### Proportional Clicking
- Click speed and duration are dynamically adjusted depending on the distance of the fish from the center of the progress bar.
  - **Closer to Center**: Faster, shorter clicks to stabilize the progress bar.
  - **Farther from Center**: Slower, longer clicks to bring the fish back towards the center.

### Progress Bar Detection
- Detects the progress bar using color thresholds (white, green, and red).
- Dynamically calculates the dead zone based on the width of the progress bar:
  - **Smaller Bars**: Smaller dead zones for finer control.
  - **Larger Bars**: Larger dead zones for smoother adjustments.

### Adaptive Behavior
- Automatically adjusts behavior based on fish movement:
  - Subtle or slow fish movements result in quicker, smaller adjustments.
  - Rapid fish movements trigger longer holds to counteract drastic shifts.

### Visual Debugging
- Displays a visualization of the detected fish and progress bar for debugging purposes:
  - Green rectangles highlight the detected fish.
  - White rectangles outline the detected progress bar.

### Efficient Performance
- Implements optimized logic to reduce unnecessary clicks and hold actions.
- Includes brief sleep intervals to minimize CPU usage.

## Updates

### Latest Updates
1. **Dynamic Click Proportionality**:
   - Clicks are now directly proportional to the fish’s position within the progress bar.
   - Ensures precise adjustments to keep the fish inside the bar at all times.

2. **Dead Zone Calculation**:
   - Dead zones are dynamically adjusted based on the width of the progress bar, ensuring optimal control regardless of bar size.

3. **Improved Mouse Control**:
   - Clicks are now efficient and hold actions are only triggered when necessary.
   - Adjustments prevent the progress bar from moving unnecessarily.

4. **Enhanced Visualization**:
   - Real-time display of fish and progress bar positions for easier debugging.

5. **Efficient Template Matching**:
   - Supports multiple fish templates for better detection accuracy.
   - Threshold-based logic ensures reliable fish tracking.

## How to Use

1. **Prerequisites**:
   - Install required libraries:
     ```bash
     pip install opencv-python pyautogui
     ```
   - Place `fish_template.png` and `new_fish_template.png` in the same directory as the script.

2. **Run the Script**:
   - Ensure the game window is open and visible on your screen.
   - Adjust the `screen_region` variable in the script to match the coordinates of your game window.
   - Execute the script:
     ```bash
     python progress_bar_detection.py
     ```

3. **Key Controls**:
   - Press `ESC` to exit the script at any time.

## Known Limitations
- **Template Sensitivity**: Ensure the fish templates are accurate representations of the in-game fish.
- **Screen Resolution**: The script’s performance may vary across different screen resolutions. Adjust `screen_region` as needed.

## Troubleshooting
- **Fish Not Detected**:
  - Verify that `fish_template.png` and `new_fish_template.png` are in the correct location.
  - Ensure the templates match the in-game fish appearance.

- **Progress Bar Not Detected**:
  - Check that the color thresholds in the script match the in-game progress bar colors.

- **Click Behavior Seems Off**:
  - Adjust `click_speed` or proportionality constants to fine-tune the response.

## Future Improvements
- Add more robust template matching to handle variations in fish appearance.
- Implement adaptive learning to improve control precision over time.
- Enhance multi-monitor support for better usability.

## Credits
Developed using:
- OpenCV for image processing.
- PyAutoGUI for mouse control.

### Feedback
If you encounter any issues or have suggestions for improvement, feel free to contribute or report them!

