<div align="center">

# Wasiq Nauman

### Applied AI Engineer building efficient, reliable ML systems

[Portfolio](https://wasiqnauman.github.io/) · [Email](mailto:wasiq.qureshi@hotmail.com) · Seattle, WA

</div>

I turn machine-learning ideas into measured systems: inference infrastructure, agentic tooling, and recommendation pipelines. I am interested in PhD research at the intersection of **efficient ML systems**, **agentic AI**, and **reliable model deployment**.

## Open-source impact

I contribute to [Code Puppy](https://github.com/mpfaffenberger/code_puppy), an open-source agentic coding system:

- **[Synthetic provider integration](https://github.com/mpfaffenberger/code_puppy/pull/192)** — shipped provider status commands and a quota client, making model availability and usage limits observable from the agent CLI.
- **[Cross-platform tool reliability](https://github.com/mpfaffenberger/code_puppy/pull/339)** — fixed a Windows parsing bug that corrupted regex backslashes and file paths before they reached ripgrep, causing valid searches to silently return no matches.

## Selected work

| Project | What I explored |
| --- | --- |
| **[VeloInference](https://github.com/wasiqnauman/veloinference)** | Model-agnostic inference gateway with asynchronous dynamic batching, deadline-aware scheduling, and pluggable vLLM/Triton backends. |
| **[GBDT C++ Engine](https://github.com/wasiqnauman/GBDT-Cpp-Engine)** | Benchmark-driven C++17 runtime for low-latency tree-model inference, compared with scikit-learn, XGBoost, and LightGBM Python APIs. |
| **[Fashion Recommendation System](https://github.com/wasiqnauman/Fashion-Recommendation-System)** | Two-stage recommender on the H&M dataset, separating candidate generation from ranking. |

## Questions I want to pursue

- How can scheduling and batching improve inference throughput without violating latency targets?
- How do we make autonomous agents dependable across models, tools, providers, and operating systems?
- Which systems optimizations meaningfully improve the quality–latency–cost frontier?

**Working with:** Python · C++ · PyTorch · FastAPI · vLLM · Triton · LangChain · Docker · AWS

I am looking to collaborate with researchers working on **ML systems, efficient inference, and reliable agentic AI**. If these questions overlap with your lab's work, [let's talk](mailto:wasiq.qureshi@hotmail.com).
