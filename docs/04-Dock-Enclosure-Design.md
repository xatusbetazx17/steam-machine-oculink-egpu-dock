# Dock Enclosure Design (GPU + PSU + Ports)

This document defines the **final design targets** for a clean “one-box” external dock:
- Holds a **desktop GPU**
- Holds a **PSU**
- Holds the **OCuLink → PCIe dock board**
- (Optional) Holds a **USB‑C NVMe enclosure** for SteamOS + games
- Exposes a tidy rear panel: **OCuLink + USB‑C + GPU HDMI/DP + Dock power**

---

## 1) Design goals

1. **Clean exterior**  
   Minimal visible cables, rear ports aligned, no dangling adapters.

2. **Mechanical safety**  
   GPU is secured. OCuLink cable plugs into a rigid connector. No stress on PCB connectors.

3. **Thermals first**  
   GPU has fresh intake air and a real exhaust path. Filters are accessible for cleaning.

4. **Universal compatibility (within reason)**  
   Enclosure targets a practical “max GPU size class” so most desktop GPUs can fit.

---

## 2) Two recommended enclosure approaches

### Option A — Mini‑ITX case conversion (recommended)
Use a small PC case that already supports:
- GPU mounting with PCI slot brackets
- SFX or ATX PSU mount
- Fan mounts + airflow path

**Why it’s easiest:** the GPU’s HDMI/DP ports naturally land on the rear panel via the normal bracket.

You only need to add:
- A rear **panel-mounted OCuLink port**
- A rear **USB‑C pass-through** (optional)

### Option B — Custom “console dock” enclosure (advanced)
A custom enclosure can look like a console accessory, but requires:
- Your own rear I/O plate design
- Your own GPU mount/bracket strategy
- Careful airflow ducting

If you want maximum “any GPU” support, Option A is usually the simplest.

---

## 3) GPU fit targets (size classes)

Because “any GPU” is impossible to guarantee (cards vary wildly), this project defines *size classes*.

### Recommended target: “Large / 3-slot capable”
Design for:
- GPU length: up to **330 mm**
- GPU thickness: up to **3-slot** (approx. 60 mm)
- GPU height: up to **150–160 mm**
- Power connectors: 2x 8‑pin **or** 12VHPWR (depends on GPU)

This covers a large portion of modern mid/high-end GPUs.

### Size class table (use in your repo docs)

| Class | GPU length | GPU thickness | Who it’s for |
|---|---:|---:|---|
| S (small) | ≤ 220 mm | ≤ 2-slot | very compact dock |
| M (standard) | ≤ 300 mm | ≤ 2.5-slot | most midrange GPUs |
| L (large) | ≤ 330 mm | ≤ 3-slot | “universal” target |
| XL (extreme) | > 330 mm | 3.5–4-slot | avoid unless building a large case |

> Tip: Always add clearance for **power plugs** on the GPU (top/side connectors may need extra room).

Use **templates/GPU-Fit-Worksheet.md** to record real measurements.

---

## 4) Internal layout (recommended)

### Layout concept (simple + reliable)
Keep GPU and PSU in distinct zones, and keep storage away from GPU exhaust.

```
[Front / Intake]                         [Rear / Exhaust + Ports]
┌───────────────────────────────────────────────────────────────────┐
│  GPU zone (fresh intake)            PSU zone                        │
│  ┌─────────────────────────┐        ┌─────────────────────────┐     │
│  │  GPU fans intake air     │        │ PSU intake not blocked  │     │
│  │  GPU exhaust to rear/side│        │ PSU exhaust to rear     │     │
│  └─────────────────────────┘        └─────────────────────────┘     │
│                                                                   │
│  (Optional) USB‑C NVMe enclosure mounted away from GPU exhaust     │
└───────────────────────────────────────────────────────────────────┘
Rear panel: OCuLink + (optional) USB‑C + GPU HDMI/DP + AC power
```

### Dock layout checklist
- [ ] GPU has a direct path to **fresh intake air**
- [ ] Dock has **at least 2 fans** (1 intake + 1 exhaust) if the GPU isn’t getting enough natural flow
- [ ] PSU intake is not pressed against a solid wall
- [ ] USB‑C NVMe enclosure is not sitting in the GPU exhaust stream
- [ ] Dust filters are removable without disassembling everything

---

## 5) Rear panel port plan (final look)

Minimum rear I/O:
- **GPU ports:** HDMI/DP (from the GPU bracket)
- **OCuLink port:** panel-mount (from Steam Machine → dock)
- **Dock power:** PSU AC inlet / cord
- Optional: **USB‑C pass-through** (Steam Machine → dock NVMe/hub)

Suggested rear layout (example):
```
┌───────────────────────────────────────────────────────┐
│  [GPU HDMI/DP bracket]   [OCuLink] [USB‑C]  [AC power] │
└───────────────────────────────────────────────────────┘
```

---

## 6) PSU integration (how to power the dock)

A desktop PSU normally expects a motherboard to signal “turn on”.
To run a PSU in a dock you need one of these patterns:

- **Pattern A (best):** Dock board provides ATX control features  
- **Pattern B (simple):** ATX 24‑pin jumper (PS_ON to GND) + PSU switch  
- **Pattern C (clean DIY):** External dock power switch module controlling PS_ON  

Keep mains wiring inside the PSU. Avoid custom AC wiring unless you know exactly what you’re doing.

---

## 7) “Dock spec” you can publish in your repo

If you want a single, clear published spec, here is a good baseline:

**Dock enclosure target spec (recommended)**
- Supports GPUs up to **330 mm length** and **3-slot thickness**
- Supports **SFX or ATX PSU** (pick one target to simplify the design)
- Minimum cooling: **2 case fans** + dust filters
- Rear ports: GPU HDMI/DP, OCuLink input, (optional) USB‑C pass-through, dock power
- Internal mounts: GPU support bracket or anti-sag support, tie-down points for cable management

---

## 8) Notes about performance expectations
This build typically uses an M.2 NVMe slot which is often **PCIe x4** electrically.
So:
- The dock slot is physical x16
- The actual link to the Steam Machine is often PCIe x4 (generation depends on the Steam Machine)

This is expected and normal for M.2-based eGPU builds.
