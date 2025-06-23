# 📈 Leads Tracker - Progressive Web App (PWA)

A clean, installable **Leads Tracker** app built with **vanilla JavaScript** and **Firebase Realtime Database**, designed to help users save, manage, and track leads like URLs or contact details. Built as a **Progressive Web App (PWA)**, it works offline, syncs in real time, and features a favicon and install prompt for a native-like experience.

## 🌟 Features

- 🔗 Add and save leads manually or from the current browser tab
- ☁️ Store leads in the **Firebase Realtime Database** (live sync across devices)
- 🔒 Secure and scalable backend (configurable Firebase rules)
- 💾 Offline-ready with **Service Worker**
- 🧭 Installable via **Web App Manifest**
- 📱 Mobile-friendly UI and responsive design
- ⭐ Includes a custom **favicon** and PWA icon set

## 🚀 Demo

[Live Demo](#)  
_https://leads-tracker-app-priya.netlify.app/_

## 🛠️ Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Firebase Realtime Database
- Firebase SDK
- Service Workers
- Web App Manifest
- Favicon/Icon set

## 📸 Screenshots

> *(Optional: Add screenshots or a GIF of your app in use on both mobile and desktop)*

## 📦 Project Structure

```plaintext
leads-tracker/
├── index.html             # Main HTML file
├── index.css              # Stylesheet
├── index.js               # JavaScript logic + Firebase
├── site.webmanifest       # PWA Manifest file
├── /icons/                # App icons (for PWA + favicon)
│   ├── favicon.ico
│   ├── favicon-16*16.png
│   └── favicon-32*32.png
````

## 🔥 Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project
3. Enable **Realtime Database** (test mode for development)
4. Get your Firebase config from **Project Settings > Web App**
5. Paste it into your `script.js` file:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "your-app.firebaseapp.com",
  databaseURL: "https://your-app.firebaseio.com",
  projectId: "your-app",
  storageBucket: "your-app.appspot.com",
  messagingSenderId: "SENDER_ID",
  appId: "APP_ID"
};
firebase.initializeApp(firebaseConfig);
```

6. Use the Firebase SDK to read/write leads in real time

## 📲 Installing the App (PWA)

1. Open the app in a supported browser (like Chrome)
2. Click the **Install** button in the browser toolbar or choose **Add to Home Screen**
3. The app will launch with its own icon and splash screen like a native app

## 🌐 Favicon and Icons

* **favicon.ico** is linked in the HTML `<head>`:

  ```html
  <link rel="icon" href="icons/favicon.ico" />
  ```
* PWA icons are defined in `manifest.json`:

  ```json
  "icons": [
    {
      "src": "icons/icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icons/icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
  ```

## ⚙️ Deployment

* You can deploy to:

  * **Firebase Hosting**
  * **GitHub Pages**
  * **Netlify**
* Make sure your `manifest.json`, `sw.js`, and icons are in the root or properly referenced

## 🔐 Firebase Rules (Development)

```json
{
  "rules": {
    ".read": "true",
    ".write": "true"
  }
}
```

⚠️ **Not secure for production.** Set proper rules or use Firebase Auth for real users.

## 🙌 Contributing

Pull requests and feature suggestions are welcome!
Feel free to fork the repo and open a PR.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

Made with 💻 by [Priya Singh](https://github.com/pri-sin)

```
