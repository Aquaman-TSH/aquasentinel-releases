# 21. Reference

Quick lookups: default safe ranges, network ports, supported hardware and a short glossary.

**In this chapter:** [Default safe ranges](#default-safe-ranges) · [Supported hardware](#supported-hardware) · [Network ports](#network-ports) · [Glossary](#glossary)

---

## Default safe ranges

Every tank is judged against the safe range for its **type**. These are the out-of-the-box defaults; you can change any of them for a tank type in [Settings → Water](18-settings.md#water). A range of `0 – 0` means *any* detectable amount is a problem.

| Parameter | Freshwater | Planted | Saltwater (fish) | Reef | Brackish |
|---|---|---|---|---|---|
| **pH** | 6.5 – 7.8 | 6.5 – 7.2 | 8.1 – 8.4 | 8.2 – 8.4 | 7.5 – 8.5 |
| **Temperature (°F)** | 72 – 82 | 72 – 82 | 74 – 80 | 75 – 79 | 72 – 82 |
| **Ammonia (ppm)** | 0 | 0 | 0 | 0 | 0 |
| **Nitrite (ppm)** | 0 | 0 | 0 | 0 | 0 |
| **Nitrate (ppm)** | 0 – 30 | 5 – 30 | 0 – 20 | 0 – 5 | 0 – 20 |
| **GH (dGH)** | 4 – 12 | 3 – 8 | 8 – 12 | 8 – 12 | 6 – 20 |
| **KH (dKH)** | 3 – 8 | 2 – 6 | 8 – 12 | 8 – 11 | 5 – 15 |
| **Phosphate (ppm)** | 0 – 0.5 | 0.1 – 1.0 | 0 – 0.1 | 0 – 0.03 | 0 – 0.5 |
| **ORP (mV)** | 300 – 450 | 200 – 400 | 350 – 450 | 350 – 450 | 300 – 450 |
| **EC (µS/cm)** | 0 – 1,500 | 0 – 1,500 | 40,000 – 60,000 | 40,000 – 60,000 | 1,000 – 20,000 |
| **Salinity (ppt)** | 0 – 1 | 0 – 1 | 30 – 37 | 33 – 36 | 5 – 25 |
| **TDS (ppm)** | 0 – 500 | 0 – 500 | 30,000 – 38,000 | 30,000 – 38,000 | 500 – 12,000 |

How far outside the range a reading is matters too: a little over on nitrate is a water change, while any ammonia is urgent. The tank [health score](03-tanks.md#tank-health-score) takes that into account.

> [!NOTE]
> On saltwater, reef and brackish tanks the EC reading is shown in **mS/cm** (for example 53.00 mS/cm) rather than tens of thousands of µS/cm. This is display only; stored values don't change.

---

## Supported hardware

Aquatic Sentinel is **hardware-agnostic**: it works with equipment you already own or can buy off the shelf. More in [Devices](09-devices.md).

| Family | Examples | Control |
|---|---|---|
| **Tuya / Smart Life** | Plugs, power strips, lights, thermostats, water-quality monitors (including the PH-W218 8-in-1 meter), leak sensors, sprinkler valves and water timers, and "Other" for devices the app doesn't recognise yet | Cloud and local network |
| **Kasa / TP-Link** | Smart plugs and strips, including the newer firmware | Local network (account optional) |
| **Magic Home / Zengge** | RGB and white LED controllers | Local network |
| **Govee** | WiFi leak sensors (some models only report to the Govee app) | Cloud |
| **ESPHome** | DIY ESP32 / ESP8266 sensors and switches with the web server enabled | Local network |
| **Bluetooth (BLE)** | YINMIK BLE-C600 7-in-1 water-quality meter; single-colour LED controllers | Bluetooth (desktop) |
| **Zigbee** | The ZG-109TDS TDS / EC / temperature probe, via a USB coordinator | Built-in radio (desktop) |
| **Seachem / AquaVitro Sentia** | The Sentia doser | Cloud |
| **CoralVue Hydros** | Hydros controllers (preview) | Cloud |

---

## Network ports

| Port | Used for |
|---|---|
| **3480** (TCP, on the computer running the app) | The built-in web server — the address you open from a phone or another computer |
| **6668** (TCP, on your local network) | Tuya devices in local mode |
| **6666 / 6667** (UDP, local network) | Tuya devices announcing themselves, so the app can find their address |
| **9999** (TCP/UDP) and **80** (TCP), **20002** (UDP) — local network | Kasa / TP-Link plugs: older firmware answers on 9999; newer firmware (KLAP) on port 80 |
| **5577** (TCP/UDP, local network) | Magic Home / Zengge controllers |
| **443** (HTTPS, outbound) | The AI provider you chose, the Tuya cloud, weather, Cloudflare Tunnel |

---

## Glossary

| Term | Meaning |
|---|---|
| **Cloud mode / Local mode** | How Aquatic Sentinel talks to a device. *Cloud* goes through the manufacturer's service — works anywhere, needs internet. *Local* talks to the device directly on your network — faster, and works without internet. Devices that stop answering locally fall back to the cloud automatically. |
| **Local key** | A secret code a Tuya device needs for local control. The app can fetch it for you once your Tuya account is connected. |
| **EC** | Electrical conductivity of the water — a quick proxy for how much is dissolved in it. Used to estimate salinity and, with a ratio you set, nitrate. |
| **TDS** | Total dissolved solids, in ppm. |
| **ORP** | Oxidation-reduction potential, in millivolts — a general measure of water "cleanliness". Falling ORP is the signal behind the [ammonia risk](04-parameters.md#ammonia-risk-early-warning) warning. |
| **GH / KH** | General hardness / carbonate hardness (alkalinity). Low KH lets pH swing. |
| **PAR / PPFD** | The light plants and corals can actually use — a measurement of how many photons reach a spot, in µmol/m²/s. |
| **Photoperiod** | The hours of light a tank gets each day. |
| **Inhabitant** | Anything living in a tank: a fish, an invertebrate, a coral, a plant. |
| **Scene** | A named group of device actions that run together ("Feeding Time"). |
| **Recipe** | A ready-made [automation](12-automations.md) you install with one click. |
| **Profile** | The description that tells Aquatic Sentinel what a kind of device can do and how to show it. |
| **Trend Watch** | The early-warning box that flags slow drifts in your readings. |
| **Pairing** | Approving a phone for [remote access](16-remote-access.md) by scanning a QR code. |
| **Prerelease / beta** | Every build so far is a beta: complete enough to use, still changing. All Pro features are unlocked free while it lasts. |

---

← [20. Troubleshooting](20-troubleshooting.md) · [Manual home](README.md)
