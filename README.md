<div align="center">

# Wasiq Nauman

### Applied AI Engineer building efficient, reliable ML systems

[Portfolio](https://wasiqnauman.github.io/) · [Email](mailto:wasiq.qureshi@hotmail.com) · Seattle, WA

</div>

I turn machine-learning ideas into measured systems: inference infrastructure, agentic tooling, and recommendation pipelines. I am interested in research at the intersection of **efficient ML systems**, **agentic AI**, and **reliable model deployment**.

## Open-source impact

I contribute to [Code Puppy](https://github.com/mpfaffenberger/code_puppy), a widely-used, actively maintained agentic AI coding assistant (170,000+ Downloads, Python, 800+ ⭐, 260+ forks).

- **[Synthetic provider integration](https://github.com/mpfaffenberger/code_puppy/pull/192)** — shipped provider status commands and a quota client, making model availability and usage limits observable from the agent CLI.
- **[Cross-platform tool reliability](https://github.com/mpfaffenberger/code_puppy/pull/339)** — fixed a Windows parsing bug that corrupted regex backslashes and file paths before they reached ripgrep, causing valid searches to silently return no matches.

## Selected work

| Project | What I explored |
| --- | --- |
| **[VeloInference](https://github.com/wasiqnauman/veloinference)** | Model-agnostic inference gateway with asynchronous dynamic batching, deadline-aware scheduling, and pluggable vLLM/Triton backends. |
| **[GBDT C++ Engine](https://github.com/wasiqnauman/GBDT-Cpp-Engine)** | Benchmark-driven C++17 runtime for low-latency tree-model inference, compared with scikit-learn, XGBoost, and LightGBM Python APIs. |
| **[Fashion Recommendation System](https://github.com/wasiqnauman/Fashion-Recommendation-System)** | Two-stage recommender on the H&M dataset, separating candidate generation from ranking. |

## Questions I want to pursue

1. How can AI agents detect and recover from mistakes during long, multistep tasks with minimal human supervision?
     Small reasoning errors can compound into failed tasks; agents need reliable verification, error correction, and oversight.

  2. How can we reduce the compute, memory, and energy required for AI reasoning while preserving accuracy?
     More capable reasoning must become affordable to run at scale, creating research opportunities in algorithms, model compression, and hardware-aware systems.

  4. How can AI choose the next scientific experiment to maximize discovery from limited data and laboratory budgets?
     Useful scientific AI must identify promising experiments and produce discoveries that survive physical validation.

**Working with:** Python · C++ · PyTorch · FastAPI · vLLM · Triton · LangChain · Docker · AWS

I am looking to collaborate with researchers working on **ML systems, efficient inference, and reliable agentic AI**. If these questions overlap with your lab's work, [let's talk](mailto:wasiq.qureshi@hotmail.com).
