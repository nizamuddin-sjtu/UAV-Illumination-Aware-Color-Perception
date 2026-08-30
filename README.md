# UAV Illumination-Aware Color Perception

Multi-task UAV color perception with uncertainty weighting, LOIO testing, and coverage-risk analysis.

## Overview

This project evaluates illumination-aware multi-task color perception for UAV systems. It includes color-only and bucket-classifier ablations, uncertainty weighting, leave-one-illumination-out testing, and decision-policy analysis.

## Highlights

- Multi-task color and illumination learning
- Uncertainty-weighted training
- LOIO and out-of-distribution evaluation
- Coverage-risk and failure analysis

## Notebook

The full experiment is provided in [uavpaper.ipynb](uavpaper.ipynb). It is configured for Kaggle and expects the datasets described in the notebook to be attached through the **Add Input** panel.

## Running the experiment

1. Create a Kaggle notebook or open the included notebook in Jupyter.
2. Attach the required dataset and enable a GPU accelerator where noted.
3. Install the listed dependencies.
4. Run the notebook from top to bottom.

`ash
pip install -r requirements.txt
`

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

## License

This project is available under the MIT License.
