# Awesome Quantization
A curated list of papers on neural network quantization, including post-training quantization, quantization-aware training, mixed-precision methods, data-free quantization, hardware-aware methods, and surveys.

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
