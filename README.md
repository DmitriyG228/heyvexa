# Hey Vexa 👋🤖

*The first real‑time meeting co‑pilot that ********************************************************************************************************************************************************************************listens, thinks, and speaks******************************************************************************************************************************************************************************** to actively assist your calls.*

---

## 🎯 What makes it different?

Most “AI note‑takers” just sit in a call and dump a doc later. **Hey Vexa** is the first open‑source bot that *actively* joins the conversation.
Say **“Hey Vexa, research this problem and come back with the report”** (or any custom command) and the agent will 

**1. Invoke an agent with access  to your favorite MVP - tools (revious meetings, RAG, company docs, web search, etc)**

2. **Response with a natural voice that answer back into the meeting — instantly.**

Built on top of the **[Vexa real‑time transcription API](https://github.com/Vexa-ai/vexa)**, which only requires the addition of an extra endpoint  adds just one missing piece: a lightweight \`playback\` endpoint so the bot can talk.

---

## 🗺️ Project Roadmap

### **0 – Vexa Core Upgrade**de\*\* 
effort: light

* update `@vexa-bot` to playback sound, obtained through redis MQ so an external service can stream r `audio/wav` back into the call.
* Extend @bot-manager with /playback  `** endpoint **` to queue the audio  playback jobs via Redis

### **MVP 1  – Hey Vexa MVP\*\*** easy
effort: easy

1. **Transcript Listener** – poll Vexa’s real‑time caption stream.
2. **Wake‑word Detector** – regex for *“Hey, Vexa”* triggers an agent.
3. simple LLM one pass response
4. TTS speach generation
5. **Agent Invocation** – send recent context → LLM → TTS → `POST /playback`.

### **Product – MCP‑Powered Agent** should be easy

effort: should be easy

* replace LLM call with the MCP enables agent

---

### 🤝 Call for Collaboration

We’re looking for **backend hackers, prompt engineers, TTS/LLM enthusiasts, DevRel storytellers, and testers** to help build this in the open.
👉 Hop into the [Discord](https://discord.gg/vexa), pick an issue, and say *“Hey Vexa, I’m in!”*
