# HabiTrack

> **Productivity Monitoring & Mobile Usage Control System**

**HabiTrack** is an open-source project designed to boost personal productivity by integrating PC activity tracking with mobile usage management. By monitoring your active development time (e.g., in VSCode, IntelliJ) and correlating it with controlled mobile app usage, HabiTrack rewards consistent work with designated "free" phone time.

## Table of Contents

1. [Features](#features)  
2. [Project Architecture](#project-architecture)  
3. [Tech Stack](#tech-stack)  
4. [Installation & Setup](#installation--setup)  
   - [Backend Setup](#backend-setup)  
   - [Desktop Tracker](#desktop-tracker)  
   - [Mobile App](#mobile-app)  
5. [Usage](#usage)  
6. [Roadmap](#roadmap)  
7. [Contributing](#contributing)  
8. [Code of Conduct](#code-of-conduct)  
9. [License](#license)  
10. [Support & Contact](#support--contact)  

---

## Features

1. **PC Activity Monitoring**  
   - Tracks user's active time in IDEs (VSCode, IntelliJ, etc.) and other productivity apps.  
   - Logs session data for insight into work patterns.

2. **Mobile Usage Restriction**  
   - Cross-platform mobile app (iOS/Android) restricts or limits access to selected apps.  
   - Can lock screen, manage notifications, and set daily usage quotas.

3. **Reward System**  
   - Work-to-reward ratio (e.g., 30 mins of work = 10 mins phone time).  
   - Notifications when reward time is nearing its limit.

4. **Real-Time Sync**  
   - Uses WebSockets or Firebase to sync data between desktop client and mobile app in real-time.  
   - Ensures instant updates on usage stats.

5. **Gamification & Motivation**  
   - Progress tracking, streaks, badges, and achievements to encourage consistent productivity.  
   - Option to share accomplishments or compete with friends.

---

## Project Architecture

```
HabiTrack/
├── backend/
│   ├── src/
│   │   └── ... (API endpoints, user auth, activity logging)
│   ├── package.json
│   └── ...
├── desktop/
│   ├── electron-app/
│   │   └── ... (Electron code for desktop tracker)
│   └── ...
├── mobile/
│   ├── src/
│   │   └── ... (React Native screens & components)
│   ├── package.json
│   └── ...
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── LICENSE
└── README.md
```

- **Backend**: Handles user authentication (OAuth), activity logging, and real-time sync with databases.  
- **Desktop**: Electron-based (or browser extension) tracker that monitors active time in IDEs.  
- **Mobile**: React Native app that enforces restrictions, usage time, and displays reward status.

---

## Tech Stack

- **Frontend**  
  - **Desktop Tracker**: [Electron](https://www.electronjs.org/), possibly a browser extension  
  - **Mobile**: [React Native](https://reactnative.dev/) for cross-platform deployment  

- **Backend**  
  - **Server**: [Node.js](https://nodejs.org/) with Express or NestJS (TBD)  
  - **Database**: [Firebase](https://firebase.google.com/) or [MongoDB](https://www.mongodb.com/)  
  - **Real-Time Sync**: Firebase real-time DB / Firestore or WebSocket-based  

- **APIs**  
  - **Platform Hooks**: IDE usage stats (VSCode extensions, IntelliJ plugins), OS-level tracking  
  - **Device Management**: Android’s Device Admin API (for advanced controls), iOS restrictions (where possible)

---

## Installation & Setup

### Backend Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/king04aman/HabiTrack.git
   cd HabiTrack/backend
   ```

2. **Install dependencies**  
   ```bash
   npm install
   ```

3. **Set environment variables**  
   - Create a `.env` file in the `backend/` directory.  
   - Add your database credentials, OAuth keys (Google, Microsoft), etc.  
   - *(This will be updated with time as configurations are finalized.)*  

4. **Run the server**  
   ```bash
   npm run dev
   ```
   - Defaults to `http://localhost:3000` (adjust if needed).

### Desktop Tracker

1. **Navigate to the desktop folder**  
   ```bash
   cd HabiTrack/desktop/electron-app
   ```

2. **Install dependencies**  
   ```bash
   npm install
   ```

3. **Run the Electron app**  
   ```bash
   npm start
   ```
   - This will launch the desktop tracker window.

### Mobile App

1. **Navigate to the mobile folder**  
   ```bash
   cd HabiTrack/mobile
   ```

2. **Install dependencies**  
   ```bash
   npm install
   ```

3. **Run on Android or iOS**  
   ```bash
   # For Android:
   npm run android

   # For iOS (on Mac):
   npm run ios
   ```
   - Make sure you have an Android emulator or iOS simulator set up.

---

## Usage

1. **Create an Account**  
   - Sign up using Google or Microsoft OAuth within the desktop or mobile app.  

2. **Pair Your Devices**  
   - Link the desktop tracker to the mobile app using a unique code or QR scan.  

3. **Configure Restrictions & Rewards**  
   - In the mobile app, select which apps to restrict or set global phone usage limits.  
   - Adjust the work-to-reward ratio (default: 30 min of work for 10 min of phone time).  

4. **Start Working**  
   - When you begin coding or using productivity apps, the desktop tracker logs time.  
   - Earn “reward minutes” to use on your phone.  

5. **Monitor Progress**  
   - Check real-time sync on your phone to see how much reward time you have.  
   - Receive notifications when your reward time is running low.

---

## Roadmap

HabiTrack is an **ongoing** project. The development plan is split into phases:

- **Phase 1 (Target: Feb 2025)**  
  - Basic PC activity tracking and logging  
  - Initial mobile app with manual restrictions  
  - Simple reward system (manual reset)  
  - Basic authentication (OAuth)  

- **Phase 2**  
  - Real-time sync between desktop and mobile  
  - Advanced mobile controls (App-specific locks, notifications)  
  - Gamification elements (streaks, badges)  

- **Phase 3**  
  - IDE-specific plugins (VSCode, IntelliJ)  
  - Dashboard & Analytics for productivity insights  
  - Community features (optional)  

*(Additional phases will be added as the project evolves.)*

---

## Contributing

HabiTrack is open to community contributions! We welcome bug reports, feature requests, and pull requests. Please refer to our [CONTRIBUTING.md](CONTRIBUTING.md) for details on:

- Branch naming & commit message format  
- How to open issues & pull requests  
- Project coding style & best practices  

---

## Code of Conduct

Please note that this project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

---

## License

HabiTrack is licensed under **GPLv3**.  
Please see the [LICENSE](LICENSE) file for more details regarding usage, distribution, and contributions under this license.

---

## Support & Contact

- **Issues & Requests**: Submit a [GitHub Issue](https://github.com/king04aman/HabiTrack/issues) to report bugs or request features.  
- **Discussions**: Join the [GitHub Discussions](https://github.com/king04aman/habitrack/discussions).  
- **Contact**: For direct inquiries, email `king04aman+github@gmail.com`.  
- **Stay Updated**: Watch this repo and join discussions for the latest updates.
