<div align="center">

# Wasiq Nauman Qureshi

**Applied AI Engineer** · efficient ML systems · LLM inference infrastructure · agentic AI

[Portfolio](https://wasiqnauman.github.io/) · [Email](mailto:wasiq.qureshi@hotmail.com) 

</div>

---

## Open Source Contributions

**Patches contributed to production systems used by thousands of developers.**

|            PR             | Repository                                                                                              | Impact                                                                                                                                                                                                     |
| :-----------------------: | :------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  **#163** ✅&nbsp;merged  | **[NandhaKishorM/laya](https://github.com/NandhaKishorM/laya)** · **24.1k ★** · 2.1k forks              | Shipped configurable option-label overrides for a non-autoregressive decision engine serving **100+ languages**. Pre-inference validation; default path stays byte-for-byte compatible.                    |
|  **#339** ✅&nbsp;merged  | **[mpfaffenberger/code_puppy](https://github.com/mpfaffenberger/code_puppy)** · 830 ★ · 170k+ downloads | Fixed a Windows ripgrep bug where `shlex.split` corrupted regex (`\b`, `\d+`) and paths (`C:\Users`) → **silent zero-match results**. Backslashes preserved, real errors surfaced, regression tests added. |
|  **#192** ✅&nbsp;merged  | **[mpfaffenberger/code_puppy](https://github.com/mpfaffenberger/code_puppy)** · 830 ★ · 170k+ downloads | Built the Synthetic provider status plugin + authenticated quota client — live usage limits, remaining quota, and renewal time from the agent CLI.                                                         |
| **#63** ✅&nbsp;merged | **[code_puppy_core_plugins](https://github.com/mpfaffenberger/code_puppy_core_plugins)**                | Removed scan-time code execution from the tool registry: static AST parsing of metadata, deferred imports, `sys.path` precedence preserved, partial-module cleanup on failure. **47 tests** passing.       |
| **#970** 🔄&nbsp;in review | **[mpfaffenberger/code_puppy](https://github.com/mpfaffenberger/code_puppy)** · 830 ★ · 170k+ downloads | Made the registry-scan fix mandatory for every install: raised the core dependency floor to the patched plugin release (`0.0.70`). Validated across **8,339 tests** on Python 3.13. |

---

## Research & Papers

### 🧠 SynthMRI — latent diffusion for synthetic multi-modal brain-tumour MRI

**[Code](https://github.com/wasiqnauman/SynthMRI)** · **[Paper](https://github.com/wasiqnauman/SynthMRI/blob/main/paper/main.pdf)** · BraTS 2020 · 258 / 37 / 74 patient split

<p>
<img alt="FID" src="https://img.shields.io/badge/FID-10.45_(real_ceiling_9.55)-blue">
<img alt="Memorization" src="https://img.shields.io/badge/copied_samples-0.97_%E2%86%92_0.04-green">
<img alt="Dice" src="https://img.shields.io/badge/downstream_Dice-%2B0.027-green">
<img alt="SSIM" src="https://img.shields.io/badge/SSIM-0.833_%E2%86%92_0.883-green">
</p>

- **Near-real generation:** FID **10.45** @ 256 px vs **9.55** real→real ceiling.
- **Fixed memorisation, not quality:** affine latent augmentation + dropout drove copied training samples **97% → 4%** while improving FID **26.22 → 20.85**.
- **Synthetic data helps downstream segmentation:** **+0.027** mean Dice (256 px); **+0.021** Dice at only 10% real via pre-training.
- **Diagnosed the bottleneck:** frozen SD-VAE decoder costs 0.06–0.07 Dice; fine-tuning it lifts SSIM **0.833 → 0.883** and cuts per-modality FID **35–75%**.
- **Cheap:** full 128 px run trains in **1.5 h on a single RTX A6000**.

### ⚡ VeloInference — async dynamic-batching inference gateway

**[Code](https://github.com/wasiqnauman/veloinference)** · **[Paper](https://github.com/wasiqnauman/veloinference/blob/main/paper/main.pdf)** · Qwen2.5-1.5B · RTX 3060

<p>
<img alt="Requests" src="https://img.shields.io/badge/requests-6%2C912-blue">
<img alt="Conditions" src="https://img.shields.io/badge/conditions-48_(4_paths_%C3%97_4_rates_%C3%97_3_seeds)-blue">
<img alt="p95" src="https://img.shields.io/badge/p95_penalty-%2B1.05%E2%80%931.51_s-red">
<img alt="R2" src="https://img.shields.io/badge/serial--occupancy_R%C2%B2-0.9985-green">
</p>

- **Counterintuitive, measured result:** batching at the gateway before an already-batching engine made p95 latency **+1.05–1.51 s worse** at 1.0–1.8 req/s.
- **Mechanism found:** a nominal **1 ms** wait inflated to **767–833 ms** queue delay because the coordinator serialises backend calls; the serial-occupancy model matches measured group sizes at **R² = 0.9985** (0.86% MAPE).
- **Rigorous harness:** absolute-time open-loop arrivals, paired by seed, with validity gates that reject incomplete runs.

---

## Tech Stack

<div align="center">

**Languages & Core**

<img alt="Python, C++, C,CUDA " src="https://skillicons.dev/icons?i=py,cpp,c" height="44" />

**ML & Deep Learning**

<img alt="PyTorch, TensorFlow, scikit-learn, OpenCV" src="https://skillicons.dev/icons?i=pytorch,tensorflow,scikitlearn" height="44" />
<br/>
<img alt="Hugging Face" src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" />
<img alt="NumPy" src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img alt="Pandas" src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />

**LLM Systems, Agents & Inference**

<img alt="vLLM" src="https://img.shields.io/badge/vLLM-1C1C1C?style=for-the-badge&logo=vllm&logoColor=white" />
<img alt="LangChain" src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" />
<img alt="Triton" src="https://img.shields.io/badge/Triton-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img alt="CUDA" src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
<img alt="FastAPI" src="https://skillicons.dev/icons?i=fastapi" height="28" />

**Data, MLOps & Cloud**

<img alt="PostgreSQL, Redis, Kafka, MongoDB, MySQL" src="https://skillicons.dev/icons?i=postgres,redis,kafka,mongodb,mysql" height="44" />
<br/>
<img alt="Docker, Kubernetes, AWS, GCP, Azure" src="https://skillicons.dev/icons?i=docker,kubernetes,aws,gcp,azure" height="44" />
<br/>

<br/>
<img alt="MLflow" src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" />
<img alt="Weights & Biases" src="https://img.shields.io/badge/W%26B-FFBE00?style=for-the-badge&logo=weightsandbiases&logoColor=black" />

**Also:** RAG · LoRA/QLoRA fine-tuning · quantization · DDIM/DDPM · dynamic batching · deadline-aware scheduling · LLM evals · distributed training

</div>

---

## Systems Projects

| Project                                                                                           | What it does                                          | Signal                                                    |
| :------------------------------------------------------------------------------------------------ | :---------------------------------------------------- | :-------------------------------------------------------- |
| **[GBDT-Cpp-Engine](https://github.com/wasiqnauman/GBDT-Cpp-Engine)**                             | C++17 gradient-boosted-tree inference runtime         | Beats scikit-learn, XGBoost & LightGBM Python APIs on CPU |
| **[Fashion-Recommendation-System](https://github.com/wasiqnauman/Fashion-Recommendation-System)** | Two-stage recommender on the H&M dataset              | Candidate generation separated from ranking               |
| **[digital-wallet](https://github.com/wasiqnauman/digital-wallet)**                               | Async wallet over WebSockets + REST + custom protocol | Real-time transactions, SQL persistence, fault tolerance  |

---

<div align="center">

Open to ML-systems / inference / agentic-AI roles — [let's talk](mailto:wasiq.qureshi@hotmail.com)

</div>

