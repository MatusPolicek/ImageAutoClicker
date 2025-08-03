# AutoClicker - Smart Image Detection

A powerful Windows application that automatically detects images on your screen and performs customizable actions. Simply capture screenshots of UI elements you want to interact with, and the app will find and click them automatically with intelligent timing and mouse movement.

## Key Features

### 🎯 **Multi-Image Detection**
- Add unlimited target images with individual settings for each
- Advanced OpenCV template matching with multi-scale detection (0.8x to 1.2x)
- Individual confidence thresholds and ROI (Region of Interest) areas per image
- Enable/disable images independently for flexible automation

### ⚡ **Advanced Action System**
- **Multiple Action Types**: Left click, right click, double click, key presses
- **Custom Sequences**: Chain multiple actions per detected image
- **Intelligent Timing**: Separate pre-delay and post-delay for each action
- **Key Press Support**: Single keys, combinations, or repeated presses

### 🎛️ **Professional Interface**
- Clean, intuitive tree view showing all images and their status
- Comprehensive tabbed dialog for image and action management
- Real-time status feedback and execution information
- Always-on-top option to keep controls accessible

### 🎯 **Smart ROI System**
- **Global ROI**: Set master search area for all images
- **Individual ROI**: Per-image search regions for precise targeting
- **Interactive Selection**: Click and drag to define search areas visually
- **ROI Preview**: Visual overlay showing all active regions

### 🖱️ **Intelligent Mouse Movement**
- ROI-aware random mouse movement that avoids all detection areas
- Configurable buffer zones around restricted regions
- Smart fallback to screen corners when needed
- Prevents pattern detection by automation-aware applications

### ⚙️ **Advanced Features**
- **Configuration Management**: Save and load complete setups for different applications
- **Multi-threading**: Responsive interface that never freezes during operation
- **Performance Optimized**: Screenshot caching and smart timing prevent system overload
- **Safety Features**: Built-in failsafes and duplication prevention
- **Hotkey Control**: F9 to start/stop from anywhere, even when app is minimized

## Quick Start Guide

### 1. **Setup Your Images**
1. Run `AutoClicker.exe`
2. Click **"➕ Add Images"** and select screenshots of UI elements you want to automate
3. Each image appears in the main list with a status indicator

### 2. **Configure Actions**
1. Select an image and click **"✏️ Edit Selected"**
2. In the **Image Settings** tab:
   - Adjust confidence threshold (0.8 is usually perfect)
   - Set individual ROI if you want to limit search area
3. In the **Actions** tab:
   - Add multiple actions (clicks, key presses)
   - Set timing delays before and after each action
   - Reorder actions with up/down buttons

### 3. **Fine-tune Detection**
- Use **"📍 Select ROI"** to limit search areas for faster detection
- Use **"👁️ Preview ROI"** to visualize all active search regions
- Test individual images with **"🧪 Test Selected"** before running

### 4. **Run Automation**
- Click **"▶️ Start (F9)"** or press **F9** to begin
- The app scans your screen and executes actions when images are found
- Press **F9** again to stop at any time

### 5. **Save Your Setup**
- Use **File → Save Configuration** to store your complete setup
- Load saved configurations with **File → Load Configuration**

## How It Works

AutoClicker uses advanced computer vision to find and interact with specific images on your screen, making it perfect for automating repetitive tasks in games, applications, or workflows.

### 🔍 **Detection Engine**
The application continuously scans your screen using OpenCV's template matching technology:

1. **Screenshot Capture**: Takes periodic screenshots of your screen
2. **Multi-Scale Matching**: Searches for your target images at different scales (80% to 120%)
3. **Confidence Analysis**: Only triggers actions when matches exceed your confidence threshold
4. **ROI Processing**: Limits searches to specific screen regions for speed and accuracy

### ⚡ **Action Execution**
When a target image is found, the system executes your configured actions:

