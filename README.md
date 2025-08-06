# Hey Vexa 👋

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

[![Join Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/Ga9duGkVz9)

**Vexa Main Project Repo** [![Parent repo stars](https://img.shields.io/github/stars/Vexa-ai/vexa?style=social&label=⭐)](https://github.com/Vexa-ai/vexa/stargazers)


*The first real‑time meeting co‑pilot that **listens, thinks, and speaks** to actively assist your Google Meet / Zoom / MS Teams calls.*

---

Most "AI note‑takers" just sit in a call and dump a doc later. **Hey Vexa** is the first open‑source bot that *actively* joins the conversation.
Say **"Hey Vexa, research this problem and come back with the report"** (or any custom command) and the agent will 

**1. Invoke an agent with access to your favorite MVP tools (previous meetings, RAG, company docs, web search, etc)**

**2. Response with a natural voice that answers back into the meeting — instantly.**

Built on top of the **[Vexa real‑time transcription API](https://github.com/Vexa-ai/vexa)**, which only requires the addition of an extra endpoint. It adds just one missing piece: a lightweight `playback` endpoint so the bot can talk.

---

## 🗺️ Project Roadmap

### **Phase 0 – Vexa Core Upgrade**
*effort: light*

* update `@vexa-bot` to playback sound, obtained through Redis MQ so an external service can stream `audio/wav` back into the call.
* Extend @bot-manager with `/playback` endpoint to queue the audio playback jobs via Redis

### **MVP 1 – Hey Vexa MVP**
*effort: easy*

1. **Transcript Listener** – poll Vexa's real‑time caption stream.
2. **Wake‑word Detector** – regex for *"Hey, Vexa"* triggers an agent.
3. Simple LLM one pass response
4. TTS speech generation
5. **Agent Invocation** – send recent context → LLM → TTS → `POST /playback`.

### **Product – MCP‑Powered Agent**
*effort: should be easy*

* Replace LLM call with the MCP-enabled agent

[![Join Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/Ga9duGkVz9)
---

### 🤝 Call for Collaboration

We're looking for **backend hackers, prompt engineers, TTS/LLM enthusiasts, DevRel storytellers, and testers** to help build this in the open.
👉 Hop into the [Discord](https://discord.gg/Ga9duGkVz9), pick an issue, and say *"Hey Vexa, I'm in!"*
