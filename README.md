# TransDiffusion: An Occlusion-Aware Generative Framework for Monocular Depth Estimation

TransDiffusion is a novel occlusion-aware generative framework for monocular depth estimation and single-image 3D reconstruction. Unlike conventional methods that treat occlusion implicitly, this work explicitly models visibility and separates occlusion reasoning from generative depth reconstruction.

**The proposed pipeline integrates:**

- Vision Transformer-based feature extraction
- Token-level occlusion prediction
- Cross-attention-based occlusion reasoning
- Diffusion-based depth generation

This structured approach improves robustness, interpretability, and reconstruction accuracy in occluded regions.

# Methodology

**The framework consists of four main stages:**

- Occlusion-aware feature extraction
- Occlusion reasoning via cross-attention
- Diffusion-based depth reconstruction
- Depth refinement

![TransDiffusion](https://github.com/user-attachments/assets/eadc1cbb-6f6a-4348-ba75-2fbb575c7d6e)

We introduced an explicit token-level occlusion prediction integrated
into a Vision Transformer backbone for single-image
3D reconstruction. We propose a cross-attention-based occlusion
reasoning module that hallucinates latent representations
for occluded regions using visible evidence. We develop
an occlusion-conditioned diffusion framework that separates
visibility reasoning from generative depth modeling, enabling
structured and interpretable reconstruction under occlusion.

# Key Ideas
**Separate what is seen from what must be inferred**
 - Occlusion-Aware Conditioning Tokens.
 - Dual-Path Diffusion (Visible vs Occluded).
 - Attention Explainability Module for Occlusion Reasoning.
 - Occlusion-Specific Loss & Evaluation.

**We proposed**
 - Transformer-based occlusion reasoning module.
 - Dual-path diffusion for visible and occluded geometry.
 - Attention explainability for understanding hallucination.
   
**Key Contributions**

- Explicit token-level occlusion modeling using Vision Transformer
- Cross-attention reasoning module for hallucinating occluded regions
- Occlusion-conditioned diffusion model for structured depth reconstruction
- Improved performance over baseline methods on NYU Depth V2
   
# Experimentation
**Datasets**

 NYUDV2

 **Evaluation Metrics**
 
 RMSE (Lower is better)
 
 Abs Rel (Lower is better)
 
 δ₁, δ₂ accuracy (Higher is better)

   **Hardware**
   
 GPU: NVIDIA Tesla T4
 
 CPU: Kaggle / Colab default 
 
 Device: cuda
 
**Software**

 Framework: PyTorch
 
 Environment: Colab / Kaggle
 
 Optimizer: AdamW

 # Implementation Process

 Firstly, install all the required dependencies: pip install -r requirements.txt
  Than, run the .py file. Don't forget to update the paths to the dataset files in the code '!py TD_Final_Code.py'
  
**To install the project:**
- Clone the repository: git clone 'https://github.com/jivandhital/TransDiffusion.git'
- cd TransDiffusion
- pip install -r requirements.txt and 
- Download the NYUD Depth V2 dataset: Download and unzip the dataset from "https://drive.google.com/file/d/1GdYTZkjeT3391XOw-7rfJrFaXQU1zFom/view?usp=drive_link" folder

# Dataset

- This project uses the NYU Depth V2 dataset.
- Preprocess images to 224×224 resolution
- Normalize depth values to [0, 1]

Official Link: https://cs.nyu.edu/~fergus/datasets/nyu_depth_v2.html

Externl Drive Link: "https://drive.google.com/file/d/1GdYTZkjeT3391XOw-7rfJrFaXQU1zFom/view?usp=drive_link" folder
 
# Experimental Results

- Demonstrates improved reconstruction accuracy and robustness in occluded regions.

<img width="934" height="613" alt="SOTA result-modified" src="https://github.com/user-attachments/assets/78f5caa1-b5b4-41c3-b1cc-dd04498d75c8" />

<img width="1669" height="651" alt="Result11" src="https://github.com/user-attachments/assets/fcbd0aa0-df32-4f7d-9a97-e52262f3d631" />

<img width="1663" height="649" alt="Result22" src="https://github.com/user-attachments/assets/6167cd6f-0a61-4c6a-9822-103d63ceed11" />

# Conclusion and Future Works
 - Occlusion recovery requires explicit uncertainty modeling.
 - Explicit occlusion reasoning improved reconstruction.
 - Our framework separates observed and inferred geometry.

**Future work**
 - Multi-view extension.
 - Improve occlusion precision and extend to full 3D representations.
 - Evaluate on larger datasets.

# Acknowledgements

Thank you to my project supervisor, Dr. Saad Bin Ahmed, for providing continuous feedback and guidance throughout the completion of this research project.
- NYU Depth V2 Dataset
- Prior works: AdaBins, BinsFormer, Diffusion-based depth models

