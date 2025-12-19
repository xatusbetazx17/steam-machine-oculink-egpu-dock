# Legal / Safety / Risk Notes

This project is a **community / hobby mod concept**. It is not an official Valve product.

## Warranty & damage risk
- Opening hardware and modifying chassis ports can void warranties.
- Incorrect installation can permanently damage:
  - motherboard M.2 slot
  - PCIe dock board
  - GPU
  - PSU
- You accept responsibility for your hardware.

## Electrical safety
- A PSU contains dangerous voltages. Do not open the PSU.
- Avoid DIY AC wiring. Use the PSU’s normal AC input and switch.
- Do not operate the dock if you see damaged insulation or exposed conductors.

## ESD (static) safety
- Use an anti-static strap when handling internal components.
- Avoid building on carpet.
- Store boards in anti-static bags.

## Hot-plug risk
This style of eGPU connection is **not** treated like a hot-plug USB device.
- Power down before disconnecting the OCuLink cable.
- Treat it as semi-permanent.

## Thermal risk
- High temperatures can cause instability, throttling, and component wear.
- Always design airflow first and keep dust filters clean.

## Fire safety
- Don’t block PSU/GPU vents.
- Don’t leave the dock running unattended the first few times. Validate thermals.
- Use a quality PSU and avoid no-name adapters/cables.
