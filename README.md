# Steam Machine OCuLink eGPU Dock (M.2 → OCuLink) — Documentation Pack

This repository is a **build + design documentation pack** for a clean external eGPU solution for a Steam Machine that **does not** expose a native OCuLink port or USB4/Thunderbolt eGPU port on the rear I/O.

**Core idea**
- Use the Steam Machine’s **internal M.2 Key‑M NVMe slot** as the PCIe “exit” via an **M.2 → OCuLink adapter**
- Put the **desktop GPU + PSU** in an **external dock enclosure**
- Run SteamOS + games from an **external USB‑C (10Gbps) NVMe SSD**, optionally mounted *inside* the dock for a clean look

```
Steam Machine (internal M.2 used for OCuLink)      External Dock (GPU + PSU + SSD)
┌──────────────────────────────────────────┐      ┌───────────────────────────────────┐
│  M.2 Key‑M → OCuLink → rear panel port   │=====>│  OCuLink → PCIe x16 slot → GPU     │
│                                          │      │  PSU powers GPU + dock board      │
│  USB‑C (10Gbps) → external NVMe SSD      │----->│  (optional) USB‑C NVMe inside     │
└──────────────────────────────────────────┘      └───────────────────────────────────┘
                         HDMI/DP from GPU to display
```

## Important warnings (read first)
- This is an **invasive hardware mod** (opening the Steam Machine, routing a PCIe cable, adding a panel port). You can **void warranty** and **permanently damage hardware** if done incorrectly.
- Treat the eGPU as **semi‑permanent**. Avoid “hot unplug”. **Power down** before disconnecting the OCuLink cable.
- Plan for **cooling**. A clean dock must still have a controlled intake/exhaust airflow path and dust filters.

(These warnings match the intent of the original concept guides this repo is based on.)

## What’s inside this repo
- A complete set of Markdown docs you can copy into a GitHub repo.
- “Spec checklists” for Steam Machine requirements (what must be true for the mod to work).
- Dock enclosure design targets (GPU size classes, airflow layouts, rear port layout).
- Risk + thermal guidance + troubleshooting + validation steps.

## Suggested repo structure
```
.
├─ README.md
├─ docs/
│  ├─ 00-Quickstart.md
│  ├─ 01-SteamMachine-Requirements.md
│  ├─ 02-BOM.md
│  ├─ 03-Internal-Mod.md
│  ├─ 04-Dock-Enclosure-Design.md
│  ├─ 05-Thermals.md
│  ├─ 06-Operations.md
│  ├─ 07-Troubleshooting.md
│  ├─ 08-Validation.md
│  ├─ 09-Legal-Safety.md
│  └─ 10-FAQ.md
└─ templates/
   ├─ Build-Checklist.md
   └─ GPU-Fit-Worksheet.md
```

## Start here
Go to **docs/00-Quickstart.md**.

---

## Credits / source notes
This documentation pack is derived from two concept PDFs prepared for Marcelo Collado (Dec 16, 2025):
- *SteamOS eGPU Clean Dock Build (M.2 → OCuLink concept)*
- *Steam Machine + OCuLink eGPU: Step‑by‑Step Visual Guide*

It is **not** an official Valve document.
