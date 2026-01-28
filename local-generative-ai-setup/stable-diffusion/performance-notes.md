# 📊 Performance Benchmarks: Stable Diffusion

**Hardware Context:**
* **Device:** Laptop HP VICTUS Ryzen 7 7445HS
* **GPU:** NVIDIA RTX 3050, 6GB VRAM
* **RAM:** 16GB DDR5

## Test Case 1: Standard Generation
* **Model:** Realistic_Vision_V5.1_fp16-no-ema.safetensors
* **Resolution:** 512x512
* **Sampling Method:** Euler a
* **Sampling Steps:** 20
* **Batch Size:** 1
* **Result:**
    * Time taken: **4-5 seconds**
    * Iterations per second (it/s): **5.10 it/s**

## Test Case 2: High Quality / Upscale
* **Model:** Realistic_Vision_V5.1_fp16-no-ema.safetensors
* **Resolution:** 1024x1024
* **Sampling Method:** DPM++ 2M Karras
* **Sampling Steps:** 30
* **Result:**
    * Time taken: **35-45 seconds**
    * VRAM Usage: **95% Peak**

## 🔧 Optimizations Applied
* **`--xformers`**: Enabled to speed up attention mechanism.

## 📝 Observations
* Enabling xformers reduced generation time by approx 20%.
* Generating images above 1024x1024 significantly drops `it/s` due to shared system RAM swapping.