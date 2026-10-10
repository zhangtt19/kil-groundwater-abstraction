# Kil groundwater: abstraction and river exchange

**A steady-state MODFLOW case comparing 10 and 20 L/s pumping in an esker aquifer near Örebro, Sweden.**

[中文说明](README.zh-CN.md) · [All figures](docs/FIGURES.md) · [Models](models/README.md) · [Water budgets](data/water-budgets.csv)

![Groundwater model and revised head distribution](figures/revised-heads.png)

## Engineering question

What changes when groundwater abstraction is doubled? I developed a conceptual and numerical groundwater model to examine how additional pumping is balanced by recharge, drains and groundwater discharge to rivers.

The study combines geological interpretation, hydraulic-conductivity zoning, groundwater-head comparison and scenario water budgets. Its main decision point is the effect of pumping on groundwater–surface-water exchange.

## Model setup

| Item | Representation |
|---|---|
| Software | GMS / MODFLOW; steady-state analysis |
| Setting | Kil esker aquifer near Örebro; geological mapping from SGU |
| Grid | 20 × 20 m cells |
| Model bottom elevation | 30 m |
| Conductivity zones | 15, 20, 30, 46, 100 and 120 m/day |
| Recharge | (0.65 − 0.40) × 0.75 / 365 ≈ 0.000514 m/day |
| River stages | 43.9 and 44.0 m; corresponding bed elevations 42.9 and 43.0 m |
| Drain | Elevation 48 m; conductance 50 m²/day |
| Pumping | 10 L/s (864 m³/day) and 20 L/s (1,728 m³/day) |

![Conductivity zones](figures/conductivity-zones.png)

## Scenario water budgets

Values below are reported magnitudes. Recharge enters the groundwater model; the well, drains and net groundwater contribution to the river remove water.

| Component, m³/day | 10 L/s | 20 L/s |
|---|---:|---:|
| Recharge | 3,035.24 | 3,035.24 |
| Pumping | 864.00 | 1,728.00 |
| Drain outflow | 396.81 | 387.21 |
| Groundwater discharge to rivers | 1,774.42 | 920.01 |

Doubling pumping reduces the modelled groundwater contribution to rivers by **854.41 m³/day**, approximately **48%**. Most of the additional pumping is balanced by reduced river discharge from the aquifer. This percentage describes the groundwater budget component, rather than total river flow.

## Model assessment

![Head comparison](figures/head-comparison.png)

The analysis compares simulated and observed heads and adjusts the representation of topography. Remaining head discrepancies are relevant when interpreting the scenarios. The model supports a comparison of abstraction impacts under its steady-state assumptions; it does not establish a sustainable pumping limit from water balance alone.

## Files

The [gallery](docs/FIGURES.md) includes the catchment, geology, stratigraphy, conceptual model, model domain, head comparison and conductivity zoning. The [10 and 20 L/s archives](models/README.md) contain the GMS projects and MODFLOW input packages. Numerical budget values are also available as [CSV](data/water-budgets.csv).

Analysis: **Tianshu Zhang**.
