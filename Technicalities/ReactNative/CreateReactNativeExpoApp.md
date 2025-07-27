# 📱 How to Create a React Native App Using Expo (2025 Guide)

## 🧰 Prerequisites

Make sure you have the following tools installed:

- [**Node.js**](https://nodejs.org/) – install the LTS version
- [**VS Code**](https://code.visualstudio.com/) – recommended editor
- [**Expo CLI**](https://docs.expo.dev/) – the fastest way to build React Native apps

---

## ⚙️ Steps to Create Your React Native Project

### 1. Install Expo CLI

In your terminal, run:

```bash
npm install -g expo-cli
```

> 💡 If you're using `npx`, you can skip the global install:
```bash
npx create-expo-app@latest
```

---

### 2. Create the Expo Project

Run:

```bash
npx create-expo-app your-app-name
```

Replace `your-app-name` with whatever you want your project to be called.

You'll be prompted to pick a template — choose:

- **blank (TypeScript)** — if you want TypeScript
- **blank (JavaScript)** — if you want JS (you can add TypeScript later)

---

### 3. Navigate Into Your Project

```bash
cd your-app-name
```

Start the dev server:

```bash
npm start
```

This opens the **Expo Developer Tools** in your browser.

---

### 4. Run Your App

You have 3 options to test your app:

#### ✅ Using a Phone (recommended)
- Install the **Expo Go** app from Google Play / App Store
- Scan the QR code shown in your terminal or browser
- Your app will run instantly

#### 🖥️ Using an Emulator
- For Android: install Android Studio and set up an AVD
- For iOS: use Xcode + iOS Simulator (macOS only)

---

## 🗂️ Folder Structure Overview

```
your-app-name/
├── assets/              # Images, fonts, etc.
├── node_modules/
├── App.js               # Entry point (or App.tsx)
├── package.json
├── babel.config.js
└── .gitignore
```

---

## 📌 Next Steps

- Start editing `App.js` or `App.tsx`
- Install libraries with `npm install` or `npx expo install`
- Use the [Expo docs](https://docs.expo.dev/) to explore camera, maps, notifications, etc.

---

## 📦 Useful Expo Commands

| Command                     | What It Does                          |
|----------------------------|----------------------------------------|
| `npm start` or `npx expo start` | Starts dev server (Metro Bundler)     |
| `npx expo install <pkg>`   | Installs Expo-compatible packages      |
| `npx expo run:android`     | Builds and runs on Android emulator    |
| `npx expo run:ios`         | Builds and runs on iOS (macOS only)    |
| `npx expo export`          | Builds static files for deployment     |

---

## 🔥 Tips for Success

- Use `expo install` instead of `npm install` for native packages — it ensures compatibility.
- Enable **hot reload** in Expo Go for live changes.
- For production apps, use `eas build` for cloud builds (CI/CD ready).
- Don’t eject unless absolutely necessary.

---

> Written with 💻 and ☕ by [AKR]