1. **Pre-Action Delay**: Waits for UI to stabilize (if configured)
2. **Action Sequence**: Performs clicks, key presses, or combinations in order
3. **Smart Mouse Movement**: Moves cursor away from detection areas to avoid interference
4. **Post-Action Delay**: Prevents immediate re-detection of the same element
5. **Scan Pause**: Uses intelligent timing to prevent system overload

### 🧠 **Intelligence Features**
- **Duplication Prevention**: Smart timing prevents accidental double-actions
- **ROI Awareness**: Mouse movement avoids all active search regions
- **Adaptive Timing**: Uses your delay settings to optimize scan frequency
- **Multi-threading**: Keeps the interface responsive during operation
- **Memory Optimization**: Caches screenshots efficiently to reduce CPU usage
## Common Use Cases

### 🎮 **Gaming Automation**
- Auto-collect resources, rewards, or daily bonuses
- Automate repetitive crafting or farming sequences
- Handle idle game progression while AFK
- Navigate through menus and dialogs automatically

### 💼 **Productivity & Work**
- Automate form filling and data entry tasks
- Handle repetitive software workflows
- Auto-click through installation wizards
- Manage multiple application windows efficiently

### 🔄 **System Maintenance**
- Automate software updates and patches
- Handle routine system dialogs and confirmations
- Manage background application processes
- Schedule and execute maintenance routines

## Advanced Configuration Tips

### 🎯 **Optimizing Detection Accuracy**
- **High Confidence (0.9-1.0)**: Use for unique, detailed images with consistent appearance
- **Medium Confidence (0.7-0.8)**: Best for most UI elements and buttons
- **Low Confidence (0.5-0.6)**: Use for images that might change slightly (colors, text)

### ⏱️ **Timing Best Practices**
- **Pre-Delay**: Allow time for UI animations or loading (0.1-0.5s typical)
- **Post-Delay**: Prevent re-detection of same element (0.2-1.0s typical)
- **Action Sequences**: Use shorter delays between related actions (0.1-0.2s)

### 📍 **ROI Strategy**
- **Individual ROI**: Use for elements that appear in specific screen areas
- **Global ROI**: Set to exclude taskbars, sidebars, or other static UI elements
- **Multiple ROIs**: Combine global and individual ROIs for maximum precision

## System Requirements & Installation

### 💻 **System Requirements**
- **Operating System**: Windows 10 or Windows 11
- **Memory**: 4GB RAM minimum (8GB recommended)
- **Storage**: 50MB free disk space
- **Display**: Any resolution supported

### 📥 **Installation**
1. Download `AutoClicker.exe` 
2. Run the executable - no installation required!
3. The application is portable and can be run from any folder
4. Windows may show a security warning for unsigned executables - click "Run anyway"

### 🔒 **Security Note**
This application requires screen capture and input simulation permissions to function. Some antivirus software may flag automation tools as potentially unwanted programs (PUP). The application is safe to use and does not collect or transmit any data.

## Pro Tips for Best Results

### 📸 **Creating Target Images**
1. **Use Screenshots**: Capture images directly from your target application using Print Screen
2. **Crop to Essential Elements**: Include only the button/element you want to click, not surrounding areas
3. **Avoid Text-Heavy Images**: UI buttons with icons work better than pure text
4. **Consistent Conditions**: Capture images under the same lighting/theme settings you'll use

### 🎯 **Optimizing Performance**
1. **Start with Default Settings**: Use 0.8 confidence and test before adjusting
2. **Use ROI Regions**: Limit search areas to dramatically improve speed and reduce false positives
3. **Test Thoroughly**: Always use "Test Selected" to verify detection before running automation
4. **Monitor Resource Usage**: Close unnecessary applications to ensure smooth operation

### 🔧 **Troubleshooting Detection Issues**
1. **Lower Confidence**: Try 0.6-0.7 if images aren't being detected
2. **Check Image Quality**: Ensure target images are clear and not blurry
3. **Verify Visibility**: Make sure target elements are not covered by other windows
4. **Update Screenshots**: Re-capture images if the application UI has changed

