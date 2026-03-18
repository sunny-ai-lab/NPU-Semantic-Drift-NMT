# NPU Semantic Drift in Neural Machine Translation

This repository accompanies the paper:

**"Systematic Analysis of Hardware-Induced Semantic Drift: Meaning-Aware Evaluation of NPU-Accelerated Neural Machine Translation"**

## Overview

This project investigates semantic degradation caused by hardware-aware optimization in neural machine translation (NMT), particularly under NPU-oriented INT8 deployment.

## Key Contributions

- Definition of **hardware-induced semantic drift**
- Proposal of a **Meaning-Aware Evaluation (MAE)** framework
- Empirical comparison between GPU (BF16) and NPU (INT8)
- Identification of systematic patterns:
  - Affective Compression
  - Cultural Neutralization
  - Pragmatic Over-Generalization

## Dataset

- Korean–French subtitle dataset (2,039 sentence pairs)
- 500-sentence subset used for human evaluation

## Experimental Setup

- Model: NLLB-200 (600M)
- GPU baseline: BF16 precision
- NPU deployment: INT8 quantization (ONNX + PTQ)
- Hardware: FuriosaAI Warboy NPU

## Key Findings

- BLEU: stable (−0.4)
- chrF: stable (−0.5)
- Semantic retention: −21.1 percentage points (p < 0.001)

## Reproducibility

The repository provides the full pipeline:

- ONNX conversion
- INT8 quantization
- Meaning-aware evaluation framework

## Author

Mi-Ae Yang  
Chosun University  
## Citation

If you use this work, please cite:

Yang, M.-A. (2026). Systematic Analysis of Hardware-Induced Semantic Drift: Meaning-Aware Evaluation of NPU-Accelerated Neural Machine Translation.
