[![@rphi's Holopin board](https://holopin.me/mranaydongre)](https://holopin.io/@mranaydongre)

```python
class AnayDongre:
    role      = "ML Engineer"
    code      = ["Python", "Rust", "C++", "CUDA", "TypeScript"]
    focus     = ["LLM Inference", "Training Infrastructure", "Open Source"]
    research  = ["Speculative Decoding", "KV Cache Optimization", "PEFT"]
    
    kaggle    = "3x Master"
    school    = "MSCS @ Cal Poly Pomona (Dec 2026)"
    
    def current_work(self):
        return [
            "Contributing to sglang, nano-vllm, CocoIndex",
            "Building EigenTune — SVD-based PEFT (pip install eigentune)",
            "Competing in Kaggle NVIDIA Nemotron Reasoning Challenge",
        ]
```

---

### Merged & Shipped

> I contribute code to ML infrastructure projects that other engineers depend on.

**[CocoIndex](https://github.com/cocoindex-io/cocoindex)** — PR [#1010](https://github.com/cocoindex-io/cocoindex/pull/1010) merged. Built `SplitBySeparators` as a native **Rust crate** with PyO3 bindings. GIL-free text splitting for ETL hot paths where every millisecond matters.

**[sglang](https://github.com/sgl-project/sglang)** — Active contributor. LLM serving framework for structured generation and fast inference.

**[nano-vllm](https://github.com/GeeeekExplorer/nano-vllm)** — Contributing to lightweight LLM inference engine. 12.9k stars.

**[Hugging Face Hub](https://github.com/huggingface) · [PyTorch-Lightning](https://github.com/Lightning-AI/pytorch-lightning)** — Bug fixes, patches, examples.

---

### Things I Built

<table>
<tr>
<td width="50%" valign="top">

**[EigenTune](https://github.com/MrAnayDongre/eigentune)** — PEFT via SVD

[![PyPI](https://img.shields.io/pypi/v/eigentune?color=3775A9&logo=pypi&logoColor=white)](https://pypi.org/project/eigentune/)

Decomposes weight matrices via SVD. Freezes U/V. Learns 4-bit scalars. **99.5% fewer trainable params**, matching full fine-tuning.

Ships with CUDA kernels, GGUF/ONNX export, and HuggingFace Trainer integration.

```
pip install eigentune
```

</td>
<td width="50%" valign="top">

**[Nano LLAMA](https://huggingface.co/DrNerd/LLAMA-3-From-Scratch)** — from scratch

221M-param decoder-only transformer. RMSNorm, RoPE, SwiGLU, mixed-precision, gradient checkpointing. Trained on a **single 4GB GPU**.

Reproducible scripts. No cloud budget required.

</td>
</tr>
</table>

---

### Research

**[Transactional KV Caching for Speculative Decoding under Paged KV Memory](https://www.techrxiv.org/)** — *TechRxiv (IEEE)*, 2026

Draft tokens inflate KV cache pages and fragment memory at high load. TransKV treats speculative writes as a transaction — buffer drafts, commit only accepted tokens, roll back the rest. Exact output equivalence, better throughput.

**Blockchain-Based E-Voting with Proof-of-Work and ML** — *IET Blockchain*, 2023 (peer-reviewed)

---

### Stack

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Rust-000?style=flat-square&logo=rust&logoColor=white" />
<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
<img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/JAX-A8B9CC?style=flat-square&logo=google&logoColor=white" />
<img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/K8s-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
</p>


---

<p align="center">
<b>AWS ML Specialty</b> · <b>3x Kaggle Master</b> · <b>Codeforces</b> · <b>Akuna Capital Trading Competition</b>
</p>

<p align="center">
<a href="https://linkedin.com/in/anayd"><img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
<a href="https://www.kaggle.com/adhoppin"><img src="https://img.shields.io/badge/-Kaggle-20BEFF?style=flat-square&logo=kaggle&logoColor=white" /></a>
<a href="mailto:dongreanay@gmail.com"><img src="https://img.shields.io/badge/-Email-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
<a href="https://medium.com/@dongreanay"><img src="https://img.shields.io/badge/-Medium-000?style=flat-square&logo=medium&logoColor=white" /></a>
<a href="https://pypi.org/project/eigentune/"><img src="https://img.shields.io/badge/-PyPI-3775A9?style=flat-square&logo=pypi&logoColor=white" /></a>
</p>
