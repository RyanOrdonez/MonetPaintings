# Monet Style Transfer with GANs 🎨

This project explores artistic image generation using Generative Adversarial Networks (GANs) for the Kaggle challenge: [“GANs – Getting Started (Monet Paintings)”](https://www.kaggle.com/competitions/gan-getting-started/). The objective is to transform real-world photographs into images that emulate the painting style of Claude Monet.

## 🧠 Models Implemented

### 1. **DCGAN** (Deep Convolutional GAN)
- Generates entirely new Monet-like images from random noise.
- Pure generative approach with no photo reference.
- Result: Abstract, creative outputs — but not suitable for content-specific transformation.

### 2. **Style Transfer** (Perceptual, pretrained)
- Uses a pretrained TensorFlow model to blend the content of a photo with the style of a Monet painting.
- Requires a style image per transformation.
- Result: Highly textured, stylized visuals — great for individual examples but not scalable.

### 3. **CycleGAN** (Unpaired Image-to-Image Translation)
- Learns a mapping between photo and Monet domains using cycle-consistency loss.
- Requires no paired training data.
- Result: Most successful and scalable model for full-dataset translation.

## 🔬 Evaluation

### 📈 Quantitative Results (Lower = Better)
| Model          | Kaggle Public Score |
|----------------|---------------------|
| **CycleGAN**   | **71.34**           |
| Style Transfer | 53.14               |
| DCGAN          | 312.97              |

> **Note**: Style Transfer used a pretrained model and is not a GAN — included here as a comparison.

### 👁️‍🗨️ Qualitative Insights
- **CycleGAN** preserved structure and produced consistent, Monet-like stylizations.
- **Style Transfer** excelled in texture but lacked generalization.
- **DCGAN** was creative, but outputs were structurally incoherent.

## 📁 Project Structure


## 📌 Key Takeaways

- **CycleGAN** was the most effective GAN model for the task, excelling at unpaired image-to-image translation.
- **Style Transfer** was a strong stylistic tool, but lacked scalability.
- **DCGAN** performed poorly in this context but demonstrated the generative potential of noise-based GANs.

## 🚀 Future Work

- Add FID / LPIPS metrics for objective scoring.
- Explore hybrid models that combine CycleGAN and perceptual loss.
- Build a web app to apply Monet-style filters to user-uploaded photos.

---

🧠 Created for the *Intro to Deep Learning (DTSA 5511)* course by Ryan Ordonez.
