# FMCNet: A Fourier-Guided Mamba-Convolution Hybrid Network for Efficient Hyperspectral Anomaly Detection

---

## Code Availability

The implementation of FMCNet will be made publicly available upon acceptance of the paper.

---

## Abstract

Hyperspectral anomaly detection (HAD) aims to identify rare and unknown targets that deviate from dominant background patterns in hyperspectral remote sensing imagery. Recent deep learning-based detectors have improved detection performance, but many of them rely on deeply stacked architectures or self-attention-based global modeling, resulting in non-negligible computational overhead when processing high-dimensional hyperspectral data. To address this accuracy--efficiency trade-off, we propose FMCNet, a Fourier-guided Mamba--convolution hybrid network for efficient hyperspectral anomaly detection. FMCNet adopts a depth-configurable dual-branch reconstruction architecture in which Fourier-basis priors are embedded before spectral state-space modeling and spatial convolutional modeling. In the spectral branch, spectral Fourier bias maps ordered selected-channel indices to channel-wise guidance terms and injects them before Mamba state-space modeling, thereby conditioning spectral dependency learning with Fourier-basis channel-order cues. In the spatial branch, adaptive Fourier positional encoding generates coordinate-aware cues and concatenates them with the input feature before depthwise separable convolution, thereby conditioning convolutional spatial modeling without self-attention-based pairwise spatial interactions. The spectral and spatial representations are further integrated by a spatial--spectral fusion gating module, which assigns competitive adaptive weights to the two branches to stabilize feature aggregation and suppress redundant background responses. The fused representation is used to reconstruct the hyperspectral background, and the anomaly map is generated from pixel-wise residuals between the input and reconstructed hyperspectral image. Experiments on six public hyperspectral datasets show that FMCNet achieves the highest AUC scores among the compared methods and provides a favorable accuracy--efficiency trade-off, with lower inference time than recent deep learning-based detectors.

---

## Detection Results

<p align="center"><img src="./images/DetectionResults.png" width="100%"></p>
<p align="center"><i>Detection results of different methods on the six real datasets</i></p>
