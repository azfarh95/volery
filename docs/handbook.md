# Volery handbook

Everything Volery can do, in plain language. New here? Start with
**[Get Scout running](getting-started-scout.md)** first — this handbook is the reference you
come back to.

**Contents**
- [The three lanes: Scout, Sage, Dove](#the-three-lanes)
- [Chatting](#chatting)
- [Scout — your on-device model](#scout--your-on-device-model)
- [Sage — bring your own cloud model](#sage--bring-your-own-cloud-model)
- [Tools — what Scout can do for you](#tools--what-scout-can-do-for-you)
- [Voice: dictation & voice notes → reports](#voice)
- [Personalize — make it yours](#personalize--make-it-yours)
- [Your data & privacy](#your-data--privacy)
- [FAQ & troubleshooting](#faq--troubleshooting)

---

## The three lanes

Volery's agents are birds in a flock. You switch between them with the chips at the top of the
chat; each shows a status dot.

- **🐦 Scout — on your phone.** Free, offline, private, no account. Runs the model you downloaded.
  Always available. *Start here.*
- **☁️ Sage — a cloud model you bring.** When you want a bigger brain, plug in your own provider
  (OpenAI, Claude, Groq, and more) or your own computer. Your key, your data path — Volery never
  routes it through us.
- **🕊️ Dove — the hive (advanced).** Memory + tools on your own server/box. Only appears in the
  sideloaded owner build; it's hidden on the Google Play version.

You can keep all three set up and switch per message.

---

## Chatting

- **New chat:** the **＋** in the top bar. Your past chats live in the **history drawer** (the menu
  icon, top-left).
- **Starter prompts:** on an empty chat, tap a chip like *Summarize this*, *Translate this*,
  *Explain like I'm five*, or *Draft a quick reply*. You can edit these in Personalize.
- **Share an image:** tap the **📎** attach button to send a photo or screenshot. This only works
  with a **multimodal** Scout model (a **Gemma-4** model) or a vision-capable Sage model.
- **On each reply:** share, delete, regenerate, or stop a running answer.
- **If a cloud reply fails:** Volery offers **Retry** or an **"Ask {other lane}"** chip so you can
  fall back (e.g. hand it to Scout).
- **Voice input:** tap the **🎙️ mic** in the input bar and speak instead of typing.

---

## Scout — your on-device model

Scout is the heart of Volery: a real AI model running on your phone.

### Getting a model
Volery ships without a model (to stay small), so you download one **once**. Full walkthrough:
**[Get Scout running](getting-started-scout.md)**. In short: **Settings ⚙ ▸ 🐦 Scout ▸ Model ▸
Browse models ▸ pick one ▸ Download**.

### Managing models
In **Settings ▸ 🐦 Scout**:
- **This device** — a readiness verdict for your phone, plus **"Verify it can run (load test)."**
- **On this phone** — your installed models. **Tap a row to make it active**; the tick shows which
  one Scout uses. **Delete** any you don't need to free storage.
- **Browse models** — the in-app catalogue (from Hugging Face) with sizes, RAM estimates, and a
  **✅ / ⚠️ / ❌** fit badge for your phone. You can also paste a **direct model link** if you have one.
- **Fit badges:** ✅ runs well (≤45% of RAM) · ⚠️ tight, may be slow (≤60%) · ❌ over the safe limit.
  Volery warns before you load anything too big.

### The engine
Scout runs a small local engine on your phone that the app talks to.
- **Starting it:** by default it starts on your **first message** (you'll see *"Scout is waking
  up…"*). You can also turn on **"Start automatically on launch"** in the Engine section.
- **Tuning (optional):** GPU or CPU backend, idle-stop timer, pause-on-low-battery, response
  creativity (temperature / top-K / top-P), and max context length. Defaults are sensible — you
  don't need to touch these.
- **Test Scout** runs a quick benchmark so you can see how fast your phone is.

### Picking a model — quick guide
Want it to **see images**? Choose **Gemma-4 E4B** (best, 3.4 GB) or **E2B** (lighter, 2.4 GB).
Want **fast on a modest phone**? **Gemma 3 1B** (0.6 GB) or **Qwen2.5 1.5B** (1.5 GB).
Want **the best reasoning** and don't need images? **Phi-4 mini** (3.6 GB). When unsure, pick the
largest model showing a ✅ for your phone.

---

## Sage — bring your own cloud model

Sage is for when you want a bigger model than your phone can run. You bring the provider and the
key; **your key stays on the device**, and your messages go only to the provider *you* choose.

**Set it up:** **Settings ⚙ ▸ ☁️ Sage**:
1. **Profile** — create a named profile (you can keep several, e.g. "OpenAI 4o" and "Groq Llama").
2. **Provider** — pick one:
   - **OpenAI**, **Anthropic (Claude)**, **OpenRouter**, **Groq**, **Google Gemini**, **DeepSeek**,
     **Together AI**, **Mistral**, **xAI (Grok)**
   - **My computer (Tailscale)** — talk to a model running on your own PC over your private network
     (there's a 5-step setup guide inline)
   - **Custom (OpenAI-compatible)** — any endpoint that speaks the OpenAI API
3. **API key** — paste your key from the provider (masked; tap *Show key* to check it). Get keys
   from your provider's dashboard.
4. **Model** *(optional)* — leave blank for the provider's default, or tap **Fetch models** to pick
   from a live list (with prices).
5. **Test connection** — confirms it works and shows the round-trip time.

Extras per profile: a system-prompt override, a prompt library, temperature/max-tokens, and a
**budget + spend estimate** so you can keep an eye on cost.

Until a provider + key are set, the Sage lane will say *"Set up Sage in Settings."*

---

## Tools — what Scout can do for you

Tools let the AI *do* things, not just talk. Turn them on in **Settings ⚙ ▸ Tools**, or straight
from the chat's **🧰 tool tray** (the *"Tools · N on"* bar above the input — tap to expand). When
you enable a tool that needs a permission (calendar, contacts, location), Volery asks for it when
you tap **Save**. A 🔒 marks tools still waiting on a permission.

### Native tools (on your phone — private)
Work with both Scout and Sage:

- **Time & date**, **Battery status**, **Device info**, **Flashlight**
- **Calculator** — exact math
- **Notes** — remember & recall things (with an in-settings viewer)
- **Timer** and **Set alarm**
- **Calendar** — read your events, and **add a calendar event**
- **Contacts** — look up a contact
- **Location** (coarse) — used by directions
- **Directions (Google Maps)** — *"How do I get to Sentosa?"* opens Maps with the route
- **Call** — opens the dialer, pre-filled
- **Draft a text (SMS)** and **Draft an email** — composed for you to review and send
- **Clipboard** — read/replace clipboard text

These run **on the phone**; nothing is sent to a server. Actions like calling, texting, or adding
an event are **pre-filled for you to confirm** — Volery never sends on its own.

### Connector tools (optional — reach the web)
Enable in **Settings ▸ Tools ▸ Connectors**:
- **Keyless:** Wikipedia, Read a link, Crypto price
- **Need a free key (paste it inline):** Web search (Tavily/Brave), Weather (OpenWeatherMap),
  News (NewsAPI)

Each has a **Test** button so you can confirm it works.

*(The owner/sideload build also has self-hosted tools and MCP servers for advanced setups.)*

---

## Voice

### Dictate a message
Tap the **🎙️ mic** in the chat input and speak — it becomes your message.

### Voice notes → structured reports
Tap the **🎙️ voice-notes** icon in the top bar to open Notes:
1. **Hold** the mic to record (a lecture, a meeting, a thought) — you'll see a live transcript and
   timer. **Release** to save.
2. Volery offers **"Make report"** — Scout turns the raw transcript into a clean, structured
   Markdown report **on your phone**. Long recordings are handled in chunks.

Speech recognition **prefers the on-device engine**, so your audio stays private where your phone
supports it.

---

## Personalize — make it yours

**Settings ⚙ ▸ 🎨 Personalize:**
- **Theme** — system / light / dark, **Material You**, an accent colour (or a custom hex).
- **Scout's identity** — rename it, pick a **persona** preset, and add an *"About you"* so it
  answers in a way that fits you. Set per-agent colours and avatars (emoji or an image).
- **Chat appearance presets** — *Volery, Minimal, Terminal, Classic, Big & clear.*
- **Readability** — text size, density, **font** (System / Serif / Mono), rounded or square
  bubbles, timestamps on/off, haptics.
- **Chat backgrounds** — a few built-ins or your own image.
- **Starter prompts** — edit the chips that show on an empty chat.

---

## Your data & privacy

**Settings ⚙ ▸ Data & privacy:**
- **Private by default** — Scout runs 100% on-device; your messages and tool data (calendar,
  contacts, location, notes, voice) stay on your phone. The only thing that leaves is what you
  explicitly send to **your own** Sage provider.
- **App lock** — require your device PIN/biometric to open Volery.
- **Backup & move** — export your settings (keys excluded) or an **encrypted backup** (keys
  included) to move to a new phone. Import to restore.
- **Storage** — see how much space models and data use, and clear data if needed.
- **Replay the welcome tour** — re-run the intro any time.

Full policy: <https://azfarh95.github.io/volery-legal/>.

---

## FAQ & troubleshooting

**"⚠️ Scout couldn't start."** No model is active. **Settings ▸ 🐦 Scout ▸ Model** — install one
and tap its row to select it, then send a message.

**Does Scout work with no internet?** Yes — once a model is downloaded, Scout is fully offline.
Only **Sage** (a cloud model you chose) uses the internet.

**Do I need an account or to sign up?** No. Scout needs nothing. Sage needs a key from *your*
provider, not from us.

**Which model should I download?** The largest one showing a **✅** for your phone. For images,
pick a **Gemma-4** model. See the [start guide](getting-started-scout.md#which-model-should-i-pick).

**Replies are slow.** The model may be large for your phone (⚠️/❌ badge) — try a smaller one. The
*first* message after starting the engine is always slower (it loads the model); later ones are quick.

**It stops replying when the screen is off.** Some phones (Honor/Huawei/Xiaomi) freeze background
apps — allow Volery to run in the background in your battery settings.

**My phone is too small for Scout.** Use **Sage** instead — a cloud model you bring — which runs no
model on the phone.

**Where's Dove?** It's an advanced lane for running your own server, only in the sideloaded owner
build — hidden on the Play version.

**How do I get the app?** Join the **Google Play closed test** (recommended), or sideload the APK
from [Releases](../../releases) (Android 8.0+, arm64). Found a bug?
[Open an issue](../../issues).
