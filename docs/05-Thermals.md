# Thermals & Overheating Prevention

Heat is the #1 enemy of stability for small form-factor systems and external docks. This section defines:
- thermal targets
- airflow rules
- “what to change first” when temps are too high

---

## 1) Steam Machine thermal rules

- Do **not** place the Steam Machine directly on top of the dock exhaust.
- Leave clearance around Steam Machine vents: **a few inches on each side** is a good baseline.
- Keep the new internal OCuLink pigtail away from the Steam Machine fan intake/exhaust paths.

If you see higher CPU temps after the mod, re-check cable routing and airflow blockage.

---

## 2) Dock airflow rules (GPU + PSU)

### Minimum recommended
- At least **one intake** and **one exhaust** fan in the dock enclosure (if the enclosure is closed)
- Dust filters on intake(s)

### GPU airflow
- Ensure the GPU fans pull **fresh air**, not recycled hot air.
- Avoid sealed boxes with no real intake.

### PSU airflow
- Keep PSU intake unobstructed.
- PSU exhaust should exit the case cleanly (usually rear).

---

## 3) Practical thermal targets

### GPU target
Under a long gaming load:
- Aim to keep **GPU core temperature below the mid‑80s °C**
- Avoid **sustained thermal throttling**

Exact limits vary by GPU model, but “mid‑80s °C core” is a reasonable sanity target.

### Storage (USB‑C NVMe enclosure) target
- Keep the enclosure out of direct GPU exhaust.
- If the SSD throttles, move it to a cooler zone or add airflow.

---

## 4) If temperatures are too high: fix order

1) **Airflow first**
- Increase intake and exhaust
- Improve fan placement
- Clean filters
- Reduce cable clutter blocking air

2) **Fan curves next**
- Increase case fan speeds under load
- Adjust GPU fan curve (within safe limits)

3) **Power/voltage tuning last**
- Consider a small power limit reduction on the GPU
- Undervolt if you know what you’re doing

---

## 5) Noise vs cooling tips
- Use **larger fans** (120mm/140mm) if the enclosure allows
- Use rubber fan mounts to reduce vibration
- Keep dust filters clean; clogged filters raise temperatures quickly

---

## 6) Monitoring checklist
Recommended telemetry to watch during a long gaming session:
- GPU core temperature
- GPU hotspot temperature (if available)
- GPU clocks (watch for drops = throttling)
- GPU power draw
- Steam Machine CPU temperature
- SSD temperature (if readable)

Log results for 20–40 minutes of real gameplay to get meaningful data.
