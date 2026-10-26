# LinearV: Training-Free Value Space Arithmetic for Rectifying Prior Attribute Bias in Text-to-Image Diffusion Models

The source code of LinearV.
<img width="1337" height="452" alt="image" src="https://github.com/user-attachments/assets/38fc5e67-6132-44e3-b6cf-4017145a7836" />

# 1. Introduction
Despite the remarkable photorealism achieved by large-scale text-to-image diffusion models, they exhibit a persistent failure mode known as Prior Attribute Bias. When prompted with counter-intuitive concepts that contradict training data statistics (e.g., "a gray strawberry" or "a square apple"), models frequently ignore the explicit textual condition in favor of the implicit canonical prior. Existing approaches attempt to mitigate this through two strategies: enforcing spatial alignment via computationally expensive test-time optimization, or manipulating text embeddings. Both remain ineffective against strong structural priors. In this work, we identify that a core limitation lies in the semantic representation: the cross-attention Value projection acts as a "prior filter", embedding canonical traits directly into the object's feature representation. Consequently, even with perfect spatial alignment, the object's inherent features conflict with the target attribute. To address this, we introduce LinearV, a training-free framework that decouples attribute binding into two complementary processes: (1) GenPointer enforces spatial alignment by injecting the object's positional information into the attribute's attention mechanism; and (2) VDebias resolves the semantic conflict via targeted semantic steering in the Value Space, explicitly neutralizing the canonical prior. To rigorously evaluate this problem, we further introduce the Counter-Intuitive Attribute Benchmark (CIAB), a curated set of 240 prompts spanning color, shape, and texture. Extensive experiments across multiple diffusion backbones demonstrate that LinearV significantly outperforms state-of-the-art methods. Notably, LinearV achieves a relative gain of over 11.8% in target alignment, measured by Disentangled BLIP-VQA, over the strongest baselines in challenging structural category, confirming its effectiveness in deep semantic modifications.

# 2. Results

<img width="1136" height="655" alt="image" src="https://github.com/user-attachments/assets/75eb0bbc-d41f-490f-b245-7ec0b928d207" />


# 3. Contact
* [taidvt@uit.edu.vn](taidvt@uit.edu.vn)
