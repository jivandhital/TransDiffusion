# TransDiffusion: An Occlusion-Aware Generative Framework for Monocular Depth Estimation

Reconstructing a complete 3D geometry from any
single RGB image remains challenging due to severe occlusions
and the inherent ambiguity of missing visual information. Existing
single-image depth and 3D reconstruction methods typically
rely on implicit hallucination, forcing generative models to infer
occluded geometry without explicit visibility reasoning. This
work proposes an occlusion-aware reconstruction framework
that explicitly separates visible and occluded regions prior to
generative modeling. Our method employs a Vision Transformer
to extract patch-level representations and predict tokenlevel
occlusion likelihoods. An occlusion reasoning module then
hallucinates latent features for occluded regions using crossattention
guided by visible evidence. The resulting occlusionaware
representation conditions a lightweight diffusion-based
depth generator, enabling structured hallucination of hidden
geometry while preserving visible structure. Experiments on
the NYU Depth V2 dataset demonstrate that explicit occlusion
reasoning improves reconstruction robustness and interpretability,
particularly near occlusion boundaries. Qualitative results
further show meaningful occlusion masks and reduced depth
error in occluded regions.

# Methodology
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
  
**To implementation the project:**
- Clone the repository: git clone 'https://github.com/jivandhital/TransDiffusion.git' and 
- Download the NYUD Depth V2 dataset: Download and unzip the dataset from "https://drive.google.com/file/d/1GdYTZkjeT3391XOw-7rfJrFaXQU1zFom/view?usp=drive_link" folder

# Dataset

Download the NYUD Depth V2 dataset: Download and unzip the NYUDV2 dataset from "https://drive.google.com/file/d/1GdYTZkjeT3391XOw-7rfJrFaXQU1zFom/view?usp=drive_link" folder
 
# Experimental Results

<img width="835" height="326" alt="Result11" src="https://github.com/user-attachments/assets/c94250a0-9f0a-4a8a-ae87-4a2490352c6b" />


# Conclusion and Future Works
 - Occlusion recovery requires explicit uncertainty modeling.
 - Explicit occlusion reasoning improved reconstruction.
 - Our framework separates observed and inferred geometry.

**Future work**
 - Multi-view extension.
 - Improve occlusion precision and extend to full 3D representations.
 - Evaluate on larger datasets.



