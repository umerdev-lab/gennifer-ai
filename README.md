<div align="center">

<br>

```
 ██████╗ ███████╗███╗   ██╗███╗   ██╗██╗███████╗███████╗██████╗      █████╗ ██╗
██╔════╝ ██╔════╝████╗  ██║████╗  ██║██║██╔════╝██╔════╝██╔══██╗    ██╔══██╗██║
██║  ███╗█████╗  ██╔██╗ ██║██╔██╗ ██║██║█████╗  █████╗  ██████╔╝    ███████║██║
██║   ██║██╔══╝  ██║╚██╗██║██║╚██╗██║██║██╔══╝  ██╔══╝  ██╔══██╗    ██╔══██║██║
╚██████╔╝███████╗██║ ╚████║██║ ╚████║██║██║     ███████╗██║  ██║    ██║  ██║██║
 ╚═════╝ ╚══════╝╚═╝  ╚═══╝╚═╝  ╚═══╝╚═╝╚═╝     ╚══════╝╚═╝  ╚═╝    ╚═╝  ╚═╝╚═╝
```

### Your Personal AI. Your Digital Companion. Your Computer, Under Your Control.

<br>

*Gennifer AI is a futuristic personal desktop assistant — powered by Google Gemini — that understands your voice, remembers who you are, and interacts with your computer on your behalf.*

<br>

