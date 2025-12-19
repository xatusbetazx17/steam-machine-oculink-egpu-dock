# Steam Machine Requirements (Compatibility Checklist)

This project assumes a Steam Machine that *does not* expose a rear-panel eGPU interface (no OCuLink port, and potentially no USB4/Thunderbolt eGPU support). The workaround is to exit PCIe via the **internal M.2 Key‑M NVMe slot**.

## 1) Hard requirements (must be true)

### A. An M.2 Key‑M NVMe slot that carries PCIe lanes
You need an **M.2 “Key‑M” NVMe slot** (the slot typically used for an internal NVMe SSD).

- ✅ Works: M.2 Key‑M NVMe (PCIe x4) slot
- ❌ Does NOT work: M.2 Key‑E Wi‑Fi slot (common for Wi‑Fi cards)
- ❌ Does NOT work: mSATA, SATA-only sockets, proprietary SSD modules

**Why it matters:** the eGPU link is a PCIe link. If the slot does not carry PCIe lanes, an OCuLink adapter cannot provide a real eGPU connection.

### B. Physical access + clearance
You must be able to:
- Open the chassis (without destroying structural parts)
- Reach the M.2 slot
- Mount an adapter and route a short cable **without blocking fans/heatsinks**

### C. External boot support (if the M.2 slot is “consumed”)
If the Steam Machine only has *one* M.2 slot and you use it for OCuLink, you may need to run SteamOS from external storage.

Minimum:
- Ability to boot from a **USB storage** device (USB‑A or USB‑C)

Recommended:
- USB‑C port capable of **10Gbps** so a USB‑C NVMe enclosure performs well.

### D. BIOS/firmware stability
At minimum, the firmware should reliably:
- Enumerate the external PCIe device at boot (the eGPU dock)
- Allow the system to boot consistently with the dock connected and powered

## 2) Strongly recommended requirements (make the build easier)

### Two M.2 slots (best-case scenario)
If the Steam Machine has **two** M.2 slots:
- Use one for the internal NVMe SSD (keep internal storage)
- Use the other for the OCuLink exit

This is the cleanest “no external OS drive” version.

### A clean panel-mount location
The best builds add a **panel-mounted OCuLink port** so the cable plugs into the chassis, not into a loose internal adapter.

You want:
- A flat metal surface / backplate
- Space behind it for the connector
- Room for strain relief

## 3) “Future Steam Machine release” spec sheet (what to look for)
If you’re evaluating a *new* Steam Machine revision for this mod, check:

**Internal**
- M.2 NVMe Key‑M slot (PCIe x4 preferred)
- Enough clearance around the M.2 area for an adapter + short pigtail
- Case design that allows a clean rear port mod

**External I/O**
- USB‑C 10Gbps port (for external NVMe enclosure)
- Optional but great: USB4 / Thunderbolt (could support simpler eGPU options without internal mods)

**Thermals**
- Vents not blocked when placed next to the dock
- Internal cooling not compromised by cable routing

## 4) Compatibility “go / no-go” worksheet

Answer these before you buy parts:

- [ ] Does the Steam Machine have an **M.2 Key‑M NVMe** slot?
- [ ] Can you remove/replace the internal NVMe drive?
- [ ] Is there space to route a cable to a panel port without blocking fans?
- [ ] Can it boot from USB storage reliably?
- [ ] Do you have a plan for storage (external NVMe via USB‑C, or a second internal drive)?
- [ ] Are you OK with an invasive mod (warranty risk + hardware damage risk)?

If any of the first 4 are “No”, stop here — the build will likely not be viable without a different approach.
