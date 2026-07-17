<p align="center">
  <img src="docs/banner.png" alt="IAMX — AI Digital Humans for Unreal Engine" width="100%">
</p>

<h1 align="center">Bring your characters to life.</h1>

<p align="center">
  <b>IAMX turns any MetaHuman into a living, thinking digital human</b> — one that hears you, looks you in the eye,<br>
  answers in real time with perfectly synced lips, remembers you tomorrow, and can actually <i>do</i> things.
</p>

<p align="center">
  <a href="https://iamx.live"><img src="https://img.shields.io/badge/🌐_website-iamx.live-6d8bff?style=for-the-badge" alt="Website"></a>
  <a href="../../releases"><img src="https://img.shields.io/badge/⬇_download-v1_alpha-a468ff?style=for-the-badge" alt="Download"></a>
  <a href="../../issues"><img src="https://img.shields.io/badge/💬_feedback-wanted!-2ea043?style=for-the-badge" alt="Feedback"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Unreal_Engine-5.3_·_5.4_·_5.5_·_5.6_·_5.7_·_5.8-313131?logo=unrealengine" alt="UE versions">
  <img src="https://img.shields.io/badge/price-free-2ea043" alt="Free">
  <img src="https://img.shields.io/badge/platform-Win64-blue" alt="Win64">
</p>

---

> ### ⚠️ v1 **ALPHA**
> This is the first public release of IAMX. It works — we use it in production kiosks and live streams — but you *will* find rough edges.
> **Your feedback genuinely shapes this product.** Every bug report and feature request gets read: [open an issue](../../issues/new/choose) — it matters more than you think. 💜

---

## ✨ What you get

| | Feature | What it means |
|---|---------|---------------|
| 🗣️ | **Real-time voice conversation** | Two-way, streamed, interruptible (barge-in). Speak — it answers in seconds, in 30+ languages. |
| 👄 | **Real-time lip sync** | The character's mouth and full facial performance follow every word — on MetaHumans or your own custom rig. |
| 👁️ | **Eye & head tracking** | The character finds your camera and holds eye contact while you talk, like a person would. |
| 🧠 | **Your choice of AI brain** | GPT, Claude, Gemini (including Gemini Live realtime) or local Ollama — swappable per character from the panel. |
| 📷 | **Camera vision** | The character sees through a camera and reacts to what's in front of it. |
| 🙋 | **Memory that persists** | Recognizes returning people, summarizes past sessions, greets visitors by name — across days, not turns. |
| 📚 | **Knowledge base (RAG)** | Upload PDF / TXT / CSV — your character answers from *your* documents, not the open internet. |
| 🎭 | **Emotion engine** | An 8-dimensional emotional core drives facial expression, voice tone and gestures. Mood shifts as the conversation does. |
| ⚡ | **Actions** | Function calling into your own APIs — bookings, lookups, e-mail, calendar, messaging. The character *does*, not just says. |
| 🎮 | **Interaction modes** | Push-to-talk, voice-activated, wake word, or proximity — walk up to an NPC and just start talking; walk away and it stops listening. |
| 👥 | **Multi-NPC scenes** | Several characters in one level, each with its own personality; only the one you're near answers. NPC-to-NPC conversations too. |
| 📖 | **Scenario studio** | A no-code visual graph editor for goals, decisions and branching dialogue. |
| 💬 | **Built-in chat UI** | Optional on-screen chat panel with mic button, live transcription and streamed replies. |
| 🖥️ | **Every surface** | The same character runs as a game NPC, a 24/7 kiosk, a one-line web embed, or a cloud-streamed MetaHuman. |

Everything is configured live from the **[IAMX panel](https://iamx.live)** — personality, voice, AI model, features. No rebuilds, no redeploys: save in the panel, see it in the next reply.

> 🧩 **How it works:** the plugin is a lightweight client. All AI runs in the IAMX cloud and streams back to Unreal — your project stays lean, your machine stays cool, and every character update ships server-side without touching your build.

---

## 🚀 Installation

### 1 — Get the plugin

Download the ZIP matching your engine version from **[Releases](../../releases)**:

| Engine | Package |
|--------|---------|
| UE 5.3 | `IAMX_UE5_3_Win64.zip` |
| UE 5.4 | `IAMX_UE5_4_Win64.zip` |
| UE 5.5 | `IAMX_UE5_5_Win64.zip` |
| UE 5.6 | `IAMX_UE5_6_Win64.zip` |
| UE 5.7 | `IAMX_UE5_7_Win64.zip` |
| UE 5.8 | `IAMX_UE5_8_Win64.zip` |

Extract the `IAMX` folder into your project's `Plugins/` directory (create it if it doesn't exist):

