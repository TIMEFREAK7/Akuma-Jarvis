# Vortex AI OS Mobile - Installation & Setup Guide

This guide provides step-by-step instructions for installing and setting up Vortex AI OS on your OnePlus 11 phone.

## Prerequisites

Before you begin, ensure your OnePlus 11 meets these requirements:

- **Android Version**: Android 7.0 (API 24) or higher
- **RAM**: 8GB minimum (12GB+ recommended for optimal performance)
- **Storage**: 20GB free space (4GB for app + 16GB for model)
- **Internet**: Wi-Fi connection recommended for model download (~4GB)
- **Battery**: Fully charged or plugged in during setup

## Part 1: Preparing Your Phone

### Step 1.1: Enable Unknown Sources

To install the app from an APK file, you need to enable installation from unknown sources:

1. Open **Settings** on your OnePlus 11
2. Scroll down and tap **Security & Privacy**
3. Tap **More security settings**
4. Find **Install apps from unknown sources**
5. Tap your file manager (e.g., "Files" or "File Manager")
6. Toggle the switch to **ON**
7. Return to Settings and confirm the change

### Step 1.2: Check Storage Space

1. Open **Settings**
2. Tap **Storage**
3. Check that you have at least 20GB free space
4. If not, delete unnecessary files or apps

### Step 1.3: Connect to Wi-Fi

1. Open **Settings**
2. Tap **Wi-Fi**
3. Select your Wi-Fi network
4. Enter the password if required
5. Confirm connection

## Part 2: Installing Vortex AI OS

### Step 2.1: Download the APK

**Option A: Download on Phone**

1. Open your phone's browser
2. Navigate to the download link provided
3. Tap the download button
4. Wait for download to complete
5. Tap the notification to open the file

**Option B: Transfer from Computer**

1. Download the APK file on your computer
2. Connect your OnePlus 11 to your computer via USB
3. Enable **File Transfer** mode on your phone
4. Copy the APK file to your phone's storage
5. Disconnect and navigate to the file using your file manager

### Step 2.2: Install the App

1. Open your file manager
2. Navigate to the Downloads folder (or where you saved the APK)
3. Tap the **vortex-ai-os.apk** file
4. A dialog will appear asking for permission
5. Tap **Install**
6. Wait for the installation to complete (usually 30-60 seconds)
7. Tap **Open** to launch the app, or **Done** to close

### Step 2.3: Grant Permissions

When you launch the app for the first time, it will request permissions:

1. **Storage**: Tap **Allow** to store the model and data
2. **Internet**: Tap **Allow** to download the model
3. Confirm any other permission requests

## Part 3: Initial Setup Wizard

### Step 3.1: Welcome Screen

1. Launch **Vortex AI OS**
2. Read the welcome message
3. Review the key features
4. Tap **Next: Download Model**

### Step 3.2: Download Gemma Model

This step downloads the Gemma-3n-E4B-it model (~4GB):

1. Ensure you're connected to Wi-Fi
2. Ensure your phone is plugged in (recommended)
3. Tap **Download Model (~4GB)**
4. A progress bar will show the download status
5. **Do not close the app** during download
6. Wait for the download to complete (10-30 minutes depending on connection)
7. Once complete, the app will automatically proceed to the next step

**Troubleshooting Download Issues:**

- **Download Fails**: Check your internet connection and try again
- **Storage Full**: Free up at least 10GB of space
- **Slow Download**: Move closer to your Wi-Fi router or try a different network
- **Connection Drops**: Stay connected to Wi-Fi throughout the download

### Step 3.3: Initialize Model

1. The app will initialize the downloaded model
2. This may take 1-2 minutes on first launch
3. **Do not close the app** during initialization
4. A progress indicator will show the status
5. Once complete, tap **Continue**

### Step 3.4: Setup Complete

1. Review the completion message
2. Tap **Start Using Vortex AI OS**
3. The app will launch to the main chat interface

## Part 4: First Time Usage

### Step 4.1: Create Your First Project

1. Go to the **Projects** tab (folder icon)
2. Tap the **+** button in the bottom-right
3. Enter a project name (e.g., "My First Chat")
4. Optionally add a description
5. Tap **Create**

### Step 4.2: Start Chatting

1. Go to the **Chat** tab (chat bubble icon)
2. Type a message in the input box
3. Tap the send button (arrow icon)
4. Wait for the response (1-5 seconds)
5. Continue the conversation

### Step 4.3: Explore Features

- **Chat Tab**: Main conversation interface
- **Projects Tab**: Manage your projects
- **Models Tab**: View model information and specifications
- **Settings Tab**: Adjust app preferences

## Part 5: Optimization Tips

### Battery Life

- Keep your phone plugged in during long sessions
- Close other apps to reduce CPU usage
- Use a dark theme (already enabled by default)

