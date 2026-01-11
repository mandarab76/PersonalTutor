# 🎓 Omkar Tutor (Mobile AI Companion)

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()
[![Platform](https://img.shields.io/badge/Platform-PWA%20%7C%20Mobile-orange.svg)]()

> **A voice-first, syllabus-aware AI tutor designed for the students of Omkar English Medium School.**



## 📖 Overview

**Omkar Tutor** is a lightweight, mobile-first web application designed to help students navigate the gap between their private school textbooks and the standard CBSE curriculum. 

It is built as a **Progressive Web App (PWA)** that runs entirely in the browser using "Vanilla" JavaScript, leveraging the **Web Speech API** for voice recognition and **OpenAI's GPT-4o** for intelligence.

### 🌟 Key Features
* **Dual Persona System:**
    * 🦄 **Mrunal Mode (Class 4):** Playful, visual, and simple. Maps vague keywords (e.g., "The Mars Story") to specific textbook chapters.
    * 🪄 **Gargi Mode (Class 8):** Strict, exam-focused, and concise. Focuses on definitions, formulae, and high-order thinking.
* **Zero-Touch Interface:** Designed for children who prefer speaking over typing.
* **Privacy-Focused:** API keys are stored locally on the device (LocalStorage); no backend server required.
* **Offline-Ready UI:** Installs as a native app on Android/iOS via "Add to Home Screen."

---

## 🚀 Quick Start (Deployment)

Since this app uses a single-file architecture (`index.html`), deployment is instant via GitHub Pages.

### Prerequisites
* A GitHub Account.
* An OpenAI API Key (`sk-...`).

### Steps
1.  **Fork/Clone** this repository.
2.  **Upload** the `index.html` file to the root of your repository.
3.  **Enable GitHub Pages:**
    * Go to **Settings** > **Pages**.
    * Under **Source**, select `Deploy from a branch`.
    * Select Branch: `main` (or `master`) folder: `/ (root)`.
    * Click **Save**.
4.  **Launch:** Wait ~1 minute. Your app will be live at:
    > `https://<your-username>.github.io/<repo-name>/`

---

## 📱 Mobile Installation

To get the full "App Experience" on a phone (Redmi Note, Pixel, iPhone, etc.):

1.  Open your deployed GitHub Pages URL in **Chrome** (Android) or **Safari** (iOS).
2.  **Grant Permissions:** Tap "Allow" when asked for Microphone access.
3.  **Install:**
    * **Android:** Tap the Three Dots Menu (⋮) → **Add to Home Screen**.
    * **iOS:** Tap the Share Button (⬆️) → **Add to Home Screen**.
4.  **Launch:** Open the new icon on your home screen. It will open full-screen without the browser address bar.

---

## ⚙️ Configuration

### 1. Setting the API Key
On the first launch, the app will ask for your OpenAI API Key.
* Paste your key (`sk-xxxx...`).
* Click **Save**.
* *Security Note:* The key is saved in your phone's browser `LocalStorage`. It is never sent to any server other than OpenAI.

### 2. Updating the Syllabus
To teach the AI about new chapters or exams, edit the `MRUNAL_SYLLABUS` object inside `index.html`:

```javascript
// Inside index.html script tag
const MRUNAL_SYLLABUS = {
    "keyword": "Official Chapter Title (Context)",
    "mars": "A Holiday on Mars (Half Yearly Exam)",
    "turkish": "The Turkish Cap (Cycle Test 1)"
};
