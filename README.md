<div align="center">

# UniteRide
<img src="markdown-resource/Logo.svg" alt="UniteRide Logo" width="1000"/>

**A unified Android bus tracking application for Hong Kong public transport.**

[![Android](https://img.shields.io/badge/Platform-Android%2012%2B-3DDC84?style=flat-square&logo=android&logoColor=white)](https://developer.android.com/)
[![Java](https://img.shields.io/badge/Language-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Target SDK](https://img.shields.io/badge/Target%20SDK-Android%2015-3DDC84?style=flat-square&logo=android&logoColor=white)](https://developer.android.com/about/versions/15)
[![Google Maps](https://img.shields.io/badge/Google%20Maps%20SDK-Integrated-4285F4?style=flat-square&logo=googlemaps&logoColor=white)](https://developers.google.com/maps/documentation/android-sdk)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

[Installation](#install-requirement) · [Build Guide](#build-your-own) · [Report Bug](https://github.com/Chung1045/UniteRide/issues) · [Request Feature](https://github.com/Chung1045/UniteRide/issues)

</div>

---

## Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Screenshots](#screenshots)
- [Install Requirement](#install-requirement)
- [Build Your Own](#build-your-own)
- [Permissions](#permissions)
- [Libraries](#libraries)
- [Contributors](#contributors)

---

## About the Project

UniteRide is an Android bus tracking application that provides real-time information about bus locations and schedules sourced from Hong Kong Government's Open Data Platform. It is designed to help commuters plan journeys more efficiently with accurate, up-to-date transit data — all in a single unified interface.

The application covers route information and estimated arrival times for:

- **KMB** — Kowloon Motor Bus
- **CTB** — Citybus
- **GMB** — Green Minibus

> This project was developed as a group assignment for the Mobile Application Development course (COMP S313F) at Hong Kong Metropolitan University in 2025.
>
> The application was originally named **"9 Rush To Bus"** during development — a Cantonese idiom describing the act of rushing to catch a bus. It was later renamed **UniteRide** to better reflect its unified, multi-operator scope.

---

## Features

| Category | Feature |
|---|---|
| **Transit Data** | Real-time bus tracking with estimated arrival times |
| **Route Information** | Full route listings for KMB, CTB, and GMB |
| **Discovery** | Nearby bus route discovery based on current location |
| **Search** | Bus route search by route number or destination |
| **Maps** | Google Maps integration for visual route guidance |
| **News** | RTHK Traffic News integration (Cantonese only) |
| **Notifications** | Push notifications for tracked bus routes |
| **Language** | Traditional Chinese, Simplified Chinese, and English |
| **Appearance** | Dark mode support |

---

## Screenshots

<div align="center">
  <img src="https://raw.githubusercontent.com/randombytebit/UniteRide/master/markdown-resource/Screenshot%202026-04-27%20at%2019.17.57.png" alt="Screenshot 1" width="220"/>
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/randombytebit/UniteRide/master/markdown-resource/Screenshot%202026-04-27%20at%2019.19.50.png" alt="Screenshot 2" width="220"/>
  &nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/randombytebit/UniteRide/master/markdown-resource/Screenshot%202026-04-27%20at%2019.20.09.png" alt="Screenshot 3" width="220"/>
</div>

---

## Install Requirement

| Requirement | Detail |
|---|---|
| Platform | Android |
| Minimum SDK | Android 12 (API 31) |
| Target SDK | Android 15 (API 35) |

Download the latest release APK from the [Releases](https://github.com/Chung1045/UniteRide/releases) page and install it on your Android device.

---

## Build Your Own

> **Note:** A valid Google Maps API Key is required to build the application and use Google Maps SDK features. If you do not have one, apply for a key at [Google Cloud Console](https://console.cloud.google.com/).

### Prerequisites

| Requirement | Detail |
|---|---|
| Operating System | macOS / Linux / Windows |
| IDE | [Android Studio](https://developer.android.com/studio) or any IDE with Android support |
| Google Maps API Key | Required — obtain from Google Cloud Console |
| Version Control | git |

### Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/Chung1045/UniteRide.git
   ```

2. **Open the project** in Android Studio or your preferred IDE.

3. **Create the required property files** in the root directory of the project if they are not already present:

   - `local.properties`
   - `gradle.properties`
   - `secret.properties`

4. **Add the SDK path** to `local.properties` (Android Studio typically generates this automatically):

   ```properties
   sdk.dir=/path/to/your/Android/sdk
   ```

5. **Add your Google Maps API Key** to `secret.properties`:

   ```properties
   MAPS_API_KEY=YOUR_GOOGLE_MAPS_API_KEY
   ```

   Replace `YOUR_GOOGLE_MAPS_API_KEY` with your actual key. This value is referenced securely at build time and is not committed to version control.

6. **Build and run** the application from your IDE using a connected Android device or emulator running Android 12 or higher.

---

## Permissions

| Permission | Required | Purpose |
|---|---|---|
| Network Access | Yes | Fetching real-time bus data from open APIs |
| Location | Optional | Nearby bus route discovery |
| Notifications | Optional | Bus tracking alerts |

**Privacy Note:** Location data is processed locally on-device and is not transmitted to any external server by this application. However, when using Android Location Services, location data may be sent to Google for processing. Please refer to the [Google Privacy Policy](https://policies.google.com/privacy) for details.

---

## Libraries

| Library | Purpose |
|---|---|
| [JSoup](https://jsoup.org/) | HTML parsing for web-sourced transit data |
| [OkHttp](https://square.github.io/okhttp/) | HTTP networking for API requests |
| [Google Maps SDK for Android](https://developers.google.com/maps/documentation/android-sdk) | Map rendering and route visualization |
| [SQLite](https://www.sqlite.org/) | Local data persistence |

---

## Contributors

| Contributor | GitHub |
|---|---|
| randombytebit | [@randombytebit](https://github.com/randombytebit) |
| Chung1045 | [@Chung1045](https://github.com/Chung1045) |

---

<div align="center">

UniteRide · COMP S313F · Hong Kong Metropolitan University · 2025

</div>
