# FAQ

## Can this dock support “any desktop GPU”?
Not literally any GPU (sizes and power vary), but you can design the enclosure for a large “target class” (example: up to 330mm length and 3-slot thickness). Very large 4-slot GPUs may not fit unless you intentionally build a big case.

## Will performance be the same as a normal desktop?
Usually not identical. Many M.2-based eGPU builds run the GPU over a PCIe x4 link. That is still fast, but can bottleneck some workloads. Real impact depends on game, resolution, and GPU.

## Can I hot-plug the OCuLink cable?
Treat it as **not hot-plug friendly**. Shut down before disconnecting for best stability and to avoid risk.

## Do I need to move SteamOS to an external drive?
Only if the Steam Machine uses the only M.2 slot for the eGPU link. If the system has a second internal drive option, you can keep internal storage.

## Why does the monitor need to plug into the eGPU?
That makes the eGPU act as the primary graphics output and avoids extra overhead or complexity.

## Can I use a normal Thunderbolt eGPU enclosure instead?
Only if the Steam Machine supports USB4/Thunderbolt with eGPU support. This repo focuses on the M.2 → OCuLink method for systems that don’t.

## What’s the most common reason these builds fail?
Mechanical + cable issues:
- no strain relief
- sharp cable bends
- mixed connector types
- poor airflow

## How do I keep it looking clean?
- Panel-mount the ports (OCuLink and optionally USB‑C)
- Keep cables short and parallel
- Label both ends of cables
- Use a dock enclosure with a rear I/O panel
