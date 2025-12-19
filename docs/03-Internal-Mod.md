# Steam Machine Internal Mod (M.2 → OCuLink “Clean Port”)

Goal: install an **M.2 Key‑M → OCuLink adapter** and route it to a **rigid, panel-mounted external connector**.

A panel mount is strongly recommended because it protects the M.2 slot from plug/unplug force.

---

## Safety first
- Power down completely, unplug the power cable, and wait a minute.
- Discharge static (anti-static strap recommended).
- Never force connectors. If something needs force, something is wrong.

---

## 1) Pre-flight checks

### Confirm the correct M.2 slot
You want the **M.2 Key‑M NVMe** slot (normally used for an internal NVMe SSD).

Common mistake: buying an adapter meant for a Wi‑Fi M.2 slot.

### Confirm clearance
Check:
- space above the M.2 slot for the adapter board
- cable bend radius (avoid sharp folds)
- no fan blades or heatsink fins will rub the cable

---

## 2) Build steps (high level)

1. **Open the case** and locate the M.2 NVMe SSD.
2. **Remove the NVMe SSD** (if installed).
3. Install the **M.2 → OCuLink adapter** into the M.2 slot and secure with the M.2 screw.
4. Connect a **short internal OCuLink pigtail**.
5. Route the pigtail to your chosen rear panel spot.
6. Install a **panel-mount OCuLink port** on a rigid backplate.
7. Add **strain relief** inside the case:
   - The goal is that **tugging on the external cable does NOT stress the M.2 slot**.
8. Close the case after confirming:
   - the new cable does not block a fan intake/exhaust path
   - the cable cannot touch fan blades
   - the connector is aligned so the external cable plugs in straight

---

## 3) Strain relief patterns (recommended)

### Pattern A — “Tie-down near the port”
- Tie the pigtail to a case anchor point within 1–2 inches of the panel port.
- This makes the panel connector take the force, not the M.2 slot.

### Pattern B — “Clamp the cable”
- Use an adhesive cable clamp or small bracket to pin the cable lightly.
- Do not crush or kink the cable.

---

## 4) Panel port placement tips

Choose a location that:
- is structurally rigid (metal is ideal)
- allows a straight plug-in path
- leaves enough room behind the panel for the connector body
- does not interfere with existing rear I/O or vents

---

## 5) Common failure modes (avoid these)

- **Loose cable hanging out of the case** → eventually stresses the M.2 slot.
- **Sharp cable bends** → increases the chance of instability/disconnects.
- **No strain relief** → plug/unplug force transfers into the motherboard.
- **Cable routed across a fan intake** → higher temps + possible fan contact.
- **Mixing OCuLink connector types** → won’t connect correctly.

---

## 6) After-install checklist

- [ ] Panel port is solid (does not flex)
- [ ] Internal pigtail has strain relief
- [ ] No cable contact with fans/heatsinks
- [ ] The case closes without crushing the cable
- [ ] External cable plugs in smoothly and straight
