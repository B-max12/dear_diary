📖 Dear Diary

Your memories. Your thoughts. Your private space.

Dear Diary is a privacy-focused, AI-powered digital diary designed to turn everyday journaling into a meaningful personal experience.

It combines traditional journaling with AI conversations, intelligent diary search, rich media memories, privacy controls, biometric protection, reminders, reflection tools, and personal organization — while keeping privacy and user ownership at the center of the experience.

✨ Overview

Dear Diary is not just a notes application.

It is designed as a private digital space where users can write, remember, reflect, search, and talk.

Users can create diary entries containing text and rich media, organize their memories, revisit previous moments, and interact with an AI companion that can understand and work with their diary content.

Core Philosophy
             ┌─────────────────────┐
             │      YOUR LIFE      │
             └──────────┬──────────┘
                        │
                        ▼
              ┌─────────────────┐
              │   Dear Diary    │
              └────────┬────────┘
                       │
       ┌───────────────┼────────────────┐
       ▼               ▼                ▼
   📝 Journal       🧠 Reflect       🔐 Protect
       │               │                │
       ▼               ▼                ▼
   Memories        AI Companion     Privacy
       │               │                │
       └───────────────┼────────────────┘
                       ▼
              🌱 Personal Growth
🚀 Features
📝 Personal Journaling

Create personal diary entries with:

Rich text
Titles
Dates
Private thoughts
Personal reflections
Memories
Attachments
Searchable content
Entry metadata

Every entry is designed to feel like a page from a personal diary rather than a generic notes document.

🤖 AI Companion

Dear Diary includes an AI-powered companion designed specifically around the user's personal diary.

Instead of treating the AI as a generic chatbot, the system can work with the user's own diary context.

Two AI Modes
💬 Talk to AI

A conversational mode for talking naturally with the AI companion.

Examples:

"Talk to me."

"I'm feeling confused today."

"Help me think about something."

"What do you remember about my recent entries?"
🔎 Search My Diary

A separate mode focused on finding information from previous diary entries.

Examples:

"When did I write about my university?"

"Find my entries about friendship."

"What did I write last month?"

"Show me the entries where I mentioned Paris."

Keeping these two modes separate prevents normal conversation from being confused with diary retrieval.

🧠 AI Architecture
flowchart TD

    U[User] --> UI[Dear Diary UI]

    UI --> MODE{AI Mode}

    MODE -->|Talk to AI| CHAT[AI Conversation]
    MODE -->|Search Diary| SEARCH[Diary Search]

    CHAT --> CONTEXT[Context Manager]
    SEARCH --> RETRIEVAL[Diary Retrieval]

    RETRIEVAL --> DB[(Diary Database)]
    RETRIEVAL --> EMB[Embeddings / Semantic Search]

    CONTEXT --> MEMORY[Relevant Personal Context]

    MEMORY --> LLM[LLM Provider]
    RETRIEVAL --> LLM

    LLM --> RESPONSE[AI Response]
    RESPONSE --> UI
🔐 Privacy & Security

Privacy is one of the fundamental principles of Dear Diary.

Diary applications contain extremely personal information, therefore security cannot be treated as an optional feature.

Security Layers
                    ┌──────────────────────┐
                    │       USER           │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   App Authentication │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Biometric / App Lock │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Authorization / RLS  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Secure API Layer     │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Protected Database   │
                    └──────────────────────┘
Security Goals
User-specific data isolation
Database-level authorization
Secure authentication
Biometric protection
Protected media access
Secure API communication
No client-side exposure of privileged secrets
Environment-based configuration
Production-safe API key management
Automatic lock when leaving protected areas

Important: API secrets must never be shipped as publicly accessible frontend credentials. Production deployments should use a secure server-side/API gateway architecture wherever privileged keys are required.

🔑 Authentication & App Lock

Dear Diary can provide multiple layers of protection.

App Launch
    │
    ▼
Authentication
    │
    ▼
Biometric Enabled?
   / \
 Yes  No
 │     │
 ▼     ▼
Fingerprint   App
 / Face       Access
 │
 ▼
Today / Home

The lock system is designed to avoid interrupting legitimate workflows such as:

Selecting a photo
Selecting a video
Recording audio
Opening a system file picker
Returning from media selection

The application should lock when the user actually leaves or backgrounds the protected application rather than treating every system UI transition as an app exit.

📸 Rich Memories

Diary entries can contain more than text.

Supported content may include:

🖼️ Images
🎙️ Audio
🎥 Video
📝 Text
📎 Attachments

Example:

┌─────────────────────────────────────┐
│              22 September            │
│                                     │
│  A quiet evening...                 │
│                                     │
│  ┌───────────┐  ┌───────────┐       │
│  │   Photo   │  │   Photo   │       │
│  └───────────┘  └───────────┘       │
│                                     │
│  🎙️ Voice Memory                    │
│                                     │
│  "I want to remember this day..."   │
└─────────────────────────────────────┘
📅 Reminders

