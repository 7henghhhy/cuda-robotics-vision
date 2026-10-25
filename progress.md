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

## Day 2–4 — PyTorch Tensor fundamentals

### Completed

- Completed the PyTorch Tensor tutorial study in Colab, covering tensor creation, dtype, shape, indexing/slicing, joining, arithmetic, single-element extraction, in-place operations, and the NumPy bridge.
- Explained the difference between CPU storage and accelerator storage. `torch.rand(...)` creates a CPU tensor by default; the tensor must be explicitly moved with `.to(...)` and its device printed again to verify the move.
- Explained Python object references versus C values/pointers, including rebinding versus mutating an existing object.
- Explained PyTorch `copy_(y)` versus `clone()`: `copy_` writes into an existing destination tensor, while `clone()` allocates an independent data copy.

### Evidence and limits

- Source notebook: PyTorch `tensorqs_tutorial.ipynb` opened in Google Colab.
- Observed tutorial output: shape `torch.Size([3, 4])`, dtype `torch.float32`, and device `cpu` before the later accelerator-transfer step.
- The Colab runtime displayed a T4 accelerator, but no CUDA timing or benchmark result was collected. This learning record does not claim RTX 4060 performance.

## Day 5 — PyTorch autograd

### Completed

- Completed Day 5 through the PyTorch autograd material: `requires_grad`, `grad_fn`, and disabling gradient tracking.

### Evidence and limits

- Completion was confirmed by the user on 2026-10-25.
- The exact Day 5 code and raw output were not saved in this repository, so no numerical result is claimed.

### Next session: Day 6

Continue GPU Puzzles 1–2 and keep the short indexing notes under `docs/`.

### Evidence policy

Do not add speedup percentages, GPU timings, or correctness claims until they are produced by a recorded command and saved raw output.
