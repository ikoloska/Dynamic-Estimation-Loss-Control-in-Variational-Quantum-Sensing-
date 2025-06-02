# Dynamic Estimation Loss Control in Variational Quantum Sensing via Online Conformal Inference

This repository contains a Google Colab notebook exploring an online control framework for variational quantum sensing (VQS). The approach dynamically updates variational parameters and provides deterministic error bars on estimates using online conformal inference.

## Overview

This notebook implements a quantum-classical hybrid approach for variational quantum sensing (VQS). It integrates a Variational Quantum Circuit (VQC) with a classical Long Short-Term Memory (LSTM) network.

- **VQC:** Prepares the quantum probes using PennyLane.
- **LSTM:** Processes the measurements for estimation using PyTorch.
- **Conformal Prediction (ARC):** Provides estimation sets with guaranteed coverage based on LSTM outputs.
- **Training Loop:** Optimizes both VQC and LSTM parameters.

## Notebook Contents

The notebook is structured as follows:

1.  **Introduction:** Containing a brief description.
2.  **Imports and Setup:** Imports necessary libraries (PennyLane, PyTorch, NumPy, Matplotlib, etc.) and sets up the Google Colab environment (mounting Google Drive).
3.  **Variational Quantum Circuit (VQC) Definition:** Defines the VQC using PennyLane, including the circuit structure, gates, and parameters.
4.  **Classical LSTM Model:** Defines the LSTM model using PyTorch, including the layers and forward pass.
5.  **Adaptive Risk Control (ARC) Function:** Implements the ARC algorithm for constructing estimation sets based on LSTM output probabilities.
6.  **Training and Evaluation:** Contains the main training loop, including data generation, LSTM training, VQC training (using the soft set loss from ARC), and periodic evaluation of coverage and set size.
7.  **Results Visualization:** Plots the coverage and set size over training epochs.
8.  **Saving Results:** Saves the experimental results to a pickle file.

## Requirements

To run this notebook, you will need:

-   Google Colab environment
-   Python 3
-   Required libraries:
    -   `pennylane`
    -   `torch`
    -   `numpy`
    -   `matplotlib`
    -   `pandas`
    -   `sympy==1.12` (Note: A specific version is required)

These libraries are installed within the notebook using `!pip install`.

## Usage

1.  Open the notebook in Google Colab.
2.  Ensure you have a Google Drive account connected if you plan to save results, or change the lines of code where indicated to your location.
3.  Run the cells.

## Key Concepts

-   **Variational Quantum Sensing (VQS):** Utilizing quantum circuits with trainable parameters for sensing and estimation tasks.
-   **Quantum-Classical Hybrid Models:** Combining a variational quantum sensing probe with classical computational resources.
-   **Long Short-Term Memory (LSTM):** A type of recurrent neural network well-suited for sequential data.
-   **Conformal Inference:** A framework for producing estimation sets with guaranteed coverage, providing informative estimates.
-   **Adaptive Risk Control (ARC):** An algorithm within Conformal Inference that adaptively adjusts parameters to maintain a desired error rate.

## Potential Extensions

-   Implement the VQC on a real quantum hardware.
-   Explore different VQC architectures and entanglement strategies.
-   Experiment with different LSTM architectures or other classical models.
-   Apply the framework to different sensing tasks.
-   Investigate the impact of different Conformal Prediction algorithms and noise mitigation strategies.


## Citation

@article{nikoloska2025dynamic,
  title={Dynamic Estimation Loss Control in Variational Quantum Sensing via Online Conformal Inference},
  author={Nikoloska, Ivana and Joudeh, Hamdi and van Sloun, Ruud and Simeone, Osvaldo},
  journal={arXiv preprint arXiv:2505.23389},
  year={2025}
}
