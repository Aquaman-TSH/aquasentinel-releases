# 14. Voice

Hands wet, or elbow-deep in the sump? Talk to your tank. Aquatic Sentinel understands spoken commands for switching devices, setting timers, reading your water parameters and logging tests — and it can speak alerts back to you.

**In this chapter:** [Starting a voice command](#starting-a-voice-command) · [What you can say](#what-you-can-say) · [When it isn't sure](#when-it-isnt-sure) · [Teaching it your words](#teaching-it-your-words) · [Voice macros](#voice-macros) · [Spoken alerts and narration](#spoken-alerts-and-narration)

> [!NOTE]
> Voice commands are a **desktop** feature (Windows and Linux). They need a microphone, and they are part of the Pro features that are **unlocked free during the beta**. The wake word and voice commands haven't been tried on the Android build yet.

---

## Starting a voice command

There are two ways:

- **Press Ctrl+Shift+A.** A listening panel appears — speak your command.
- **Say the wake word, "Hey Sentinel".** This is **off by default**. Turn it on in **Settings → Voice → Wake Word**; the sensitivity slider there balances false triggers against missed ones.

On a phone or another computer using remote access there is a microphone button in the page header instead (a coloured dot shows whether it is listening).

Aquatic Sentinel turns your speech into text using the best engine available — OpenAI Whisper if you've given it an OpenAI key (**Settings → Voice**), otherwise your computer's built-in speech recognition. On Linux the assistant listens through your AI provider.

---

## What you can say

Most commands are understood **instantly and offline**, with no AI call. Say them naturally; you don't need the exact words.

### Devices and scenes

| Say | What happens |
|---|---|
| *"Turn on the sump return pump"* / *"Turn off the heater"* | Switches the device. |
| *"Change the reef light to 50%"* / *"Dim the reef light to 20%"* | Sets a light's brightness. Add *"in the frag tank"* if two lights share a name. |
| *"Slowly dim the reef light to 20%"* | Fades instead of jumping — five minutes by default. |
| *"Dim the reef light to 20% over 30 minutes"* | Fades over the time you name. Starting a fade stops any light mode already running on that light, and tells you so. |
| *"Activate feeding time"* | Runs a [scene](11-scenes-schedules-timers.md#scenes). |

Give your devices clear names — *Sump Return Pump* rather than *Plug 3* — so they're recognised reliably. Locked outlets ([Devices → Lock an outlet](09-devices.md#locking-an-outlet-in-place)) can't be switched by voice, which is exactly the point.

### Timers and alarms

| Say | What happens |
|---|---|
| *"Set a timer for 20 minutes"* | Starts a countdown. |
| *"Set a timer called water change for 15 minutes"* | A named timer, so the announcement tells you what finished. |
| *"Set an alarm in 10 minutes"* | An alarm that rings in 10 minutes. |
| *"Cancel the timer"* | Cancels it. |
| *"Snooze 5 minutes"* | Snoozes a timer that has gone off. |
| *"Dismissed"* (or *stop*, *quit*, *abort*) | Dismisses it. |
| *"What timers are running?"* / *"How much time is left on the timer?"* | Reads them back. |

Times like *"an hour and a half"*, *"half an hour"* and *"1 hour and 15 minutes"* are all understood. Timers and alarms live on the [Timers page](11-scenes-schedules-timers.md#timers-and-alarms).

### Water parameters and tank status

| Say | What happens |
|---|---|
| *"What is the pH in the reef tank?"* | Reads a single value. |
| *"Parameters for the reef tank"* | Reads the latest test. |
| *"How is the reef tank doing?"* | Reads a summary: latest parameters, last maintenance and any active alerts. |
| *"Log pH 8.1, ammonia 0, nitrite 0 for the reef tank"* | Logs a water test by voice. |
| *"Mark water change done for the reef tank"* | Logs the maintenance task. |

### Other

| Say | What happens |
|---|---|
| *"What time is it?"* | The time (and date). |
| *"What's the weather?"* / *"What's the forecast?"* | Needs the weather set up in **Settings → Devices → Weather**. |
| *"Help"* | Describes what voice can do. |
| *"Silence"* | Emergency silence for the alarms. |

### Anything else — the AI fallback

If the built-in understanding doesn't recognise a sentence, Aquatic Sentinel can ask your AI provider to *rephrase* it into one of the commands above — *"Can you kill the lights over the reef"* becomes *"turn off the reef light"* — or to pick a scene, macro or automation rule you named. The AI only chooses; the same checks, locks and confirmations still apply, and it can never invent a device or scene that doesn't exist.

---

## When it isn't sure

Each command gets a confidence score:

- **High (65% or more)** — it just does it.
- **Medium (35–65%)** — it asks you to confirm before acting ("Did you mean…?"). Say *yes* or *no*.
- **Low (under 35%)** — it says it didn't understand.

---

## Teaching it your words

If it mishears you — it's *"quite"* when you said *"quiet"* — teach it. In **Settings → Voice**:

- **Voice Vocabulary** lets you add your own names and synonyms for devices and commands. It learns from corrections and applies them before the normal matching.
- **Voice Debug** shows the microphone level, the raw transcript of what it heard, which recognition engine is in use, and a log of recent voice events — the first place to look when a command misbehaves.

---

## Voice macros

A **voice macro** turns one spoken phrase into a sequence of steps — for example *"Good morning"* → turn the lights on, announce the tank status, log a feeding. Steps can switch devices, speak a message, wait, or read out tank status. Build them in **Settings → Voice → Voice Macros**.

---

## Spoken alerts and narration

Aquatic Sentinel can speak as well as listen:

- **Alerts are spoken** — a leak, an offline device, a timer going off — using a voice you choose in **Settings → Voice** (with speed, pitch and volume).
- **Narrate AI responses** makes the AI assistant read its replies aloud.
- **Alarms duck, they don't mute.** When a spoken message plays over an alarm, the alarm drops to a low volume for the message and then comes back — you always hear both.
- **Emergency silence.** **Ctrl+Shift+S** (or the on-screen **Silence** button) quiets every active alarm at once, even if the app is minimised.

---

← [13. AI](13-ai.md) · [Manual home](README.md) · **Next:** [15. The Library](15-library.md) →
