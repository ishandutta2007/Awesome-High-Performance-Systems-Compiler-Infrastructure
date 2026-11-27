# Awesome-High-Performance-Systems-Compiler-Infrastructure

# Awesome-High-Performance-Systems-Compiler-Infrastructure

Top High Performance Systems Compiler Infrastructure (Opensource) 🌟 Star if you like it! 🌟

A curated list of top high-performance systems programming tools, compiler toolchains, MLIR/IR frameworks, GPU/accelerator compilers, and interactive compilation sandboxes—featuring commercial SaaS/Hosted platforms alongside their open-source equivalents.

---

## Table of Contents

- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source Equivalents & Tools](#open-source-equivalents--tools)
  - [Core Compiler Toolchains & Backends](#core-compiler-toolchains--backends)
  - [MLIR, Tensor & AI Accelerator Compilers](#mlir-tensor--ai-accelerator-compilers)
  - [GPU, Heterogeneous & HPC Parallel Compilers](#gpu-heterogeneous--hpc-parallel-compilers)
  - [Self-Hosted Compiler Explorers & Code Sandboxes](#self-hosted-compiler-explorers--code-sandboxes)
  - [High-Performance Systems Languages & Build Infrastructure](#high-performance-systems-languages--build-infrastructure)
- [Contributing](#contributing)

---

## SaaS/Hosted Platforms

Commercial, cloud-hosted compiler platforms, online assembly/IR playgrounds, and managed heterogeneous compute toolkits.

* **[Modular Mojo Cloud & MAX Platform](https://modular.com)** - Commercial AI systems infrastructure and cloud-accelerated Mojo execution engine built on MLIR for heterogeneous hardware.
* **[Compiler Explorer (godbolt.org)](https://godbolt.org)** - Hosted interactive web platform allowing developers to compile code across dozens of compilers and inspect generated assembly and IR in real time.
* **[Rust Playground](https://rust-lang.org)** - Official hosted web environment for compiling, executing, benchmarking, and inspecting MIR/LLVM-IR/Assembly for Rust code.
* **[Intel Tiber Developer Cloud (oneAPI Cloud)](https://intel.com)** - Cloud-hosted development environment providing access to Intel compilers (ICX/IFX), SYCL, and Xeon/Gaudi hardware.
* **[NVIDIA CUDA Toolkit & NGC Cloud](https://nvidia.com)** - Proprietary GPU computing platform, NVCC compiler suite, and cloud container registry for high-performance CUDA workloads.
* **[Codasip Cloud / Codasip Studio](https://codasip.com)** - Commercial SaaS/cloud processor design and automated LLVM-based compiler generation environment for custom RISC-V cores.
* **[Celerity Runtime & Cloud Ecosystem](https://github.io)** - Distributed accelerator programming model and high-level C++ runtime scaling SYCL applications across multi-GPU clusters.
* **[LLVM / Clang / GCC Hosted Sandboxes (Wandbox & OnlineGDB)](https://wandbox.org)** - Cloud-hosted multi-compiler sandboxes providing instant browser-based execution for multiple versions of GCC and Clang.

---

## Open-Source Equivalents & Tools

Free and open-source software (FOSS) compiler infrastructures, intermediate representation (IR) frameworks, GPU/AI compilers, and self-hosted sandboxes.

### Core Compiler Toolchains & Backends

* **[LLVM Project](https://github.com)** - Modular and reusable open-source compiler and toolchain technologies forming the backbone of modern high-performance languages.
* **[Clang](https://llvm.org)** - Production-quality open-source C, C++, Objective-C, and CUDA compiler front-end for LLVM with fast compilation and expressive diagnostics.
* **[GCC (GNU Compiler Collection)](https://gnu.org)** - The foundational open-source optimizing compiler supporting C, C++, Fortran, Ada, Go, and Rust across dozens of architectures.
* **[Cranelift](https://github.com)** - Fast, secure, pure-Rust code generator and compiler backend designed for low-latency JIT and AOT compilation.
* **[QBE Compiler Backend](https://c9x.me)** - Lightweight, pure-C compiler backend aiming to provide 70% of LLVM's optimization performance in 10% of the code size.
* **[Mold](https://github.com)** - Ultra-fast, modern drop-in replacement linker for Unix systems engineered to maximize multi-core CPU throughput during systems builds.

### MLIR, Tensor & AI Accelerator Compilers

* **[MLIR (Multi-Level Intermediate Representation)](https://llvm.org)** - Open-source hybrid IR infrastructure within LLVM for building reusable, domain-specific compilers and hardware accelerators.
* **[OpenAI Triton](https://github.com)** - Open-source Python-like language and MLIR-based compiler for writing custom deep learning compute kernels at peak GPU efficiency.
* **[IREE (Intermediate Representation Execution Environment)](https://github.com)** - End-to-end MLIR-based compiler and runtime targeting CPUs, GPUs, and mobile/edge accelerators via Vulkan, Metal, and CUDA.
* **[Apache TVM](https://github.com)** - Open-source machine learning compiler framework for CPUs, GPUs, and specialized ML accelerators with automated kernel tuning.
* **[OpenXLA / StableHLO](https://github.com)** - Open-source domain-specific compiler for linear algebra that accelerates TensorFlow, PyTorch, and JAX models across diverse hardware.
* **[Meta Astryx](https://github.com)** - Open-source high-performance systems and compiler infrastructure project by Meta for next-generation compute workloads.
* **[Halide](https://github.com)** - Open-source domain-specific language and compiler designed to write fast, portable image processing and tensor pipelines separating algorithm from schedule.

### GPU, Heterogeneous & HPC Parallel Compilers

* **[AdaptiveCpp (formerly hipSYCL)](https://github.com)** - Independent, open-source implementation of SYCL and C++ standard parallelism targeting NVIDIA, AMD, and Intel GPUs via LLVM.
* **[AMD ROCm / HIP](https://github.com)** - Open-source software stack and compiler toolchain (amdclang++) enabling portable high-performance GPU computing.
* **[Celerity Runtime](https://github.com)** - Open-source C++ distributed accelerator runtime bringing SYCL's single-source programming model to multi-GPU HPC clusters.
* **[Chapel](https://github.com)** - Open-source parallel programming language and compiler designed from the ground up for productive, scalable supercomputing.
* **[Taichi Lang](https://github.com)** - Open-source imperative, parallel programming language embedded in Python that compiles numerical/simulation kernels to CUDA, Vulkan, and CPU.
* **[Enzyme](https://github.com)** - Open-source LLVM plugin performing high-performance automatic differentiation (AD) directly on statically analyzable LLVM IR.

### Self-Hosted Compiler Explorers & Code Sandboxes

* **[Compiler Explorer (Self-Hosted)](https://github.com)** - Full open-source codebase behind godbolt.org, deployable locally or on private infrastructure with custom toolchains.
* **[Rust Playground (Self-Hosted)](https://github.com)** - Open-source frontend and Docker-based sandbox backend powering the official Rust Playground.
* **[Judge0](https://github.com)** - Robust, scalable open-source online code execution system supporting 60+ compilers and languages via REST API.
* **[Piston](https://github.com)** - High-performance, general-purpose open-source code execution engine utilizing isolated containers for untrusted compilation.

### High-Performance Systems Languages & Build Infrastructure

* **[Rust (rustc)](https://github.com)** - Open-source systems programming language compiler guaranteeing memory safety and fearless concurrency without garbage collection.
* **[Zig](https://github.com)** - General-purpose open-source systems programming language and drop-in C/C++ cross-compiler toolchain featuring compile-time execution (comptime).
* **[Odin](https://github.com)** - Data-oriented, high-performance open-source systems programming language built on LLVM for modern hardware architectures.
* **[Bazel](https://github.com)** - Fast, scalable, multi-language open-source build and test system supporting distributed caching and remote execution for massive compiler codebases.
* **[Ninja](https://github.com)** - Small, ultra-fast open-source build system focused on speed, used as the primary backend generator for LLVM, Clang, and CMake.

---

## Contributing

Contributions are welcome! Feel free to open a Pull Request to add more open-source compilers, MLIR dialects, HPC runtimes, or systems programming infrastructure.

1. Fork the repository.
2. Add your project under the appropriate category with a concise description.
3. Submit a Pull Request.
