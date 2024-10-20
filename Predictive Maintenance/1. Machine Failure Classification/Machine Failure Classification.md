# Machine Predictive Maintenance Classification

_For the Code click on the link_
[🔗 Code Section](https://github.com/SPritamDas/Portfolio-Projects/blob/main/Predictive%20Maintenance/1.%20Machine%20Failure%20Classification/predictive-maintenance-final-project.ipynb)

## Overview
This project aims to predict machine failures using a synthetic dataset that reflects real-world scenarios in predictive maintenance. It includes both binary classification to determine whether a machine has failed and multiclass classification to identify the type of failure.

---

## Dataset
The **Machine Predictive Maintenance Classification Dataset** consists of **10,000 data points** with **14 features**. This dataset simulates predictive maintenance situations commonly encountered in the industry.

### Dataset Features
| Feature                  | Description                                               |
|--------------------------|-----------------------------------------------------------|
| **UID**                  | Unique identifier ranging from 1 to 10,000               |
| **ProductID**            | Quality variants (L: Low, M: Medium, H: High)            |
| **Air Temperature [K]**  | Generated with a random walk process (σ = 2 K)           |
| **Process Temperature [K]** | Generated with a random walk process + 10 K (σ = 1 K) |
| **Rotational Speed [rpm]** | Calculated from 2860 W power with noise                |
| **Torque [Nm]**         | Normally distributed around 40 Nm (σ = 10 Nm)             |
| **Tool Wear [min]**     | Varies by quality variant (H/M/L: +5/3/2 minutes)         |
| **Target**               | Indicates machine failure (binary)                        |
| **Failure Type**         | Type of failure (multiclass)                             |

### Target Variables
**Important:** There are two targets. Avoid using either as features to prevent data leakage:
- **Target:** Failure or Not
- **Failure Type:** Type of Failure

| Target Variable       | Description                                  |
|-----------------------|----------------------------------------------|
| **Failure**           | 1 (Failed), 0 (Not Failed)                  |
| **Failure Type**      | Categories include Heat Dissipation, etc.   |

---

## Acknowledgements
Dataset derived from: [UCI AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset)

## Usability
- **License:** CC0: Public Domain
- **Expected Update Frequency:** Never

## Tags
- Earth and Nature
- Manufacturing
- Multiclass Classification
- Binary Classification
- Physics

---

## Dataset File
- [predictive_maintenance.csv](predictive_maintenance.csv) (531.01 kB)

### Label Distribution
| Failure Type              | Count | Percentage |
|---------------------------|-------|------------|
| **No Failure**            | 9,700 | 97%        |
| **Heat Dissipation Failure** | 100   | 1%         |
| **Other Failures**        | 200   | 2%         |


---

## Code
The code for this project can be found in the [notebook](https://github.com/SPritamDas/Portfolio-Projects/blob/main/Predictive%20Maintenance/1.%20Machine%20Failure%20Classification/predictive-maintenance-final-project.ipynb).
