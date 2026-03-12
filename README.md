# Xavier - Android Accessibility App for Locked-In Syndrome

**Xavier** is an Android accessibility service that enables **hands-free smartphone control** using **eye-tracking** and **EEG brain signals** for users with Locked-In Syndrome.

## Key Features
- **Gaze-controlled cursor**: Tracks eye movements via front camera (Eyedid SDK)
- **Blink gestures**: Left/right blink for click/menu toggle
- **Edge swipes**: Fixation on screen borders triggers navigation swipes
- **EEG concentration detection**: Auto camera on/off via MindRove Arc 1 headset
- **Custom overlays**: Navigation menu, custom keyboard with layered letters

**Navigation Menu** (blink-activated): Back | Home | Recent Apps  
**Custom Keyboard**: 3-group letter layers → 9 individual letters + Shift/Space/Back/Emoji

## Setup Process
1. **Accessibility**: Enable service in Android Settings → Installed Services
2. **Camera calibration**: Set camera coordinates (x,y mm from screen top-left)
3. **Eye calibration**: Focus on 5 red points (4 corners + center)
4. **EEG training**: Random Forest model detects eyes open/closed state

**EEG Processing**: 6-channel → Butterworth filter → Random Forest → Binary (eyes open/closed)

## Power Consumption
Primary drain: **Camera** (eye-tracking)  
Mitigation: EEG auto-toggle when eyes closed  
CPU usage: Low (efficient processing)

## Requirements
- Android API 23+ (target 33)
- Front camera permission
- Internet (SDK license)
- MindRove Arc 1 EEG headset (optional)

**Target users**: Locked-In Syndrome patients requiring total hands-free control.
