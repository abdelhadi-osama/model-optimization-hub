# 🚀 Model Optimization Hub

Welcome to the **Model Optimization Hub**! This repository documents the journey of taking deep learning models from the research/training phase and making them blazing-fast, lightweight, and **ready for production**. 

This hub sits under the umbrella of the SAIR PyTorch module and explores the crucial steps of the deep learning inference optimization pipeline, including graph optimization, quantization, and edge deployment.

---

## 📚 Core Learning Resources

This repository is heavily inspired by and structured around the following foundational texts:

### 1. Ultimate ONNX for Deep Learning Optimization
<img src="https://m.media-amazon.com/images/I/71c6t42fGqL._SL1500_.jpg" alt="Ultimate ONNX Cover" width="250" align="right">

* **Author:** Meet Patel[cite: 1]
* **Focus:** Design, Optimize, and Deploy Deep Learning Models Using ONNX for Scalable Production and Edge AI Systems.[cite: 1]
* **Key Topics:** 
  * Overcoming the hurdles of deployment to build practical, performant systems at the edge.[cite: 1]
  * Model conversion from frameworks like PyTorch and TensorFlow into ONNX.[cite: 1]
  * Applying post-training quantization (PTQ) to shrink FP32 models into INT8 precision for faster compute.[cite: 1]
  * Utilizing tools like ONNX Simplifier and ONNX Runtime to prune redundant nodes and execute models efficiently.[cite: 1]

<br><br><br>

### 2. Deep Learning with PyTorch & Mastering PyTorch (2nd Ed.)
<img src="https://m.media-amazon.com/images/I/81Mv7J1eZKL._SL1500_.jpg" alt="Deep Learning with PyTorch Cover" width="250" align="right">

* **Authors:** Eli Stevens, Luca Antiga, and Thomas Viehmann (Deep Learning with PyTorch)
* **Focus:** 
  * **Mastering PyTorch (2nd Edition):** Chapter 13
  * **Deep Learning with PyTorch:** Chapter 15
* **Key Topics:** 
  * Extracting and compiling PyTorch models using **TorchScript**.
  * Detaching models from the heavy PyTorch Python dependency for C++ production environments.
  * Bridging the gap between the PyTorch training ecosystem and production deployment.

<br><br><br>

---

## 🗂️ Repository Structure

Our workspace is divided into specific pipelines to keep the learning modular and organized:

* 📁 **`onnx-ecosystem/`**
  * Contains notes, scripts, and exported `.onnx` models.
  * Explores the universal ONNX format, graph optimizations using ONNX Simplifier, and execution via ONNX Runtime.[cite: 1]
* 📁 **`torchscript-export/`**
  * Dedicated to PyTorch's native JIT compiler (TorchScript).
  * Contains examples of tracing and scripting PyTorch models for deployment without Python overhead.
* 📁 **`comparisons/`**
  * Benchmarks and workflow comparisons between deploying with ONNX Runtime versus TorchScript.
  * Notes on the pros and cons of each approach depending on the target hardware.

---

## 🎯 Primary Goal: Production Readiness

A model is only as good as its ability to run in the real world. This repository focuses on the "after-training" lifecycle:
1. **Exporting:** Translating models from PyTorch (`.pt`) into production-friendly formats (`.onnx` or TorchScript).
2. **Graph Optimization:** Fusing layers (like Conv+BatchNorm) and eliminating dead code.[cite: 1]
3. **Quantization:** Reducing the precision of weights (e.g., FP32 to INT8) to save memory and increase speed on edge devices.[cite: 1]
4. **Deployment:** Running inference efficiently using lightweight runtimes instead of heavy training frameworks.

---
*Created as part of the [SAIR_Jr Applied Deep Learning with PyTorch](https://github.com/SAIR-Org/SAIR_Jr/tree/main/4_Applied%20Deep%20Learning%20with%20PyTorch) track.*