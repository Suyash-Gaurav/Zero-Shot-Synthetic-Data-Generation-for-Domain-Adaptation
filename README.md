# Zero-Shot Synthetic Data Generation for Domain Adaptation

## Complete Methodology Implementation

This notebook implements the complete methodology described in the thesis proposal "Zero-Shot Synthetic Data Generation for Domain Adaptation". The implementation covers all three phases:

1. **Phase 1**: Training a Generative Model with Meta-Learning
2. **Phase 2**: Conditioning for Zero-Shot Generation
3. **Phase 3**: Evaluating Synthetic Data

### Key Features:
- Integration with state-of-the-art pre-trained models from Hugging Face
- Meta-learning implementation using Reptile algorithm
- Comprehensive evaluation framework
- Real dataset integration (CheXpert, MIMIC-CXR, TCIA)
- Efficient computational implementation with mixed-precision training

# Phase 1: Training a Generative Model with Meta-Learning

## Objective
Train a generative model on diverse source domains to capture domain-invariant features, optimized for rapid adaptation to unseen domains.

## Key Components
1. **Stable Diffusion v2** as the generative backbone
2. **Reptile meta-learning** for domain adaptation
3. **CLIP text encoder** for domain conditioning
4. **LoRA fine-tuning** for computational efficiency

# Phase 2: Conditioning for Zero-Shot Generation

## Objective
Condition the generative model to produce synthetic data for unseen domains using metadata (text prompts or image embeddings).

## Key Components
1. **Text conditioning** using CLIP-guided synthesis
2. **Image conditioning** using DINOv2 embeddings
3. **DDIM sampling** for efficient generation
4. **Classifier-free guidance** for quality control

# Phase 3: Evaluating Synthetic Data

## Objective
Assess synthetic data's fidelity and utility for downstream tasks in unseen domains.

## Key Components
1. **Fidelity metrics**: FID using Swin Transformer
2. **Utility assessment**: ViT fine-tuning for downstream tasks
3. **Diversity metrics**: Precision and Recall for Distributions (PRD)
4. **Expert qualitative assessment** framework
