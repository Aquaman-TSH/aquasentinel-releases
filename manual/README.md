# Aquatic Sentinel — User Manual

**For version 1.6.0-beta.3.82.21** · [Download the latest release](https://github.com/Aquaman-TSH/aquasentinel-releases/releases) · [Join the Beta Discord](https://discord.gg/AhDD86t4m2)

![The Dashboard](images/dashboard.png)

Aquatic Sentinel looks after your aquariums so you can enjoy them. It keeps your water tests, livestock, equipment and chores in one place; controls the smart plugs, lights and sensors you already own; watches your readings and warns you *before* a small drift becomes a loss; and answers your questions with an AI advisor that knows your tanks. It runs on Windows, Linux or an Android phone, keeps your data on your own computer, and during the beta every feature is unlocked and free.

This manual walks through all of it, one page of the app at a time.

---

## New to Aquatic Sentinel? Start here

1. **[Install it and meet the screen](01-getting-started.md)** — Windows, Linux or Android, and a tour of the left menu.
2. **[Add your first tank](03-tanks.md#adding-a-tank)** and **[log a water test](04-parameters.md#logging-a-test)**.
3. **[Set up the free AI](13-ai.md#set-up-your-ai)** — a Google Gemini key takes about three minutes and costs nothing.
4. **[Add a smart plug](09-devices.md#connecting-tuya)** and put it on a **[schedule](11-scenes-schedules-timers.md#schedules)**.
5. **[Open it on your phone](16-remote-access.md)** to keep an eye on things from anywhere.

---

## Contents

### Your aquariums
| | |
|---|---|
| **[1. Getting started](01-getting-started.md)** | Install, first launch, the screen, shortcuts and built-in help. |
| **[2. The Dashboard](02-dashboard.md)** | Your home page: alerts, tasks, Trend Watch, tanks and the live camera. |
| **[3. My Tanks](03-tanks.md)** | Tanks, inhabitants, the health score, calculators and photos. |
| **[4. Water parameters](04-parameters.md)** | Logging tests, charts, alert rules, the nitrate estimate and the ammonia early warning. |
| **[5. Health](05-health.md)** | A health record for every animal, benchmarks, care tips and AI analysis. |
| **[6. Journal](06-journal.md)** | The diary of everything that happens in a tank. |
| **[7. Maintenance](07-maintenance.md)** | Recurring chores that don't slip. |
| **[8. PAR mapping](08-par-mapping.md)** | Map where the light actually lands. |

### Devices and control
| | |
|---|---|
| **[9. Devices](09-devices.md)** | Plugs, lights, sensors, leak detectors, dosers — and how to connect them. |
| **[10. Power](10-power.md)** | Energy use and cost, live and over time. |
| **[11. Scenes, schedules and timers](11-scenes-schedules-timers.md)** | One-tap scenes, daily schedules, countdown timers and alarms. |
| **[12. Automations](12-automations.md)** | Rules that react to your water and your devices. |

### Help from the app
| | |
|---|---|
| **[13. AI features](13-ai.md)** | The assistant, photo diagnosis, the test-vial reader and the ✨ Helper. |
| **[14. Voice](14-voice.md)** | Talk to your tank. |
| **[15. The Library](15-library.md)** | Encyclopedia, disease guide, research notes, DIY Corner and Price Scout. |

### Everywhere you are
| | |
|---|---|
| **[16. Remote access and your phone](16-remote-access.md)** | See and control your tanks from anywhere, securely. |
| **[17. Android](17-android.md)** | Turn a spare phone into an always-on tank controller. |

### Settings, safety and support
| | |
|---|---|
| **[18. Settings](18-settings.md)** | Every setting, by category. |
| **[19. Backup and your data](19-backup-and-data.md)** | Automatic backups, restoring, and moving computers. |
| **[20. Troubleshooting and FAQ](20-troubleshooting.md)** | Fixes by symptom, and how to report a bug. |
| **[21. Reference](21-reference.md)** | Default safe ranges, supported hardware, network ports and a glossary. |

---

## I want to…

| I want to… | Go to |
|---|---|
| Know if my tank is OK right now | [Dashboard](02-dashboard.md) · [Health](05-health.md) |
| Be warned about ammonia between tests | [Ammonia risk](04-parameters.md#ammonia-risk-early-warning) |
| Stop a pump or heater being switched off by accident | [Locking an outlet](09-devices.md#locking-an-outlet-in-place) |
| Turn lights on and off every day | [Schedules](11-scenes-schedules-timers.md#schedules) |
| Switch several things at once for feeding | [Scenes](11-scenes-schedules-timers.md#scenes) |
| Turn the heater off if the tank gets too warm | [Automations](12-automations.md) |
| Get alerted if a leak sensor trips | [Leak sensors](09-devices.md#leak-sensors) |
| Check on my tank from work | [Remote access](16-remote-access.md) |
| Use a spare phone as a tank controller or camera | [Android](17-android.md) · [Live Camera](02-dashboard.md#live-camera) |
| Ask what's wrong with a sick fish | [AI photo diagnosis](15-library.md#ai-photo-diagnosis) · [Assistant](13-ai.md) |
| Log a water test without typing | [Test-vial reader](04-parameters.md#logging-a-test) · [Voice](14-voice.md) |
| Find out how much my equipment costs to run | [Power](10-power.md) |
| Back up my data | [Backup](19-backup-and-data.md) |
| Report a bug | [Reporting a bug](20-troubleshooting.md#reporting-a-bug) |

---

## What's new in 3.82.21

- **Android.** The whole app now runs on an Android phone or tablet — a complete always-on tank controller. → [Chapter 17](17-android.md)
- **Ammonia early warning.** Aquatic Sentinel watches your ORP between tests and tells you when to test for ammonia. → [Ammonia risk](04-parameters.md#ammonia-risk-early-warning)
- **Trend Watch** on the Dashboard and Parameters page flags slow drifts in ORP, pH and EC. → [Trend Watch](02-dashboard.md#trend-watch)
- **Live tank camera**, shareable from a phone through remote access. → [Live Camera](02-dashboard.md#live-camera)
- **File a Bug** in the left menu writes the report for you. → [Reporting a bug](20-troubleshooting.md#reporting-a-bug)
- **Choose your layout** — Auto, Phone or Desktop. → [Appearance](18-settings.md#appearance)
- **Pairing for remote access** — approve each phone with a QR code. → [Pairing](16-remote-access.md#pairing-choosing-who-can-connect)
- **Seachem / AquaVitro Sentia doser** support. → [Dosers](09-devices.md#dosers-valves-and-controllers)
- **Devices that stop answering locally fall back to the cloud** instead of showing offline.
- **A real way to clear power history**, a clearer port-busy message, an update prompt that no longer freezes the app, and a long list of fixes from real-world testing.

The full list is in the [release notes](https://github.com/Aquaman-TSH/aquasentinel-releases/releases).

---

## How to read this manual

- **Bold** names are things you click or see on screen exactly as written — **Settings → System → Remote Access** means *open Settings, choose System, then open the Remote Access section*.
- **Callout boxes** mark a tip, a note, or something worth pausing on.
- Every chapter ends with links to the previous and next chapters, and each opens with a list of what's inside.
- Screenshots are taken from a demonstration set-up with invented tanks and devices; yours will show your own.

---

## Help and feedback

This is a beta, and your feedback shapes it.

- **Found something wrong?** Use **File a Bug** in the app's left menu — it writes the report for you.
- **Questions, ideas, and photos of your tank:** the [Beta Discord](https://discord.gg/AhDD86t4m2).
- **Something not covered here?** The app's own **Help & About** page has a searchable feature guide, and every page has a **?** button with tips for that page.

© 2026 EasyAquatix.
