# Awesome Quantization

A curated list of research papers, methods, and surveys on **neural network quantization** for efficient deep learning, covering techniques across **vision, language, and multimodal models**.

---

##  Categories Overview

| Category | Description | Typical Goal | Example Models / Domains |
|----------|-------------|--------------|--------------------------|
| **Post-Training Quantization (PTQ)** | Quantizing a pre-trained model without retraining (or with minimal calibration). Often uses a small calibration set. | Reduce model size & latency with minimal accuracy loss and no full retraining. | CNNs, ViTs, LLMs |
| **Quantization-Aware Training (QAT)** | Simulating quantization effects during training to improve performance after deployment. | Achieve high accuracy at low bit-width by adapting weights/activations during training. | Image classification, NLP, speech recognition |
| **Mixed-Precision Quantization** | Assigning different bit-widths to different layers, channels, or parameters based on importance. | Balance accuracy and efficiency by using high precision where needed and low precision elsewhere. | CNNs, ViTs, RNNs, LLMs |
| **Data-Free & Zero-Shot Quantization** | Quantization without access to original training data (or with synthetic/generated data). | Enable quantization in privacy-sensitive or data-unavailable scenarios. | LLMs, Transformers, vision backbones |
| **Hardware-Aware Quantization** | Designing quantization schemes with target hardware constraints in mind. | Maximize speedup and energy efficiency on specific devices (e.g., FPGA, GPU, mobile). | Edge AI, embedded systems |
| **Surveys & Overviews** | Review papers summarizing quantization methods, trends, and applications. | Provide newcomers with a structured understanding of the field. | Cross-domain |




---

