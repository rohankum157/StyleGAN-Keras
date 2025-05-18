# StyleGAN-Keras
Keras implementation of StyleGAN based on NVIDIA’s paper. Supports style-based image generation (4×4 to 256×256) with AdaIN. Includes SPADE normalization for semantic synthesis. Mixing regularity included; progressive growth not yet implemented. Open for contributions.

StyleGAN-Keras

A Keras implementation of StyleGAN, based on the research paper

A Style-Based Generator Architecture for Generative Adversarial Networks
by Tero Karras et al., NVIDIA (2018).

This repository also includes an implementation of Spatially-Adaptive Normalization (SPADE) adapted from:

Semantic Image Synthesis with Spatially-Adaptive Normalization
by Taesung Park et al., NVIDIA (2019).

⸻

🔬 Project Highlights
	•	Style-Based Generator Architecture with control over coarse-to-fine style levels.
	•	Implements AdaIN (Adaptive Instance Normalization) and includes SPADE code (AdaIN.py).
	•	Provides different configurations:
	•	stylegan.py → Basic StyleGAN generator/discriminator.
	•	mixing-stylegan.py → Incorporates style mixing regularities.
	•	Growth/Progressive training is not implemented yet — Contributions are welcome!

⸻

🧱 Architecture
	•	Input (Z-space): Latent vector mapped via an MLP to intermediate latent space (W).
	•	Style Blocks: Influence generator at different resolutions using AdaIN.
	•	Resolution: Configurable from 4×4 up to 32×32 in rows and 256×256 in columns.
	•	Noise Injection: Per-layer noise is added to encourage stochastic variation.

⸻

🧪 SPADE Integration

Code for SPADE (Spatially-Adaptive Denormalization) is available in AdaIN.py, offering a foundation for experimentation with conditional image generation based on segmentation maps or other spatial data.
