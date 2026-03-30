# TransDiffusion
TransDiffusion: An Occlusion-Aware Generative Framework for Monocular Depth Estimation

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
