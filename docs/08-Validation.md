# Validation & Test Plan

A clean build is not complete until it is:
- mechanically secure
- electrically safe
- thermally stable
- repeatable (boots the same way every time)

---

## 1) Mechanical validation

### Steam Machine side
- [ ] Panel port is rigid (no flex)
- [ ] Internal pigtail has strain relief
- [ ] Cable does not touch fan blades/heatsinks
- [ ] Case closes without crushing the cable

### Dock side
- [ ] GPU is secured (screws/bracket)
- [ ] GPU has anti-sag support if needed
- [ ] PSU is mounted securely
- [ ] No loose metal shavings or conductive debris
- [ ] Cables are tied down and not touching fan blades

---

## 2) Electrical validation

- [ ] PSU is a reputable unit (stable 12V rail)
- [ ] GPU power connectors fully seated
- [ ] Dock board power connectors fully seated
- [ ] No exposed mains wiring (keep AC inside PSU)

Optional (recommended):
- [ ] Use a multimeter to check for shorts if you did any custom wiring/mods.

---

## 3) Boot & detection tests

Perform 10 repeat boots using the correct power sequence:
1) Dock PSU ON
2) Steam Machine ON

Acceptance:
- GPU is detected every boot
- Display output from GPU is reliable

---

## 4) Load & thermal tests

### Test A — Real gameplay
- 20–40 minutes of a demanding game
- Record GPU core temp and clock stability
- Record Steam Machine CPU temp

Acceptance:
- No disconnects
- No sustained throttling beyond what is normal for your GPU
- GPU core not living above the mid‑80s °C for long stretches

### Test B — “Worst case” stress
- A GPU stress tool or a very demanding game scene
- Confirm dock airflow can keep temps stable

---

## 5) Cable stability tests
With the system OFF:
- Confirm cable does not wiggle the internal port
- Confirm strain relief prevents pulling on connectors

Never “wiggle test” cables while running.

---

## 6) Maintenance validation
- Confirm dust filters can be removed/cleaned without tearing down the whole dock.
