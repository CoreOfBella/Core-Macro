# Fishing Macro Script - README

## Summary
This script is a fishing macro designed to assist users in a fishing minigame by dynamically tracking the fish and progress bar on-screen. Developed with OpenCV and PyAutoGUI, it uses advanced image recognition and adaptive mouse control to stabilize and keep the fish within the bounds of the progress bar efficiently.

## License and Copyright
This script was entirely developed by ChatGPT, an AI created by OpenAI, and is free to use, modify, and distribute as long as:
1. The derivative works or modifications are also provided free of charge.
2. Proper credit is given to ChatGPT/OpenAI in any distributed works derived from this script.

**Copyright Notice:**
- The original script and its derivatives are released under a Creative Commons Zero (CC0) license, effectively placing it in the public domain.
- You are free to copy, modify, and use this script for personal or public projects under the condition that any use remains non-commercial and free.

## How This Script Was Created
This script was written entirely with the assistance of ChatGPT in collaboration with a user, providing feedback and adjustments along the way. The creation process involved:
- Detailed conversations and clarifications about user needs and functionality.
- Iterative development, including real-time adjustments based on testing feedback.
- Integration of image recognition and mouse automation using Python libraries OpenCV and PyAutoGUI.

### Features Implemented
- Fish detection via template matching.
- Dynamic dead zone calculation based on progress bar width.
- Adaptive clicking and holding behavior based on fish position.
- Real-time debugging visualization for both fish and progress bar detection.

## Usage Instructions
### Prerequisites
1. **Install Required Libraries:**
   ```bash
   pip install opencv-python pyautogui
   ```
2. **Templates:** Place `fish_template.png` and `new_fish_template.png` in the same directory as the script.
3. **Adjust Region:** Modify the `screen_region` variable in the script to match your game window’s position.

### Running the Script
1. Open your game and ensure the fishing interface is visible on-screen.
2. Run the script in a terminal:
   ```bash
   python progress_bar_detection.py
   ```
3. Press `ESC` at any time to exit the script.

### Windows and macOS Compatibility
- The script works on both Windows and macOS systems as long as Python is installed and the required libraries are set up.
- For macOS users, ensure the script has screen recording permissions (System Preferences > Security & Privacy > Screen Recording).

## Disclaimer
This script is designed as a learning tool and gaming aid. Use responsibly and respect the terms of service of any games where you apply this tool.

