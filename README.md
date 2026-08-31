<h1 align="center">UAV Illumination-Aware Color Perception</h1>

<p align="center">
  <a href="https://doi.org/10.1109/I2CT61223.2024.10543537"><img src="https://img.shields.io/badge/Paper-IEEE_I2CT-2f6f9f.svg" alt="Paper"></a>
  <a href="uavpaper.ipynb"><img src="https://img.shields.io/badge/Notebook-uavpaper.ipynb-F37626.svg" alt="Notebook"></a>
  <a href="https://www.kaggle.com/nizamuddinmaitlo"><img src="https://img.shields.io/badge/Datasets-Kaggle-20BEFF.svg" alt="Kaggle datasets"></a>
  <a href="https://scholar.google.com/citations?user=bvyKhaEAAAAJ&hl=en"><img src="https://img.shields.io/badge/Publications-Google_Scholar-4285F4.svg" alt="Google Scholar"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/Code_License-MIT-2ea44f.svg" alt="MIT License"></a>
</p>

<p align="center"><b>Nizamuddin Maitlo</b></p>

<p align="center">Multi-task UAV color perception with uncertainty weighting, LOIO testing, and coverage-risk analysis.</p>

## 🔥 Overview

This repository evaluates illumination-aware multi-task color perception for UAV systems. It compares color-only and joint color/illumination models, uncertainty weighting, held-out-illumination testing, and selective decision policies.

## ✨ Contributions

- Multi-task color and illumination learning.
- Uncertainty-weighted training and targeted ablations.
- Leave-one-illumination-out and out-of-distribution evaluation.
- Coverage-risk, policy, and failure analysis.

## 🧪 Experimental protocol

- The notebook uses the nine-color, four-illumination folder hierarchy.
- Color-only, multi-task, non-uncertainty, and bucket-classifier variants are compared.
- Selective prediction is evaluated with coverage-risk tables and failure breakdowns.

## 📓 Notebook

The complete experiment is implemented in [uavpaper.ipynb](uavpaper.ipynb). Data discovery, preprocessing, training, evaluation, and export steps are kept together so the workflow can be reviewed and rerun from top to bottom.

## 🛠️ Installation

Create a Python environment and install the listed dependencies:

```bash
python -m pip install -r requirements.txt
```

The notebook is configured for Kaggle. A CUDA-capable GPU is recommended where GPU training is enabled.

## 📦 Datasets

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

| Resource | Purpose | Link |
|---|---|---|
| Different Colors in Challenging Lightening v2 | Multi-task color and illumination perception | [Kaggle dataset](https://www.kaggle.com/datasets/nizamuddinmaitlo/different-colors-in-challenging-lightening-v2) |

On Kaggle, attach the dataset through **Add Input** before running the notebook. External datasets remain subject to the licenses and terms on their source pages.

## 🚀 Running the experiment

### Kaggle

1. Upload or import [uavpaper.ipynb](uavpaper.ipynb).
2. Attach the dataset listed above through **Add Input**.
3. Enable a GPU accelerator when required by the configured model.
4. Run the notebook from top to bottom.

### Local Jupyter

```bash
python -m pip install -r requirements.txt
jupyter notebook uavpaper.ipynb
```

Dataset paths may need to be changed when running outside Kaggle.

## ♻️ Reproducibility

- Keep the documented train, validation, and test protocol unchanged when comparing models.
- Fit thresholds, calibration parameters, and feature transformations without using final test labels.
- Record the random seed, package versions, accelerator, and dataset version for each run.
- Treat saved tables and figures under the notebook's output directory as generated artifacts rather than source files.

## 📚 Paper information

The publications below describe the earlier challenging-light color-recognition work and the dataset used for illumination-aware evaluation.

| Publication | Venue | Year | Link |
|---|---|---:|---|
| Color Recognition in Challenging Lighting Environments: CNN Approach | 2024 IEEE 9th International Conference for Convergence in Technology (I2CT), 1–7 | 2024 | [DOI](https://doi.org/10.1109/I2CT61223.2024.10543537) |
| Color-in-Context: A 12K-Image Dataset for Color Recognition Under Varied Illumination | Preprints | 2026 | [DOI](https://doi.org/10.20944/preprints202604.0505.v1) |

## ⭐ Citation

For research building on this repository, cite the relevant publication or dataset descriptor:

```bibtex
@inproceedings{maitlo2024color,
  title     = {Color Recognition in Challenging Lighting Environments: CNN Approach},
  author    = {Maitlo, Nizamuddin and Noonari, Nooruddin and Ghanghro, Sajid Ahmed and Duraisamy, Sathishkumar and Ahmed, Fayaz},
  booktitle = {2024 IEEE 9th International Conference for Convergence in Technology (I2CT)},
  pages     = {1--7},
  year      = {2024},
  doi       = {10.1109/I2CT61223.2024.10543537}
}
```

```bibtex
@article{maitlo2026colorincontext,
  title   = {Color-in-Context: A 12K-Image Dataset for Color Recognition Under Varied Illumination},
  author  = {Maitlo, Nizamuddin and Noonari, Nooruddin and Ahmed, Fayaz and Hussain, Afifa},
  journal = {Preprints},
  year    = {2026},
  doi     = {10.20944/preprints202604.0505.v1}
}
```

## ⚠️ Scope and limitations

The benchmark does not reproduce every aerial camera, weather condition, material, or flight dynamic. Multi-task gains and coverage-risk settings should be revalidated for the target sensor and mission.

## 📄 License

Repository code is released under the [MIT License](LICENSE). Datasets and publications retain their own licenses and terms.

## 🤝 Acknowledgements

The experiments use public datasets, open-source Python libraries, and Kaggle compute infrastructure. We thank the dataset contributors and software maintainers who support reproducible research.
