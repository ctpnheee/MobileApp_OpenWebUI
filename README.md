# OpenMobileUI

A mobile client application for [OpenWebUI](https://github.com/open-webui/open-webui) that allows you to connect to OpenWebUI servers and interact with AI models directly from your mobile device.

## 📱 Features

- **Multi-Server Management**: Add, modify, and manage multiple OpenWebUI server connections
- **AI Conversations**: Chat with various AI models available on your OpenWebUI servers
- **Conversation History**: View and resume previous conversations
- **Model Selection**: Choose from available AI models on your connected servers
- **Markdown Support**: Rich text rendering for AI responses
- **Secure Storage**: API keys and sensitive data stored securely using Expo Secure Store
- **Offline Caching**: Conversations and data cached locally with SQLite
- **Push Notifications**: Get notified about important events
- **Conversation Controls**: Manage conversation parameters and settings
- **Copy to Clipboard**: Easily copy messages and responses

## 🛠️ Tech Stack

- **Framework**: React Native with Expo
- **Language**: TypeScript
- **Navigation**: Expo Router
- **Database**: SQLite (expo-sqlite)
- **Secure Storage**: Expo Secure Store
- **UI Components**: React Native core components with custom styling
- **Markdown Rendering**: react-native-markdown-display
- **Notifications**: Expo Notifications

## 📋 Prerequisites

- Node.js (version 18 or higher recommended)
- npm or yarn
- Expo CLI
- For iOS development: macOS with Xcode
- For Android development: Android Studio

## 🚀 Getting Started

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/MobileApp_OpenWebUI.git
cd MobileApp_OpenWebUI
```

2. Install dependencies:

```bash
npm install
```

### Running the App

#### Development with Expo Go

```bash
npm start
```

Then scan the QR code with:
- **iOS**: Camera app
- **Android**: Expo Go app

#### Development Build

For a more native experience with custom native modules:

```bash
npm run android
# or
npm run ios
```

## 📱 Usage

### Adding a Server

1. Launch the app
2. Tap the **+** button on the home screen
3. Enter your OpenWebUI server details:
   - Server name (display name)
   - Server address (e.g., `https://your-openwebui-server.com`)
   - API key (from your OpenWebUI account settings)
4. Tap "Add" to save

### Starting a Conversation

1. Select a server from the home screen
2. Choose an AI model from the model selector
3. Type your message and tap send
4. View the AI's response with markdown formatting support

### Managing Conversations

- **View History**: Tap the history icon to see past conversations
- **Control Settings**: Access conversation parameters and controls
- **Copy Messages**: Long press on messages to copy them
- **Delete Conversations**: Swipe to delete in the history view

## 🏗️ Project Structure

```
MobileApp_OpenWebUI/
├── app/                          # Application screens and components
│   ├── _layout.tsx              # Root layout with navigation
│   ├── index.tsx                # Home screen (server selection)
│   ├── conversation.tsx         # Main chat interface
│   ├── historique.tsx           # Conversation history
│   ├── parametres.tsx           # Settings screen
│   ├── SelecteurModele.tsx      # Model selection component
│   └── styles/                  # Screen-specific styles
├── bdd/                         # Database management
│   ├── bddListeServeurs.ts     # Server list database operations
│   ├── bddParametresApplication.ts # App settings storage
│   └── cache/                   # Caching system
├── classes/                     # Custom error classes
│   ├── BddError.ts             # Database error handling
│   └── FetchError.ts           # Network error handling
├── gestionGlobaleBackend/      # Backend integration layer
│   ├── bddListeServeursEtCache.ts
│   └── requetesServeurAvecCacheEtNotification/
├── outils/                      # Utility functions
│   ├── fonctionsOutils.ts      # Helper functions
│   ├── notificationService.ts  # Notification handling
│   └── ParserMessage.tsx       # Message parser component
├── requetesServeur/            # Server API requests
│   ├── requetesBasiques.ts     # Basic API calls
│   ├── requetesGestionConversation.ts # Conversation management
│   └── outils/                  # Request utilities
├── test/                        # Test files
├── types/                       # TypeScript type definitions
│   ├── dataTypes.ts            # Data structure types
│   └── typesBDD.ts             # Database types
└── assets/                      # Images and static resources
```

## 🧪 Testing

Run the test suite:

```bash
npm test
```

## 🔒 Security

- API keys are stored securely using Expo Secure Store
- Secure communication with HTTPS endpoints
- Local data encrypted at rest
- No sensitive data logged in production

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Known Issues

- Please check the [Issues](https://github.com/yourusername/MobileApp_OpenWebUI/issues) page for current bugs and feature requests

## 📧 Support

For support, please open an issue on GitHub or contact the maintainers.

## 🙏 Acknowledgments

- [OpenWebUI](https://github.com/open-webui/open-webui) for the amazing backend platform
- The React Native and Expo teams for excellent mobile development tools
- All contributors who help improve this project

---

Made with ❤️ for the OpenWebUI community