Dear Diary can provide offline-friendly diary reminders.

Users can:

Create reminders
Receive notifications
Mark reminders as Done
Snooze reminders
Snooze for 10 minutes
Continue using the diary without an internet connection where platform capabilities allow
Reminder Flow
flowchart LR

    CREATE[Create Reminder] --> STORE[Local Storage]
    STORE --> SCHEDULER[Notification Scheduler]
    SCHEDULER --> NOTIFY[Notification]
    NOTIFY --> ACTION{User Action}

    ACTION -->|Done| COMPLETE[Completed]
    ACTION -->|Snooze| SNOOZE[10 Minute Snooze]
    SNOOZE --> SCHEDULER
🙏 Letter to God

Dear Diary also provides a dedicated reflective writing space for personal conversations with God.

Possible categories include:

🙏 Prayer
🌙 Wish
✨ Dream
💔 Loss
🌱 Hope
💭 Just a Talk
❓ Question
🤍 Confession
😔 Guilt
🔁 Bad Habit
💌 Answer

The purpose is not to turn these entries into ordinary notes, but to preserve them as a separate reflective part of the user's diary.

🧭 Application Architecture
flowchart TB

    CLIENT[Client Application]

    CLIENT --> AUTH[Authentication]
    CLIENT --> DIARY[Diary Module]
    CLIENT --> AI[AI Companion]
    CLIENT --> MEDIA[Media Manager]
    CLIENT --> LOCK[Security / App Lock]
    CLIENT --> REMINDERS[Reminder Engine]

    DIARY --> API[Application API]

    AI --> AIAPI[AI Gateway]

    MEDIA --> STORAGE[(Object Storage)]

    API --> DATABASE[(PostgreSQL)]

    AIAPI --> PROVIDER[LLM Provider]

    DATABASE --> RLS[Row Level Security]

    RLS --> USERDATA[User-Owned Data]
🏗️ High-Level System Design
                         ┌─────────────────────┐
                         │     Mobile / Web    │
                         │      Frontend       │
                         └──────────┬──────────┘
                                    │
                   ┌────────────────┼────────────────┐
                   │                │                │
                   ▼                ▼                ▼
             Authentication      Diary API       AI Gateway
                   │                │                │
                   │                ▼                ▼
                   │           PostgreSQL       LLM Provider
                   │                │
                   │                ▼
                   │          Storage / Media
                   │
                   ▼
             User Session
🗄️ Data Model

A simplified database design:

