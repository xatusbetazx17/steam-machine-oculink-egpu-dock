# Troubleshooting

Start with the simple “physical layer” checks first: cable seating, power sequence, and display wiring.

---

## 1) No display on monitor/TV
### Checklist
- [ ] Monitor/TV is connected to the **dock GPU** (HDMI/DP on the GPU), not the Steam Machine
- [ ] Dock PSU is ON
- [ ] GPU is fully seated in the PCIe slot
- [ ] OCuLink cable is fully seated (both ends)
- [ ] Try a different HDMI/DP cable or a different GPU output port

---

## 2) GPU not detected in SteamOS
### Checklist
- [ ] Confirm the power sequence: dock PSU ON first, then Steam Machine ON
- [ ] Power down fully and re-seat:
  - GPU in the dock slot
  - OCuLink cable
- [ ] Confirm the dock board is powered correctly by the PSU
- [ ] Confirm you did not mix OCuLink connector types (SFF variants must match)

---

## 3) Random disconnects / instability under load
Most common causes:
- cable strain near connectors
- sharp cable bends
- overheating
- insufficient power delivery

### Checklist
- [ ] Add / improve strain relief (both Steam Machine and dock side)
- [ ] Reroute cable to avoid sharp bends
- [ ] Improve dock airflow and clean filters
- [ ] Confirm PSU wattage and connectors are correct for your GPU
- [ ] Re-check that the dock board power connectors are firmly seated

---

## 4) High temperatures
### GPU running hot
- Increase dock intake/exhaust airflow first
- Ensure GPU fans have fresh intake air
- Move the USB‑C NVMe enclosure away from GPU exhaust

### Steam Machine running hotter after mod
- Confirm the internal pigtail is not blocking airflow
- Check that the case fully closes and vents aren’t obstructed

---

## 5) External NVMe boot issues
- Try a different USB‑C cable (short, high-quality)
- Try a different USB port
- Update BIOS/firmware if possible
- Some enclosures are more boot-friendly than others; test early before final assembly

---

## 6) “It works sometimes” (intermittent)
Intermittent behavior is often:
- a connector not fully seated
- cable bend strain
- heat-related throttling/disconnect

Simplify to debug:
1) Run with the dock open-air temporarily (better cooling, easy access)
2) Use the shortest stable cable routing
3) Re-introduce the enclosure once stable