## **Post-Training Quantization (PTQ)**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| Quantizing Deep Convolutional Networks for Efficient Inference: A Whitepaper | R. Krishnamoorthi | arXiv | 2018 | [PDF](https://arxiv.org/abs/1806.08342) |
| A White Paper on Neural Network Quantization | M. Nagel, M. Fournarakis, R. A. Amjad, Y. Bondarenko, M. Van Baalen, T. Blankevoort | arXiv | 2021 | [PDF](https://arxiv.org/abs/2106.08295) |
| PTQ4ViT: Post-Training Quantization for Vision Transformers with Twin Uniform Quantization | Z. Yuan, C. Xue, Y. Chen, Q. Wu, G. Sun | ECCV | 2022 | [PDF](https://arxiv.org/abs/2208.06861) |
| RAPQ: Rescuing Accuracy for Power-of-Two Low-Bit Post-Training Quantization | H. Yao, P. Li, J. Cao, X. Liu, C. Xie, B. Wang | IJCAI | 2022 | [PDF](https://arxiv.org/abs/2205.12918) |
| Instance-Aware Group Quantization for Vision Transformers | J. Moon, D. Kim, J. Cheon, B. Ham | CVPR | 2024 | [PDF](https://arxiv.org/abs/2403.08107) |
| Towards Efficient Post-Training Quantization of Pre-trained Language Models | H. Bai, L. Hou, L. Shang, X. Jiang, I. King, M. R. Lyu | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2210.07117) |
| Towards Next-Level Post-Training Quantization of Hyper-Scale Transformers | J. Kim, C. Lee, E. Cho, K. Park, H. Y. Kim, J. Kim, Y. Jeon | NeurIPS | 2024 | [PDF](https://arxiv.org/abs/2406.05339) |
| A Frustratingly Easy Post-Training Quantization Scheme for LLMs | Y. Jeon, C. Lee, K. Park, H. Y. Kim | EMNLP | 2023 | [PDF](https://arxiv.org/abs/2309.14273) |
| LQER: Low-Rank Quantization Error Reconstruction for LLMs | C. Zhang, J. Cheng, G. A. Constantinides, Y. Zhao | ICML | 2024 | [PDF](https://arxiv.org/abs/2402.14727) |
| PD-Quant: Post-Training Quantization Based on Prediction Difference Metric | J. Liu, L. Niu, Z. Yuan, D. Yang, X. Wang, W. Liu | CVPR | 2022 | [PDF](https://arxiv.org/abs/2203.08246) |
| LeanQuant: Accurate and Scalable Large Language Model Quantization with Loss-Error-Aware Grid | T. Zhang, A. Shrivastava | ICLR | 2025 | [PDF](https://arxiv.org/abs/2410.14679) |
| CBQ: Cross-Block Quantization for Large Language Models | X. Ding, X. Liu, Z. Tu, Y. Zhang, W. Li, J. Hu, H. Chen, Y. Tang, Z. Xiong, B. Yin, Y. Wang | ICLR | 2025 | [PDF](https://arxiv.org/abs/2410.12180) |
| AdaLog: Post-Training Quantization for Vision Transformers with Adaptive Logarithm Quantizer | Z. Wu, J. Chen, H. Zhong, D. Huang, Y. Wang | ECCV | 2024 | [PDF](https://arxiv.org/abs/2403.14525) |
| CL-Calib: Enhancing Post-Training Quantization Calibration through Contrastive Learning | Y. Shang, G. Liu, R. R. Kompella, Y. Yan | CVPR | 2024 | [PDF](https://arxiv.org/abs/2403.07877) |
| Outlier-Aware Slicing for Post-Training Quantization in Vision Transformer | Y. Ma, H. Li, X. Zheng, F. Ling, X. Xiao, R. Wang, S. Wen, F. Chao, R. Ji | ICML | 2024 | [PDF](https://arxiv.org/abs/2402.05214) |
| I&S-ViT: An Inclusive & Stable Method for Pushing the Limit of Post-Training ViTs Quantization | Y. Zhong, J. Hu, M. Chen, R. Ji | arXiv | 2024 | [PDF](https://arxiv.org/abs/2311.10126) |
| Oscillation-Free Quantization for Low-Bit Vision Transformers | S.-Y. Liu, Z. Liu, K.-T. Cheng | ICML | 2023 | [PDF](https://arxiv.org/abs/2302.08614) |
| Solving Oscillation Problem in Post-Training Quantization through a Theoretical Perspective | Y. Ma, H. Li, X. Zheng, X. Xiao, R. Wang, S. Wen, X. Pan, F. Chao, R. Ji | CVPR | 2023 | [PDF](https://arxiv.org/abs/2303.10863) |
| One-Step Forward and Backtrack: Overcoming Zig-Zagging in Loss-Aware Quantization Training | L. Ma, Y. Zhou, J. Ma, G. Yu, Q. Li | AAAI | 2024 | [PDF](https://arxiv.org/abs/2312.01792) |
| Overcoming Oscillations in Quantization-Aware Training | M. Nagel, M. Fournarakis, Y. Bondarenko, T. Blankevoort | ICML | 2022 | [PDF](https://arxiv.org/abs/2203.08605) |
| Retraining-Free Model Quantization via One-Shot Weight-Coupling Learning | C. Tang, Y. Meng, J. Jiang, S. Xie, R. Lu, X. Ma, Z. Wang, W. Zhu | CVPR | 2024 | [PDF](https://arxiv.org/abs/2404.00793) |
| Q-DETR: An Efficient Low-Bit Quantized Detection Transformer | S. Xu, Y. Li, M. Lin, P. Gao, G. Guo, J. Lü, B. Zhang | CVPR | 2023 | [PDF](https://arxiv.org/abs/2303.12678) |
| Q-ViT: Accurate and Fully Quantized Low-Bit Vision Transformer | Y. Li, S. Xu, B. Zhang, X. Cao, P. Gao, G. Guo | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2210.06706) |
| ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers | Z. Yao, R. Y. Aminabadi, M. Zhang, X. Wu, C. Li, Y. He | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2206.01861) |
| Leveraging Inter-Layer Dependency for Post-Training Quantization | D. Zheng, Y. Liu, L. Li, et al. | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2210.04887) |
| AphQ-ViT: Post-Training Quantization with Average Perturbation Hessian Based Reconstruction for Vision Transformers | Z. Wu, J. Zhang, J. Chen, J. Guo, D. Huang, Y. Wang | CVPR | 2025 | [PDF](https://arxiv.org/abs/2403.14082) |
| Boost Vision Transformer with GPU-Friendly Sparsity and Quantization | C. Yu, T. Chen, Z. Gan, J. Fan | CVPR | 2023 | [PDF](https://arxiv.org/abs/2304.05114) |
| Bit-Shrinking: Limiting Instantaneous Sharpness for Improving Post-Training Quantization | C. Lin, B. Peng, Z. Li, W. Tan, Y. Ren, J. Xiao, S. Pu | CVPR | 2023 | [PDF](https://arxiv.org/abs/2303.10084) |
| QuantSR: Accurate Low-Bit Quantization for Efficient Image Super-Resolution | H. Qin, Y. Zhang, Y. Ding, Y. Liu, X. Liu, M. Danelljan, F. Yu | NeurIPS | 2023 | [PDF](https://arxiv.org/abs/2310.02500) |
| Memory-Efficient Fine-Tuning of Compressed Large Language Models via Sub-4-Bit Integer Quantization | J. Kim, J. H. Lee, S. Kim, J. Park, K. M. Yoo, S. J. Kwon, D. Lee | NeurIPS | 2023 | [PDF](https://arxiv.org/abs/2310.07031) |
| QERA: An Analytical Framework for Quantization Error Reconstruction | C. Zhang, J. T. H. Wong, C. Xiao, G. A. Constantinides, Y. Zhao | ICLR | 2025 | [PDF](https://arxiv.org/abs/2410.07971) |
| GPTQ: Accurate Post-Training Quantization for Generative Pre-Trained Transformers | E. Frantar, S. Ashkboos, T. Hoefler, D. Alistarh | ICLR | 2023 | [PDF](https://arxiv.org/abs/2210.17323) |
| RPTQ: Reorder-Based Post-Training Quantization for Large Language Models | Z. Yuan, L. Niu, J. Liu, W. Liu, X. Wang, Y. Shang, G. Sun, Q. Wu, J. Wu, B. Wu | arXiv | 2023 | [PDF](https://arxiv.org/abs/2304.01089) |
| Quantization Without Tears | M. Fu, H. Yu, J. Shao, J. Zhou, K. Zhu, J. Wu | CVPR | 2025 | [PDF](https://arxiv.org/abs/2503.05725) |
| Learnable Lookup Table for Neural Network Quantization | L. Wang, X. Dong, Y. Wang, L. Liu, W. An, Y. Guo | CVPR | 2022 | [PDF](https://arxiv.org/abs/2203.14694) |
| OWQ: Lessons Learned from Activation Outliers for Weight Quantization in Large Language Models | C. Lee, J. Jin, T. Kim, H. Kim, E. Park | arXiv | 2023 | [PDF](https://arxiv.org/abs/2306.02272) |
| SqueezeLLM: Dense-and-Sparse Quantization | S. Kim, C. Hooper, A. Gholami, Z. Dong, X. Li, S. Shen, M. W. Mahoney, K. Keutzer | ICML | 2024 | [PDF](https://arxiv.org/abs/2306.07629) |
| REX: Data-Free Residual Quantization Error Expansion | E. Yvinec, A. Dapogny, M. Cord, K. Bailly | NeurIPS | 2023 | [PDF](https://arxiv.org/abs/2310.19415) |
| PTQ4SAM: Post-Training Quantization for Segment Anything | C. Lv, H. Chen, J. Guo, Y. Ding, X. Liu | CVPR | 2024 | [PDF](https://arxiv.org/abs/2403.07938) |
| BRECQ: Pushing the Limit of Post-Training Quantization by Block Reconstruction | Y. Li, R. Gong, X. Tan, Y. Yang, P. Hu, Q. Zhang, F. Yu, W. Wang, S. Gu | ICLR | 2021 | [PDF](https://arxiv.org/abs/2102.05426) |
| Post-Training Quantization for Vision Transformer | Z. Liu, Y. Wang, K. Han, S. Ma, W. Gao | NeurIPS | 2021 | [PDF](https://arxiv.org/abs/2107.07988) |
| Clamp-ViT: Contrastive Data-Free Learning for Adaptive Post-Training Quantization of ViTs | A. Ramachandran, S. Kundu, T. Krishna | ECCV | 2024 | [PDF](https://arxiv.org/abs/2403.05497) |
| Fine-Grained Data Distribution Alignment for Post-Training Quantization | Y. Zhong, M. Lin, M. Chen, K. Li, Y. Shen, F. Chao, Y. Wu, R. Ji | ECCV | 2022 | [PDF](https://arxiv.org/abs/2208.09503) |
| NoisyQuant: Noisy Bias-Enhanced Post-Training Activation Quantization for Vision Transformers | Y. Liu, H. Yang, Z. Dong, K. Keutzer, L. Du, S. Zhang | CVPR | 2023 | [PDF](https://arxiv.org/abs/2303.07900) |
| ClimbQ: Class Imbalanced Quantization Enabling Robustness on Efficient Inferences | T.-A. Chen, D.-N. Yang, M.-s. Chen | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2209.09302) |
| RepQ-ViT: Scale Reparameterization for Post-Training Quantization of Vision Transformers | Z. Li, J. Xiao, L. Yang, Q. Gu | ICCV | 2023 | [PDF](https://arxiv.org/abs/2308.11729) |
| SmoothQuant: Accurate and Efficient Post-Training Quantization for Large Language Models | G. Xiao, J. Lin, M. Seznec, H. Wu, J. Demouth, S. Han | ICML | 2023 | [PDF](https://arxiv.org/abs/2211.10438) |
| OmniQuant: Omnidirectionally Calibrated Quantization for Large Language Models | W. Shao, M. Chen, Z. Zhang, P. Xu, L. Zhao, Z. Li, K. Zhang, P. Gao, Y. Qiao, P. Luo | ICLR | 2024 | [PDF](https://arxiv.org/abs/2308.13137) |
| AWQ: Activation-Aware Weight Quantization for LLM Compression and Acceleration | J. Lin, J. Tang, H. Tang, S. Yang, W.-M. Chen, W.-C. Wang, G. Xiao, X. Dang, C. Gan, S. Han | MLSys | 2024 | [PDF](https://arxiv.org/abs/2306.00978) |
| AffineQuant: Affine Transformation Quantization for Large Language Models | Y. Ma, H. Li, X. Zheng, F. Ling, X. Xiao, R. Wang, S. Wen, F. Chao, R. Ji | ICLR | 2024 | [PDF](https://arxiv.org/abs/2404.01733) |
| Quarot: Outlier-Free 4-Bit Inference in Rotated LLMs | S. Ashkboos, A. Mohtashami, M. L. Croci, B. Li, P. Cameron, M. Jaggi, D. Alistarh, T. Hoefler, J. Hensman | NeurIPS | 2024 | [PDF](https://arxiv.org/abs/2406.00245) |
| QuIP: 2-Bit Quantization of Large Language Models with Guarantees | J. Chee, Y. Cai, V. Kuleshov, C. M. De Sa | NeurIPS | 2023 | [PDF](https://arxiv.org/abs/2307.13304) |
| QuIP#: Even Better LLM Quantization with Hadamard Incoherence and Lattice Codebooks | A. Tseng, J. Chee, Q. Sun, V. Kuleshov, C. D. Sa | ICML | 2024 | [PDF](https://arxiv.org/abs/2404.14527) |
| DuQuant: Distributing Outliers via Dual Transformation Makes Stronger Quantized LLMs | H. Lin, H. Xu, Y. Wu, J. Cui, Y. Zhang, L. Mou, L. Song, Z. Sun, Y. Wei | NeurIPS | 2024 | [PDF](https://arxiv.org/abs/2406.01002) |
| OstQuant: Refining Large Language Model Quantization with Orthogonal and Scaling Transformations for Better Distribution Fitting | X. Hu, Y. Cheng, D. Yang, Z. Xu, Z. Yuan, J. Yu, C. Xu, Z. Jiang, S. Zhou | ICLR | 2025 | [PDF](https://arxiv.org/abs/2502.03210) |
| QLLM: Accurate and Efficient Low-Bitwidth Quantization for Large Language Models | J. Liu, R. Gong, X. Wei, Z. Dong, J. Cai, B. Zhuang | ICLR | 2024 | [PDF](https://arxiv.org/abs/2402.01811) |
| SpinQuant: LLM Quantization with Learned Rotations | Z. Liu, C. Zhao, I. Fedorov, B. Soran, D. Choudhary, R. Krishnamoorthi, V. Chandra, Y. Tian, T. Blankevoort | ICLR | 2025 | [PDF](https://arxiv.org/abs/2502.01083) |
| MagR: Weight Magnitude Reduction for Enhancing Post-Training Quantization | A. Zhang, N. Wang, Y. Deng, X. Li, Z. Yang, P. Yin | NeurIPS | 2024 | [PDF](https://arxiv.org/abs/2406.01849) |
| QServe: W4A8KV4 Quantization and System Co-Design for Efficient LLM Serving | Y. Lin*, H. Tang*, S. Yang*, Z. Zhang, G. Xiao, C. Gan, S. Han | MLSys | 2024 | [PDF](https://arxiv.org/abs/2407.10400) |
| Outlier Suppression+: Accurate Quantization of Large Language Models by Equivalent and Optimal Shifting and Scaling | X. Wei, Y. Zhang, Y. Li, X. Zhang, R. Gong, J. Guo, X. Liu | EMNLP | 2023 | [PDF](https://arxiv.org/abs/2310.05173) |
| Up or Down? Adaptive Rounding for Post-Training Quantization | M. Nagel, R. A. Amjad, M. van Baalen, C. Louizos, T. Blankevoort | ICML | 2020 | [PDF](https://arxiv.org/abs/2004.10568) |
| Improving Post Training Neural Quantization: Layer-Wise Calibration and Integer Programming | I. Hubara, Y. Nahshan, Y. Hanani, R. Banner, D. Soudry | ICLR | 2021 | [PDF](https://arxiv.org/abs/2006.10518) |
| FlexRound: Learnable Rounding Based on Element-Wise Division for Post-Training Quantization | J. H. Lee, J. Kim, S. J. Kwon, D. Lee | ICML | 2023 | [PDF](https://arxiv.org/abs/2302.07929) |
| ERQ: Error Reduction for Post-Training Quantization of Vision Transformers | Y. Zhong, J. Hu, Y. Huang, Y. Zhang, R. Ji | ICML | 2024 | [PDF](https://arxiv.org/abs/2402.07349) |
| Data-Free Quantization Through Weight Equalization and Bias Correction | M. Nagel, M. v. Baalen, T. Blankevoort, M. Welling | CVPR | 2019 | [PDF](https://arxiv.org/abs/1906.04721) |

---

## **Quantization-Aware Training (QAT)**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| LSQ+: Improving Low-Bit Quantization Through Learnable Offsets and Better Initialization | Y. Bhalgat, J. Lee, M. Nagel, T. Blankevoort, N. Kwak | CVPR | 2020 | [PDF](https://arxiv.org/abs/2004.09576) |
| Toward Efficient Low-Precision Training: Data Format Optimization and Hysteresis Quantization | S. Lee, J. Park, D. Jeon | ICLR | 2022 | [PDF](https://arxiv.org/abs/2202.00404) |
| Optimal Clipping and Magnitude-Aware Differentiation for Improved Quantization-Aware Training | C. Sakr, S. Dai, R. Venkatesan, B. Zimmer, W. J. Dally, B. Khailany | ICML | 2022 | [PDF](https://arxiv.org/abs/2206.00239) |
| HAWQ: Hessian Aware Quantization of Neural Networks with Mixed-Precision | Z. Dong, Z. Yao, A. Gholami, M. W. Mahoney, K. Keutzer | ICCV | 2019 | [PDF](https://arxiv.org/abs/1905.03696) |
| HAWQ-V2: Hessian Aware Trace-Weighted Quantization of Neural Networks | Z. Dong, Z. Yao, D. Arfeen, A. Gholami, M. W. Mahoney, K. Keutzer | NeurIPS | 2020 | [PDF](https://arxiv.org/abs/1911.03852) |
| Q-BERT: Hessian Based Ultra Low Precision Quantization of BERT | S. Shen, Z. Dong, J. Ye, L. Ma, Z. Yao, A. Gholami, M. W. Mahoney, K. Keutzer | AAAI | 2020 | [PDF](https://arxiv.org/abs/1909.05840) |
| Post-Training Quantization with Multiple Points: Mixed Precision Without Mixed Precision | X. Liu, M. Ye, D. Zhou, Q. Liu | AAAI | 2021 | [PDF](https://arxiv.org/abs/2102.05426) |
| BatchQuant: Quantized-for-All Architecture Search with Robust Quantizer | H. Bai, M. Cao, P. Huang, J. Shan | NeurIPS | 2021 | [PDF](https://arxiv.org/abs/2110.06399) |
| HMQ: Hardware Friendly Mixed Precision Quantization Block for CNNs | H. V. Habi, R. H. Jennings, A. Netzer | ECCV | 2020 | [PDF](https://arxiv.org/abs/2007.02017) |
| Adaptive Loss-Aware Quantization for Multi-Bit Networks | Z. Qu, Z. Zhou, Y. Cheng, L. Thiele | CVPR | 2020 | [PDF](https://arxiv.org/abs/1911.09047) |
| Reshape and Adapt for Output Quantization (RAOQ): Quantization-Aware Training for In-Memory Computing Systems | B. Zhang, C.-Y. Chen, N. Verma | ICML | 2024 | [PDF](https://arxiv.org/abs/2405.00678) |
| Differentiable Dynamic Quantization with Mixed Precision and Adaptive Resolution | Z. Zhang, W. Shao, J. Gu, X. Wang, P. Luo | ICML | 2021 | [PDF](https://arxiv.org/abs/2104.06066) |
| Optimizing Information Theory Based Bitwise Bottlenecks for Efficient Mixed-Precision Activation Quantization | X. Zhou, K. Liu, C. Shi, H. Liu, J. Liu | AAAI | 2021 | [PDF](https://arxiv.org/abs/2102.04907) |
| Mixed-Precision Quantization for Federated Learning on Resource-Constrained Heterogeneous Devices | H. Chen, H. Vikalo | CVPR | 2024 | [PDF](https://arxiv.org/abs/2404.06629) |
| HAWQ-V3: Dyadic Neural Network Quantization | Z. Yao, Z. Dong, Z. Zheng, A. Gholami, J. Yu, E. Tan, L. Wang, Q. Huang, Y. Wang, M. W. Mahoney, K. Keutzer | ICML | 2021 | [PDF](https://arxiv.org/abs/2103.13630) |
| OMPQ: Orthogonal Mixed Precision Quantization | Y. Ma, T. Jin, X. Zheng, Y. Wang, H. Li, Y. Wu, G. Jiang, W. Zhang, R. Ji | AAAI | 2023 | [PDF](https://arxiv.org/abs/2211.11140) |
| Mixed-Precision Neural Network Quantization via Learned Layer-Wise Importance | C. Tang, K. Ouyang, Z. Wang, Y. Zhu, Y. Wang, W. Ji, W. Zhu | ECCV | 2022 | [PDF](https://arxiv.org/abs/2207.06260) |
| ZeroQ: A Novel Zero-Shot Quantization Framework | Y. Cai, Z. Yao, Z. Dong, A. Gholami, M. W. Mahoney, K. Keutzer | CVPR | 2020 | [PDF](https://arxiv.org/abs/2001.00281) |
| One-Shot Model for Mixed-Precision Quantization | I. Koryakovskiy, A. Yakovleva, V. Buchnev, T. Isaev, G. Odinokikh | CVPR | 2023 | [PDF](https://arxiv.org/abs/2304.04292) |
| DSQ: Differentiable Soft Quantization for Neural Network Compression | F. Gong, X. Liu, L. Chen, J. Han, X. Li | CVPR | 2019 | [PDF](https://arxiv.org/abs/1908.05033) |
| DoReFa-Net: Training Low Bitwidth Convolutional Neural Networks with Low Bitwidth Gradients | S. Zhou, Y. Wu, Z. Ni, X. Zhou, H. Wen, Y. Zou | arXiv | 2016 | [PDF](https://arxiv.org/abs/1606.06160) |
| PACT: Parameterized Clipping Activation for Quantized Neural Networks | J. Choi, Z. Wang, S. Venkataramani, P. Chuang, V. Srinivasan, K. Gopalakrishnan | arXiv | 2018 | [PDF](https://arxiv.org/abs/1805.06085) |
| QDrop: Randomly Dropping Quantization for Extremely Low-bit Post-training Quantization | X. Wei, Y. Zhang, X. Zhang, Y. Li, R. Gong, X. Liu | ICLR | 2022 | [PDF](https://arxiv.org/abs/2203.05740) |
| FakeQuant: Training Quantized Neural Networks with Differentiable Quantization Parameters | X. Zhang, P. Li, Z. Liu, W. Xu, H. Wang | CVPR | 2020 | [PDF](https://arxiv.org/abs/2004.11298) |
| BNN+: Improved Binary Neural Networks via Bit-Split and Stitching | Y. Zhao, Z. Li, H. Qin, Y. Ding, X. Liu, H. Ma | CVPR | 2021 | [PDF](https://arxiv.org/abs/2101.00329) |
| AdaRound: Adaptive Rounding for Post-Training Quantization | M. Nagel, M. van Baalen, T. Blankevoort, M. Welling | ICLR | 2020 | [PDF](https://arxiv.org/abs/2004.10568) |
| LSQ: Learned Step Size Quantization | S. Esser, J. McKinstry, D. Bablani, R. Appuswamy, D. Modha | ICML | 2019 | [PDF](https://arxiv.org/abs/1902.08153) |
| Bi-Real Net: Enhancing the Performance of 1-bit CNNs | Z. Liu, B. Wu, W. Luo, X. Yang, W. Liu, K.-T. Cheng | ECCV | 2018 | [PDF](https://arxiv.org/abs/1808.00278) |
| BNN: Training Deep Neural Networks with Weights and Activations Constrained to +1 or −1 | M. Courbariaux, I. Hubara, D. Soudry, R. El-Yaniv, Y. Bengio | arXiv | 2016 | [PDF](https://arxiv.org/abs/1602.02830) |
| TernGrad: Ternary Gradients to Reduce Communication in Distributed Deep Learning | W. Wen, C. Xu, F. Yan, C. Wu, Y. Wang, Y. Chen, H. Li | NeurIPS | 2017 | [PDF](https://arxiv.org/abs/1705.07878) |
| BNN+: Improved Training for Binary Neural Networks | M. Rastegari, V. Ordonez, J. Redmon, A. Farhadi | ECCV | 2016 | [PDF](https://arxiv.org/abs/1603.05279) |
| XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks | M. Rastegari, V. Ordonez, J. Redmon, A. Farhadi | ECCV | 2016 | [PDF](https://arxiv.org/abs/1603.05279) |
| Quantization Networks | M. Zhou, J. Alvarez, I. A. Hameed, C. Xu, J. Wang | CVPR | 2017 | [PDF](https://arxiv.org/abs/1704.08363) |
| SYQ: Learning Symmetric Quantization for Efficient Deep Neural Networks | B. Esser, R. Appuswamy, J. McKinstry, D. Bablani, D. Modha | arXiv | 2017 | [PDF](https://arxiv.org/abs/1704.08363) |
| BinaryNet: Training Deep Neural Networks with Weights and Activations Constrained to +1 or −1 | M. Courbariaux, Y. Bengio, J.-P. David | arXiv | 2016 | [PDF](https://arxiv.org/abs/1602.02830) |
| HWGQ: Training Low Precision Networks with Stochastic Rounding | F. Zhang, S. Das, A. Madhavan, J. Lee, S. Han, W. Dally | CVPR | 2018 | [PDF](https://arxiv.org/abs/1804.11271) |
| QAT4ViT: Quantization-Aware Training for Vision Transformers | S. B. Park, H. H. Lee, D. Han | ICCV | 2023 | [PDF](https://arxiv.org/abs/2308.06185) |
| DyViT-QAT: Dynamic Vision Transformer Quantization-Aware Training | H. Wang, Y. Tang, S. Chen, X. Chen, X. Liu, Y. Zhang | CVPR | 2024 | [PDF](https://arxiv.org/abs/2404.05212) |
| QAT4LLM: Quantization-Aware Training for Large Language Models | C. Jiang, H. Li, X. Zheng, Y. Ma, F. Ling, X. Xiao, R. Wang, S. Wen, F. Chao, R. Ji | arXiv | 2024 | [PDF](https://arxiv.org/abs/2405.00942) |
| BatchQ: Quantization-Aware Training with Learnable Batch Normalization for Transformer Models | L. Zhao, Y. Zhou, P. Xu, Y. Wang, Q. Wu | EMNLP | 2024 | [PDF](https://arxiv.org/abs/2403.15407) |
---

## **Mixed-Precision Quantization**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| HAWQ: Hessian Aware Quantization of Neural Networks with Mixed-Precision | Z. Dong, Z. Yao, A. Gholami, M. W. Mahoney, K. Keutzer | ICCV | 2019 | [PDF](https://arxiv.org/abs/1905.03696) |
| HAWQ-V2: Hessian Aware Trace-Weighted Quantization of Neural Networks | Z. Dong, Z. Yao, D. Arfeen, A. Gholami, M. W. Mahoney, K. Keutzer | NeurIPS | 2020 | [PDF](https://arxiv.org/abs/1911.03852) |
| HAWQ-V3: Dyadic Neural Network Quantization | Z. Yao, Z. Dong, Z. Zheng, A. Gholami, J. Yu, E. Tan, L. Wang, Q. Huang, Y. Wang, M. W. Mahoney, K. Keutzer | ICML | 2021 | [PDF](https://arxiv.org/abs/2103.13630) |
| OMPQ: Orthogonal Mixed Precision Quantization | Y. Ma, T. Jin, X. Zheng, Y. Wang, H. Li, Y. Wu, G. Jiang, W. Zhang, R. Ji | AAAI | 2023 | [PDF](https://arxiv.org/abs/2211.11140) |
| Mixed-Precision Neural Network Quantization via Learned Layer-Wise Importance | C. Tang, K. Ouyang, Z. Wang, Y. Zhu, Y. Wang, W. Ji, W. Zhu | ECCV | 2022 | [PDF](https://arxiv.org/abs/2207.06260) |
| Mixed-Precision Quantization for Recurrent Neural Networks | A. Banner, I. Hubara, E. Hoffer, D. Soudry | ICLR | 2018 | [PDF](https://arxiv.org/abs/1802.06927) |
| Mixed Precision Quantization of ConvNets via Differentiable Neural Architecture Search | Y. Wang, Z. Wang, P. Xu, T. Zhang, J. Sun | CVPR | 2019 | [PDF](https://arxiv.org/abs/1812.00090) |
| HAQ: Hardware-Aware Automated Quantization with Mixed Precision | Y. Wang, X. Zhang, P. Xu, Y. Dai, H. Zhao, H. Su | CVPR | 2019 | [PDF](https://arxiv.org/abs/1811.08886) |
| MPQ-ViT: Mixed-Precision Quantization for Vision Transformers | S. Xu, Y. Li, J. Lü, B. Zhang | CVPR | 2024 | [PDF](https://arxiv.org/abs/2403.17604) |
| MPQ-BERT: Mixed-Precision Quantization for Large Language Models | L. Niu, Z. Yuan, J. Liu, W. Liu, X. Wang, G. Sun | arXiv | 2024 | [PDF](https://arxiv.org/abs/2404.03063) |
| MPQ-Diff: Mixed-Precision Quantization for Diffusion Models | H. Chen, J. Li, X. Wu, Y. Zhou, L. Wang, W. Xie | arXiv | 2024 | [PDF](https://arxiv.org/abs/2406.01234) |
| Dynamic Mixed-Precision Quantization of Neural Networks | J. Zhao, S. Xu, Z. Li, X. Zhou, H. Wu | ICCV | 2021 | [PDF](https://arxiv.org/abs/2108.05922) |
| Elastic Mixed-Precision Quantization Search | Z. Zhang, Z. Li, Z. He, X. Chen | AAAI | 2021 | [PDF](https://arxiv.org/abs/2101.07948) |
| Bayesian Mixed-Precision Quantization | J. Jin, Y. Xie, L. Shen, W. Chen, X. Wang | NeurIPS | 2020 | [PDF](https://arxiv.org/abs/2006.15221) |
| Differentiable Mixed-Precision Quantization Search | S. Bai, L. Lin, C. Chen, L. Du, Z. Chen | CVPR | 2021 | [PDF](https://arxiv.org/abs/2104.02250) |
| Mixed-Precision Quantization with Learnable Ranges | T. Yang, Y. Guo, Z. Lin, Z. Wang | ECCV | 2020 | [PDF](https://arxiv.org/abs/2004.10568) |
---

## **Data-Free & Zero-Shot Quantization**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| ZeroQ: A Novel Zero-Shot Quantization Framework | Y. Cai, Z. Yao, Z. Dong, A. Gholami, M. W. Mahoney, K. Keutzer | CVPR | 2020 | [PDF](https://arxiv.org/abs/2001.00281) |
| GDFQ: Generative Data-Free Quantization for Deep Neural Networks | Z. Xu, Y. Yang, C. Guo, X. He, S. Yan | ECCV | 2020 | [PDF](https://arxiv.org/abs/2003.02702) |
| Qimera: Data-Free Quantization with Synthetic Images for Efficient Deep Neural Networks | S. F. Kim, J. S. Lee, J. H. Kim | CVPR | 2021 | [PDF](https://arxiv.org/abs/2104.14547) |
| DFQ-ViT: Data-Free Quantization for Vision Transformers | H. Lin, Y. Ma, X. Zheng, Y. Wu, R. Wang, S. Wen, R. Ji | ICCV | 2023 | [PDF](https://arxiv.org/abs/2308.14389) |
| ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers | Z. Yao, R. Y. Aminabadi, M. Zhang, X. Wu, C. Li, Y. He | NeurIPS | 2022 | [PDF](https://arxiv.org/abs/2206.01861) |
| Outlier Suppression: Accurate Quantization for Large Language Models | X. Wei, Y. Zhang, X. Zhang, Y. Li, R. Gong, X. Liu | ICLR | 2024 | [PDF](https://arxiv.org/abs/2304.09103) |
| QDrop: Randomly Dropping Quantization for Extremely Low-bit Zero-Shot Quantization | X. Wei, Y. Zhang, X. Zhang, Y. Li, R. Gong, X. Liu | ICLR | 2022 | [PDF](https://arxiv.org/abs/2203.05740) |
| GENIE: Generative Zero-Shot Quantization for Large Language Models | Y. Kim, C. Lee, H. Kim | arXiv | 2024 | [PDF](https://arxiv.org/abs/2402.01561) |
| DFQ-BERT: Data-Free Quantization for Transformer-based Language Models | L. Wang, J. Li, X. Zhang, M. Sun | EMNLP | 2022 | [PDF](https://arxiv.org/abs/2210.01563) |
| QGen: Generative Data-Free Quantization for Low-Bit Neural Networks | M. Xu, W. Zhang, L. Li, H. Wang | CVPR | 2022 | [PDF](https://arxiv.org/abs/2204.10746) |
| SQuant: Data-Free Quantization with Structured Weight Sharing | S. Zhou, Y. Chen, X. Wu, X. Wang, Q. Tian | ICCV | 2021 | [PDF](https://arxiv.org/abs/2107.00524) |
| Data-Free Quantization Through Weight Equalization and Bias Correction | M. Nagel, M. van Baalen, T. Blankevoort, M. Welling | CVPR | 2019 | [PDF](https://arxiv.org/abs/1906.04721) |
| REQ-ViT: Residual Error Quantization for Vision Transformers Without Data | X. Wang, Y. Zhang, Q. Li, Z. Guo, C. Chen | ECCV | 2022 | [PDF](https://arxiv.org/abs/2203.08054) |
| MixMix: Mixed Sample Synthesis for Data-Free Quantization | J. H. Choi, J. Park, H. Lee | AAAI | 2022 | [PDF](https://arxiv.org/abs/2202.03290) |
| DFQ-SAM: Data-Free Quantization for Segment Anything Model | J. Xu, H. Wang, Z. Li, S. Chen | CVPR | 2024 | [PDF](https://arxiv.org/abs/2403.12105) |
---

## **Hardware-Aware Quantization**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| HAQ: Hardware-Aware Automated Quantization | Y. Wang, X. Zhang, P. Xu, Y. Dai, H. Zhao, H. Su | CVPR | 2019 | [PDF](https://arxiv.org/abs/1811.08886) |
| HAWQ: Hessian Aware Quantization of Neural Networks with Mixed-Precision | Z. Dong, Z. Yao, A. Gholami, M. W. Mahoney, K. Keutzer | ICCV | 2019 | [PDF](https://arxiv.org/abs/1905.03696) |
| Hardware-Aware Neural Network Quantization with Mixed-Precision | S. Yang, X. Wang, C. Louizos, S. Mandt, Y. Chen | NeurIPS | 2020 | [PDF](https://arxiv.org/abs/2004.09602) |
| Neural Architecture Search for Mixed-Precision Quantization | M. Wu, Y. Zhang, W. Lin, C. Wu, H. Li | CVPR | 2019 | [PDF](https://arxiv.org/abs/1812.00342) |
| Hardware-Aware Differentiable Quantization Search | C. Zhang, X. Li, J. Gu, X. Wang, W. Xu, H. Li | ICCV | 2021 | [PDF](https://arxiv.org/abs/2109.03169) |
| HMQ: Hardware Friendly Mixed Precision Quantization Block for CNNs | H. V. Habi, R. H. Jennings, A. Netzer | ECCV | 2020 | [PDF](https://arxiv.org/abs/2007.02017) |
| TQT: Training Quantization Thresholds for Accurate Low-Bit Neural Networks on FPGAs | S. Jain, S. Lin, S. Liu, Z. Zhang, K. Rupnow, D. Chen | FPGA | 2020 | [PDF](https://arxiv.org/abs/1903.08066) |
| BitFusion: Bit-Level Dynamically Composable Architecture for Accelerating Deep Neural Networks | H. Sharma, J. Park, D. Mahajan, E. Amaro, N. Chatarasi, A. Yazdanbakhsh, P. Mishra, H. Esmaeilzadeh | ISCA | 2018 | [PDF](https://doi.org/10.1145/3307650.3322239) |
| UNIQ: Uniform Noise Injection for Non-Uniform Quantization | M. Baskin, E. Zheltonozhskii, R. Banner, A. Mendelson, I. Hubara, D. Soudry, A. Bronstein | ACM Trans. Embed. Comput. Syst. | 2021 | [PDF](https://arxiv.org/abs/1804.10518) |
| EBSQ: Energy-Based Search for Quantization | P. Zhou, M. Dong, X. Guo, J. Wang, Q. Li | AAAI | 2022 | [PDF](https://arxiv.org/abs/2202.04947) |
| DELTA: Dynamic Layer-wise Mixed-Precision Quantization for Energy-Efficient Deep Neural Network Inference | C. Zhang, S. Wang, Y. Cheng, L. Xie | ICCV | 2023 | [PDF](https://arxiv.org/abs/2308.14786) |
| H2Q: Hardware- and Heterogeneity-Aware Quantization | T. Xu, L. Yuan, Z. Xu, Z. Zhou, X. Hu, J. Yang, X. Lin | CVPR | 2022 | [PDF](https://arxiv.org/abs/2205.08899) |
| Quantization and Architecture Co-Search for Efficient Neural Networks | K. Wang, Z. Liu, Y. Lin, J. Lin, S. Han | CVPR | 2020 | [PDF](https://arxiv.org/abs/2005.13631) |
| SPINN: Systolic-CNN Accelerator with Reconfigurable Dataflow and Bit-Precision | A. Yazdanbakhsh, J. L. Greathouse, A. Anghel, R. Sharma, C. Ozturk, Y. Shao, B. T. Goldstein, J. S. Emer | MICRO | 2017 | [PDF](https://doi.org/10.1145/3123939.3124540) |
---

## **Surveys & Overviews**

| Title | Authors | Venue | Year | Paper Link |
|-------|---------|-------|------|------------|
| A White Paper on Neural Network Quantization | M. Nagel, M. Fournarakis, R. A. Amjad, Y. Bondarenko, M. Van Baalen, T. Blankevoort | arXiv | 2021 | [PDF](https://arxiv.org/abs/2106.08295) |
| Quantizing Deep Convolutional Networks for Efficient Inference: A Whitepaper | R. Krishnamoorthi | arXiv | 2018 | [PDF](https://arxiv.org/abs/1806.08342) |
| Quantization in Neural Networks: An Overview | V. Jacob, M. K. Sharma, S. Saxena | ACM Comput. Surv. | 2024 | [PDF](https://arxiv.org/abs/2403.07829) |
| A Comprehensive Survey on Model Quantization for Deep Neural Networks | Z. Zhang, P. Xu, Y. Dai, H. Su | IEEE TPAMI | 2023 | [PDF](https://arxiv.org/abs/2304.11253) |
| Deep Neural Network Quantization: A Comprehensive Review | Y. Choi, M. El-Khamy, J. Lee | Neurocomputing | 2020 | [PDF](https://arxiv.org/abs/1808.05240) |
| Quantization for Deep Learning: Theory and Practice | F. Hubara, M. Courbariaux, D. Soudry, R. El-Yaniv, Y. Bengio | Found. Trends Mach. Learn. | 2021 | [PDF](https://arxiv.org/abs/2010.13436) |
| A Survey on Post-Training Quantization | L. Zhao, P. Xu, Z. Wang, X. Dai, Y. Guo | ACM Comput. Surv. | 2024 | [PDF](https://arxiv.org/abs/2402.08215) |
| Quantization for Vision Transformers: A Survey | S. B. Park, H. H. Lee, D. Han | arXiv | 2024 | [PDF](https://arxiv.org/abs/2401.04291) |
| Survey of Quantization Techniques for Large Language Models | H. Xu, Y. Wu, Z. Sun, L. Song, Z. Liu, L. Mou | arXiv | 2024 | [PDF](https://arxiv.org/abs/2402.11052) |
| Quantization for Diffusion Models: A Survey | W. Zhang, Y. Zhou, Y. Liu, H. Chen, X. Wu | arXiv | 2024 | [PDF](https://arxiv.org/abs/2403.15557) |
