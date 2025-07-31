# Image-Based AutoClicker

A sophisticated image-based autoclicker application that can detect multiple images on your screen and automatically click on them with advanced features.

## Features

- **Multi-Image Detection**: Add and manage multiple target images simultaneously
- **Advanced Image Matching**: Uses OpenCV template matching with multi-scale detection
- **Modern GUI Interface**: Clean, color-coded tkinter interface with intuitive controls
- **ROI (Region of Interest)**: Limit search area for faster detection and better accuracy
- **Smart Mouse Movement**: Moves mouse to different screen quadrants after clicking to avoid detection
- **Configurable Settings**: 
  - Adjustable confidence threshold for image matching
  - Customizable click delay between detections
  - Maximum click limit option
  - Mouse movement distance control
- **Hotkey Support**: F9 hotkey to start/stop clicking
- **Real-time Feedback**: Shows detection status, click count, and confidence scores
- **Performance Optimized**: Screenshot caching and early exit for faster detection

## How to Use

1. **Add Target Images**: 
   - Click "➕ Add Images" to select one or multiple image files
   - Hold Ctrl/Cmd to select multiple images at once
   - Manage your images with Remove and Clear All options

2. **Configure Settings**:
   - **Confidence Threshold**: Higher values (0.8-1.0) = more precise matching, lower values (0.3-0.7) = more flexible matching
   - **Click Delay**: Time in seconds between each detection attempt
   - **Max Clicks**: Maximum number of clicks (0 = unlimited)
   - **Mouse Movement**: Enable/disable random mouse movement after clicking
   - **ROI Coordinates**: Set specific screen area to search (format: x1,y1,x2,y2)

3. **Set ROI (Optional)**: 
   - Use "📍 Set ROI" button to interactively select a screen region
   - Or manually enter coordinates in x1,y1,x2,y2 format
   - Leave empty to search entire screen

4. **Test Detection**: Use the "🔍 Test Detection" button to verify images can be found on screen

5. **Start Clicking**: 
   - Click "▶️ Start Clicking" or press F9 to begin
   - Press F9 again or click "⏹️ Stop Clicking" to stop

## How It Works

1. **Multi-Scale Template Matching**: Uses OpenCV's advanced template matching with multiple scale factors (0.8x to 1.2x) for robust detection
2. **Screenshot Caching**: Implements intelligent screenshot caching to reduce CPU usage and improve performance
3. **ROI Processing**: When ROI is set, only processes the specified screen region for faster detection
4. **Confidence Scoring**: Only clicks when the match confidence exceeds your threshold
5. **Precise Clicking**: Clicks at the center of the detected image with pixel-perfect accuracy
6. **Smart Mouse Movement**: After clicking, moves mouse to opposite screen quadrant to avoid pattern detection

## Safety Features

- **Thread Safety**: GUI remains responsive during operation with multi-threaded architecture
- **Error Handling**: Graceful handling of image loading, detection errors, and system exceptions
- **Performance Monitoring**: Real-time feedback on detection confidence and system status

## Supported Image Formats

- PNG
- JPG/JPEG
- BMP
- TIFF
- GIF

## Tips for Best Results

1. **Use High-Quality Images**: Screenshots work best as target images
2. **Avoid Generic Images**: Choose unique, distinctive images for better detection accuracy
3. **Optimize Confidence**: Start with 0.8 and adjust based on detection results
4. **Test Before Running**: Always use "Test Detection" to verify image recognition
5. **Set ROI for Speed**: Define specific screen regions to dramatically improve detection speed
6. **Multiple Scales**: The app automatically handles different image sizes, but original scale works best
7. **Stable Lighting**: Consistent screen brightness and color settings improve detection reliability
8. **Unique Targets**: Use images with distinctive colors, shapes, or text for better recognition

## System Requirements

- Windows 10/11 (Primary support)
- Python 3.8+
- Required Python packages:
  - OpenCV (cv2)
  - PyAutoGUI
  - NumPy
  - Pillow (PIL)
  - pynput
  - tkinter (included with Python)

## Installation

1. Clone or download the repository
2. Install required packages: `pip install opencv-python pyautogui numpy pillow pynput`
3. Run: `python main.py`

## Troubleshooting

**Images not detected**:
- Lower the confidence threshold (try 0.6-0.7)
- Ensure target images are visible and not obscured
- Check if images have changed size or appearance
- Try setting a smaller ROI around the target area

**Poor performance**:
- Set ROI to limit search area
- Remove unused images from the list
- Increase click delay to reduce CPU usage
- Close unnecessary applications

**Clicking in wrong location**:
- Increase confidence threshold for better accuracy
- Use more distinctive/unique target images
- Verify image quality and clarity
- Test detection before running

## Disclaimer

This tool is for automation and productivity purposes. Please use responsibly and in accordance with the terms of service of any applications you interact with. The developers are not responsible for any misuse of this software.
