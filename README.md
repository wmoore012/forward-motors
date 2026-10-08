# Forward Motors

> **Archived.** Active work is in the course repo, [uncc-dl/Fall-2026-DSBA-6165-Group-10](https://github.com/uncc-dl/Fall-2026-DSBA-6165-Group-10) (`notebooks/02_stage3_eda.ipynb`). This repo stays public because that notebook loads `data/vin_recovery_candidates.csv.gz` from here; please don't delete or rename it.

DSBA 6165 Deep Learning project (UNC Charlotte), Mam Salan Njie and Will Moore.

Forward Motors helps used-car buyers decide which auction vehicles deserve a closer look before bidding, combining auction price prediction, prediction ranges and visible-damage detection.

## Stage 3: Data collection and analysis

[`Forward_Motors_Stage3_EDA_Final.ipynb`](Forward_Motors_Stage3_EDA_Final.ipynb) is the exploratory data analysis notebook. It includes the saved outputs from our run.

**To rerun:** open it in Google Colab and choose *Runtime → Run all*.

- **Part A, auction prices:** [Vehicle Sales Data](https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data) (Kaggle, version 1). Downloaded automatically with `kagglehub` and verified by SHA-256.
- **Part B, damage images:** [CarDD](https://cardd-ustc.github.io/). Our copy comes directly from the authors, who share it only after a licensing request. Anyone else gets a public Kaggle copy ([issamjebnouni/cardd](https://www.kaggle.com/datasets/issamjebnouni/cardd), about 3 GB), downloaded automatically. Its image, annotation and per-class counts match our release.

No data files are stored in this repository.
