# Simulation-Based Inference for Neutrino Parameter Tuning

## Overview

This repository implements a **Simulation-Based Inference (SBI)** framework for neutrino interaction parameter tuning. The model is trained on simulated datasets and used to infer posterior distributions for physics parameters governing neutrino cross sections and interaction modeling.

The framework is applied and evaluated on datasets corresponding to:

- MicroBooNE  
- T2K  
- NuWro  

The goal is to obtain calibrated posterior distributions for model parameters given observed binned event spectra.

---

## Methodology

We use neural posterior estimation (NPE) to approximate the posterior distribution

\[
p(\theta \mid x)
\]

where:

- \(\theta\) are neutrino interaction model parameters  
- \(x\) represents simulated or observed histogrammed data  

The model is trained on pairs \((\theta, x)\) generated from forward simulations. After training, the network provides amortized posterior inference for new observations.

---

## Features

- Neural posterior estimation using `sbi`
- Parameter normalization and inverse mapping
- Support for histogram-based likelihood-free inference
- Posterior sampling and diagnostics
- Coverage validation using:
  - Simulation-Based Calibration (SBC)
  - TARP diagnostic
- Evaluation on MicroBooNE, T2K, and NuWro datasets

---

## Repository Structure

