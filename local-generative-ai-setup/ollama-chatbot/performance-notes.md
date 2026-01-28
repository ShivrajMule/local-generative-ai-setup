# 🧠 LLM Performance Benchmarks

**Host Environment:** Ollama (Local)
**Hardware Context:**
* **Device:** Laptop HP VICTUS Ryzen7 7445HS
* **GPU:** NVIDIA RTX 3050, 6GB VRAM
* **RAM:** 16GB DDR5

## Model 1: The Generalist (Daily Driver)
* **Model:** `llama3.1:8b`
* **Use Case:** Email drafting, summarization, general queries.
* **Performance:**
  * **Speed:** aprox 40 to 45 tokens/sec
  * **VRAM Usage:** ~4.7 GB
  * **Observation:** The most balanced model. Fast response time with reliable instruction following.

## Model 2: The Specialist (Coding)
* **Model:** `qwen2.5-coder:7b`
* **Use Case:** Python scripts, debugging, SQL queries.
* **Performance:**
  * **Speed:** aprox 50 tokens/sec (Faster than Llama3.1 due to smaller param count)
  * **Accuracy:** Significantly better at one-shot code generation than Llama 3.1.
  * **Context Window:** Handles large code blocks without losing coherence.

## Model 3: The Logician (Reasoning)
* **Model:** `deepseek-r1:7b`
* **Use Case:** Complex logic puzzles, algorithm design, math problems.
* **Performance:**
  * **Speed:** aprox 35 tokens/sec (Slower due to Chain-of-Thought processing)
  * **Behavior:** Outputs distinct `<think>` traces before answering.
  * **Observation:** Outperforms Llama 3.1 on multi-step logic problems by breaking them down first.