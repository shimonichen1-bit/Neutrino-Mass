# Neutrino-Mass

# Neutrino Mass Estimation via Beta Decay Spectrum Analysis

This repository contains the data processing, calibration, and statistical analysis pipelines for estimating the upper bound of the neutrino rest mass, conducted as part of Laboratory C (מעבדה ג') at Tel Aviv University.

##  Project Overview
The experiment investigates the continuous energy spectrum of electrons emitted during beta decay ($\beta^{-}$). By precisely analyzing the endpoint energy of the spectrum using a Kurie plot representation, we can deduce information regarding the missing energy carried away by the anti-neutrino, placing an upper limit on its rest mass.

The experimental setup consists of:
* A radioactive beta source.
* A plastic scintillator or detector system coupled with a PMT.
* An analog signal processing chain (Pre-amplifier, Main Amplifier, and Pulsers).
* A Multi-Channel Analyzer (MCA) for digitization and data acquisition.

---

##  Analysis Pipeline & Structure

The analysis is divided into three logical steps, corresponding to the scripts and execution order in this repository:

### 1. MCA Linearity Verification (`mca_linearity.py`)
Before converting channels to energy, we verify that the MCA electronic readout responds linearly to input pulse heights.
* **Method:** Pulses of varying relative amplitudes ($1/\text{Attenuation}$) are injected using a precision pulser. 
* **Peak Extraction:** Centroids are extracted via local **Gaussian fitting** to achieve sub-channel resolution.
* **Statistical Output:** An unweighted linear regression ($y = ax + b$) is performed. Instrumental and mechanical systematic uncertainties ($\sigma_{\text{sys}}$) are self-consistently quantified by forcing a reduced chi-squared $\chi_{\nu}^2 = 1$ on the residual scatter.

### 2. Energy Calibration (Upcoming)
* Translating the validated MCA channels into physical energy units (MeV) using known calibration gamma/beta sources and their corresponding Compton edges or conversion electron peaks.

### 3. Beta Spectrum & Kurie Plot Fitting (Upcoming)
* Processing the raw beta spectrum data.
* Applying the Fermi function corrections.
* Constructing a **Kurie Plot** to perform a linear fit near the endpoint energy ($E_0$), from which the neutrino mass limit is derived.

---

##  Prerequisites & Installation

To run the analysis scripts locally or within GitHub Codespaces, you need a Python 3 environment with the following scientific packages installed:

```bash
pip install numpy scipy matplotlib
