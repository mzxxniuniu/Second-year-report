# Ethical Robustness in Algorithmic Construction Scheduling

Pilot experiment data for the second-year progress report of a doctoral study at the University of Manchester.

## Data

`scheduler_results.csv` contains 11,200 rows from the pilot experiment: 100 project instances × 7 algorithm variants × 16 disruption cells.

### Columns

| Column | Description |
|--------|-------------|
| seed | Project instance index (0–99) |
| disruption | Mean disruption intensity δ (0.00, 0.10, 0.20, 0.30) |
| regime | Disruption type: uniform or heterogeneous |
| kappa | Beta precision parameter κ (4, 16, 64; blank for uniform) |
| algorithm | Crew-assignment algorithm variant |
| makespan | Project completion time |
| imbalance | Absolute workload difference between crews (φ_MM) |
| workload_A | Total workload assigned to Crew A |
| workload_B | Total workload assigned to Crew B |

### Algorithms

- **POOL-LBA**: Pool resource model with post-hoc load-balancing labels
- **SLOT-G-DEF / SLOT-G-LBA**: Slot model, greedy priority, default / load-balancing assignment
- **SLOT-LFT-DEF / SLOT-LFT-LBA**: Slot model, latest finish time priority
- **SLOT-RAND-DEF / SLOT-RAND-LBA**: Slot model, random priority

### Reproducibility

All results were generated with `PYTHONHASHSEED=17` (Python 3). Each project instance is seeded by its index (0–99).

## Contact

Zixuanxuan Ma, Department of Mechanical, Aerospace and Civil Engineering, University of Manchester.
