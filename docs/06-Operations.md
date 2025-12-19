# Operations (SteamOS Setup + Daily Use)

This build is most stable when you treat the eGPU dock as a “semi-permanent” accessory and follow consistent power sequencing.

---

## 1) SteamOS storage plan

### Scenario A — Only one M.2 slot (common)
If the Steam Machine only has one M.2 slot and you used it for OCuLink, then:
- Install SteamOS + games to a **USB‑C NVMe enclosure**.
- Optionally mount that enclosure inside the dock so the outside stays clean.

### Scenario B — Two M.2 slots (best)
If the Steam Machine has two M.2 slots:
- Keep SteamOS on the internal NVMe.
- Use the second M.2 for the OCuLink eGPU link.

---

## 2) Installing SteamOS to the external NVMe (high level)

1. Put an NVMe SSD into the USB‑C enclosure.
2. Connect it to the Steam Machine.
3. Boot a SteamOS installer USB.
4. Install SteamOS onto the external NVMe drive.
5. In BIOS/firmware, set USB storage as the first boot device if needed.

> Important: Some systems behave differently based on USB port, cable quality, and enclosure chipset. If boot is flaky, try a different port/cable.

---

## 3) Display setup (critical)

For best performance and least complexity:
- Plug your TV/monitor **directly into the GPU in the dock** (HDMI/DP from the eGPU).
- Do not use the Steam Machine’s original HDMI/DP for gaming output when you intend to use the eGPU.

---

## 4) Power on / power off sequence (stability rules)

### Power ON
1. Turn **dock PSU ON** (GPU powered and ready)
2. Turn **Steam Machine ON**

### Power OFF
1. **Shut down SteamOS** fully
2. Turn **dock PSU OFF**

Avoid unplugging the OCuLink cable while the system is running.

---

## 5) Minimal cable list (final “clean look”)
A tidy finished setup usually shows only:

- OCuLink cable: Steam Machine → dock
- USB‑C cable: Steam Machine → dock (to external NVMe / hub)
- HDMI/DP cable: dock GPU → TV/monitor
- Power: Steam Machine power + dock PSU power

---

## 6) Maintenance schedule
- Every **2–8 weeks**: clean dust filters and check intakes.
- Every few months: re-check strain relief and connector tightness.
- After moving the setup: inspect panel ports and internal cable routing.
