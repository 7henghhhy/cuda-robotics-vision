# CUDA Robotics Vision

CUDA kernels and GPU benchmarks for robotic vision preprocessing.

## Project goal

Implement and measure a small robotics-vision preprocessing pipeline on an NVIDIA RTX 4060 Laptop GPU:

- CPU reference implementation
- naive CUDA kernel
- at least one measured optimization
- numerical correctness tests
- kernel-time and end-to-end H2D/kernel/D2H benchmarks

The first candidate operation is RGB-to-grayscale or image normalization. The operation will be fixed after the W1–W2 input/output contract is written.

## 12-week milestone

| Milestone | Status |
|---|---|
| Repository and experiment log | In progress |
| PyTorch fundamentals through D5 | Complete |
| GPU indexing preparation | In progress |
| `vector_add` CUDA warm-up | Not started |
| Image preprocessing kernel | Not started |
| Correctness tests | Not started |
| Benchmark CSV and plots | Not started |
| README results and technical report | Not started |

## Repository layout

```text
src/          CUDA and C++ source code
tests/        correctness tests
benchmarks/   benchmark runners and generated experiment notes
docs/         design notes and technical report
progress.md   dated learning and experiment log
```

## Hardware and measurement policy

Primary benchmark machine: Lenovo Legion Y7000P with RTX 4060 Laptop GPU.

Current development machine: Apple Silicon Mac. It is suitable for Python/PyTorch preparation, documentation, CPU reference implementations, and light analysis. It does not run NVIDIA CUDA. CUDA compilation and RTX 4060 measurements must be performed later on the Y7000P.

Every performance claim must record the GPU/software environment, input size, warm-up policy, repetition count, timer scope, and raw measurements. Kernel time and end-to-end time must not be reported as the same metric.

## Build placeholder

Run this on the CUDA machine after the first CUDA source file is added:

```bash
cmake -S . -B build
cmake --build build
```

## Related resources

- [CUDA Programming Guide](https://docs.nvidia.com/cuda/cuda-programming-guide/index.html)
- [CUDA C++ Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/index.html)
- [NVIDIA CUDA Samples](https://github.com/NVIDIA/cuda-samples)
- [GPU Puzzles](https://github.com/srush/GPU-Puzzles)

## Current status

See [progress.md](progress.md). No benchmark result has been recorded yet.
