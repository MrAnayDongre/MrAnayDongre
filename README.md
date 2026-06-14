<div align="center">
    
# Anay Dongre

### ML Systems Engineer

*I build LLM inference systems, agentic AI platforms, and GPU kernels.*

<img width="1881" height="836" alt="github_readme_page" src="https://github.com/user-attachments/assets/4b38cb4d-bb62-4f34-a777-e3ad4eaeaf2b" />

<a href="https://linkedin.com/in/anayd"><img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white&logoWidth=14" height="25" /></a>&nbsp;
<a href="https://medium.com/@dongreanay"><img src="https://img.shields.io/badge/-Blog-000?style=flat-square&logo=medium&logoColor=white" height="25" /></a>&nbsp;
<a href="https://scholar.google.com/citations?user=PDD7atoAAAAJ"><img src="https://img.shields.io/badge/-Scholar-4285F4?style=flat-square&logo=googlescholar&logoColor=white" height="25" /></a>&nbsp;
<a href="https://pypi.org/project/eigentune/"><img src="https://img.shields.io/badge/-PyPI-3775A9?style=flat-square&logo=pypi&logoColor=white" height="25" /></a>&nbsp;
<a href="mailto:dongreanay@gmail.com"><img src="https://img.shields.io/badge/-Email-EA4335?style=flat-square&logo=gmail&logoColor=white" height="25" /></a>


</div>

---

### 🔨 Shipped

<table>
<tr>
<td width="50%" valign="top">

<h4><a href="https://github.com/MrAnayDongre/PatchQuest">PatchQuest</a></h4>

**Agentic coding harness for small models**

12-phase deterministic pipeline that makes small and open-weight models reliable on real repository tasks. Tree-sitter symbol extraction builds a code graph for repo intelligence. SecretGuard credential scanning. 4-tier command-risk gating. Docker sandboxing with network isolation. Mock mode for keyless evaluation. Solo-built end-to-end.

<a href="https://www.python.org"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /></a>
<a href="https://fastapi.tiangolo.com"><img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" /></a>
<a href="https://react.dev"><img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" /></a>
<a href="https://www.sqlite.org"><img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" /></a>
<a href="https://www.docker.com"><img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" /></a>

8 LLM providers including
<a href="https://build.nvidia.com"><img src="https://img.shields.io/badge/NVIDIA_NIM-76B900?style=flat-square&logo=nvidia&logoColor=white" /></a>

</td>
<td width="50%" valign="top">

<h4><a href="https://github.com/MrAnayDongre/eigentune">EigenTune</a>&ensp;<a href="https://pypi.org/project/eigentune/"><img src="https://img.shields.io/pypi/v/eigentune?color=3775A9&logo=pypi&logoColor=white&style=flat-square" /></a></h4>

**CUDA kernels for SVD-based model optimization**

Parameter-efficient fine-tuning via SVD decomposition. Decomposes weight matrices, freezes U/V bases, learns lightweight scalars. Hand-written CUDA kernels managing GPU shared memory, thread synchronization, and warp-level execution. Profiled with Nsight Compute. ONNX export for cross-architecture deployment. HuggingFace Trainer integration. Full test suite, CI/CD.

<a href="https://developer.nvidia.com/cuda-toolkit"><img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white" /></a>
<a href="https://isocpp.org"><img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" /></a>
<a href="https://pytorch.org"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" /></a>
<a href="https://onnx.ai"><img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white" /></a>

**700+ installs** · `pip install eigentune`

</td>
</tr>
<tr>
<td width="50%" valign="top">

<h4><a href="https://huggingface.co/DrNerd/LLAMA-3-From-Scratch">Nano LLAMA</a></h4>

**221M-parameter transformer from scratch**

