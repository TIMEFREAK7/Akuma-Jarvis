# Vortex AI OS - Mobile Edition

A completely free, on-device AI assistant for OnePlus 11 phones powered by Google's Gemma-3n-E4B-it model.

## Features

✅ **Completely Free** - No API costs, no subscriptions  
✅ **On-Device AI** - All processing happens locally on your phone  
✅ **Offline Capable** - Works without internet after initial setup  
✅ **Private** - Your data never leaves your device  
✅ **Fast** - Optimized for mobile hardware  
✅ **Easy to Use** - Simple, intuitive interface  

## System Requirements

- **Device**: OnePlus 11 (or compatible Android device with 8GB+ RAM)
- **OS**: Android 7.0 (API 24) or higher
- **RAM**: 8GB minimum (12GB+ recommended)
- **Storage**: 20GB free space (for model download and caching)
- **Internet**: Required for initial setup and model download only

## Installation

### Step 1: Download the App

1. Download the APK file from the releases page
2. Transfer it to your OnePlus 11 or download directly on the device

### Step 2: Enable Installation from Unknown Sources

1. Go to **Settings** → **Security**
2. Enable **Unknown Sources** or **Install Unknown Apps**
3. Select your file manager or browser as the app to allow installations

### Step 3: Install the App

1. Open the APK file
2. Tap **Install**
3. Wait for installation to complete
4. Tap **Open** to launch the app

### Step 4: Initial Setup

1. Launch **Vortex AI OS**
2. Follow the setup wizard
3. Download the Gemma-3n-E4B-it model (~4GB)
4. Wait for model initialization
5. Start chatting!

## Usage

### Creating a Project

1. Go to the **Projects** tab
2. Tap the **+** button
3. Enter a project name and optional description
4. Tap **Create**

### Starting a Conversation

1. Go to the **Chat** tab
2. Select a project (or create one)
3. Type your message in the input box
4. Tap the send button

### Viewing Model Information

1. Go to the **Models** tab
2. View model status, specifications, and capabilities

### Adjusting Settings

1. Go to the **Settings** tab
2. Toggle options as desired
3. Settings are saved automatically

## Performance Tips

- **Close other apps** to free up memory
- **Keep your phone plugged in** for longer sessions
- **First response takes longer** as the model loads into memory
- **Subsequent responses are faster** (1-5 seconds)
- **Works best with 8GB+ RAM** devices

## Troubleshooting

### "Ollama not found" Error

This error does not apply to the mobile version. If you see model-related errors:

1. Check that you have at least 20GB free storage
2. Restart the app
3. Try downloading the model again

### App Crashes

1. Close other apps to free up memory
2. Restart your phone
3. Reinstall the app
4. Check that you have at least 8GB RAM available

### Slow Responses

1. Close other apps
2. Ensure your phone has enough free RAM
3. Keep the phone plugged in
4. Try restarting the app

### Model Download Fails

1. Check your internet connection
2. Ensure you have at least 10GB free storage
3. Try again later (server might be busy)
4. Use a Wi-Fi connection for faster download

## Architecture

The app uses the following technology stack:

- **React Native** - Cross-platform mobile framework
- **Expo** - Development and build platform
- **TensorFlow Lite** - On-device AI inference
- **Gemma-3n-E4B-it** - Google's lightweight LLM model
- **SQLite** - Local data storage
- **Zustand** - State management

## Data Storage

All data is stored locally on your device:

- **Chat History**: Stored in SQLite database
- **Projects**: Stored in SQLite database
- **Gemma Model**: Stored in app cache directory
- **Settings**: Stored in SQLite database

Data is never sent to external servers.

## Privacy & Security

- ✅ All processing happens on your device
- ✅ No data collection or tracking
- ✅ No external API calls
- ✅ No account required
- ✅ No advertisements
- ✅ Open-source model (Gemma)

## Uninstalling

1. Go to **Settings** → **Apps**
2. Find **Vortex AI OS**
3. Tap **Uninstall**
4. Confirm uninstallation

To completely remove all data:

1. Uninstall the app
2. Go to **Settings** → **Storage**
3. Clear cache and app data

## Development

### Prerequisites

- Node.js 18+
- npm or yarn
- Expo CLI
- Android Studio (for building APK)

### Setup

```bash
# Install dependencies
npm install

# Start development server
npm start

# Run on Android device
npm run android
```

### Building APK

```bash
# Build APK
npm run build:android

# The APK will be available in the output directory
```

## Troubleshooting Development

### Port Already in Use

```bash
# Kill the process using port 8081
lsof -ti:8081 | xargs kill -9
```

### Module Not Found

```bash
# Clear cache and reinstall
rm -rf node_modules
npm install
```

### Build Fails

```bash
# Clean build
npm run build:android -- --clean
```

## Performance Optimization

The app is optimized for mobile performance:

- **Model Quantization**: 8-bit integer quantization for reduced memory
- **Lazy Loading**: Components load on-demand
- **Async Operations**: All heavy operations are asynchronous
- **Memory Management**: Careful memory handling to prevent crashes
- **Battery Optimization**: Minimal background processing

## Future Enhancements

- Voice input support
- Image generation
- Multiple model support
- Conversation export
- Cloud sync (optional)
- Advanced analytics

## License

Vortex AI OS is free and open-source software.

## Support

For issues, questions, or suggestions:

1. Check the troubleshooting section above
2. Review the in-app help
3. Check the GitHub issues page

## Credits

- **Gemma Model**: Google DeepMind
- **React Native**: Meta
- **TensorFlow Lite**: Google
- **Expo**: Expo team

## Version History

### v1.0.0 (Initial Release)
- On-device Gemma-3n-E4B-it integration
- Chat interface with conversation history
- Project management
- Model information and status
- Settings and preferences
- SQLite local storage
- Complete offline functionality

---

**Vortex AI OS v1.0.0 - OnePlus 11 Edition**  
Completely Free • On-Device • Private • Fast
