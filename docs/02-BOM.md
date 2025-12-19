# Bill of Materials (BOM)

This BOM is written to be vendor-neutral. The important part is **compatibility** (correct slot type, matching OCuLink connector type, PSU capacity, enclosure size).

> Tip: Match OCuLink connector type across adapter, cable, and dock (SFF variants must match).

---

## A) Steam Machine internal parts (the “clean port”)

| Item | Purpose | Notes |
|---|---|---|
| M.2 (Key‑M) → OCuLink adapter | Converts internal M.2 PCIe lanes to OCuLink | Must be **Key‑M NVMe**, not Wi‑Fi |
| Short internal OCuLink pigtail | Connects adapter to the panel port | Avoid sharp bends; add strain relief |
| Panel-mount OCuLink port / backplate | Rigid external connector | Metal backplate recommended |
| Strain relief hardware | Protects the M.2 slot | Clamp / zip tie mount / adhesive tie-down |
| Cable grommet / edge trim | Protects cables at cutouts | Optional if you cut metal/plastic |

---

## B) External dock core parts

| Item | Purpose | Notes |
|---|---|---|
| OCuLink → PCIe x16 dock board | Provides the physical PCIe x16 slot | Link is typically **PCIe x4** electrically |
| Desktop GPU | The eGPU | Size + power depend on enclosure targets |
| PSU (SFX or ATX) | Powers GPU + dock board | Choose wattage based on GPU |
| Enclosure / chassis | Holds everything | Mini‑ITX style cases are easiest |
| Case fans (at least 2) | Intake + exhaust airflow | Prefer larger fans if case allows |
| Dust filters | Keeps temps stable over time | Clean regularly |

---

## C) Storage for SteamOS + games (recommended)

| Item | Purpose | Notes |
|---|---|---|
| USB‑C (10Gbps) NVMe enclosure | External OS/game drive | Mount inside dock for clean look |
| NVMe SSD | SteamOS + games | Size based on library |
| High-quality USB‑C cable | Connects Steam Machine to dock | Short + reliable cable preferred |

Optional upgrades:
- USB hub inside the dock (rear USB-A ports)
- Ethernet adapter inside dock (rear RJ‑45 port)
- External power switch module for clean PSU control
- Temperature monitoring overlay (e.g., MangoHud) / fan tools

---

## D) Tools & supplies

- Precision screwdriver set
- Anti-static strap (recommended)
- Zip ties / Velcro straps
- Rubber grommets / edge trim
- Rotary tool / metal file (only if you cut a backplate)
- Thermal paste (only if you remove the CPU cooler)
- Multimeter (recommended for sanity checks)

---

## E) PSU sizing rule-of-thumb (safe, simple)
- Pick a **quality** PSU.
- Choose a wattage that covers **GPU power + headroom**.

Practical guidance:
- Midrange GPUs: often fine with **650W**
- Higher-end GPUs: consider **750–850W**
- Very high-end GPUs: check vendor recommendation and add headroom

Also confirm the PSU has the right connectors (6/8‑pin PCIe and/or 12VHPWR depending on the GPU).
