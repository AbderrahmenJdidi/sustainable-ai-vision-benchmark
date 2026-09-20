# Toward Sustainable AI: Assessing and Reducing the Environmental Footprint of Deep Learning Models

**End of Studies Project** — Royal Military College of Canada (Mitacs Globalink) & ENSI  
Author: Abderrahmen Jedidi  
Supervisors: Dr. Samar Garrab (RMC), Dr. Moncef Tagina (ENSI)

## Project Overview

This project designs, implements and validates a **hardware-aware benchmarking and optimization system** for deep learning vision models. The goal is to measure and reduce the energy and carbon footprint of modern vision architectures throughout their lifecycle (training + inference).

The work consists of three main parts:

1. **General benchmarking methodology**  
   Validated on 9 general-purpose vision architectures (CNNs, Vision Transformers and hybrids) on both NVIDIA A100 GPU and AMD EPYC CPU under statistically rigorous conditions (multiple independent runs + 95 % confidence intervals).

2. **Precision agriculture case study**  
   Applied the same methodology to crop disease classification using two datasets that span the lab-to-field domain shift:
   - PlantVillage (laboratory-controlled)
   - Paddy Doctor (real-field smartphone images)  
   Nine architectures were fine-tuned and evaluated for accuracy, domain-shift robustness and energy/carbon cost.

3. **Model compression + Carbon Break-Even Point**  
   Extended the system with structured pruning and quantization, plus a novel indicator (Carbon Break-Even Point) that tells whether the one-time energy cost of an optimization is recovered by deployment-time savings.

All experiments were run on the Digital Research Alliance of Canada (Narval) HPC cluster using CodeCarbon for process-level energy tracking.

## Key Results (high level)

- Theoretical metrics (parameters, GFLOPs) correlate only moderately with real energy consumption.
- Energy rankings invert between GPU and CPU, especially for transformers.
- Efficient hybrid and modern CNN models (e.g. CoAtNet-0, EfficientNet variants, MobileViT) offer the best accuracy–energy trade-offs on both platforms.
- Large foundation models (e.g. DINOv2-Base) are frequently dominated on both accuracy and carbon cost under realistic agricultural data regimes.

## Full Experimental Artefacts

- General vision architectures benchmark: [Figshare](https://figshare.com/s/1e036476cae2effbd7ce)
- Crop disease classification study: [Figshare DOI](https://doi.org/10.6084/m9.figshare.33233721)

(The Figshare repositories contain code, configuration files, energy logs, result tables and statistical summaries.)

## Related Documents

- Full engineering thesis (PFE Report)
- Two research manuscripts currently under preparation / review

## Citation

If you use any part of this work, please cite the corresponding Figshare datasets and the forthcoming papers.

---

*This repository serves as the public entry point for the project. The complete experimental material is archived on Figshare for long-term reproducibility.*
