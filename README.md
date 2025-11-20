<div align="center">

# Radar-based Flood Nowcasting Using Machine Learning Algorithms: An Application in the Hydraulic Node of Milan

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Numpy](https://img.shields.io/badge/Numpy-✔-blue)](https://numpy.org/)
[![Pandas](https://img.shields.io/badge/Pandas-✔-blue)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-✔-orange)](https://matplotlib.org/)
[![Cartopy](https://img.shields.io/badge/Cartopy-✔-green)](https://scitools.org.uk/cartopy/docs/latest/)
[![Properscoring](https://img.shields.io/badge/Properscoring-✔-blue)](https://properscoring.readthedocs.io/)
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

Code release for the paper **"DA AGGIUNGERE"**

Paper: [\AGGIUNGERE]()

Data: [\AGGIUNGERE]()

---

## 📂 Repository Structure

This repository is organized into dedicated folders, each containing scripts for specific processing and analysis workflows. Below is a clear overview of each directory and its purpose.

- [**data/**](./data) - contains *`download_all`*, used to download **input** and **prediction files**, and shapefiles used in subsequent notebooks;
- [**ens/**](./ens) — contains *`{month}_{model}_ens`*, used to concatenate **input** and **prediction files** and visualize all 20 ensemble members;
- [**mean/**](./mean) — contains *`{month}_{model}_mean`*, used to compute the ensemble **mean**.
- [**std/**](./std) — contains *`{month}_{model}_std`*, used to compute the ensemble **standard deviation**.
- [**iqr/**](./iqr) — contains *`{month}_{model}_iqr`*, used to compute the ensemble **interquartile range** (IQR);
- [**com/**](./com) — contains *`{month}_ld_gpt_scores`*, used to calculate spatial metrics between observed and predicted rasters at the **meteorological context scale**;
- [**com_bac/**](./com_bac) — contains *`{month}_ld_gpt_scores_bac`*, used to calculate spatial metrics between observed and predicted rasters at the **hydrological context scale**.

---

## ⚙️ How to run

### Install dependencies
Clone the repository and install dependencies:

```bash
git clone https://github.com/<username>/LDCast-GPTCast-performance-evaluation.git
cd LDCast-GPTCast-performance-evaluation
pip install -r requirements.txt
```

Or, with Conda:

```bash
conda env create -f environment.yml
conda activate LDCast-GPTCast-eval
```

### Download input and prediction files

Open the notebook *`download_all`* in the [`data/`](./data) folder and download input and prediction files.

### Concatenate input and prediction files

Open the notebooks in the [`ens/`](./ens) folder and run them to concatenate input and prediction files and visualize the ensemble members.

### Compute ensemble statistics

After running the notebooks in [`ens/`](./ens), run the scripts in [`mean/`](./mean), [`std/`](./std) and [`iqr/`](./iqr) folders to compute ensemble mean, standard deviation and interquartile range. Note: if you are only interested in spatial metrics, running scripts in [`mean/`](./mean) is sufficient.

### Compute spatial metrics

Once ensemble statistics are calculated, you can run the scripts in [`com/`](./com) and [`com_bac/`](./com_bac) to compute spatial metrics at the meteorological and hydrological context scale.

---