### Performance

- Close apps running in the background
- Restart your phone if the app feels slow
- Keep at least 5GB free storage
- Ensure adequate RAM is available

### Storage

- Conversations are stored locally, so they don't use cloud storage
- The model file (~4GB) is cached on your device
- You can delete old conversations to free up space

## Part 6: Troubleshooting

### Installation Issues

**Error: "App not installed"**
- Ensure you enabled "Install from Unknown Sources"
- Try downloading the APK again
- Restart your phone and try again

**Error: "Insufficient Storage"**
- Delete unnecessary files or apps
- Ensure you have at least 20GB free space
- Clear your phone's cache

### Setup Issues

**Model Download Fails**
- Check your internet connection
- Ensure you're on Wi-Fi (not mobile data)
- Try again later if the server is busy
- Restart your phone and try again

**Model Initialization Fails**
- Ensure you have at least 8GB free RAM
- Close other apps
- Restart your phone
- Reinstall the app

### Runtime Issues

**App Crashes**
- Close other apps to free up memory
- Restart your phone
- Clear the app cache (Settings → Apps → Vortex AI OS → Storage → Clear Cache)
- Reinstall the app

**Slow Responses**
- Close other apps
- Ensure your phone has adequate free RAM
- Keep your phone plugged in
- Restart the app

**"Model Not Loaded" Error**
- Restart the app
- Restart your phone
- Reinstall the app

## Part 7: Uninstalling

To remove Vortex AI OS from your OnePlus 11:

1. Open **Settings**
2. Tap **Apps**
3. Find **Vortex AI OS**
4. Tap **Uninstall**
5. Confirm the uninstallation

To completely remove all data:

1. Uninstall the app (see above)
2. Open **Settings** → **Storage**
3. Tap **Manage Storage**
4. Find **Vortex AI OS**
5. Tap **Delete** to remove cached data

## Part 8: Advanced Configuration

### Changing Settings

1. Go to the **Settings** tab
2. Toggle options as desired:
   - **Auto-save Conversations**: Automatically save chat history
   - **Notifications**: Receive app notifications
   - **Analytics**: Help improve the app (anonymous)

### Backing Up Data

To back up your conversations:

1. Connect your phone to a computer
2. Enable **File Transfer** mode
3. Navigate to: `Internal Storage → Android → data → com.vortex.aios`
4. Copy the `vortex.db` file to your computer

### Restoring Data

To restore backed-up conversations:

1. Connect your phone to a computer
2. Enable **File Transfer** mode
3. Navigate to: `Internal Storage → Android → data → com.vortex.aios`
4. Replace the `vortex.db` file with your backup
5. Restart the app

## Part 9: Performance Benchmarks

Typical performance on OnePlus 11:

| Operation | Time |
|-----------|------|
| App Launch | 2-3 seconds |
| Model Load (first time) | 5-10 seconds |
| First Response | 3-5 seconds |
| Subsequent Responses | 1-3 seconds |
| Model Download | 10-30 minutes (Wi-Fi) |
| Model Initialization | 1-2 minutes |

## Part 10: FAQ

**Q: Is it really completely free?**
A: Yes! No API costs, no subscriptions, no hidden charges.

**Q: Does it need internet?**
A: You need internet to download the model initially. After that, it works offline.

**Q: Can I use it without the internet?**
A: Yes, completely offline after the initial model download.

**Q: How much storage does it use?**
A: About 4GB for the model + variable storage for conversations (usually <100MB).

**Q: Can I delete the model to free up space?**
A: Yes, but you'll need to re-download it to use the app again.

**Q: Is my data private?**
A: Yes, 100% private. All data stays on your device.

**Q: Can I use other models?**
A: Currently only Gemma-3n-E4B-it is supported. Future versions may support other models.

**Q: What if I run out of storage?**
A: Delete old conversations or other apps to free up space.

**Q: Can I export my conversations?**
A: You can back up the database file (see Part 8).

## Part 11: Getting Help

If you encounter issues:

1. Check the Troubleshooting section above
2. Review the in-app help
3. Restart your phone
4. Reinstall the app
5. Check the GitHub issues page

## Part 12: System Requirements Summary

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| Android Version | 7.0 (API 24) | 11.0+ |
| RAM | 8GB | 12GB+ |
| Storage | 20GB free | 30GB+ free |
| Processor | Snapdragon 888 | Snapdragon 8 Gen 1+ |
| Battery | 4000mAh | 5000mAh+ |

---

**Congratulations!** You've successfully installed and set up Vortex AI OS on your OnePlus 11. Enjoy your completely free, on-device AI assistant!

For the latest updates and support, visit the official repository.

**Vortex AI OS v1.0.0 - OnePlus 11 Edition**  
Completely Free • On-Device • Private • Fast
