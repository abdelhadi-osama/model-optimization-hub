# 🚀 Model Optimization Hub

Welcome to the **Model Optimization Hub**! This repository documents the journey of taking deep learning models from the research/training phase and making them blazing-fast, lightweight, and **ready for production**. 

This hub sits under the umbrella of the SAIR PyTorch module and explores the crucial steps of the deep learning inference optimization pipeline, including graph optimization, quantization, and edge deployment.

---

## 📚 Core Learning Resources

This repository is heavily inspired by and structured around the following foundational texts:


<div align="center">

<img src="https://img.shields.io/badge/REQUIRED_READING-MODEL_OPTIMIZATION-D32F2F?style=for-the-badge&logo=bookstack&logoColor=white" alt="Mandatory reading badge"/>

<table>
<tr>
<td align="center" width="33%">
<img src="https://imgs.search.brave.com/zEqR4U-XPtZaS6HU6kcJCfMz4290nSfKWb34hB3KT8E/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9tLm1l/ZGlhLWFtYXpvbi5j/b20vaW1hZ2VzL0kv/NDFwSnFiVEIxcEwu/anBn" alt="Deep Learning with PyTorch cover" width="150"/>
<br/>
<strong>Deep Learning with PyTorch</strong>
<br/>
<em>Eli Stevens, Luca Antiga, and Thomas Viehmann</em>
<br/><br/>
<img src="https://img.shields.io/badge/📖 Read_Chapter_15-Deployment-4CAF50?style=flat-square" alt="Read Chapter 15"/>
<br/><sub>Bridging PyTorch to production environments</sub>
</td>

<td align="center" width="33%">
<img src="https://imgs.search.brave.com/ms-KM4Lt2g2D0AtEKWqLc3XFNRf5QrWU16ehl5EeEd4/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9pNS53/YWxtYXJ0aW1hZ2Vz/LmNvbS9zZW8vTWFz/dGVyaW5nLVB5VG9y/Y2gtU2Vjb25kLUVk/aXRpb24tQ3JlYXRl/LWFuZC1kZXBsb3kt/ZGVlcC1sZWFybmlu/Zy1tb2RlbHMtZnJv/bS1DTk5zLXRvLW11/bHRpbW9kYWwtbW9k/ZWxzLUxMTXMtYW5k/LWJleS1QYXBlcmJh/Y2stOTc4MTgwMTA3/NDMwOF8zYTZhZGZk/NC05NTM5LTRlNzgt/YjY0OC05NzQ4NTQ1/MjNmNjEuNWE4Mjdj/YWI1YjkxZGUzYTQy/YzgzNjEzZWMxYTMw/NjUuanBlZz9vZG5I/ZWlnaHQ9NTczJm9k/bldpZHRoPTU3MyZv/ZG5CZz1GRkZGRkY" alt="Mastering PyTorch cover" width="150"/>
<br/>
<strong>Mastering PyTorch<br/>(2nd Edition)</strong>
<br/>
<em>Ashish Ranjan</em>
<br/><br/>
<img src="https://img.shields.io/badge/📖 Read_Chapter_13-TorchScript-2196F3?style=flat-square" alt="Read Chapter 13"/>
<br/><sub>Exporting and tracing PyTorch models</sub>
</td>

<td align="center" width="33%">
<img src="https://m.media-amazon.com/images/I/71c6t42fGqL._SL1500_.jpg" alt="Ultimate ONNX cover" width="150"/>
<br/>
<strong>Ultimate ONNX for Deep Learning Optimization</strong>[cite: 1]
<br/>
<em>Meet Patel</em>[cite: 1]
<br/><br/>
<img src="https://img.shields.io/badge/📖 Read_In_Parallel-ONNX_Ecosystem-EE4C2C?style=flat-square" alt="Read ONNX Book"/>
<br/><sub>Scalable production and Edge AI systems</sub>[cite: 1]
</td>
</tr>
</table>

</div>
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
