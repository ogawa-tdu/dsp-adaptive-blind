# dsp-adaptive-blind
Educational Jupyter notebooks for adaptive and blind signal processing. A minimal, clean implementation set for educational demonstration and hands-on experimentation.

- Adaptive Signal Processing (LMS, ALE, ANC)
- Blind Source Separation (JADE, FastICA, SOBI)
- Designed for seminars, lectures, and hands-on practice.

Run notebooks directly in Google Colab via the badges below.  
Repository: https://github.com/ogawa-tdu/dsp-adaptive-blind

## Repository Structure
```
notebooks/  
├── ASP/  
│   └── DSP_ASP_01_LMS.ipynb
│   ├── DSP_ASP_02_ALE.ipynb
│   └── DSP_ASP_03_ANC.ipynb  
└── BSS/  
    ├── DSP_BSS_01_JADE.ipynb  
    ├── DSP_BSS_02_FastICA.ipynb  
    └── DSP_BSS_03_SOBI.ipynb  
```
### Algorithmic Structure

Adaptive Signal Processing
- LMS : System identification
- ALE : Periodic signal enhancement
- ANC : Reference-based noise cancellation

Blind Source Separation
- JADE / FastICA : Higher-order statistics (ICA)
- SOBI : Second-order statistical BSS

## Adaptive Signal Processing (ASP) Notebooks

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

## Blind Source Separation (BSS) Notebooks

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
- librosa (audio demo)

## Planned Additions
- ILRMA
- Deep Learning based BSS

## License
MIT License. Free for educational, research, and commercial use.
