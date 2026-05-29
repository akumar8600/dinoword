# 🦕 WORDLEY – Installation Guide

## What's in this folder?
```
wordley-pwa/
├── index.html      ← The complete app
├── manifest.json   ← Makes it installable
├── sw.js           ← Offline support
├── icon-192.png    ← App icon (Android)
└── icon-512.png    ← App icon (large)
```

---

## ✅ OPTION 1: Install as App on Android (PWA) — No PC Needed!

### Step 1: Host it for FREE (takes 2 minutes)

**Using Netlify Drop (easiest):**
1. On your phone/tablet, go to: **https://app.netlify.com/drop**
2. You'll see a drag-and-drop area
3. Since you're on mobile, tap the upload button
4. Upload ALL 5 files from this folder
5. Netlify gives you a FREE link like: `https://amazing-name-123.netlify.app`

**Alternative – Using GitHub Pages (free):**
1. Go to **https://github.com** → Sign up free
2. Create a new repository called `wordley`
3. Upload all 5 files
4. Go to Settings → Pages → Deploy from main branch
5. Your app is live at: `https://yourusername.github.io/wordley`

---

### Step 2: Install on Android as App

1. Open **Chrome** on your Android phone/tablet
2. Go to your Netlify/GitHub Pages URL
3. Tap the **three-dot menu (⋮)** in Chrome
4. Tap **"Add to Home screen"** or **"Install app"**
5. Tap **Install** on the popup
6. 🎉 Wordley icon appears on your home screen!
7. Opens fullscreen like a real app — no browser bar!

---

## ✅ OPTION 2: Real APK (No PC – Cloud Build via Expo)

Since you don't have a PC, you can build a real APK in the cloud:

### Step 1: Set up Expo (free)
1. Go to **https://expo.dev** on your phone's browser
2. Create a free account
3. This is Expo's cloud build service — it builds APKs for you!

### Step 2: Use GitHub Codespaces (free browser-based coding)
1. Go to **https://github.com** and sign in
2. Create a new repo
3. Click **Code → Codespaces → Create codespace**
4. A full VS Code opens in your browser!
5. Run these commands in the terminal:
```bash
npx create-expo-app wordley --template blank
cd wordley
# Copy your app code into App.js
npx expo install expo-web-browser
eas build -p android --profile preview
```
6. Expo builds the APK in the cloud
7. Download the `.apk` link they email you
8. Install it on Android!

---

## 📱 Quick Answer: What Should You Do?

**Since you only have a phone/tablet:**

➡️ **Use Option 1 (PWA via Netlify Drop)** — it takes 5 minutes, works great, and installs like a real app. 95% of the experience of a native app!

The app already:
- Works offline (words you've seen are cached)
- Has its own home screen icon
- Opens fullscreen with no browser bar
- Saves your score & streak locally
- Works on ALL Android phones & tablets

---

## 🔑 Important: Anthropic API Key

The app calls Claude AI for word meanings and quizzes.
When you open the hosted app, it uses the Claude API automatically through Claude.ai's artifact system.

If hosting yourself on Netlify/GitHub Pages, you'll need to add your API key:
1. Get a free key at **https://console.anthropic.com**
2. In `index.html`, find the fetch call to `api.anthropic.com`
3. Add the header: `"x-api-key": "YOUR_KEY_HERE"`

---

Made with 💜 for your little word explorer!
