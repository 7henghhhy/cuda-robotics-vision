# Progress Log

Repository: `cuda-robotics-vision`

Remote: https://github.com/7henghhhy/cuda-robotics-vision

## Current development environment

- Operating system: macOS 26.6.2
- Architecture: Apple Silicon `arm64`
- Python: 3.14.7
- Git: 2.54.0
- CUDA status: not applicable on this Mac; do not install NVIDIA drivers or CUDA Toolkit here.
- MPS may be used for PyTorch experiments if the installed PyTorch build supports it, but MPS results are not CUDA/RTX 4060 benchmark results.

## Day 1 — Repository setup

### Completed

- Created the local project skeleton.
- Defined the Project A minimum scope: correctness, CUDA kernel, optimization comparison, and benchmark.
- Defined the measurement rule: report kernel time separately from end-to-end transfer time.
- Added the initial build placeholder and resource links.

### Not yet verified

- NVIDIA GPU model and VRAM on the Y7000P.
- `nvidia-smi` output.
- `nvcc --version`.
- CMake CUDA configuration.
- Any CUDA kernel output or performance number.

These checks are intentionally deferred until the Y7000P is available.

### Next session: Day 2

Read the PyTorch Tensor tutorial and run five small tensor examples covering shape, dtype, reshape/view, indexing, and device.

On the current Mac, use CPU or MPS for the device comparison. Do not label the result as CUDA performance.

### Evidence policy

Do not add speedup percentages, GPU timings, or correctness claims until they are produced by a recorded command and saved raw output.
