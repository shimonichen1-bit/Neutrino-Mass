# Neutrino Mass Estimation via Beta Decay Spectrum - Physics Lab C

## Overview
This repository contains the data analysis, visualization, and source code for the Neutrino Mass experiment conducted as part of the Advanced Physics Laboratory C. 

This project investigates the continuous energy spectrum of electrons emitted during beta decay ($\beta^{-}$). While standard theory provides the fundamental framework for the decay shape, this study uses spectral and residual analysis of the Kurie plot to detect deviations near the endpoint energy, allowing us to place an upper limit on the neutrino rest mass.

The research focuses on the analytical processing of the digitized beta spectrum. Experimental Methodology is divided into two distinct analytical phases:

  1. Phase A: System Linearity Verification 
  2. Phase B: Kurie Plot Fitting & Endpoint Analysis – Applying Fermi function corrections to the raw beta spectrum and performing a linear fit near the endpoint energy ($E_0$) to estimate the neutrino mass.

## Project Structure
* [scripts/](scripts/) – Contains the core analysis code (e.g., `mca_linearity.py`).
* [data/](data/) – Raw experimental data files and MCA spectrum outputs.
* [output/](output/) – Final high-resolution graphs and vector plots (e.g., `mca_linearity_plot.pdf`).
* [report/](report/) – https://www.overleaf.com/read/ytwpfnbtzgqh#6df9f4.

## Requirements
To run the scripts, you will need:
* Python 3.x
* NumPy, SciPy, pandas, Matplotlib, os, and re

