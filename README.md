# Dear Diary — Expanded Feature Atlas (v1.3.1)

> A private, offline-first vintage journal and personal memory companion.

## Product description

Dear Diary combines expressive writing, memory archiving, visual reflection, map-based storytelling, privacy tools, and optional cloud services in a vintage-inspired Flutter experience. The product is designed to help people capture everyday moments and preserve a lasting personal record.

## Feature directory — one-line names

1. Today’s Dashboard
2. Rich Diary Editor
3. Lifetime Stamping System
4. Interactive Map Picker
5. Entry Library & Search
6. Category & Mood Manager
7. Archival Timeline
8. Single-Page Statistics
9. Mood Intelligence
10. Emotion Arc & Resilience
11. Life Correlator
12. Sunday Summary
13. Time Mirror
14. World Map & Footsteps
15. Global Location Search
16. Multi-Modal Routing Engine
17. Turn-by-Turn GPS Navigation
18. Spoken Voice Guidance (TTS)
19. Google Sign-In
20. Google Calendar Sync
21. Gmail Digest Dispatcher
22. Cloud Supabase Sync
23. Voice Journal
24. Photo Album
25. Video Library
26. Biometric App Lock
27. Wax Seal Workshop
28. E2EE Cloud Backup
29. Gratitude Jar
30. Time Capsules
31. Letters to God
32. Dream Journal
33. Circle of Trust (@Mentions)
34. Routine & Habit Tracker
35. Reminders & Smart Alarms
36. AUR LABs Ecosystem

## Detailed features

### 🖋️ Core Journaling & Writing

#### 1. Today’s Dashboard
Daily overview featuring daily quote inspiration, mood check-in, recent memories, and prompt suggestions.

#### 2. Rich Diary Editor
WYSIWYG rich text editor with fountain pen ink styles, vintage paper parchment textures, and formatting.

#### 3. Lifetime Stamping System
Permanently stamp entries with a wax seal badge at the bottom of the page, rendering them permanently read-only.

#### 4. Interactive Map Picker
Tap the toolbar pin to open an interactive full-screen map, search cities or drop pins, and save coordinates.

#### 5. Entry Library & Search
Full-text indexed search across all past entries with filtering by category, date, mood, and tag.

#### 6. Category & Mood Manager
Color-coded organization system for Personal, Travel, Work, Dreams, Spiritual, and custom notebook sections.

#### 7. Archival Timeline
Continuous chronological stream of entries rendered like a vintage chronicle scroll through your life's chapters.

### 📊 Insights & Single-Page Dashboard

#### 8. Single-Page Statistics
Viewport-fitted, non-scrollable dashboard showing total entries, streaks, words, category breakdown, and mood distribution.

#### 9. Mood Intelligence
Deep psychological breakdown of your emotional patterns, valence, arousal, and dominant mood frequencies.

#### 10. Emotion Arc & Resilience
Visual wave-chart showing your emotional trajectory and sentiment shifts across weeks and months.

#### 11. Life Correlator
Cross-correlates external habits (sleep, exercise, routine, spiritual practice) with your happiness index.

#### 12. Sunday Summary
Automated weekly Sunday retrospective synthesizing your triumphs, struggles, and personal growth lessons.

#### 13. Time Mirror
Reflective tool showing what you were thinking, feeling, and journaling exactly 1 month, 1 year, or 5 years ago.

### 🗺️ World Maps, GIS & Navigation (Free & Open Source)

#### 14. World Map & Footsteps
Full-screen vector world map rendering all your geotagged memories as interactive pins with OpenFreeMap styles.

#### 15. Global Location Search
High-speed debounced place and landmark autocomplete powered by Komoot's Photon search engine.

#### 16. Multi-Modal Routing Engine
OSRM routing calculating turn-by-turn routes for Driving (Car), Walking (Pedestrian), and Cycling (Bicycle).

#### 17. Turn-by-Turn GPS Navigation
Live turn-by-turn guidance screen featuring real-time speedometer, heading-aligned 3D compass camera, and ETA countdown.

#### 18. Spoken Voice Guidance (TTS)
Text-To-Speech audio announcements ("In 200 meters, turn left") with anti-spam cooldown and one-tap mute.

### ☁️ Google Cloud & Supabase Integration

#### 19. Google Sign-In
One-tap native OAuth login and registration exchanging Google credentials with Supabase Auth.

#### 20. Google Calendar Sync
Two-way calendar integration displaying your Google events directly on the diary's calendar view.

#### 21. Gmail Digest Dispatcher
Automatically draft and email weekly diary highlights, gratitude summaries, and PDF exports via the Gmail API.

#### 22. Cloud Supabase Sync
Offline-first synchronization engine with PostgreSQL triggers enforcing lifetime immutability on stamped records.

### 🎙️ Multi-Modal Media Archiving

#### 23. Voice Journal
Dedicated audio recorder for spoken stream-of-consciousness thoughts with live waveform and playback scrubbers.

#### 24. Photo Album
Pure Dart image compression engine creating thumbnail grids and full-screen lightbox galleries.

#### 25. Video Library
Video diary recorder and player to capture moving memories and milestone moments.

### 🛡️ Security, Privacy & Crafts

#### 26. Biometric App Lock
Biometric lock (fingerprint/face recognition) and master PIN lock protecting the application on launch.

#### 27. Wax Seal Workshop
Interactive digital wax seal crafter that lets you design personalized sigils and sheen finishes.

#### 28. E2EE Cloud Backup
Client-side AES-GCM-256 backup snapshots with 12-word BIP-39 mnemonic phrase recovery.

### ⏰ Life Routine, Spirit & Legacy

#### 29. Gratitude Jar
Transparent glass mason jar with cork-engraved title to drop and view origami scrolls of gratitude.

#### 30. Time Capsules
Sealed digital capsules that remain locked until a designated future anniversary, birthday, or graduation date.

#### 31. Letters to God
A sacred sanctuary for personal prayers with optional lifetime wax stamping.

#### 32. Dream Journal
Specialized morning log for recording dreams, sleep quality, recurring symbols, and lucid insights.

#### 33. Circle of Trust (@Mentions)
Personal directory documenting key relationships, birthdays, milestones, and memorable conversations.

#### 34. Routine & Habit Tracker
Daily checklist and rhythm keeper to cultivate mindful morning and evening habits.

#### 35. Reminders & Smart Alarms
Exact notifications prompting you to write, breathe, and reflect at your chosen hours.

#### 36. AUR LABs Ecosystem
Official portal link to download and explore companion apps from [AUR LABs]\(https\://aurlabs.online/).

## Interactive graphs and exploration

Open **Dear_Diary_Interactive_Product_Atlas.html** for searchable feature cards, category filters, interactive feature distribution charts, and a copyable feature index. Charts summarize documented feature counts, not actual user activity.

## Technology architecture

Flutter / Dart → Riverpod & GoRouter → repositories → Drift SQLite ↔ Supabase. MapLibre, OpenFreeMap, Photon, and OSRM provide mapping and routing services.

## Implementation caveat

This documentation reflects the supplied project description; individual capabilities, integrations, security guarantees, and deployment readiness have not been independently verified.
