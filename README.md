# Patient Journey Tracker 🏥

A real-time patient location tracking system using BLE beacons, Firebase, and a live web dashboard.

## Live Dashboard
🔗 https://patient-tracker-d715a.web.app

## How It Works
1. A smartphone running nRF Connect broadcasts as a BLE beacon (simulating a patient wristband)
2. A Python script on a laptop scans for the beacon and detects signal strength (RSSI)
3. Based on RSSI, the patient's room is determined and updated in Firebase Realtime Database
4. A live web dashboard reads Firebase and displays the patient's current location in real time

## Tech Stack
- **BLE Beacon** — nRF Connect app (Android)
- **Room Scanner** — Python + Bleak library
- **Database** — Firebase Realtime Database
- **Dashboard** — HTML/CSS/JS hosted on Firebase Hosting

## Setup
1. Install dependencies: `pip install bleak requests`
2. Run the scanner: `python scanner.py`
3. Open the dashboard: https://patient-tracker-d715a.web.app

## Project Structure
patient-dashboard/
├── public/
│   └── index.html      # Live dashboard
├── firebase.json       # Firebase config
└── .firebaserc         # Firebase project link

## Future Improvements
- Multiple BLE receivers for true room-level accuracy
- RSSI fingerprinting for better location detection
- Multiple patient tracking
- Patient history and timeline log