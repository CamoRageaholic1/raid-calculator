# RAID Calculator

> **// EXPLOIT THE UNSEEN //**

![CAMOZERODAY](https://img.shields.io/badge/CAMOZERODAY-RAID%20Calculator-00d4ff?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-single--file-orange?style=for-the-badge)

A fully self-contained RAID array configuration and analysis tool with a dark cyberpunk terminal aesthetic. No build step, no dependencies — just open `index.html` in any browser.

## Features

- **All RAID Levels** — RAID 0, 1, 2, 3, 4, 5, 6, 10, 50, 60 (sorted in order)
- **Per-Drive Entry** — Each drive has its own capacity (GB/TB/PB) and RPM/type input
- **Live Mismatch Detection** — Real-time alerts for mixed HDD/SSD/NVMe arrays, RPM mismatches, and capacity differences
- **Hot Spare Support** — Add dedicated standby drives with independent speed validation
- **RAID 50/60 Groups** — Configurable sub-array grouping
- **Drive Array Visualization** — Color-coded disk map showing data, parity, and spare roles with mismatch rings
- **Capacity Efficiency Bar** — Visual storage efficiency meter
- **CAMOZERODAY Branding** — Skull shield logo embedded directly in the header

## Alert System

| Alert | Trigger |
|-------|---------|
| 🚫 Insufficient Drives | Drive count below RAID minimum |
| 💥 Zero Fault Tolerance | RAID 0 selected |
| ⚡ Mixed Drive Types | HDD + SSD/NVMe in same array |
| 🔄 RPM Mismatch | Different RPM drives in array |
| 📐 Capacity Mismatch | Different sized drives detected |
| ⚠️ Hot Spare Mismatch | Spare type/RPM differs from array |
| ⏱️ Rebuild Risk | RAID 5 with drives ≥ 4 TB |
| 🛡️ Dual Parity | RAID 6/60 confirmation |
| ✅ Healthy | All checks passed |

## Usage

```bash
git clone https://github.com/CamoRageaholic1/camozerod-raid-calculator.git
cd camozerod-raid-calculator
open index.html
```

Or just download `index.html` and open it directly — no server needed.

## RAID Level Reference

| Level | Min Drives | Fault Tolerance | Efficiency | Best For |
|-------|-----------|----------------|------------|----------|
| RAID 0 | 2 | None | 100% | Scratch/temp |
| RAID 1 | 2 | N-1 drives | 50% | OS/critical |
| RAID 2 | 3 | 1 drive | Varies | Legacy |
| RAID 3 | 3 | 1 drive | (N-1)/N | Sequential |
| RAID 4 | 3 | 1 drive | (N-1)/N | Legacy |
| RAID 5 | 3 | 1 drive | (N-1)/N | NAS/file server |
| RAID 6 | 4 | 2 drives | (N-2)/N | Large arrays |
| RAID 10 | 4 | 1 per mirror | 50% | Databases |
| RAID 50 | 6 | 1 per group | High | High-cap reads |
| RAID 60 | 8 | 2 per group | High | Enterprise |

## Tech Stack

- Vanilla HTML5 / CSS3 / JavaScript (ES6+)
- Google Fonts: Orbitron + Share Tech Mono
- Zero runtime dependencies
- CAMOZEROD logo embedded as base64 WebP

## License

MIT — do whatever you want with it.

---

*// EXPLOIT THE UNSEEN //*
