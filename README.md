<div align="center">

# TITOLO DEL PAPER/TESI

![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

</div>

<br>

## 📌 Description
This repository contains tools and scripts for evaluating the **meteorological and hydrological performance** of two radar-based nowcasting models released by [Fondazione Bruno Kessler (FBK)](https://www.fbk.eu/):

- **LDCast**
- **GPTCast**

The evaluation is carried out on two significant rainfall events over the **Seveso River Basin (Milan Hydraulic Node)**:
- **14–15 September 2023**
- **31 October–1 November 2023**

The repository includes methods for:
- Meteorological skill score calculation (e.g. CRPS, FSS, SAL)
- Hydrological validation with rainfall–runoff modeling
- Visualization of radar precipitation forecasts vs observations

---

## 📂 Repository Structure


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

