# Quickstart

This quickstart is a “big picture” view of the build. The detailed steps and safety rules are in later docs.

## 1) Confirm the Steam Machine is compatible
Before buying parts, confirm the Steam Machine has:

- **An M.2 Key‑M NVMe slot** that carries PCIe lanes (this becomes your OCuLink link)
- The ability to **boot SteamOS from external USB storage** (because the internal NVMe may be removed)
- A **USB‑C port** capable of **10Gbps** if you plan to run the OS/game drive from a USB‑C NVMe enclosure

See: **docs/01-SteamMachine-Requirements.md**

## 2) Build the Steam Machine “clean port” (M.2 → OCuLink)
Goal: a **panel‑mounted OCuLink connector** so the external cable plugs into the chassis — not into a loose internal adapter.

High-level sequence:
1. Power down, unplug, discharge static.
2. Remove the internal NVMe drive (if present).
3. Install **M.2 (Key‑M) → OCuLink adapter** in the NVMe slot.
4. Run a short internal pigtail to a **rear panel OCuLink port**.
5. Add **strain relief** so cable pulls cannot stress the M.2 slot.
6. Close the case and confirm you did not block any fan or vent.

See: **docs/03-Internal-Mod.md**

## 3) Build the external dock (GPU + PSU + ports)
Goal: the dock is one clean box with controlled airflow.

Minimum dock features:
- OCuLink input (from Steam Machine)
- PCIe x16 slot on a dock board (physical x16; typically x4 electrically)
- PSU mount (SFX or ATX depending on your design)
- Space for a desktop GPU (size depends on your enclosure targets)
- Rear exits for:
  - GPU HDMI/DP
  - Dock power
  - (Optional) USB‑C pass-through to an internal USB‑C NVMe enclosure

See: **docs/04-Dock-Enclosure-Design.md**

## 4) Install SteamOS to the external NVMe (if needed)
If the internal NVMe is removed, install SteamOS to the USB‑C NVMe enclosure drive.

See: **docs/06-Operations.md**

## 5) Daily use rules (stability)
- Connect your TV/monitor **to the dock GPU** (HDMI/DP from the eGPU).
- Power on sequence: **dock PSU ON → Steam Machine ON**
- Power off sequence: **shutdown SteamOS → dock PSU OFF**
- Avoid disconnecting OCuLink while running.

See: **docs/06-Operations.md**

## 6) Thermals & validation
- Verify clean airflow (intake + exhaust) and dust filters.
- Run a long gaming load and confirm you are not hitting sustained thermal throttling.
- Fix airflow first (fans, filters, cable routing), then consider power limits/fan curves.

See: **docs/05-Thermals.md** and **docs/08-Validation.md**
