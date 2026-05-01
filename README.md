# KFC Chamchuri Square (Bangkok, Thailand) — Customer Flow 2D Simulation

A discrete-event and agent-based 2D simulation model of customer flow and service operations at **KFC Chamchuri Square**, built with **AnyLogic**.

https://maps.app.goo.gl/DAquki5JanYc8fpX7
---

## Overview

This simulation models the real-world customer journey inside the KFC outlet at Chamchuri Square — from arrival, queuing, ordering, and service, through to exit. It is designed to analyse bottlenecks, optimise staff allocation, and evaluate service efficiency under varying demand conditions.

---

## Project Files

| File | Description | Status |
|---|---|---|
| `KFC_V2.alp` | Version 2 — early baseline model; **map layout ratio is incorrect** | ⚠️ Deprecated |
| `KFC_V3.alp` | Version 3 — original layout with individual seats; **individual seat logic is incorrect** | ⚠️ Deprecated |
| `KFC_V4_normal.alp` | Version 4 — **before** adding kiosks; customers grouped by table (correct grouping logic) | ✅ Baseline |
| `KFC_V4_kiosk.alp` | Version 4 — **after** adding 2 kiosks; used for the business case comparison | ✅ Latest |

> **KFC V4 is the current and recommended version.** V2 and V3 are kept for reference only.
> All files are **AnyLogic Project (`.alp`)** files and must be opened individually in AnyLogic.

---

## Requirements

| Requirement | Details |
|---|---|
| **Software** | [AnyLogic](https://www.anylogic.com/) (Personal Learning Edition or higher) |
| **Minimum Version** | AnyLogic 8.x |
| **OS** | Windows / macOS / Linux |

> The Personal Learning Edition (PLE) of AnyLogic is free and sufficient to open and run both model files.

---

## Getting Started

### 1. Install AnyLogic
Download and install AnyLogic from the official website:
[https://www.anylogic.com/downloads/](https://www.anylogic.com/downloads/)

### 2. Open a Model File
1. Launch **AnyLogic**.
2. Go to **File → Open**.
3. Navigate to this project folder and select the appropriate file:
   - `KFC_V4_normal.alp` — **before kiosks** (V4 baseline, recommended starting point)
   - `KFC_V4_kiosk.alp` — **after kiosks** (V4 with 2 kiosks, for business case comparison)
   - `KFC_V3.alp` — original layout (individual seats — known issues, reference only)
   - `KFC_V2.alp` — earliest version (incorrect map ratio, reference only)
4. Click **Open**.

### 3. Run the Simulation
1. Click the **Run** button (▶) in the AnyLogic toolbar, or press **F5**.
2. The 2D simulation view will open showing the KFC floor layout with animated customer agents.
3. Use the on-screen controls to **pause**, **resume**, or **adjust the simulation speed**.

---

## Model Features

- **2D Animated Floor Layout** — Faithful representation of the KFC Chamchuri Square outlet
- **Customer Agent Behaviour** — Agents follow realistic paths: enter → queue → order → collect → exit
- **Arrival Rate Modelling** — Configurable customer arrival schedules (peak hours, off-peak)
- **Service Desks & Queues** — Multiple service counters with queue logic
- **Performance Metrics** — Real-time statistics including:
  - Average waiting time
  - Queue lengths
  - Customer throughput
  - Server utilisation rates

---

## Version Differences

| Feature | V2 | V3 | V4 Normal | V4 Kiosk |
|---|---|---|---|---|
| Core customer flow | ✓ | ✓ | ✓ | ✓ |
| Map layout ratio | ❌ Wrong | ✓ | ✓ | ✓ |
| Customer grouping | Individual | Individual ❌ | By table ✓ | By table ✓ |
| Kiosk scenario | ✗ | ✗ | ✗ (before) | ✓ (after) |
| Recommended for use | Reference only | Reference only | Baseline | Business case |

> **Use V4 files for all analysis.** V2 and V3 are archived for academic reference only.

---

## Business Case — Adding 2 Self-Service Kiosks

The V4 simulation was used to evaluate the financial impact of installing 2 kiosks at KFC Chamchuri Square.

### Simulation Results

| Metric | Before (V4 Normal) | After (V4 Kiosk) |
|---|---|---|
| Walkout Rate | 32.94% | 15.74% |
| Customers Recovered | — | ~47 persons |

### Revenue & ROI

| Item | Value |
|---|---|
| Revenue per head | 128 THB |
| Average group size | 1–4 persons (avg ~2) |
| Average spend per group | ~256 THB |
| Revenue saved (47 groups × 256 THB) | **12,032 THB / period** |
| Kiosk investment cost | 120,000 THB |
| Store-level operating profit margin | 15% |
| **Estimated ROI breakeven** | **~66 days** |

> Adding 2 kiosks reduces the walkout rate by ~17 percentage points, recovering approximately 47 customer groups per period and breaking even on the hardware investment in roughly **66 days** at a 15% operating margin.

---

## Folder Structure

```
KFC_V3/
├── KFC_V2.alp          # AnyLogic model — Version 2
├── KFC_V3.alp          # AnyLogic model — Version 3
├── 3d/                 # 3D assets and resources
├── LICENSE             # Apache 2.0 License (Non-Commercial)
└── README.md           # This file
```

---

## Authors

Developed as a **Final Project** for the **Database and Simulation** course.
Simulation study subject: KFC Chamchuri Square outlet operations.

---

## Contributing

Contributions are welcome for academic and research improvements. To contribute:

1. **Fork** this repository.
2. **Create a branch** for your feature or fix: `git checkout -b feature/your-feature-name`
3. **Commit** your changes with a clear message: `git commit -m "Add: description of change"`
4. **Push** to your branch: `git push origin feature/your-feature-name`
5. **Open a Pull Request** describing your changes.

Please ensure any contributed models or assets are original work or properly licensed. Do not submit content that violates KFC's intellectual property.

---

## License

Copyright © 2026. Licensed under the **Apache License, Version 2.0** with the following additional restriction:

> **Non-Commercial Use Only.** This project and all associated files may not be used, in whole or in part, for commercial purposes without explicit written permission from the authors.

You may use, reproduce, and distribute this work for **academic, educational, and research purposes only**, subject to the terms of the Apache 2.0 License.

Full license text: [https://www.apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)

All KFC branding and trademarks are the property of their respective owners and are used solely for simulation study purposes.
