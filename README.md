# 🏭 Production Scheduling Optimization — Indonesia
**Case Study: Solo Batik Factory · Bandung Garment Factory · Jepara Furniture Factory**

This project implements and benchmarks 4 classic production scheduling algorithms on a real-world-inspired dataset from Indonesian manufacturing industries.

## Algorithms Implemented

| Algorithm | Optimization Objective | File |
|-----------|----------------------|------|
| **SPT** – Shortest Processing Time | Minimize total completion time | `src/SPT.py` |
| **WSPT** – Weighted Shortest Processing Time | Minimize total weighted completion time (∑wC) | `src/WSPT.py` |
| **EDD** – Earliest Due Date | Minimize maximum lateness | `src/EDD.py` |
| **Johnson's Rule** | Minimize makespan (2-machine flow shop) | `src/JohnsonRule.py` |

## Project Structure

```
production-scheduling/
├── data/
│   └── jobs_dataset.csv               # 30 production jobs from 3 Indonesian factories
├── notebooks/
│   └── production_scheduling.ipynb    # Full analysis + visualizations
└── src/
    ├── SPT.py
    ├── WSPT.py
    ├── EDD.py
    └── JohnsonRule.py
```

## Dataset

30 production jobs from three Indonesian factories:
- **Solo Batik Factory** – hand-drawn, stamped, and printed batik
- **Bandung Garment Factory** – modern batik clothing
- **Jepara Furniture Factory** – teak, mahogany, and rattan furniture

| Column | Description |
|--------|-------------|
| `job_id` | Unique job identifier |
| `job_name` | Product / job name |
| `processing_time` | Processing duration (hours) |
| `weight` | Job priority weight (1–5) |
| `due_date` | Deadline (hours from time 0) |
| `arrival_time` | Job arrival time |
| `factory` | Factory name |

## Getting Started

**Run the full notebook:**
```bash
jupyter notebook notebooks/production_scheduling.ipynb
```

**Run individual algorithms:**
```bash
cd src
python SPT.py
python WSPT.py
python EDD.py
python JohnsonRule.py
```

## Output Charts

- Gantt charts for all 4 algorithms side-by-side
- Bar chart comparison of tardiness, completion time, and weighted cost
- Per-factory tardiness analysis
- Algorithm recommendation summary

## Requirements

```
pandas
numpy
matplotlib
```

## Key Insights

| Business Goal | Best Algorithm |
|--------------|---------------|
| Meet customer deadlines | **EDD** |
| Prioritize high-value orders | **WSPT** |
| Maximize throughput | **SPT** |
| 2-machine flow shop makespan | **Johnson's Rule** |

---
*Dataset simulated based on Indonesian manufacturing industry characteristics*
