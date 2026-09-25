# Video Editor Web App

A modern, browser-based video editor with chroma key (green screen) capabilities, trimming, and export functionality. Built with HTML5, CSS3, and vanilla JavaScript.

## 🌟 Features

### **Core Editing**
- **Video Upload**: Drag & drop or click to upload MP4, WebM, MOV, AVI files (up to 2GB)
- **Playback Controls**: Play, pause, rewind, forward, mute with keyboard shortcuts
- **Trimming**: Set precise in/out points with visual timeline markers
- **Timeline Visualization**: Interactive timeline with playhead and trim range display

### **Chroma Key (Green Screen)**
- **Background Replacement**: Replace green screen backgrounds with custom images
- **Real-time Preview**: Toggle chroma key preview while editing
- **Color Detection**: Auto-detect green screen color or manual color picker
- **Adjustable Settings**: Fine-tune sensitivity and smoothness for clean edges

### **Export Options**
- **Multiple Formats**: MP4, WebM, MOV, Animated GIF
- **Quality Settings**: Low, Medium, High presets
- **Resolution Options**: Original, 1080p, 720p, 480p
- **Chroma Key Export**: Apply green screen effect during export

### **User Interface**
- **Responsive Design**: Works on desktop and mobile devices
- **Dark Theme**: Modern dark/light interface with gradient accents
- **Visual Feedback**: Progress indicators, status updates, and animations
- **Help System**: Comprehensive keyboard shortcuts and usage guide

## 🚀 Quick Start

1. **Upload a video**:
   - Click the "Upload Video" button
   - Or drag & drop a video file onto the placeholder area
   - Supported formats: MP4, WebM, MOV, AVI (≤2GB)

2. **Edit your video**:
   - Use playback controls to navigate
   - Set trim points using "Set In"/"Set Out" or keyboard shortcuts
   - Apply chroma key effects in the dedicated panel

3. **Export**:
   - Configure format, quality, and resolution
   - Click "Export" to process and download
   - Check "Apply Chroma Key" to include green screen effects

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| **Space** | Play/Pause |
| **← / →** | Seek 1 second |
| **Shift + ← / →** | Seek 10 seconds |
| **Ctrl + ← / →** | Seek 1 minute |
| **M** | Mute/Unmute |
| **I** | Set In Point |
| **O** | Set Out Point |
| **C** | Toggle Crop Tool |
| **Ctrl + E** | Export Video |
| **F** | Toggle Fullscreen |

## 🛠️ Technical Details

### **Architecture**
- Pure client-side implementation (no server required)
- Uses HTML5 Canvas for video processing
- Web Audio API for audio handling
- MediaRecorder API for video export
- Blob URLs for efficient file handling

### **Browser Support**
- Chrome 60+ (recommended)
- Firefox 65+
- Edge 79+
- Safari 14.1+
- **Note**: Some advanced features require modern browser APIs

### **Performance Features**
- Progressive rendering for smooth playback
- Memory-efficient blob management
- Canvas optimization for chroma key processing
- Graceful fallbacks for unsupported features

## 📁 Project Structure

```
index.html
├── HTML Structure
│   ├── Header with project controls
│   ├── Video preview section
│   ├── Editing controls panel
│   ├── Timeline visualization
│   └── Status bar
├── CSS Styling
│   ├── CSS variables for theming
│   ├── Responsive breakpoints
│   ├── Animation keyframes
│   └── Component-specific styles
└── JavaScript
    ├── File handling and upload
    ├── Video playback controls
    ├── Chroma key implementation
    ├── Export pipeline
    └── UI state management
```

## 🔧 Advanced Features

### **Chroma Key Algorithm**
- Color difference calculation with Euclidean distance
- Adjustable sensitivity and smoothness parameters
- Real-time preview with canvas compositing
- Background image overlay support

### **Export Pipeline**
- Frame-by-frame canvas capture
- Audio/video stream combination
- Quality-based bitrate adjustment
- Fallback mechanisms for browser limitations

### **State Management**
- Project state persistence
- Memory cleanup on project reset
- Error handling and user notifications
- Keyboard shortcut integration

## ⚠️ Limitations & Considerations

### **Browser Dependencies**
- MediaRecorder API required for video export
- Web Audio API needed for audio processing
- File System Access API for advanced features
- Some mobile browsers have restricted autoplay

### **Performance**
- Large videos (>1GB) may cause memory issues
- Complex chroma key effects impact performance
- Export time depends on video length and quality
- Canvas processing is CPU-intensive

### **File Handling**
- Maximum file size: 2GB
- Export formats depend on browser support
- No cloud storage - all processing is local
- Download required for final output

## 🆘 Troubleshooting

### **Common Issues**
1. **Video won't play**: Check browser autoplay permissions
2. **Export fails**: Try different format or lower quality
3. **Chroma key looks rough**: Adjust sensitivity and smoothness
4. **Audio missing in export**: Browser may not support audio capture

### **Solutions**
- Use Chrome for best compatibility
- Convert videos to MP4 before uploading
- Reduce video resolution for faster processing
- Check browser console for error details

## 🔮 Future Enhancements

Planned features for future versions:
- Video filters and color correction
- Text and title overlays
- Multiple video track support
- Audio waveform visualization
- Project saving/loading
- Social media export presets
- Cloud storage integration
- Advanced transitions and effects

## 📄 License

This program is available under the Apache 2.0 license.

## 🙏 Acknowledgments

- Font Awesome for icons
- Modern CSS features for styling
- HTML5 Media APIs for core functionality
- Browser vendors for advancing web standards

---

**Note**: This is a client-side application. All processing happens in your browser - no data is sent to external servers. Videos are processed locally and downloaded directly to your device.
## Maia Reel visual theme

The interface uses the shared Maia Reel dark theme in `www/maia-reel.css`,
loaded after the app's layout styles. It is a local static asset: no CDN, build
step or new server is needed. Media processing and user-selected video title
styles remain under the original application code's control.

The canonical stylesheet and deployment instructions are maintained in the
sibling `maia-edge-apps-deployment` repository, in `themes/maia-reel.css` and
`docs/MEDIA-THEME.md`. The PWA cache has a new version and is scoped to this app.
