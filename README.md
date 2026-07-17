# IAMX — AI Digital Humans for Unreal Engine

**Free Unreal Engine plugin for real-time, conversational AI digital humans and MetaHuman avatars** — game AI NPCs, virtual assistants, interactive kiosks and virtual influencers that see, talk and remember.

[![Website](https://img.shields.io/badge/website-iamx.live-6d8bff)](https://iamx.live)
[![Panel](https://img.shields.io/badge/control%20panel-iamx.live-a468ff)](https://iamx.live)
[![Unreal Engine](https://img.shields.io/badge/Unreal%20Engine-5.3%20–%205.8-313131)](#installation)

IAMX turns any MetaHuman (or your own character rig) into a live digital human:

- 🗣️ **Real-time two-way voice conversation** — streamed replies, interruptible (barge-in), 30+ languages
- 👄 **Real-time lip sync** — the character's mouth and face move in sync with every word
- 🧠 **Pick your AI model per character** — GPT, Claude, Gemini (incl. Gemini Live realtime), local Ollama
- 👀 **Camera vision** — the character sees and reacts to what's in front of it
- 🙋 **Face recognition & long-term memory** — greets returning people by name, remembers past sessions
- 📚 **Knowledge base (RAG)** — grounds answers in your own PDF/TXT/CSV documents
- 🎭 **Emotion engine** — mood drives facial expression, voice tone and gestures
- ⚡ **Actions** — function calling into your own APIs, e-mail, calendar, messaging
- 🖥️ **Every surface** — in-game NPCs, kiosks, web embed, live streams, cloud-streamed MetaHumans

The plugin is a lightweight client for the IAMX cloud. **Create your free account and your first character at [iamx.live](https://iamx.live)** — a free Starter plan is included; Pro/Enterprise plans unlock face recognition, memory, RAG, pixel streaming and more.

---

## Installation

1. Download the ZIP matching your engine version from **[Releases](../../releases)**:

   | Engine | Package |
   |--------|---------|
   | UE 5.3 | `IAMX_5_3_Fab.zip` |
   | UE 5.4 | `IAMX_5_4_Fab.zip` |
   | UE 5.5 | `IAMX_5_5_Fab.zip` |
   | UE 5.6 | `IAMX_5_6_Fab.zip` |
   | UE 5.7 | `IAMX_5_7_Fab.zip` |
   | UE 5.8 | `IAMX_5_8_Fab.zip` |

2. Extract the `IAMX` folder into your project's `Plugins/` directory:
   ```
   YourProject/
   └── Plugins/
       └── IAMX/
           ├── IAMX.uplugin
           ├── Source/
           └── ...
   ```
3. Open the project — Unreal will ask to compile the plugin (requires a C++ project; for Blueprint-only projects add an empty C++ class first).
4. Enable **Edit → Plugins → IAMX** if it isn't already, and restart the editor.

> Also available on **Fab** for one-click install.

## Quick start

1. Sign up at [iamx.live](https://iamx.live) and create a character in the panel (personality, voice, AI model, features).
2. In your level, select your MetaHuman (or custom character) and **Add Component → IAMX**.
3. Paste your character's **ID / token** from the panel into the component.
4. Press Play. Press **T** (default) to talk — or enable voice-activated / proximity modes on the component.

Your character's behavior, voice, model and features are all managed live from the [panel](https://iamx.live) — no rebuilds needed.

## Requirements

- Unreal Engine 5.3 – 5.8 (Win64)
- A free IAMX account ([iamx.live](https://iamx.live))
- A microphone for voice interaction

## Support

- 🐛 [Report a bug](../../issues/new?template=bug_report.yml)
- 💡 [Request a feature](../../issues/new?template=feature_request.yml)
- 🌐 [iamx.live](https://iamx.live)

## License

Free to use with the IAMX service — see [LICENSE](LICENSE.md).