Full decoder-only transformer built at the numerical level in PyTorch. Implements RMSNorm, Rotary Positional Embeddings (RoPE), SwiGLU gated activations, grouped multi-head attention, mixed-precision training (fp16/bf16), and gradient checkpointing. Trained on a single 4GB GPU with reproducible scripts. No cloud budget, no framework wrappers, just raw PyTorch.

<a href="https://pytorch.org"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" /></a>
<a href="https://huggingface.co"><img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black" /></a>

</td>
<td width="50%" valign="top">

<h4>Parameter Golf</h4>

**Mixed-precision quantization pipeline**

Custom mixed int6/int8 quantization with per-row clip-search calibration for 24–27M parameter transformers. Per-layer numerical error analysis under strict model-size constraints. Investigated accuracy-compression tradeoffs across quantization configurations.

<a href="https://pytorch.org"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" /></a>
<a href="https://www.python.org"><img src="https://img.shields.io/badge/Quantization-3776AB?style=flat-square&logo=python&logoColor=white" /></a>

</td>
</tr>
</table>

---

### 📄 Research

&ensp;📌&ensp;**[TransKV: Transactional KV Staging for Speculative Decoding under Paged KV Memory](https://www.techrxiv.org/)**
&ensp;&ensp;&ensp;&ensp;&ensp;*TechRxiv (IEEE), 2026* · Under submission to EMNLP 2026 workshop
> Speculative decoding inflates KV cache pages and fragments memory under load. TransKV isolates speculative state in staging blocks, commits only accepted tokens, rolls back the rest. **14–41% reduction** in committed-cache write traffic with formal output-equivalence proofs across Qwen2.5 model pairs.

&ensp;📌&ensp;**Blockchain-Based E-Voting with Proof-of-Work and ML** — *IET Blockchain*, 2023 (peer-reviewed)

&ensp;📌&ensp;**NeRF: A Comprehensive Survey** — *IJISRT*, 2023

---

### 🔧 Open Source

> I contribute to ML infrastructure that other engineers depend on.

&ensp;**[vLLM](https://github.com/vllm-project/vllm)** · [PR #44693](https://github.com/vllm-project/vllm/pull/44693) — Runtime memory optimization and KV-cache scheduling &ensp; ![](https://img.shields.io/badge/under_review-yellow?style=flat-square)

&ensp;**[CocoIndex](https://github.com/cocoindex-io/cocoindex)** · [PR #1010](https://github.com/cocoindex-io/cocoindex/pull/1010) — Native Rust/PyO3 crate, throughput bottleneck fix &ensp; ![](https://img.shields.io/badge/merged-brightgreen?style=flat-square)

&ensp;**[sglang](https://github.com/sgl-project/sglang)** · Structured generation, inference scheduling &ensp; ![](https://img.shields.io/badge/active-blue?style=flat-square)

&ensp;**[nano-vllm](https://github.com/GeeeekExplorer/nano-vllm)** · Lightweight LLM inference engine &ensp; ![](https://img.shields.io/badge/active-blue?style=flat-square)

---

### ✍️ Writing

&ensp;<a href="https://towardsai.net/p/machine-learning/llama-architecture-a-deep-dive-into-efficiency-and-mathematics"><img src="https://img.shields.io/badge/Towards_AI-LLaMA_Architecture_Deep_Dive-000?style=flat-square&logo=medium&logoColor=white" /></a>

&ensp;<a href="https://towardsai.net/p/machine-learning/pytorch-lightning-an-introduction-to-the-lightning-fast-deep-learning-framework"><img src="https://img.shields.io/badge/Towards_AI-PyTorch_Lightning_Introduction-000?style=flat-square&logo=medium&logoColor=white" /></a>

&ensp;<a href="https://medium.com/@dongreanay"><img src="https://img.shields.io/badge/All_Posts_→-000?style=flat-square&logo=medium&logoColor=white" /></a>

---

<div align="center">

3× Kaggle Master · Codeforces · AWS ML Specialty · Previously at Aerolift.AI and JPMorgan Chase

</div>
