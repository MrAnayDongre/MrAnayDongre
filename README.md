# Anay Dongre

ML systems engineer working on LLM inference, GPU kernels, and reliable agent runtimes.

I like working close to the model/runtime boundary: finding out where a system actually spends its time and memory, then building around that. I mostly learn by building the thing and measuring it, and I try to be honest in the benchmarks about what they don't show.

## Selected work

**[PatchQuest](https://github.com/MrAnayDongre/PatchQuest)** is a durable runtime for long-horizon software agents. Runs are checkpointed, so if a worker dies another one picks the run up where it stopped, and the patch still lands once. Any run can be replayed or forked from a checkpoint. Commands go through a sandbox and an approval policy, with a workflow engine and an eval harness on top.

**[Inference-Kernels](https://github.com/MrAnayDongre/Inference-Kernels)** is my attempt to understand LLM inference by writing it: KV cache, paged attention, fused Triton kernels, continuous batching, quantization, speculative decoding. Each piece has a correctness check and a benchmark. It's educational, and the README says so.

**[WarpServe](https://github.com/MrAnayDongre/WarpServe)** goes lower, into CUDA. Small custom kernels first, then the same ideas measured against PyTorch and CUTLASS in an end-to-end serving loop on a laptop GPU.

**[EigenTune](https://github.com/MrAnayDongre/eigentune)** freezes a layer's SVD bases and learns only a small rank-r scaling of the singular values, as a parameter-efficient fine-tuning method. `pip install eigentune`.

## Research

**[TransKV](https://doi.org/10.36227/techrxiv.177101038.80960856/v1)**: transactional KV caching for speculative decoding under paged KV memory. TechRxiv preprint.

## Open source

A few merged contributions to [CocoIndex](https://github.com/cocoindex-io/cocoindex/pulls?q=is%3Apr+author%3AMrAnayDongre+is%3Amerged), and an open [pull request to vLLM](https://github.com/vllm-project/vllm/pull/44693) on mixed-dtype RMSNorm quant fusion.

## Contact

[LinkedIn](https://linkedin.com/in/anayd) · [Email](mailto:dongreanay@gmail.com)
