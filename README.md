# Awesome High Performance Systems & Compiler Infrastructure [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A comprehensive, curated directory of high-performance compiler frameworks, intermediate representation (IR) toolchains, AI accelerator backends, heterogeneous GPU computing runtimes, and interactive compilation sandboxes. Features commercial SaaS / cloud platforms alongside battle-tested open-source ecosystems.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS & Cloud-Hosted Platforms](#saas--cloud-hosted-platforms)
- [Open-Source Equivalents & Toolchains](#open-source-equivalents--toolchains)
  - [Core Compiler Toolchains & Backends](#core-compiler-toolchains--backends)
  - [MLIR, Tensor & AI Accelerator Compilers](#mlir-tensor--ai-accelerator-compilers)
  - [GPU, Heterogeneous & HPC Parallel Compilers](#gpu-heterogeneous--hpc-parallel-compilers)
  - [Self-Hosted Compiler Explorers & Execution Sandboxes](#self-hosted-compiler-explorers--execution-sandboxes)
  - [High-Performance Systems Languages & Build Infrastructure](#high-performance-systems-languages--build-infrastructure)
- [Contributing](#contributing)

---

## Sector Overview & Market Dynamics

The high-performance systems and compiler infrastructure market represents an estimated **$17B–$22B+** sector (surging toward **$200B+ by 2035** driven by AI acceleration and specialized silicon), characterized by a **highly concentrated, winner-take-all dynamic** at the hardware-firmware layer (dominated by NVIDIA's proprietary CUDA/NVCC ecosystem) alongside an **open-standard consensus layer** coalescing around LLVM, MLIR, and Triton where hyperscalers, chipmakers, and independent startups co-develop portable domain-specific compiler backends.

---

## SaaS & Cloud-Hosted Platforms

Below are leading commercial cloud compiler platforms, managed accelerator runtimes, interactive code evaluation engines, and automated processor compiler generation suites, sorted in descending order by company valuation / market capitalization.

| Platform | Description | Starting Pricing Tier | Free Tier Limits / Evaluation | Company Valuation / Revenue |
| :--- | :--- | :--- | :--- | :--- |
| **[NVIDIA CUDA Toolkit & NGC Cloud](https://nvidia.com)** | Enterprise GPU compute stack, NVCC compiler suite, and cloud container registry for accelerated computing. | **$1.00/GPU-hour** on cloud marketplaces; **$4,500/GPU/year** for NVIDIA AI Enterprise license. | **Free forever** for standard developer CUDA toolkit; **90-day free trial** for NVIDIA AI Enterprise with full microservice access. | **~$3.5 Trillion** Market Cap (NVIDIA Corp.) |
| **[Intel Tiber Developer Cloud](https://cloud.intel.com)** | Cloud-hosted development cluster for Intel oneAPI compilers (ICX, IFX), SYCL, Xeon CPUs, and Gaudi AI accelerators. | **$0.00/hour** base tier; paid instances start on pay-as-you-go hourly rates upon portal registration. | **Free forever (Standard Tier)**: Complimentary access to Jupyter notebooks with AI toolchains and shared Intel Xeon evaluation instances. | **~$105 Billion** Market Cap (Intel Corp.) |
| **[Modular Mojo Cloud & MAX Platform](https://modular.com)** | Cloud-accelerated Mojo execution engine and MAX compiler platform built on MLIR for heterogeneous hardware. | **$0.00** developer engine; cloud API inference and server compute start at consumption-based rates. | **Free forever** local Mojo compiler and MAX developer edition for individual engineers; enterprise tier offers evaluation credits. | **$3.92 Billion** (Acquired by Qualcomm; previously valued at $1.6B Series C) |
| **[Codasip Studio Cloud](https://codasip.com)** | SaaS/cloud processor design environment and automated LLVM-based C/C++ compiler generator for custom RISC-V architectures. | **Enterprise quote** upon request (custom per-seat EDA licensing packages). | **Free proof-of-concept evaluation** upon qualified enterprise sales consultation; academic free tiers available. | **~$15 Million+** (Low-end IP division divested to onsemi for up to $14.5M; funded by €119M+ EU/venture grants) |
| **[OnlineGDB](https://onlinegdb.com)** | Cloud-hosted multi-compiler sandbox and debugger supporting interactive C, C++, Python, and Rust execution. | **Paid Premium** ad-free tier starting on monthly/annual plans without auto-renewal. | **Free forever**: 10-second compilation/run cap in text mode, 15-minute console timeout, 256 MB RAM limit, 100 KB max file size. | **~$1 Million – $5 Million** (Independent ad-supported web application processing millions of compiles) |
| **[Compiler Explorer (godbolt.org)](https://godbolt.org)** | Hosted interactive assembly and IR inspector supporting hundreds of compiler releases across dozens of languages. | **$1.00/month** community Patreon backer tier ("Warm fuzzy glow"); $5.00/month for Coder Karma recognition. | **Free forever**: Full unrestricted access to interactive assembly inspection and multi-compiler diffing (no paywalled compiler features). | **Community-backed Non-Profit** (~$3,000/month infrastructure operating cost; backed by Google, Intel, Solid Sands, & Patreon) |
| **[Rust Playground](https://play.rust-lang.org)** | Official community-hosted web sandbox for compiling, running, and inspecting MIR/LLVM-IR/Assembly for Rust code. | **$0.00** (Open community service funded by the Rust Foundation and infrastructure partners). | **Free forever**: Sandboxed code execution with a 10-second CPU execution timeout and memory caps. | **Non-Profit Infrastructure** (Supported directly by the Rust Foundation) |
| **[Wandbox](https://wandbox.org)** | Multi-compiler online playground providing instantaneous execution across bleeding-edge versions of GCC, Clang, and other languages. | **$0.00** (Community public utility maintained by melpon). | **Free forever**: Fully accessible public compilation with IP-based rate limiting, restricted CPU execution times, and sandboxed memory quotas. | **Open Community Utility** (Zero-revenue public utility supported by maintainers and open-source infrastructure) |

---

## Open-Source Equivalents & Toolchains

The foundational open-source compilers, intermediate representation dialects, kernel synthesis systems, and distributed HPC frameworks powering modern computing. Repositories are sorted in descending order by GitHub stargazer count within each category.

### Core Compiler Toolchains & Backends

* **[LLVM Project](https://github.com/llvm/llvm-project)** [![GitHub stars](https://img.shields.io/github/stars/llvm/llvm-project?style=social&color=white)](https://github.com/llvm/llvm-project/stargazers) - Modular and reusable compiler backend technologies, code optimizers, Clang frontend, and code generators powering modern programming languages.
* **[Mold](https://github.com/rui314/mold)** [![GitHub stars](https://img.shields.io/github/stars/rui314/mold?style=social&color=white)](https://github.com/rui314/mold/stargazers) - Ultra-fast, modern drop-in replacement linker designed to maximize multicore CPU utilization and drastically speed up compilation loops.
* **[GCC (GNU Compiler Collection)](https://github.com/gcc-mirror/gcc)** [![GitHub stars](https://img.shields.io/github/stars/gcc-mirror/gcc?style=social&color=white)](https://github.com/gcc-mirror/gcc/stargazers) - The bedrock open-source optimizing compiler suite supporting C, C++, Fortran, Ada, Go, and D across virtually every hardware architecture.
* **[Wasmtime](https://github.com/bytecodealliance/wasmtime)** [![GitHub stars](https://img.shields.io/github/stars/bytecodealliance/wasmtime?style=social&color=white)](https://github.com/bytecodealliance/wasmtime/stargazers) - Fast, secure, standalone WebAssembly runtime powered by the low-latency Cranelift optimizing compiler backend.
* **[CIRCT](https://github.com/llvm/circt)** [![GitHub stars](https://img.shields.io/github/stars/llvm/circt?style=social&color=white)](https://github.com/llvm/circt/stargazers) - Circuit IR Compilers and Tools applying MLIR and LLVM compiler infrastructure methodology to hardware description and Electronic Design Automation (EDA).
* **[QBE Compiler Backend](https://c9x.me/compile/)** - Minimalist, pure-C compiler backend designed to deliver 70% of LLVM's optimization performance in 10% of the code size.

### MLIR, Tensor & AI Accelerator Compilers

* **[JAX](https://github.com/google/jax)** [![GitHub stars](https://img.shields.io/github/stars/google/jax?style=social&color=white)](https://github.com/google/jax/stargazers) - Composable transformations of Python+NumPy programs with automatic differentiation and compilation via OpenXLA.
* **[tinygrad](https://github.com/tinygrad/tinygrad)** [![GitHub stars](https://img.shields.io/github/stars/tinygrad/tinygrad?style=social&color=white)](https://github.com/tinygrad/tinygrad/stargazers) - Deep learning framework and optimizing kernel compiler that prioritizes minimalism and hardware execution speed.
* **[Triton](https://github.com/triton-lang/triton)** [![GitHub stars](https://img.shields.io/github/stars/triton-lang/triton?style=social&color=white)](https://github.com/triton-lang/triton/stargazers) - Python-like programming language and MLIR-based compiler framework for generating ultra-efficient GPU compute kernels.
* **[Apache TVM](https://github.com/apache/tvm)** [![GitHub stars](https://img.shields.io/github/stars/apache/tvm?style=social&color=white)](https://github.com/apache/tvm/stargazers) - End-to-end deep learning compiler framework for CPUs, GPUs, and specialized hardware accelerators with automated auto-tuning.
* **[Halide](https://github.com/halide/Halide)** [![GitHub stars](https://img.shields.io/github/stars/halide/Halide?style=social&color=white)](https://github.com/halide/Halide/stargazers) - Domain-specific language and optimizing compiler designed for high-performance image processing and tensor pipelines, cleanly decoupling algorithm from schedule.
* **[OpenXLA / XLA](https://github.com/openxla/xla)** [![GitHub stars](https://img.shields.io/github/stars/openxla/xla?style=social&color=white)](https://github.com/openxla/xla/stargazers) - Domain-specific optimizing compiler for linear algebra, accelerating PyTorch, JAX, and TensorFlow across diverse accelerator chips.
* **[IREE](https://github.com/iree-org/iree)** [![GitHub stars](https://img.shields.io/github/stars/iree-org/iree?style=social&color=white)](https://github.com/iree-org/iree/stargazers) - Retargetable MLIR-based compiler and low-overhead runtime executing models across Vulkan, Metal, CUDA, and CPU microarchitectures.

### GPU, Heterogeneous & HPC Parallel Compilers

* **[Taichi Lang](https://github.com/taichi-dev/taichi)** [![GitHub stars](https://img.shields.io/github/stars/taichi-dev/taichi?style=social&color=white)](https://github.com/taichi-dev/taichi/stargazers) - High-performance parallel programming language embedded in Python that compiles spatial computing and physics kernels to CUDA, Metal, and Vulkan.
* **[AMD ROCm](https://github.com/ROCm/ROCm)** [![GitHub stars](https://img.shields.io/github/stars/ROCm/ROCm?style=social&color=white)](https://github.com/ROCm/ROCm/stargazers) - Open-source software development platform and compiler stack (amdclang++) for GPU-accelerated computing and machine learning.
* **[Slang](https://github.com/shader-slang/slang)** [![GitHub stars](https://img.shields.io/github/stars/shader-slang/slang?style=social&color=white)](https://github.com/shader-slang/slang/stargazers) - Shading language and multi-target compiler generating high-performance code for Direct3D, Vulkan, Metal, CUDA, and C++.
* **[Chapel](https://github.com/chapel-lang/chapel)** [![GitHub stars](https://img.shields.io/github/stars/chapel-lang/chapel?style=social&color=white)](https://github.com/chapel-lang/chapel/stargazers) - Productive, parallel open-source programming language and optimizing compiler engineered specifically for scalable distributed supercomputing.
* **[AdaptiveCpp (formerly hipSYCL)](https://github.com/AdaptiveCpp/AdaptiveCpp)** [![GitHub stars](https://img.shields.io/github/stars/AdaptiveCpp/AdaptiveCpp?style=social&color=white)](https://github.com/AdaptiveCpp/AdaptiveCpp/stargazers) - Modern multi-backend compiler supporting SYCL and C++ standard parallelism across NVIDIA, AMD, and Intel GPUs via LLVM.
* **[Enzyme](https://github.com/EnzymeAD/Enzyme)** [![GitHub stars](https://img.shields.io/github/stars/EnzymeAD/Enzyme?style=social&color=white)](https://github.com/EnzymeAD/Enzyme/stargazers) - High-performance LLVM compiler plugin performing automatic differentiation directly on LLVM IR for scientific computing and machine learning.
* **[Celerity Runtime](https://github.com/celerity/celerity-runtime)** [![GitHub stars](https://img.shields.io/github/stars/celerity/celerity-runtime?style=social&color=white)](https://github.com/celerity/celerity-runtime/stargazers) - Asynchronous C++ runtime bringing SYCL's single-source programming model to heterogeneous distributed GPU clusters.

### Self-Hosted Compiler Explorers & Execution Sandboxes

* **[Compiler Explorer (godbolt)](https://github.com/compiler-explorer/compiler-explorer)** [![GitHub stars](https://img.shields.io/github/stars/compiler-explorer/compiler-explorer?style=social&color=white)](https://github.com/compiler-explorer/compiler-explorer/stargazers) - Interactive web-based compilation investigation tool showing assembly and IR output across thousands of toolchains.
* **[Judge0](https://github.com/judge0/judge0)** [![GitHub stars](https://img.shields.io/github/stars/judge0/judge0?style=social&color=white)](https://github.com/judge0/judge0/stargazers) - Robust, scalable, multi-language sandboxed code execution engine supporting 60+ compilers and languages via REST API.
* **[Piston](https://github.com/engineer-man/piston)** [![GitHub stars](https://img.shields.io/github/stars/engineer-man/piston?style=social&color=white)](https://github.com/engineer-man/piston/stargazers) - High-performance general-purpose code execution and compilation engine running untrusted code in secure Docker containers.
* **[Rust Playground Engine](https://github.com/integer32llc/rust-playground)** [![GitHub stars](https://img.shields.io/github/stars/integer32llc/rust-playground?style=social&color=white)](https://github.com/integer32llc/rust-playground/stargazers) - Backend containerized compilation and execution engine powering play.rust-lang.org.

### High-Performance Systems Languages & Build Infrastructure

* **[llama.cpp](https://github.com/ggml-org/llama.cpp)** [![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=social&color=white)](https://github.com/ggml-org/llama.cpp/stargazers) - Pure C/C++ tensor library and quantization compiler backend providing zero-dependency high-throughput LLM inference across CPU, CUDA, Metal, and Vulkan.
* **[Rust (rustc)](https://github.com/rust-lang/rust)** [![GitHub stars](https://img.shields.io/github/stars/rust-lang/rust?style=social&color=white)](https://github.com/rust-lang/rust/stargazers) - Empowering systems language with fine-grained control, memory safety without garbage collection, and an advanced LLVM/Cranelift compiler pipeline.
* **[Julia](https://github.com/JuliaLang/julia)** [![GitHub stars](https://img.shields.io/github/stars/JuliaLang/julia?style=social&color=white)](https://github.com/JuliaLang/julia/stargazers) - High-level, high-performance dynamic programming language for technical and scientific computing, featuring an LLVM JIT optimizing compiler.
* **[Zig](https://github.com/ziglang/zig)** [![GitHub stars](https://img.shields.io/github/stars/ziglang/zig?style=social&color=white)](https://github.com/ziglang/zig/stargazers) - Robust systems programming language and drop-in C/C++ cross-compilation toolchain featuring compile-time code execution (`comptime`).
* **[Carbon Language](https://github.com/carbon-language/carbon-lang)** [![GitHub stars](https://img.shields.io/github/stars/carbon-language/carbon-lang?style=social&color=white)](https://github.com/carbon-language/carbon-lang/stargazers) - Experimental successor to C++ emphasizing performance, bidirectionality, and seamless interoperability.
* **[Bazel](https://github.com/bazelbuild/bazel)** [![GitHub stars](https://img.shields.io/github/stars/bazelbuild/bazel?style=social&color=white)](https://github.com/bazelbuild/bazel/stargazers) - Fast, scalable, multi-language build and test system supporting distributed caching and hermetic remote execution for massive compiler projects.
* **[Ninja](https://github.com/ninja-build/ninja)** [![GitHub stars](https://img.shields.io/github/stars/ninja-build/ninja?style=social&color=white)](https://github.com/ninja-build/ninja/stargazers) - Small, ultra-fast build system engineered specifically to accelerate compilation turnaround times for LLVM, Clang, and CMake.
* **[Odin](https://github.com/odin-lang/Odin)** [![GitHub stars](https://img.shields.io/github/stars/odin-lang/Odin?style=social&color=white)](https://github.com/odin-lang/Odin/stargazers) - Fast, data-oriented systems programming language built on LLVM for modern computer architectures.

---

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork this repository.
2. Add your compiler infrastructure project, MLIR dialect, or systems toolchain under the appropriate category.
3. Ensure open-source projects link to their GitHub repository with a corresponding star badge (`style=social` and `color=white`), and place them in descending order of stars within their section.
4. If submitting a SaaS product, include exact starting tier pricing, free tier limits, and company valuation / revenue metrics.
5. Submit a descriptive Pull Request.
