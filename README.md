<div align="center">

# Radar-based Flood Nowcasting Using Machine Learning Algorithms: An Application in the Hydraulic Node of Milan

![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

</div>

<br>

## 📌 Description
This repository contains tools and scripts for evaluating the **meteorological and hydrological performance** of two radar-based nowcasting models released by [Fondazione Bruno Kessler (FBK)](https://www.fbk.eu/):

- [**LDCast**](https://github.com/MeteoSwiss/ldcast)
- [**GPTCast**](https://github.com/DSIP-FBK/GPTCast)

The evaluation is carried out on two significant rainfall events over the **Seveso River basin (hydraulic node of Milan)**:
- **14 – 15 September 2023**
- **31 October – 1 November 2023**

The repository includes methods for:
- Visualization of radar precipitation forecasts vs observations
- Ensemble's basic statistics (Mean, Standard Deviation, Interquartile Range)
- Meteorological skill score calculation (CRPS, FSS, SAL, Rank Histogram)

---

## 📂 Repository Structure

This repository is organized into dedicated folders, each containing scripts for specific processing and analysis workflows. Below is a clear overview of each directory and its purpose.

- [**ens/**](./ens) — contains *`{month}_{model}_ens`*, used to download **prediction files** and visualize all 20 ensemble members;
- [**mean/**](./mean) — contains *`{month}_{model}_mean`*, used to compute the ensemble **mean**.
- [**std/**](./std) — contains *`{month}_{model}_std`*, used to compute the ensemble **standard deviation**.
- [**iqr/**](./iqr) — contains *`{month}_{model}_iqr`*, used to compute the ensemble **interquartile range** (IQR);
- [**com/**](./com) — contains *`{month}_ld_gpt_scores`*, used to calculate spatial metrics between observed and predicted rasters at the **meteorological context scale**;
- [**com_bac/**](./com_bac) — contains *`{month}_ld_gpt_scores_bac`*, used to calculate spatial metrics between observed and predicted rasters at the **hydrological context scale**.

---

## ⚙️ Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/<username>/nowcasting-evaluation-seveso.git
cd nowcasting-evaluation-seveso
pip install -r requirements.txt
```

Or, with Conda:

```bash
conda env create -f environment.yml
conda activate nowcasting-eval
```bash

