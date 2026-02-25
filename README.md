# Adaptive & Blind Signal Processing Notebooks
Educational Jupyter notebooks for adaptive and blind signal processing. A minimal, clean implementation collection for educational demonstration and hands-on experimentation.

- Adaptive Signal Processing (LMS, ALE, ANC)
- Blind Source Separation (JADE, FastICA, SOBI)
- Designed for seminars, lectures, and hands-on practice.

Run notebooks directly in Google Colab via the badges below.  
Repository: https://github.com/ogawa-tdu/dsp-adaptive-blind

Recommended Order:
FND → ASP → BSS

## Quick Start

1. Open a notebook using the **"Open in Colab"** badge.
2. Run all cells from top to bottom.
3. Modify key parameters (e.g., SNR, step size, filter order, lag number) and observe how the results change.

No installation is required if you use Google Colab.

### How to Experiment

These notebooks are designed for exploration.

- Change one parameter at a time and observe the effect.
- Try extreme values to understand failure cases.
- Compare time-domain and frequency-domain behavior.
- Ask: *Why does this work? When does it fail?*

Signal processing is best understood through controlled experimentation.

### Suggested Exploration Themes

- Stability vs. convergence speed (LMS step size)
- Noise level vs. recoverability (SNR)
- Model order vs. performance
- Assumptions vs. reality (stationarity, independence, etc.)

## Repository Structure
```
notebooks/  
├── ASP/  
│   ├── DSP_ASP_01_LMS.ipynb
│   ├── DSP_ASP_02_ALE.ipynb
│   ├── DSP_ASP_03_ANC.ipynb  
│   └── DSP_ASP_04_SysIdentification_Compare.ipynb  
├── BSS/  
│   ├── DSP_BSS_01_JADE.ipynb  
│   ├── DSP_BSS_02_FastICA.ipynb  
│   └── DSP_BSS_03_SOBI.ipynb
└── FND/
    ├── DSP_FND_01_Signal_and_Noise.ipynb
    └── DSP_FND_02_Wiener_filter.ipynb
```
### Algorithmic Structure

Adaptive Signal Processing
- LMS : System identification
- ALE : Periodic signal enhancement
- ANC : Reference-based noise cancellation

Blind Source Separation
- JADE / FastICA : Higher-order statistics (ICA)
- SOBI : Second-order statistical BSS

## Signal Processing Fundamentals (FND) Notebooks
Fundamental signal processing concepts and baselines for later algorithms (SNR, optimal filtering).

### Signal & Noise (SNR demonstration)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/FND/DSP_FND_01_Signal_and_Noise.ipynb)
Explores the relationship between SNR and signal clarity in both time and frequency domains.

### Wiener filter
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/FND/DSP_FND_02_Wiener_filter.ipynb)
Demonstrates theoretical optimal noise reduction using the Wiener filter (MMSE).
Explores frequency-domain gain design and practical limitations under real-world assumptions.

## Adaptive Signal Processing (ASP) Notebooks
Online/recursive parameter estimation: update a filter from data to track changing systems and environments.

### LMS
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/ASP/DSP_ASP_01_LMS.ipynb)
Adaptive filtering using LMS algorithm.
Demonstrates convergence behavior and coefficient identification.

### ALE
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/ASP/DSP_ASP_02_ALE.ipynb)
Noise reduction using Adaptive Line Enhancer (ALE). Demonstrates periodic component extraction from noisy signals.

### ANC
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/ASP/DSP_ASP_03_ANC.ipynb)
Adaptive Noise Cancellation (ANC) using LMS.
Implements a simplified feedforward ANC model without secondary path effects.

### SysID: LMS vs NLMS vs APA vs RLS (comparison)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/ASP/DSP_ASP_04_SysIdentification_Compare.ipynb)
Compares adaptive filters for system identification under white/colored inputs. Highlights convergence speed, stability, and parameter sensitivity (e.g., RLS forgetting factor).  
> ⚠️ **Note on RLS:**  
> RLS is sensitive to λ and initialization; inappropriate settings may cause instability.

## Blind Source Separation (BSS) Notebooks
Recover latent sources from mixtures using structural assumptions (e.g., independence, temporal diversity, low-rankness).

### JADE
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/BSS/DSP_BSS_01_JADE.ipynb)
Blind source separation using fourth-order statistics (JADE). Demonstrates separation via joint diagonalization of cumulant matrices.

### FastICA
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/BSS/DSP_BSS_02_FastICA.ipynb)
Blind source separation using fixed-point ICA (FastICA). Demonstrates the effect of nonlinearity selection on separation performance.

### SOBI
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ogawa-tdu/dsp-adaptive-blind/blob/main/notebooks/BSS/DSP_BSS_03_SOBI.ipynb)
Blind source separation using second-order statistics (SOBI). Demonstrates the impact of lag design on separation quality.

## Requirements
Tested on Google Colab (recommended)
- Python 3.9+
- NumPy
- SciPy
- Matplotlib
- librosa (optional, for audio demos)

## Planned Additions
### Signal Processing Fundamentals (FND)
- Ideal low-pass vs Wiener comparison
- Non-stationary noise example
- Causal FIR Wiener

### Adaptive Signal Processing (ASP)
- Widely Linear LMS
- Kalman Filter
- Sparse algorithm
### Blind Source Separation (BSS)
- Natural Gradient ICA
- Frequency domain ICA
- NMF based BSS
- Deep Learning based BSS
- Deep Unfolding based BSS

## License
MIT License. Free for educational, research, and commercial use.
