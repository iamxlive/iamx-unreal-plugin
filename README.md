<p align="center">
  <img src="docs/banner.png" alt="IAMX — AI Digital Humans for Unreal Engine" width="100%">
</p>

<h1 align="center">Bring your characters to life.</h1>

<p align="center">
  <b>IAMX turns any MetaHuman into a living, thinking digital human</b> — one that hears you, looks you in the eye,<br>
  answers in real time with perfectly synced lips, remembers you tomorrow, and can actually <i>do</i> things.
</p>

<p align="center">
  <a href="https://iamx.live"><img src="https://img.shields.io/badge/▶_try_the_live_demo-iamx.live-6d8bff?style=for-the-badge" alt="Live demo"></a>
  <a href="../../releases"><img src="https://img.shields.io/badge/⬇_download-v1_alpha-a468ff?style=for-the-badge" alt="Download"></a>
  <a href="../../issues"><img src="https://img.shields.io/badge/💬_feedback-wanted!-2ea043?style=for-the-badge" alt="Feedback"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Unreal_Engine-5.3_·_5.4_·_5.5_·_5.6_·_5.7_·_5.8-313131?logo=unrealengine" alt="UE versions">
  <img src="https://img.shields.io/badge/price-free-2ea043" alt="Free">
  <img src="https://img.shields.io/badge/platform-Win64-blue" alt="Win64">
  <a href="https://iamx.live/forum"><img src="https://img.shields.io/badge/community-forum-6d8bff" alt="Forum"></a>
  <a href="https://iamx.live/blog"><img src="https://img.shields.io/badge/news-blog-a468ff" alt="Blog"></a>
</p>

---

