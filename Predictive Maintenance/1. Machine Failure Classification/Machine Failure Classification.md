# Machine Predictive Maintenance Classification

## Overview
This project aims to predict machine failures using a synthetic dataset that reflects real-world scenarios in predictive maintenance. It includes binary classification to determine whether a machine has failed and multiclass classification to identify the type of failure.

## Dataset
The **Machine Predictive Maintenance Classification Dataset** consists of **10,000 data points** with **14 features**. The dataset is designed to simulate predictive maintenance situations typically encountered in the industry. Due to the challenges of obtaining and publishing real predictive maintenance datasets, this synthetic dataset has been created to fill that gap.

### Features
- **UID:** Unique identifier ranging from 1 to 10,000
- **ProductID:** Letter (L, M, H) indicating product quality variants:
  - L: Low (50% of all products)
  - M: Medium (30%)
  - H: High (20%)
- **Air Temperature [K]:** Generated using a random walk process normalized to a standard deviation of 2 K around 300 K
- **Process Temperature [K]:** Generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K
- **Rotational Speed [rpm]:** Calculated from power of 2860 W, overlaid with normally distributed noise
- **Torque [Nm]:** Normally distributed around 40 Nm with a standard deviation of 10 Nm (no negative values)
- **Tool Wear [min]:** Quality variants (H/M/L) add 5/3/2 minutes of tool wear
- **Target:** Indicates whether the machine has failed (binary)
- **Failure Type:** Type of failure (multiclass)

**Important:** There are two targets. Ensure not to use either of them as features to avoid data leakage:
- **Target:** Failure or Not
- **Failure Type:** Type of Failure

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

## Dataset File
- [predictive_maintenance.csv](predictive_maintenance.csv) (531.01 kB)

### Features Summary
| Feature                  | Description                        |
|--------------------------|------------------------------------|
| **UDI**                  | Unique Id                          |
| **Product ID**           | Product ID                         |
| **Air Temperature [K]**  | Air temp in K                     |
| **Process Temperature [K]** | Process temp in K               |
| **Rotational Speed [rpm]** | Rotational speed                 |
| **Torque [Nm]**         | Torque                             |
| **Tool Wear [min]**     | Tool wear in mins                 |
| **Target**               | If failed or not                  |
| **Failure Type**         | Type of failure                   |

### Label Distribution
- **No Failure:** 97%
- **Heat Dissipation Failure:** 1%
- **Other:** 2%
