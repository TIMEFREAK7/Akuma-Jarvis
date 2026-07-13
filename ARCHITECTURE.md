# Vortex AI OS Mobile - Architecture Design

This document outlines the architecture for the mobile version of Vortex AI OS, specifically targeting OnePlus 11 devices and leveraging the Google Gemma-3n-E4B-it model for on-device AI processing. The design prioritizes a completely free, offline-capable, and user-friendly experience.

## 1. Core Principles

-   **On-Device AI**: All Large Language Model (LLM) inference will occur directly on the device using the Gemma-3n-E4B-it model, eliminating external API costs and ensuring privacy.
-   **Completely Free**: No subscription fees, API costs, or hidden charges for the end-user.
-   **Offline Functionality**: The application will be fully functional without an internet connection after initial model download.
-   **User-Friendly**: Intuitive mobile-first UI/UX, with a focus on simplicity and ease of use.
-   **Performance Optimized**: Designed for efficient execution on mobile hardware, considering battery life and resource consumption.
-   **Cross-Platform (React Native)**: While targeting OnePlus 11, the architecture will leverage React Native with Expo to allow for potential future expansion to other Android devices or iOS.

## 2. Technology Stack

| Component         | Technology/Framework | Rationale                                                              |
| :---------------- | :------------------- | :--------------------------------------------------------------------- |
| **Frontend**      | React Native         | Cross-platform development, rich UI components, large community.       |
| **Development Kit** | Expo                 | Simplified setup, build, and deployment for React Native.              |
| **On-Device AI**  | TensorFlow Lite      | Google's framework for deploying ML models on mobile and edge devices. |
| **LLM Model**     | Gemma-3n-E4B-it      | Optimized for on-device execution, free, and from Google.              |
| **Local Storage** | SQLite (via Expo)    | Persistent, structured data storage directly on the device.            |
| **State Management**| React Context / Zustand | Efficient and scalable state management for complex UIs.               |
| **UI Library**    | React Native Paper / NativeBase | Pre-built, customizable UI components for mobile.                      |

## 3. Data Flow and Interactions

```mermaid
graph TD
    User[User Interaction] --> MobileApp[Vortex AI OS Mobile App]
    MobileApp --> ReactUI[React Native UI]
    ReactUI --> StateManagement[State Management]
    StateManagement --> LocalDB[SQLite Database]
    StateManagement --> OnDeviceAI[On-Device AI (TensorFlow Lite)]
    OnDeviceAI --> GemmaModel[Gemma-3n-E4B-it Model]
    GemmaModel --> OnDeviceAI
    OnDeviceAI --> StateManagement
    LocalDB --> StateManagement
    MobileApp --> OS[OnePlus 11 Android OS]
    OS --> Hardware[Phone Hardware (CPU, GPU, NPU, RAM)]
```

### 3.1. User Interaction

-   Users interact with the React Native UI to input queries, manage projects, and view responses.

### 3.2. React Native UI

-   Handles rendering, user input, and display of chat messages, project lists, and model status.
-   Communicates with `State Management` for data updates and `On-Device AI` for LLM inference requests.

### 3.3. State Management

-   Manages application state, including active conversations, messages, projects, and user settings.
-   Orchestrates data flow between the UI, local database, and on-device AI.

### 3.4. On-Device AI (TensorFlow Lite)

-   Loads and manages the Gemma-3n-E4B-it model.
-   Receives prompts from `State Management`.
-   Performs LLM inference locally on the device.
-   Returns generated responses to `State Management`.
-   Handles model quantization and optimization for mobile hardware.

### 3.5. Gemma-3n-E4B-it Model

-   The specific LLM model, pre-trained and optimized for mobile devices.
-   Will be integrated as a TensorFlow Lite model (`.tflite` format).

### 3.6. SQLite Database

-   Stores persistent application data:
    -   **Projects**: User-defined workspaces.
    -   **Conversations**: Chat sessions within projects.
    -   **Messages**: Individual chat messages (user input and AI responses).
    -   **Settings**: User preferences and application configuration.
-   Accessed via Expo's SQLite API.

### 3.7. OnePlus 11 Android OS & Hardware

-   The underlying operating system and hardware provide the execution environment for the React Native application and TensorFlow Lite inference.
-   Leverages the phone's CPU, GPU, and potentially Neural Processing Unit (NPU) for accelerated AI inference.

## 4. Key Features Implementation Details

### 4.1. On-Device Gemma Integration

-   **Model Acquisition**: The Gemma-3n-E4B-it model will need to be obtained in a `.tflite` format compatible with TensorFlow Lite.
-   **TensorFlow Lite Integration**: Use React Native libraries that wrap TensorFlow Lite (e.g., `@tensorflow/tfjs-react-native` or direct native module integration).
-   **Inference API**: Create a JavaScript API within the React Native app to send prompts to the loaded Gemma model and receive responses.

### 4.2. User Interface (UI)

-   **Chat Interface**: Similar to the desktop version, with streaming-like response display, markdown rendering, and conversation history.
-   **Project/Conversation Management**: Mobile-friendly navigation for creating, selecting, and managing projects and conversations.
-   **Model Management**: A simple UI to verify the Gemma model is loaded and potentially manage other local models if supported by TensorFlow Lite.
-   **Settings**: Basic settings for theme, model preferences, etc.

### 4.3. Local Data Persistence

-   **SQLite**: Use `expo-sqlite` for database operations. The schema will be similar to the desktop version (Projects, Conversations, Messages, Settings).
-   **Data Migration**: Handle initial database creation and schema updates seamlessly.

### 4.4. Setup Wizard & First-Run Experience

-   **Initial Check**: On first launch, check if the Gemma model is present and downloaded.
-   **Model Download**: If not present, guide the user through downloading the Gemma-3n-E4B-it `.tflite` file (potentially from a pre-configured URL or bundled with the app if size permits).
-   **Permissions**: Request necessary permissions (e.g., storage access) during setup.

## 5. Performance and Optimization

-   **Model Quantization**: Ensure the Gemma model is quantized (e.g., 8-bit integer) for optimal performance and reduced memory footprint on mobile devices.
-   **Asynchronous Operations**: All AI inference and database operations will be asynchronous to keep the UI responsive.
-   **Memory Management**: Carefully manage memory usage to prevent crashes and ensure smooth operation, especially during LLM inference.
-   **Battery Life**: Optimize background processes and model loading to minimize battery drain.

## 6. Distribution

-   **Android APK/AAB**: The final application will be built as an Android Application Package (APK) or Android App Bundle (AAB) for distribution.
-   **Side-loading**: Users will likely side-load the APK/AAB onto their OnePlus 11 devices.
-   **Documentation**: Clear, step-by-step installation instructions for side-loading and first-time setup.

## 7. Future Considerations

-   **Other Android Devices**: The React Native/Expo architecture allows for easy adaptation to other Android phones.
-   **Model Updates**: A mechanism for updating the Gemma model `.tflite` file without requiring a full app update.
-   **Advanced Features**: Voice input, image generation (if mobile-optimized models become available), and more complex agentic workflows.

This architecture provides a solid foundation for a free, powerful, and user-friendly AI OS experience on the OnePlus 11.