```
YourProject/
└── Plugins/
    └── IAMX/
        ├── IAMX.uplugin
        ├── Binaries/      ← prebuilt, ready to run
        └── Source/
```

Open the project — that's it. **The packages ship prebuilt Win64 binaries, so no compiler or Visual Studio is needed, and Blueprint-only projects work out of the box.** (Full source is included too — C++ projects can rebuild or step through it freely.) Also available on **Fab**.

> ⚠️ The ZIP must match your engine version exactly — a 5.3 package won't load in 5.4.

### 2 — Create your character (2 minutes)

1. Sign up free at **[iamx.live](https://iamx.live)**.
2. Create a character: personality, voice, language, AI model, features.
3. Copy the character's connection ID from the panel.

### 3 — Wire up your MetaHuman

1. Drop a MetaHuman into your level.
2. Select it → **Add Component → IAMX**.
3. Paste your character's connection ID into the IAMX component.

### 4 — Add the animation nodes

The plugin ships three AnimGraph nodes (search for **"IAMX"** in any AnimGraph's right-click menu):

**Face Animation Blueprint** (e.g. `Face_AnimBP`) — add **two** nodes into the AnimGraph, chained before the Output Pose:

```
[Input / existing pose] → [IAMX Lip Sync] → [IAMX Eye Look At] → [Output Pose]
```

- **IAMX Lip Sync** — applies the streamed facial controls (mouth, jaw, expressions) on top of the incoming pose.
- **IAMX Eye Look At** — makes the eyes find and track the player's camera during conversation.

**Body Animation Blueprint** (the MetaHuman's body AnimBP) — add **one** node the same way:

```
[Input / existing pose] → [IAMX Head Look At] → [Output Pose]
```

- **IAMX Head Look At** — turns the head (with natural limits and smoothing) toward the player while talking.

> 💡 Both edits are non-destructive: the IAMX nodes blend on top of whatever animation is already playing (idle, talk gestures, your own state machines).

### 5 — Press Play

Press **T** (default, configurable) and talk. Or enable **voice-activated** / **proximity** mode on the component and just walk up to your character.

---

## 🎛️ Interaction modes

| Mode | Behavior |
|------|----------|
| **Push-to-talk** | Hold/press a key to speak (default `T`). |
| **Voice-activated** | Always listening; detects when you start and stop speaking. |
| **Wake word** | Sleeps until it hears its name ("Hey Alara…"). |
| **Proximity** | Add a radius — the NPC only listens to the player standing near it. Perfect for multi-NPC levels. |

## 📋 Requirements

- Unreal Engine **5.3 – 5.8** (Win64) — Blueprint-only projects supported (binaries are prebuilt)
- A free **[iamx.live](https://iamx.live)** account
- A microphone

## 🐞 Known alpha limitations

- Win64 only (other platforms on the roadmap)
- MetaHuman rigs are first-class; custom rigs work via blend-shape mapping but need manual setup
- Documentation is still growing — when in doubt, [ask](../../issues)

---

## 💬 Feedback — seriously, we want it

This is an alpha. The fastest way to get a feature or a fix is to tell us:

- 🐛 **[Report a bug](../../issues/new?template=bug_report.yml)** — engine version + logs = fixed fast
- 💡 **[Request a feature](../../issues/new?template=feature_request.yml)** — tell us what you're building
- ⭐ **Star the repo** if this is useful — it genuinely helps others find it

## 📄 License

Free to use, including commercially, with the IAMX service — see [LICENSE](LICENSE.md).

<p align="center">
  <sub>Built with obsession by <a href="https://iamx.live">IAMX Interactive</a> · <a href="https://iamx.live">iamx.live</a></sub>
</p>