![Status](https://img.shields.io/badge/Status-Active%20Development-orange?style=for-the-badge&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)
![Electron](https://img.shields.io/badge/Built%20with-Electron-47848F?style=for-the-badge&logo=electron&logoColor=white)
![AI](https://img.shields.io/badge/AI-Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)
![License](https://img.shields.io/badge/License-TBD-lightgrey?style=for-the-badge)

<br>

</div>

---

<br>

## ◈ What is Gennifer AI?

Gennifer AI is a **personal desktop AI assistant** built as a native desktop application using Electron. It is designed to feel less like a traditional software tool and more like an intelligent digital presence — one that knows your name, remembers your context, responds to your voice in real time, and can take action on your computer.

The project draws inspiration from fictional AI interfaces like JARVIS: a calm, intelligent system running in the background, ready to assist whenever called upon. Unlike a simple chatbot that lives in a browser tab, Gennifer is a persistent desktop companion. It maintains a user profile, stores a knowledge base, manages multiple user profiles with face enrollment support, and connects to Google Gemini's live API for real-time voice and text conversations.

Gennifer is built for the kind of user who wants their computer to work *with* them — not just respond to typed queries.

<br>

---

<br>

## ◈ Core Capabilities

<br>

<table>
<tr>
<td width="50%" valign="top">

### 🎙️ Voice Interaction
Real-time two-way voice conversations powered by the **Gemini Live API**. Gennifer listens and responds with low latency, supporting a natural spoken dialogue rather than a command-response loop.

</td>
<td width="50%" valign="top">

### 💬 AI Conversation
Multi-turn text and voice chat backed by Google Gemini models including **Gemini 2.5 Flash**, **Gemini 2.5 Pro**, and newer preview models. Model selection is configurable per use case.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 👤 User Profiles & Identity
Gennifer maintains **named user profiles** with persistent identity data — full name, age, country, language preference, and a personal bio. Profiles are stored locally and loaded at session start.

</td>
<td width="50%" valign="top">

### 🔐 Face Enrollment
The system includes a **face enrollment and unlock mechanism**, storing face data per profile. Users can configure face-based authentication to lock and unlock the assistant.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🧠 Persistent Knowledge Base
Each profile carries a **knowledge base** that persists across sessions, allowing Gennifer to retain context about the user over time rather than starting fresh every conversation.

</td>
<td width="50%" valign="top">

### ⚙️ Agent Mode & Terminal Access
An internal agent configuration enables **developer mode** and **terminal access**, allowing Gennifer to execute system-level operations when permitted by the user.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔑 Bring Your Own API Key
Users connect their own **Google Gemini API keys**. The system auto-discovers all available models on the connected key and surfaces them for selection, including preview and experimental models.

</td>
<td width="50%" valign="top">

### ☁️ Cloud Sync Architecture
Gennifer includes a **sync client** designed to connect user data across devices when authenticated, with local-first storage as the default when offline or unauthenticated.

</td>
</tr>
</table>

<br>

### 🚧 Planned / Future Features

These capabilities are part of the roadmap and are **not yet fully implemented**:

| Feature | Description |
|---|---|
| 🖥️ Full Desktop Automation | Autonomous mouse/keyboard control to interact with any application on screen |
| 👁️ Screen Awareness | Real-time screen capture and visual understanding using Gemini's vision capabilities |
| 🌐 Web Search Integration | Live internet search with summarized results injected into conversation context |
| 🔔 Proactive Notifications | Gennifer initiates interactions based on schedule, reminders, or system events |
| 🎭 Animated AI Avatar | An expressive on-screen avatar that reacts emotionally to conversation context |
| 🔌 Plugin / Tool Ecosystem | A modular tool system allowing third-party integrations to be loaded as capabilities |
| 📱 Cross-Device Presence | Full cloud sync enabling a seamless experience across multiple machines |
| 🗣️ Custom Wake Word | Always-on voice detection with a personalized activation phrase |

<br>

---

<br>

## ◈ How It Works

```
┌─────────────────────────────────────────────────┐
│                   USER INPUT                    │
│          Voice (Microphone) / Text Chat         │
└──────────────────────┬──────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────┐
│               GENNIFER CORE                     │
│                                                 │
│   ┌─────────────────────────────────────────┐   │
│   │         User Profile & Identity         │   │
│   │    Name · Age · Language · Bio · Keys   │   │
│   └─────────────────────────────────────────┘   │
│                                                 │
│   ┌─────────────────────────────────────────┐   │
│   │         Knowledge Base (Persistent)     │   │
│   │      Long-term context across sessions  │   │
│   └─────────────────────────────────────────┘   │
│                                                 │
│   ┌─────────────────────────────────────────┐   │
│   │           Agent Configuration          │   │
│   │    Model selection · Terminal · Dev     │   │
│   └─────────────────────────────────────────┘   │
└──────────────────────┬──────────────────────────┘
                       │
          ┌────────────┴────────────┐
          ▼                         ▼
┌──────────────────┐     ┌──────────────────────┐
│  Gemini Live API │     │  Gemini Chat / Agent  │
│  (Voice / RT)    │     │  (Text / Tasks)       │
└────────┬─────────┘     └──────────┬────────────┘
         │                          │
         └─────────────┬────────────┘
                       ▼
┌─────────────────────────────────────────────────┐
│                  RESPONSE                       │
│          Voice Output / Text / Action           │
└─────────────────────────────────────────────────┘
```

<br>

---

<br>

## ◈ Technology Stack

| Layer | Technology |
|---|---|
| **Desktop Runtime** | [Electron](https://www.electronjs.org/) — cross-platform desktop shell |
| **AI / Language Model** | [Google Gemini](https://deepmind.google/technologies/gemini/) — Gemini 2.5 Flash · 2.5 Pro · 3.x series |
| **Voice / Real-Time** | Gemini Live API — low-latency bidirectional audio streaming |
| **Data Storage** | Local JSON — profiles, knowledge base, tokens, security events |
| **Authentication** | Website-based auth + device registration |
| **Sync** | Cloud sync client (local-first with remote capability) |
| **Geolocation** | Nominatim (OpenStreetMap) API |
| **Weather** | Open-Meteo API |

<br>

---

<br>

## ◈ Project Data Structure

Gennifer stores all user data in a dedicated local directory:

```
%USERPROFILE%\Documents\Gennifer Data\
│
├── installation.json          ← Installation ID, onboarding state, auth method
├── profiles.json              ← List of user profiles and active profile ID
├── device-id.json             ← Unique device identifier
├── unlock-face-enrollment.json← Face unlock configuration
│
└── Profiles\
    └── default\               ← Per-profile data directory
        ├── identity.json      ← Encrypted identity data
        ├── userProfile.json   ← Name, age, country, language, bio
        ├── knowledge-base.json← Persistent AI knowledge/memory (encrypted)
        ├── auth-tokens.json   ← Authentication session tokens
        ├── face-enrollment.json← Enrolled face data for this profile
        ├── security-events.json← Security and access log
        ├── whatsapp-command-queue.json
        └── Agents\
            └── agent-config.json  ← API keys, model selection, capabilities
```

The application itself runs as an **Electron desktop app** with two companion processes:

- `gennifer-ai` — the main application window
- `gennifer-ai-assistant` — the background assistant process

<br>

---

<br>

## ◈ Installation

### Requirements

| Requirement | Details |
|---|---|
| **Operating System** | Windows 10 / 11 (64-bit) |
| **Google Gemini API Key** | Required — [get one at Google AI Studio](https://aistudio.google.com/) |
| **Internet Connection** | Required for AI model access and voice streaming |

<br>

### Download & Install

Gennifer AI is distributed as a native Windows installer.

1. Download the latest installer from the [Releases](../../releases) page.
2. Run the installer — Gennifer will install to your user directory.
3. Launch **Gennifer AI** from the Start Menu or Desktop shortcut.

> The updater is located at `%LOCALAPPDATA%\gennifer-ai-updater\` and handles automatic updates.

<br>

### First-Time Setup

1. **Complete Onboarding** — Enter your name, age, country, and language preference.
2. **Connect a Gemini API Key** — Navigate to Settings → Agent Config and add your Google Gemini API key. Gennifer will auto-discover all available models on your key.
3. **Select Models** — Choose your preferred model for main chat and agent tasks (e.g. `gemini-2.5-flash` for fast responses, `gemini-2.5-pro` for deeper reasoning).
4. **Enable Voice** (optional) — Microphone access is required for Gemini Live voice interaction.
5. **Set Up Face Unlock** (optional) — Enroll your face via the profile security settings.

<br>

### API Key Configuration

Gennifer does **not** ship with API keys. You must provide your own:

| Key | Where to Get It | Used For |
|---|---|---|
| `Google Gemini API Key` | [Google AI Studio](https://aistudio.google.com/) | All AI features — chat, voice, agent |

> ⚠️ Never share your API key publicly. It is stored locally in your profile's `agent-config.json` in encrypted form.

<br>

---

<br>

## ◈ Running Gennifer AI

Once installed, launch from:

- **Start Menu** → Gennifer AI
- **Desktop shortcut** → Gennifer AI

The application starts two processes automatically:

```
Process 1: gennifer-ai (Main Window)
→ The primary UI — chat interface, profile management, settings

Process 2: gennifer-ai-assistant (Background)
→ The assistant process — handles background tasks, sync, and assistant presence
```

Both processes are managed automatically by the Electron shell. You do not need to start them manually.

<br>

---

<br>

## ◈ AI Interaction Flow

```
You
 │
 ├─── Speak (microphone)
 │         │
 │         ▼
 │    Gemini Live API
 │    (real-time audio stream)
 │         │
 │         ▼
 │    Gennifer processes speech
 │    + injects profile context
 │    + injects knowledge base
 │         │
 │         ▼
 │    Intent understood
 │         │
 │    ┌────┴─────────┐
 │    │              │
 │    ▼              ▼
 │  Reply         Agent Task
 │  (voice out)   (terminal / tool use)
 │
 └─── Type (text input)
           │
           ▼
      Gemini Chat API
      (multi-turn conversation)
           │
           ▼
      Context-aware response
      with profile + memory
```

<br>

---

<br>

## ◈ Security & Permissions

Gennifer AI is a personal assistant that operates with access to your system. Please review the following before use:

**Data Storage**
All user data is stored **locally** on your machine under `%USERPROFILE%\Documents\Gennifer Data\`. Sensitive fields such as identity data and knowledge base content are encrypted at rest.

**API Keys**
Your Gemini API key is stored in your local profile directory. Do not commit, share, or expose this directory. Gennifer does not transmit your API key to any server other than Google's official Gemini API endpoints.

**Terminal Access**
Agent mode includes optional terminal access. This capability allows Gennifer to run commands on your system. Enable it only if you understand the implications and trust the instructions you give the assistant.

**Face Enrollment**
Face data is stored locally per profile and is never uploaded to external servers.

**Cloud Sync**
The sync client only activates when you are signed in. In an unauthenticated state, no data leaves your machine.

**Best Practices**
- Never share your `Gennifer Data` directory publicly
- Review any terminal commands Gennifer proposes before execution
- Use profile locks for shared machines
- Keep your Gemini API key usage monitored via Google AI Studio

<br>

---

<br>

## ◈ Development

Gennifer AI is built on **Electron**, meaning the application shell is JavaScript/Node.js with a Chromium-based renderer.

### Working on the Project

```bash
# Clone the repository
git clone https://github.com/<your-username>/gennifer-ai.git
cd gennifer-ai

# Install dependencies
npm install

# Start in development mode
npm run dev
```

### Project Areas

| Area | Location | Notes |
|---|---|---|
| Main Process | `src/main/` or equivalent | Electron main process — system access, IPC |
| Renderer / UI | `src/renderer/` or equivalent | The visible interface — chat, settings, profiles |
| Agent Config | `Profiles/default/Agents/agent-config.json` | Runtime config — not source code |
| Profile Data | `Documents/Gennifer Data/` | User data — excluded from source control |

### Adding Capabilities

New tools and capabilities integrate through the agent configuration layer. To extend Gennifer:

1. Define the new tool/capability in the agent config schema
2. Implement the handler in the main process
3. Expose it to the renderer via IPC
4. Surface it in the UI settings panel

<br>

---

<br>

## ◈ Roadmap

```
COMPLETED
─────────────────────────────────────────────────────
[x] Electron desktop application shell
[x] User profile system (name, age, country, language)
[x] Multi-profile support with profile switching
[x] Face enrollment & face-based unlock
[x] Google Gemini API key integration
[x] Auto model discovery from connected API key
[x] Multi-model selection (chat model, agent model)
[x] Real-time voice via Gemini Live API
[x] Persistent knowledge base per profile
[x] Local-first encrypted data storage
[x] Developer / agent mode with terminal access
[x] Cloud sync architecture (client-side)
[x] Onboarding flow

IN PROGRESS / PLANNED
─────────────────────────────────────────────────────
[ ] Full desktop automation (mouse, keyboard control)
[ ] Screen capture and visual awareness
[ ] Live web search integration
[ ] Proactive reminders and scheduled interactions
[ ] Animated AI avatar with emotional states
[ ] Plugin / extension ecosystem
[ ] Full cross-device cloud sync
[ ] Custom wake word detection
[ ] WhatsApp / messaging integrations
[ ] macOS and Linux support
```

<br>

---

<br>

## ◈ Design Philosophy

Gennifer is designed around a single idea: **your computer should understand you**.

Most software makes you adapt to it — learning menus, commands, and workflows. Gennifer inverts that relationship. It learns your name, remembers your preferences, and speaks your language. It is built to feel less like a utility and more like a presence.

The interface is kept minimal by design. The assistant is the product, not the dashboard. Voice is a first-class input, not an afterthought. And the underlying AI — Google Gemini — is chosen for its multimodal capability and real-time streaming support, which makes the interaction feel immediate rather than mechanical.

Gennifer is named intentionally. Not "Assistant" or "Bot" — a name, because the project is built around the belief that the best AI interfaces feel like collaborators, not tools.

<br>

---

<br>

## ◈ Contributing

Contributions are welcome. Here's the standard process:

1. **Fork** the repository
2. **Create a branch** for your change
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** — keep them focused and well-scoped
4. **Test** your changes locally before submitting
5. **Commit** with a clear message
   ```bash
   git commit -m "feat: describe what this does"
   ```
6. **Push** to your fork
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Open a Pull Request** — describe what you changed and why

Please keep PRs focused on a single concern. Large, multi-purpose PRs are harder to review and slower to merge.

<br>

---

<br>

## ◈ License

> License information will be added in a future release.

<br>

---

<br>

## ◈ Author

**Umer**
Pakistan

*Built with curiosity, late nights, and a belief that personal AI should feel genuinely personal.*

<br>

---

<br>

<div align="center">

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**GENNIFER AI**

<sub>Building a more intelligent way to interact with your computer.</sub>

<br>

<sub>
Powered by Google Gemini &nbsp;·&nbsp; Built on Electron &nbsp;·&nbsp; Designed for humans
</sub>

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

</div>