### ⚡ **Advanced Automation Techniques**
1. **Action Chains**: Use multiple actions per image for complex interactions
2. **Strategic Delays**: Set pre-delays for loading screens, post-delays to prevent spam
3. **Selective Enabling**: Enable only the images you need for specific tasks
4. **Configuration Profiles**: Save different setups for different applications or scenarios

## Troubleshooting Guide

### ❌ **Images Not Being Detected**
**Problem**: The app doesn't find your target images on screen
**Solutions**:
- Lower the confidence threshold (try 0.6-0.7) in the image edit dialog
- Ensure target images are visible and not covered by other windows
- Re-capture images if the application UI has changed since original screenshot
- Check that image files aren't corrupted or too small
- Use "Test Selected" to verify detection before running

### ⚡ **Actions Not Executing Properly**
**Problem**: Images are detected but actions don't work as expected
**Solutions**:
- Increase pre-delay if UI elements need time to appear or load
- Adjust post-delay to prevent rapid re-detection of the same image
- Verify the correct action order in the Actions tab of the edit dialog
- Check that key press syntax is correct for keyboard actions
- Ensure the target application window is active and focused

### 🐌 **Poor Performance or High CPU Usage**
**Problem**: The application runs slowly or uses too much system resources
**Solutions**:
- Set ROI regions to limit search areas and improve detection speed
- Remove unused or disabled images from your list
- Increase post-delays to reduce scanning frequency
- Close unnecessary applications that may interfere with screen capture
- Lower the confidence threshold slightly to reduce processing overhead

### 🖱️ **Mouse Movement Issues**
**Problem**: Random mouse movement not working as expected
**Solutions**:
- Ensure ROI regions are properly configured and don't conflict
- Check that random mouse movement is enabled in settings
- Verify that ROI regions don't accidentally cover the entire screen
- Make sure there are accessible areas for mouse movement outside ROIs

### 💾 **Configuration Problems**
**Problem**: Settings don't save or load properly
**Solutions**:
- Check that you have write permissions in the application folder
- Use "Save Configuration" and "Load Configuration" to preserve working setups
- Restart the application if settings changes don't apply correctly
- Ensure configuration files aren't being blocked by antivirus software

### 🔒 **Security Software Interference**
**Problem**: Antivirus blocks the application or it stops working unexpectedly
**Solutions**:
- Add `AutoClicker.exe` to your antivirus whitelist/exceptions
- Temporarily disable real-time protection during setup and testing
- Run the application as administrator if permission issues occur
- Check Windows Defender exclusions if using Windows built-in security

## Safety & Legal Information

### ⚠️ **Safety Features**
- **Emergency Stop**: Press F9 at any time to immediately stop all automation
- **Failsafe Protection**: Move mouse to screen corners to trigger PyAutoGUI failsafe
- **Thread Safety**: Interface remains responsive and can be controlled during operation
- **Smart Prevention**: Built-in systems prevent accidental double-actions or loops
- **Resource Management**: Optimized to prevent system overload or freezing

### 📋 **Supported Image Formats**
- PNG (recommended for UI elements)
- JPG/JPEG (good for photos and complex images)
- BMP (uncompressed, large file size)
- TIFF (high quality, good for detailed images)
- GIF (basic support, static images only)

### ⚖️ **Legal Disclaimer**
This software is designed for legitimate automation and productivity purposes. Users are responsible for ensuring their use complies with:
- Terms of service of applications being automated
- Local laws and regulations regarding automation software
- Workplace policies if used in professional environments
- Gaming rules and anti-cheat policies if used with games

**The developers are not responsible for any misuse of this software or violations of third-party terms of service.**

### 🔒 **Privacy & Data**
- **No Data Collection**: This application does not collect, store, or transmit any personal data
- **Local Processing**: All image detection and processing happens on your computer
- **No Internet Required**: The application works completely offline
- **No Telemetry**: No usage statistics or analytics are collected or sent

---

**AutoClicker** - Making repetitive tasks automated and effortless. 
For support or questions, please refer to this documentation or the project repository.
