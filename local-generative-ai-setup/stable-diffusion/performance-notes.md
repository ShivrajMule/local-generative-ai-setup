# 📊 Performance Benchmarks: Stable Diffusion

**Hardware Context:**
* **Device:** Laptop HP VICTUS Ryzen 7 7445HS
* **GPU:** NVIDIA RTX 3050, 6GB VRAM
* **RAM:** 16GB DDR5

## Test Case 1: Standard Generation
* **Model:** Realistic Vision V5.1 (FP16)
* **Resolution:** 512x512
* **Sampling Method:** DPM++ 2M
* **Sampling Steps:** 20
* **Result:**
    * Average Speed: **4.19 it/s**
    * Generation Time: approx **5 seconds**
* **Logs:**
    > `Applying attention optimization: xformers... done`

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