> ### ⚠️ v1 **ALPHA**
> This is the first public release of IAMX. It works — we run it in production kiosks and live streams — but you *will* find rough edges.
> **Your feedback genuinely shapes this product.** Every bug report and feature request gets read: [open an issue](../../issues/new/choose) or post on the [forum](https://iamx.live/forum) — it matters more than you think. 💜

---

<p align="center">
  <img src="docs/hero-avatar.jpg" alt="IAMX MetaHuman digital human" width="72%">
</p>

## ✨ What you get

| | Feature | What it means |
|---|---------|---------------|
| 🗣️ | **Real-time voice conversation** | Two-way, streamed, interruptible (barge-in). Speak — it answers in seconds, in 30+ languages. |
| 👄 | **Real-time lip sync** | The character's mouth and full facial performance follow every word — on MetaHumans or your own custom rig. |
| 👁️ | **Eye & head tracking** | The character finds your camera and holds eye contact while you talk, like a person would. |
| 🧠 | **Your choice of AI brain** | GPT, Claude, Gemini (including Gemini Live realtime) or local Ollama — swappable per character from the panel. |
| 📷 | **Camera vision** | The character sees through a camera and reacts to what's in front of it. |
| 🎭 | **Emotion engine** | An 8-dimensional emotional core drives face, voice tone and gestures. |
| 📖 | **Scenario Studio** | No-code visual graph editor for goals, decisions and branching dialogue. |
| 📚 | **Knowledge base (RAG)** | Your character answers from *your* documents, not the open internet. |
| 🙋 | **Long-term memory** | Recognizes returning people and remembers past sessions — across days, not turns. |
| ⚡ | **Actions** | Function calling into your APIs — bookings, lookups, e-mail, calendar, messaging. |
| 📡 | **Live streaming** | Run your character as an always-on AI stream host with an operator console. |
| 🎙️ | **Podcast mode** | Two NPCs hold an unscripted conversation with each other — on any topic you set. |
| 👥 | **Multi-NPC scenes** | Several characters per level; only the one you're near answers. |
| 🖥️ | **Every surface** | Game NPC, 24/7 kiosk, one-line web embed, or cloud-streamed MetaHuman. |

Everything is configured live from the **[IAMX panel](https://iamx.live)** — save in the panel, see it in the character's next reply. No rebuilds, no redeploys.

> 🧩 **How it works:** the plugin is a lightweight client. All AI runs in the IAMX cloud and streams back into Unreal — your project stays lean, your machine stays cool, and every improvement we ship lands server-side without touching your build.

---

## 🗣️ Conversation that feels alive

- **Streamed replies** — the character starts speaking while it's still thinking; no dead air.
- **Interruptible (barge-in)** — cut it off mid-sentence like you would a person; it stops and listens.
- **Echo-guarded** — it never mistakes its own voice from your speakers for user input.
- **30+ languages** — including English and Turkish, with natural, expressive voices.
- **Four ways to start talking:**

| Mode | Behavior |
|------|----------|
| **Push-to-talk** | Hold/press a key to speak (default `T`, configurable). |
| **Voice-activated** | Always listening; detects when you start and stop speaking. |
| **Wake word** | Sleeps until it hears its name — *"Hey Alara…"*. |
| **Proximity** | Give each NPC a radius; it only listens to the player standing near it. Walk away and it stops. |

## 🎭 A face that acts, not just talks

- **Lip sync** streams from the cloud frame-by-frame, driving the full MetaHuman facial rig — jaw, lips, cheeks, brows — not just an open/close mouth.
- **Eyes and head** track the player's camera with natural limits and smoothing (two AnimGraph nodes, non-destructive over your existing animation).
- **Emotion engine:** every character carries an 8-axis emotional state (joy, trust, fear, surprise, sadness, disgust, anger, anticipation) that *decays over time* and *shifts with the conversation*. Mood drives facial expression, voice tone **and** body gestures — call your character rude and watch its face change.
- **Custom characters welcome:** not using MetaHumans? Map the facial controls to your own rig's blend shapes and everything works the same.

## 📖 Scenario Studio — direct your character

A **no-code visual graph editor** for narrative design, right in the panel:

- Chain **sections** with goals ("greet the visitor → qualify their need → book a demo").
- Add **decision branches** the AI evaluates from the conversation itself.
- Fire **triggers** into your game or website when a branch is reached.
- The character stays in-character and on-mission — it improvises the words, you control the story.

Perfect for guided sales flows, museum tours, quest-giving NPCs and training simulations.

## 📚 Knowledge & memory

- **Knowledge base (RAG):** upload PDF / TXT / CSV — even images — and your character grounds its answers in *your* content. Ask a question covered by your docs, get your answer, not an internet guess. Files are managed per tenant and toggled per character.
- **Long-term memory:** the character summarizes each session and remembers returning visitors — "Welcome back! Last time you asked about pricing…" works across days.
- **Face recognition** *(paid plans)*: on kiosks, it recognizes returning people by face and greets them by name.

## ⚡ Actions — a character that does things

- **Function calling** on every supported model: define tools in the panel, the AI decides when to call them.
- **Your APIs:** wire HTTP GET/POST actions — the character fetches live data (weather, stock, order status) and answers naturally.
- **Assistant actions:** e-mail, calendar, Telegram, WhatsApp out of the box.
- **Blueprint events:** every action, reply and lifecycle moment fires delegates in Unreal (`OnResponseReady`, `OnNPCEvent`, `OnActionTriggered`…), so your game logic can react to anything the character says or does — and you can define custom actions the AI triggers in your Blueprints.

## 📡 Live streaming & podcast mode

<p align="center">
  <img src="docs/stage.jpg" alt="IAMX AI stream host on stage" width="72%">
</p>

- **AI stream host:** run your character 24/7 as a live streamer. Viewer messages flow through a **moderated queue** — an operator console lets you approve, prioritize or inject messages while the character performs.
- **Podcast mode (NPC ↔ NPC):** two characters talk *to each other*, unscripted, on a topic you set — each with its own personality, voice and opinions. Great for AI talk shows, debates and background world-building.
- **Operator console:** watch the conversation live, steer it, and step in at any moment from the panel.

## 👥 Multi-character scenes

Put five characters in one level — each with its own personality, voice, model and knowledge. **Proximity gating** means only the NPC you're standing near hears you; the rest mind their own business. Characters can even talk to each other (NPC-to-NPC).

<p align="center">
  <img src="docs/cast.jpg" alt="IAMX characters" width="90%">
</p>
<p align="center"><sub>Every character is yours to design — personality, voice, look and mission.</sub></p>

## 🖥️ Beyond Unreal

The same character you build for Unreal also runs:

- **On your website** — one line of embed code, browser-native 3D avatar with voice.
- **As a LiveFace avatar** — a talking head from a single photo.
- **As a cloud MetaHuman** — photoreal pixel-streamed straight to the browser, no install *(paid plans)*.
- **On 24/7 kiosks** — with identity verification and verified actions for regulated industries *(enterprise)*.

## 🎛️ The panel — mission control

Everything lives at **[iamx.live](https://iamx.live)**: character personality, voice, AI model, features, knowledge files, scenarios, usage analytics and conversation reports. Change anything → the running character picks it up on the next session. **No rebuilds. Ever.**

▶ **See it live:** create a free account at **[iamx.live](https://iamx.live)** and talk to your first character in the browser playground before you even open Unreal.

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

> ### 🔓 Windows: unblock the ZIP first (important!)
> Files downloaded from the internet are tagged "blocked" by Windows, which can stop Unreal from loading the plugin's binaries (symptom: text works but **no voice and no lip sync**). **Before extracting**, right-click the ZIP → **Properties** → tick **Unblock** → OK.
> Already extracted? Run this once in PowerShell inside the extracted `IAMX` folder:
> ```powershell
> Get-ChildItem -Recurse | Unblock-File
> ```

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

**Face Animation Blueprint** (e.g. `Face_AnimBP`) — add **two** nodes, chained before the Output Pose:

```
[Input / existing pose] → [IAMX Lip Sync] → [IAMX Eye Look At] → [Output Pose]
```

- **IAMX Lip Sync** — applies the streamed facial performance (mouth, jaw, expressions) on top of the incoming pose.
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
- 🗣️ **[Join the forum](https://iamx.live/forum)** — questions, showcases, roadmap talk
- 📰 **[Read the blog](https://iamx.live/blog)** — release notes and deep dives
- ⭐ **Star the repo** if this is useful — it genuinely helps others find it

## 📄 License

Free to use, including commercially, with the IAMX service — see [LICENSE](LICENSE.md).

<p align="center">
  <sub>Built with obsession by <a href="https://iamx.live">IAMX Interactive</a> · <a href="https://iamx.live">iamx.live</a> · <a href="https://iamx.live/forum">forum</a> · <a href="https://iamx.live/blog">blog</a></sub>
</p>
