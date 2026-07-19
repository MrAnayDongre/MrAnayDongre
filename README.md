<div align="center">

<h1 id="anay-dongre">Anay Dongre</h1>
<h3 id="ml-systems-engineer--llm-inference--gpu-kernels">ML Systems
Engineer · LLM Inference · GPU Kernels</h3>
<p>I like working close to the metal on LLM inference, especially where memory movement, kernels, and serving decisions shape real performance. Most of my work starts with understanding a system from first principles, building it, and measuring what actually helps. I also enjoy carrying those ideas beyond experiments, whether that means an open-source contribution or a research result.</p>
<p><a href="https://linkedin.com/in/anayd"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" height="24" alt="LinkedIn" /></a>
<a href="https://scholar.google.com/citations?user=PDD7atoAAAAJ"><img src="https://img.shields.io/badge/Google_Scholar-4285F4?style=flat-square&logo=googlescholar&logoColor=white" height="24" alt="Google Scholar" /></a>
<a href="https://medium.com/@dongreanay"><img src="https://img.shields.io/badge/Writing-000000?style=flat-square&logo=medium&logoColor=white" height="24" alt="Writing" /></a>
<a href="mailto:dongreanay@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" height="24" alt="Email" /></a></p>
</div>

<hr />
<h2 id="selected-systems--research">Selected Systems &amp; Research</h2>
<h3 id="inference-kernels-from-scratch"><a
href="https://github.com/MrAnayDongre/Inference-Kernels">Inference
Kernels from Scratch</a></h3>
<p><strong>Triton · PyTorch · CUDA concepts · LLM serving</strong></p>
<p>Implemented the core mechanisms of modern LLM inference from first
principles: KV caching, paged KV allocation, fused
RMSNorm/RoPE/SwiGLU/softmax kernels, FlashAttention-style tiled
attention, PagedAttention-style decode, continuous batching, weight-only
quantization, and speculative decoding.</p>
<ul>
<li><strong>3.3–3.5×</strong> RMSNorm and <strong>5–6.5×</strong> RoPE
speedups over the documented PyTorch baselines</li>
<li><strong>2.14×</strong> PagedAttention-style decode speedup on the
smaller benchmark case with <strong>~36% KV-memory savings</strong></li>
<li><strong>3.19× lower average latency</strong> in the
continuous-batching simulator</li>
<li>Correctness checks, benchmark methodology, hardware details, and
implementation limitations are documented in the repository</li>
</ul>
<blockquote>
<p>Educational implementations for understanding and benchmarking the
mechanisms—not replacements for production kernels such as
FlashAttention, vLLM, cuBLAS, or TensorRT-LLM.</p>
</blockquote>
<h3
id="transkv-transactional-kv-caching-for-speculative-decoding-under-paged-kv-memory"><a
href="https://doi.org/10.36227/techrxiv.177101038.80960856/v1">TransKV:
Transactional KV Caching for Speculative Decoding under Paged KV
Memory</a></h3>
<p><strong>Research preprint · KV-cache memory · speculative
decoding</strong></p>
<p>Proposes a transactional KV-cache abstraction that separates
committed paged state from a packed speculative buffer. Only accepted
draft tokens are committed; rejected speculative KV is discarded without
rolling back committed pages.</p>
<ul>
<li>Formal cache-semantic equivalence argument</li>
<li>Kernel-facing paged-cache overlay and commit design</li>
<li>Real-GPU capacity experiments on Tesla P100 and T4 systems</li>
<li>Up to <strong>1.78× branch concurrency</strong> in the reported
capacity-limited prefix-sharing setup</li>
</ul>
<p><em>TechRxiv preprint, 2026.</em></p>
<h3 id="patchquest"><a
href="https://github.com/MrAnayDongre/PatchQuest">PatchQuest</a></h3>
<p><strong>Local-first agentic coding harness for small and open-weight
models</strong></p>
<p>Solo-built full-stack system that constrains coding agents with a
deterministic 12-phase state machine rather than open-ended autonomy.
Includes Tree-sitter symbol extraction and code-graph context, scoped
agent roles, SecretGuard credential scanning, four-tier command-risk
gating, structured patching, test execution, and Docker sandboxing with
network isolation.</p>
<p><code>Python</code> · <code>FastAPI</code> · <code>React</code> ·
<code>SQLite</code> · <code>Docker</code> · <code>Tree-sitter</code> ·
<strong>331 backend tests</strong></p>
<h3 id="eigentune--pypi"><a
href="https://github.com/MrAnayDongre/eigentune">EigenTune</a> · <a
href="https://pypi.org/project/eigentune/">PyPI</a></h3>
<p><strong>SVD-based parameter-efficient fine-tuning
package</strong></p>
<p>A PyTorch/PEFT package that decomposes linear weights as
<code>W = UΣVᵀ</code>, freezes the singular-vector bases, and learns
lightweight rank-<code>r</code> magnitude updates instead of introducing
full trainable matrices.</p>
<div class="sourceCode" id="cb1"><pre
class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="ex">pip</span> install eigentune</span></code></pre></div>
<h3 id="nano-llama"><a
href="https://huggingface.co/DrNerd/LLAMA-3-From-Scratch">Nano
LLaMA</a></h3>
<p><strong>~221M-parameter decoder-only transformer built from
scratch</strong></p>
<p>Educational PyTorch implementation of RMSNorm, RoPE, multi-head
attention, SwiGLU, weight tying, mixed-precision training,
checkpointing, and a reproducible training pipeline demonstrated on a
single ~4 GB VRAM GPU.</p>
<hr />
<h2 id="open-source">Open Source</h2>
<ul>
<li><strong><a
href="https://github.com/vllm-project/vllm/pull/44693">vLLM PR
#44693</a></strong> — Added regression coverage for mixed-dtype
<code>fused_add_rms_norm</code> RMS quant fusion; includes targeted
checks and a feasible Qwen3.5 end-to-end validation.
<strong>Open</strong></li>
<li><strong><a
href="https://github.com/cocoindex-io/cocoindex/pull/1010">CocoIndex PR
#1010</a></strong> — Added <code>SplitBySeparators</code> across the
Rust executor and Python specification; incorporated maintainer review
and passed the documented test suite. <strong>Merged</strong></li>
</ul>
<hr />
<h2 id="writing">Writing</h2>
<ul>
<li><a
href="https://towardsai.net/p/machine-learning/llama-architecture-a-deep-dive-into-efficiency-and-mathematics">LLaMA
Architecture: A Deep Dive into Efficiency and Mathematics</a></li>
<li><a
href="https://towardsai.net/p/machine-learning/pytorch-lightning-an-introduction-to-the-lightning-fast-deep-learning-framework">PyTorch
Lightning: An Introduction to the Lightning-Fast Deep Learning
Framework</a></li>
<li><a href="https://medium.com/@dongreanay">More articles</a></li>
</ul>
<hr />
<div align="center">

<p><strong>3× Kaggle Master · Codeforces · AWS Machine Learning
Specialty</strong><br />
Previously at <strong>Aerolift.AI</strong> and <strong>JPMorgan
Chase</strong></p>
</div>
