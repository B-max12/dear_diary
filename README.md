# 📔 Dear Diary — Your Vintage Journal

> A private, offline-first personal diary, life companion, and heritage journal crafted with vintage aesthetics, modern AI intelligence, Google Cloud services, and a free open-source world navigation system.

---

## ✨ Features at a Glance

### 🖋️ Rich Journaling & Memory Preservation
- **Offline-First Storage**: Powered by Drift (SQLite) for instantaneous offline read/write and automatic cloud synchronization with Supabase.
- **Multi-Modal Entries**: Write rich text with Quill, record voice memos with audio playback, attach high-resolution photo albums, and archive personal video logs.
- **Mood Intelligence & Life Correlator**: Track daily emotions, mood trends, and correlate life factors (sleep, routine, gratitude) with your emotional state.
- **Time Capsules & Letters to God**: Draft letters scheduled to unlock on future dates or preserve sacred reflections.

### 🗺️ Free World Map, Search, Routing & Navigation (New)
- **100% Free Vector Maps**: Integrated vector tile renderer via **MapLibre GL** with **OpenFreeMap** styles (`Liberty`, `Bright`, `Positron`, and `Dark`) — zero API keys and zero cost.
- **Diary Footsteps**: Pins every geotagged memory on an interactive world map. Tap any marker to view the diary entry written at that location.
- **Global Place Search**: Instant debounced autocomplete powered by the Komoot Photon OpenStreetMap engine.
- **Multi-Modal Routing**: Fast driving, walking, and cycling route calculation via OSRM with distance, duration, and ETA estimates.
- **Turn-by-Turn GPS Navigation**:
  - Live GPS tracking with heading-aligned compass camera.
  - Maneuver instruction banners with distance counters.
  - Automatic off-route deviation detection (>60m) and instantaneous rerouting.
  - Spoken voice guidance via Text-to-Speech (TTS) with one-tap mute.

### ☁️ Google Cloud Services Integration (New)
- **Google Sign-In**: Seamless one-tap authentication via Supabase OAuth with branded vintage-styled controls.
- **Google Calendar Sync**:
  - View Google Calendar events alongside diary entries in the calendar view.
  - Schedule diary reflections, reminders, and milestones directly to your primary Google Calendar.
- **Gmail Digest & Dispatcher**:
  - Automatically compose and send weekly diary digests, reflections, and PDF backups via the Gmail API.
- **Google People & Contacts API**:
  - Access contacts to tag friends and family in memories and circle of trust relationships.

### 🛡️ Security, Privacy & Heritage Vault
- **Bank Vault**: Biometric authentication (fingerprint/face recognition) and secure PIN protection.
- **Secret Compartment**: Stealth decoy vault mode for confidential entries with separate access credentials.
- **Heritage Collection**:
  - *Atmosphere Studio*: Customize vintage paper textures, ink colors, and candlelit ambiance.
  - *Wax Seal Carver*: Personalize custom digital wax seals to stamp confidential entries.
  - *Bookbinding Blueprint*: Choose leatherbound styles, stitching, and book spine embossing.
  - *Heirloom Inheritance Protocol*: Designate trusted emergency custodians for your memoirs.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Framework** | [Flutter](https://flutter.dev) (Dart 3.x, Flutter 3.47+) |
| **State Management** | [Flutter Riverpod](https://riverpod.dev) (v3 Notifiers & Providers) |
| **Routing** | [GoRouter](https://pub.dev/packages/go_router) |
| **Local Database** | [Drift](https://drift.simonbinder.eu) (SQLite offline-first) |
| **Cloud Backend** | [Supabase](https://supabase.com) (Auth, PostgreSQL, Realtime Storage) |
| **Maps & GIS** | MapLibre GL, OpenFreeMap, Komoot Photon, OSRM, Geolocator |
| **Voice & Speech** | Flutter TTS, Record, Just Audio |
| **Security** | Flutter Secure Storage, Local Auth (Biometrics) |

---

## 🚀 Getting Started

### 1. Prerequisites
- **Flutter SDK**: `>= 3.4.0 < 4.0.0`
- **Dart SDK**: `>= 3.4.0`
- **Android Studio** / **VS Code** with Flutter extensions
- Android device or emulator with Google Play Services (API 26+)

### 2. Clone and Install Dependencies
```bash
git clone https://github.com/your-username/dear_diary.git
cd dear_diary
flutter pub get
```

### 3. Environment Configuration
Create a `.env` file in the root of the project (this file is gitignored):

```env
SUPABASE_URL=https://your-project-ref.supabase.co
SUPABASE_ANON_KEY=your-supabase-anon-key

# Google OAuth Web Client ID
GOOGLE_WEB_CLIENT_ID=884365427073-bj67ckt2r3n8ei0n4n925klj1b12jnr5.apps.googleusercontent.com
```

### 4. Run Code Generation (Drift)
If modifying local database tables or schema:
```bash
dart run build_runner build --delete-conflicting-outputs
```

### 5. Launch the Application
```bash
flutter run
```

---

## 🧪 Testing & Verification

Run the comprehensive unit, widget, and routing test suite:

```bash
# Run all tests
flutter test

# Run specific feature tests
flutter test test/map_entities_test.dart
flutter test test/google_services_test.dart
flutter test test/routing_test.dart
flutter test test/auth_routing_test.dart

# Run static analysis
flutter analyze
```

---

## 📁 Project Architecture

```
lib/
├── core/
│   ├── config/          # Environment variables (Env)
│   ├── constants/       # App constants & limits
│   ├── errors/          # Failures & error handling
│   ├── routing/         # GoRouter definitions & RouteNames
│   ├── theme/           # Vintage typography, paper themes & colors
│   └── utils/           # Date formatters, UUIDs, month grid
├── data/
│   ├── local/           # Drift SQLite database, DAOs, and migrations
│   ├── remote/          # Supabase services & synchronization engine
│   └── repositories/    # Concrete repository implementations
├── domain/
│   ├── entities/        # Core business models (DiaryEntry, Mood, etc.)
│   │   └── maps/        # MapPlace, RouteResult, NavigationStep
│   └── repositories/    # Abstract repository contracts
├── presentation/
│   ├── providers/       # Riverpod providers & notifiers
│   ├── screens/         # Feature screens (Auth, Diary, Map, Vault, etc.)
│   └── widgets/         # Reusable vintage components & map controls
└── services/
    ├── google/          # Google Sign-In, Calendar, Gmail & People APIs
    ├── location/        # Footsteps tracking service
    ├── maps/            # Vector map config, Photon search, OSRM routing, TTS
    └── security/        # Biometrics, AppLock, Secure Storage
```

---

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
