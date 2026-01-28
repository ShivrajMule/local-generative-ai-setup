# Local Generative AI Implementation 🚀

This repository documents the local deployment, configuration, and optimization of Generative AI models (Stable Diffusion & Ollama) on consumer-grade hardware.

## 💻 System Specifications
* **OS:** Windows 11
* **Processor:** Ryzen 7 7445HS
* **RAM:** 16 GB DDR 5
* **GPU:** NVIDIA RTX 3050 (6GB VRAM)

---

## 🎨 Project 1: Stable Diffusion (Image Generation)
**Goal:** Run SDXL locally with optimized VRAM usage.

### Configuration
* **Interface:** Automatic1111
* **Arguments Used:** `--xformers`
* **Performance:** * Average Generation Time:4-5 seconds (512x512, Euler a, 20 steps)
  * Peak VRAM Usage: 4.8 GB
### Sample Output
![Image Description](./stable-diffusion/assets/output-1)
> Prompt: > A hyper-realistic close-up portrait of an elderly fisherman, weathered skin with deep wrinkles, salt-and-pepper beard, wearing a yellow raincoat, soft natural overcast lighting, shot on 85mm lens, f/1.8, 8k resolution, highly detailed skin texture, masterpiece, cinematic look.

Negative Prompt: > (deformed, distorted, disfigured:1.3), poorly drawn, bad anatomy, wrong anatomy, extra limb, missing limb, floating limbs, (mutated hands and fingers:1.4), disconnected limbs, mutation, mutated, ugly, disgusting, blurry, amputation, tattoo, makeup, plastic skin, smooth skin.


---

## 🤖 Project 2: Ollama (Local LLM)
**Goal:** Deploy a privacy-focused offline Chatbot.

### Setup Details
* **Engine:** Ollama
* **Models:**
    Daily Driver- llama3.1 (8B)
    Coding- qwen2.5-coder:7b
    Reasoning- deepseek-r1 (7B)
* **Latency:** Approx  tokens/second