erDiagram

    USERS ||--o{ DIARY_ENTRIES : creates
    USERS ||--o{ MEDIA : owns
    USERS ||--o{ REMINDERS : creates
    USERS ||--o{ AI_CONVERSATIONS : has
    DIARY_ENTRIES ||--o{ MEDIA : contains
    AI_CONVERSATIONS ||--o{ AI_MESSAGES : contains

    USERS {
        uuid id PK
        string email
        timestamp created_at
    }

    DIARY_ENTRIES {
        uuid id PK
        uuid user_id FK
        string title
        text content
        timestamp entry_date
        timestamp created_at
        timestamp updated_at
    }

    MEDIA {
        uuid id PK
        uuid user_id FK
        uuid diary_entry_id FK
        string type
        string storage_path
        timestamp created_at
    }

    REMINDERS {
        uuid id PK
        uuid user_id FK
        string title
        timestamp scheduled_at
        boolean completed
    }

    AI_CONVERSATIONS {
        uuid id PK
        uuid user_id FK
        string mode
        timestamp created_at
    }

    AI_MESSAGES {
        uuid id PK
        uuid conversation_id FK
        string role
        text content
        timestamp created_at
    }
🔎 Intelligent Diary Search

Diary search can operate at multiple levels.

Traditional Search
Query
  │
  ▼
Keyword Search
  │
  ▼
Database
  │
  ▼
Matching Entries
Semantic Search
User Question
      │
      ▼
Embedding
      │
      ▼
Vector Search
      │
      ▼
Relevant Diary Entries
      │
      ▼
Context Builder
      │
      ▼
AI Response

This allows users to search by meaning, not only exact words.

For example:

"When was I feeling lonely?"

can potentially find entries that never contain the exact word lonely.

🧠 AI Context Pipeline
sequenceDiagram

    participant U as User
    participant A as App
    participant R as Retrieval
    participant C as Context Builder
    participant L as LLM

    U->>A: Ask a question
    A->>R: Search relevant diary entries
    R-->>A: Relevant memories
    A->>C: Build context
    C->>L: Context + User Query
    L-->>A: Response
    A-->>U: AI Response
⚡ Performance Principles

Dear Diary is designed with performance in mind.

Goals
Fast initial rendering
Lazy loading of media
Optimized image handling
Pagination for large diary collections
Efficient database queries
Cached frequently accessed data
Background synchronization
Minimal unnecessary network requests
Streaming AI responses where supported
Media Loading
Entry Opened
     │
     ▼
Load Text Immediately
     │
     ├───────────────┐
     ▼               ▼
Load Thumbnails   Load Metadata
     │
     ▼
User Opens Media
     │
     ▼
Load Full Resolution
📂 Suggested Project Structure
dear-diary/
│
├── app/
│   ├── components/
│   ├── screens/
│   ├── navigation/
│   ├── hooks/
│   └── services/
│
├── features/
│   ├── diary/
│   ├── ai/
│   ├── authentication/
│   ├── media/
│   ├── reminders/
│   ├── profile/
│   └── settings/
│
├── lib/
│   ├── database/
│   ├── storage/
│   ├── security/
│   ├── ai/
│   └── utilities/
│
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
│
├── backend/
│   ├── api/
│   ├── middleware/
│   ├── services/
│   └── ai/
│
├── database/
│   ├── migrations/
│   ├── functions/
│   └── policies/
│
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
│
├── .env.example
├── package.json
└── README.md

Adjust this structure according to the actual framework used by the project.

🛠️ Technology Stack

The project is designed to work with a modern application stack.

Layer	Technology
Frontend	Modern React / React Native / compatible UI
Backend	API / Serverless architecture
Database	PostgreSQL
Authentication	Secure authentication provider
Storage	Object storage
AI	LLM API
Search	Full-text + semantic search
Security	RLS + authentication + biometric protection
Notifications	Native/local notification system
Version Control	Git + GitHub
⚙️ Environment Configuration

Create a local environment file:

cp .env.example .env

Example:

DATABASE_URL=
SUPABASE_URL=
SUPABASE_ANON_KEY=

AI_API_URL=
AI_API_KEY=

STORAGE_BUCKET=
⚠️ Never commit secrets

Do not commit:

.env
.env.local
.env.production
private keys
service-role keys
database passwords
AI provider secret keys

Use:

.env.example

for documenting required configuration.

🚀 Installation
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/dear-diary.git
cd dear-diary
2. Install dependencies
npm install
3. Configure environment variables
cp .env.example .env

Add the required credentials.

4. Start development server
npm run dev
🧪 Testing

Run unit tests:

npm test

Run linting:

npm run lint

Run type checking:

npm run typecheck

Run production build:

npm run build

For end-to-end testing:

npm run test:e2e
🔒 Security Checklist

Before deploying to production:

Authentication configured

Database RLS enabled

Storage policies configured

User data isolation verified

API keys removed from frontend

Production secrets stored securely

.env excluded from Git

Debug logs removed

Error messages sanitized

HTTPS enabled

Media access protected

Session expiration configured

Biometric lock tested

Background locking tested

File-picker workflow tested

Database backups configured

Rate limiting configured

AI request abuse protection configured

🧪 Critical Security Test Cases
Authentication
Login
  ↓
Authenticated
  ↓
Access own data
  ↓
Logout
  ↓
Data inaccessible
Cross-user access
User A
  │
  ├── Entry A ✓
  │
  └── Entry B ✗
       ↑
    User B's data
App Lock
App Open
   ↓
Unlock
   ↓
Use App
   ↓
Background App
   ↓
Lock
   ↓
Return
   ↓
Biometric Required
Media Picker
Diary Entry
     ↓
Open Picker
     ↓
Select Image
     ↓
Return to App
     ↓
Upload
     ↓
Save Entry

The lock system should not incorrectly treat the temporary system picker as the user leaving the application.

📊 Development Architecture
flowchart TD

    A[UI Layer] --> B[Feature Layer]

    B --> C[Application Services]

    C --> D[Repository Layer]

    D --> E[(Database)]

    C --> F[Storage]

    C --> G[AI Gateway]

    G --> H[LLM Provider]

    B --> I[Local Cache]

    I --> J[Offline State]

    J --> C

This separation helps keep UI code independent from database, storage, and AI-provider implementations.

🔌 AI Provider Abstraction

The AI layer should ideally be provider-independent.

                AI Service
                    │
          ┌─────────┴─────────┐
          │                   │
      Provider A          Provider B
          │                   │
          └─────────┬─────────┘
                    ▼
             Unified Interface
                    │
                    ▼
              Dear Diary

Example abstraction:

interface AIProvider {
  chat(messages: Message[]): Promise<AIResponse>;

  generateReflection(
    context: DiaryContext
  ): Promise<AIResponse>;

  searchRelevantEntries(
    query: string
  ): Promise<DiaryEntry[]>;
}

This allows the application to change AI providers without rewriting the entire application.

🧩 Feature Modules
Module	Responsibility
Diary	Create, edit and manage entries
AI Companion	Conversations and reflections
Diary Search	Search personal memories
Media	Images, audio and video
Authentication	User sessions
App Lock	Biometric/privacy protection
Reminders	Diary notifications
Letter to God	Reflective writing
Profile	User information
Settings	Application configuration
Developer Mode	Advanced diagnostics
Backup	Data protection and recovery
📱 User Experience

Dear Diary aims to maintain a calm, personal interface rather than feeling like an enterprise dashboard.

UX Principles
Minimal visual noise
Clear navigation
Fast interactions
Personal typography
Meaningful animations
Accessible controls
Privacy-first interactions
No unnecessary complexity

The interface should feel like opening a personal journal, not opening a database.

🌙 Design Direction

The visual identity can combine:

Modern
   +
Vintage
   +
Poetic
   +
Minimal
   +
Personal

Suggested visual language:

Soft typography
Journal-inspired layouts
Subtle transitions
Paper/card metaphors
Elegant spacing
Dark mode
Warm personal atmosphere
🧑‍💻 Developer Mode

Developer Mode is intended for debugging and advanced diagnostics.

It should be:

Explicitly opt-in
Clearly explained
Disabled by default
Separate from normal user settings

Potential diagnostics:

App Version
Database Status
Storage Status
AI Provider Status
Network Status
Sync Status
Cache Status
Debug Logs

Developer Mode must never silently expose sensitive diary content or credentials.

🛣️ Roadmap
Phase 1 — Foundation

Diary entries

Authentication

Basic AI companion

Rich media

Profile

App lock

Phase 2 — Intelligence

Semantic diary search

Better context retrieval

AI reflections

Entry summarization

Personal memory system

Smart tagging

Phase 3 — Privacy

Stronger local encryption

Secure media handling

Advanced session controls

Improved secret management

Privacy audit

Security testing

Phase 4 — Personalization

Custom AI companion personality

Custom themes

Writing statistics

Mood/reflection analytics

Personal insights

Memory timeline

Phase 5 — Advanced Platform

End-to-end encrypted synchronization

Secure backup

Cross-device synchronization

Offline-first architecture

AI model switching

Local AI support

Plugin architecture

📈 Future AI Capabilities

Potential future capabilities include:

                    ┌───────────────┐
                    │  AI Companion │
                    └───────┬───────┘
                            │
       ┌────────────┬───────┼────────┬────────────┐
       ▼            ▼       ▼        ▼            ▼
   Search        Reflect  Summarize  Recall     Organize
       │            │       │        │            │
       └────────────┴───────┼────────┴────────────┘
                            ▼
                    Personal Insight

The goal is not simply to make AI generate text.

The goal is to make AI useful around the user's own memories and writing.

🌐 Open Source

Dear Diary is intended to encourage experimentation around:

Personal AI
Privacy-first applications
Digital journaling
AI memory systems
Semantic search
Personal knowledge management
Secure media storage

Contributions, suggestions, bug reports and architectural discussions are welcome.

🤝 Contributing
Fork the repository
Create a feature branch
git checkout -b feature/my-new-feature
Make your changes
Run tests
npm test
Commit your changes
git commit -m "feat: add new diary feature"
Push the branch
git push origin feature/my-new-feature
Open a Pull Request
🐛 Bug Reports

When reporting a bug, please include:

Environment:
Device:
OS:
App Version:

Expected behavior:
Actual behavior:

Steps to reproduce:
1.
2.
3.

Screenshots / logs:

Never include:

Passwords
API keys
Authentication tokens
Private diary content
Personal documents
Database credentials
💡 Feature Requests

Before opening a feature request, consider:

What problem does it solve?
Who benefits from it?
Does it improve the diary experience?
Does it introduce privacy concerns?
Can it work offline?
Does it increase unnecessary complexity?
📜 License

Choose and add an appropriate open-source license before publishing the repository.

For example:

MIT License

or another license depending on the project's intended usage and distribution model.

❤️ Philosophy

A diary remembers what you write.
Dear Diary is built to help you understand why you wrote it.

Technology should not replace personal reflection.

It should create a safer and more meaningful space for it.

Dear Diary is built around a simple idea:

Write.
Remember.
Reflect.
Understand.
Grow.
⭐ Support the Project

If you find Dear Diary interesting:

⭐ Star the repository
🐛 Report bugs
💡 Suggest features
🔧 Contribute code
📖 Improve documentation
🗣️ Share feedback

📌 Project Status

Development Status: Active Development 🚧

Dear Diary is continuously evolving. Features, architecture, APIs and UI may change as development progresses.

👨‍💻 Author

Awab ur Rehman

Built with curiosity, code, and a love for writing.

<p align="center">

📖 Dear Diary

Your memories. Your thoughts. Your private space.

</p>
