# Get Scout running — a 3-step start

**Scout is Volery's on-device AI: it runs on your phone, works offline, and needs no account.**
This guide gets you from a fresh install to your first answer. It takes about 5 minutes plus a
one-time model download.

> **The one thing to know first:** Volery ships *without* a model inside it (that keeps the app
> small). Scout can't answer until you download one — **once**. This guide is mostly that
> download. After it, Scout just works, offline, forever.

---

## Before you start — will it run on your phone?

Scout runs a real AI model on your device, so it needs a reasonably modern phone:

- A **64-bit (arm64) Android phone**, **Android 8.0 or newer**.
- Roughly **6 GB of RAM or more**. More RAM = bigger, smarter models. (8 GB is fine; 11 GB+ runs
  the best model on the GPU.)
- **2–4 GB of free storage** for the model you download.

**You don't have to figure this out yourself** — Volery checks your phone for you and tells you
exactly what it can run (Step 2 below). If your phone is too small, it will say so plainly.

---

## Step 1 — Open Volery and meet Scout

1. Open **Volery**. The first time, a short welcome tour introduces the flock — **🐦 Scout**
   (on-device), **☁️ Sage** (a cloud model you bring), and the privacy promise. Tap through it,
   or **Skip**.
2. You land in the chat on the **Scout** lane. You'll see *"Ask Volery anything"* and a few
   tappable starter prompts.

If you type a message now, Scout will say it can't start yet — that's expected. It needs a model.
Let's get one.

---

## Step 2 — Download a model (the one-time setup)

1. Tap the **gear ⚙** (top-right of the chat) to open **Settings**.
2. Open the **🐦 Scout** tab.
3. At the top, the **"This device"** card shows a verdict for *your* phone — for example
   *"Excellent — runs the default model on the GPU"* or *"Small models only."* Tap
   **"Verify it can run (load test)"** if you want to be sure before downloading.
4. In the **Model** section, tap **"Browse models."** Volery loads a list from Hugging Face —
   each row shows the download size and a rough RAM estimate, with a fit badge:
   - ✅ **runs well** · ⚠️ **tight, may be slow** · ❌ **too big for this phone**
5. **Pick one that fits your phone** (see the cheat-sheet below), then tap **Download**. If you
   pick something large for your RAM, Volery double-checks with a *"⚠️ Large model"* prompt first.
6. Wait for the download (2–4 GB — use Wi-Fi). You'll see progress like *"…52% (1.2 GB)."* When
   it finishes: *"Installed ✓ and set active."*

That's the setup done. You never have to do it again.

### Which model should I pick?

| Model | Size | Good for | Needs about |
|---|---|---|---|
| **Gemma-4 E4B** | 3.4 GB | Best quality, **can see images** — the default | 11 GB+ RAM |
| **Gemma-4 E2B** | 2.4 GB | Lighter, still sees images | 7 GB+ RAM |
| **Phi-4 mini** | 3.6 GB | Strongest reasoning (text only) | 7 GB+ RAM |
| **Qwen2.5 1.5B** | 1.5 GB | Compact all-rounder (text only) | 5–6 GB RAM |
| **Gemma 3 1B** | 0.6 GB | Fastest, lowest RAM (text only) | 5–6 GB RAM |

**Not sure?** Trust the ✅/⚠️/❌ badge next to each model — it's calculated for *your* phone. Pick
the largest one showing ✅. If you want Scout to understand **photos and screenshots**, choose a
**Gemma-4** model (they're multimodal); the others are text-only.

---

## Step 3 — Say hello

1. Go back to the chat.
2. Type anything — or tap a starter like *"Explain like I'm five."*
3. The first time, Scout loads the model into memory: *"Scout is waking up… (first load can take
   a minute)."* This slow moment happens **only on the first message** after starting the engine.
   After that, replies are quick.

🎉 **That's Scout.** It's now running entirely on your phone — turn off Wi-Fi and mobile data and
it still works. No account, nothing sent anywhere.

---

## If something goes wrong

- **"⚠️ Scout couldn't start — check the model in Settings ▸ Scout."**
  No model is active yet, or it didn't finish downloading. Go to **Settings ▸ 🐦 Scout ▸ Model**
  and make sure a model is installed **and** selected (tap its row so it's the active one), then
  send a message to load it.
- **The download stopped.** Re-open **Settings ▸ Scout ▸ Model** and tap Download again — it
  resumes where it left off. Prefer Wi-Fi; these files are large.
- **Replies are very slow, or the app feels heavy.** Your model may be big for your phone (a ⚠️
  or ❌ badge). Download a smaller one (Qwen2.5 1.5B or Gemma 3 1B) and select it instead.
- **It won't run at all / "needs a 64-bit phone."** Scout needs an arm64 phone with ~6 GB+ RAM.
  On a smaller phone you can still use **Sage** — a cloud model you bring — see the
  [Handbook](handbook.md#sage--bring-your-own-cloud-model).
- **Replies stop when the screen is off (some Honor/Huawei/Xiaomi phones).** Their battery saver
  freezes the app. Allow Volery to run in the background in your phone's battery settings.

---

## What next?

- Want a bigger brain sometimes? Set up **Sage** (your own cloud model) — see the
  **[Handbook → Sage](handbook.md#sage--bring-your-own-cloud-model)**.
- Give Scout **tools** (calculator, maps, calendar, voice notes, and more) —
  **[Handbook → Tools](handbook.md#tools--what-scout-can-do-for-you)**.
- Make it yours (theme, name, persona) —
  **[Handbook → Personalize](handbook.md#personalize--make-it-yours)**.
