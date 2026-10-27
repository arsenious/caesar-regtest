# caesar-regtest

Test checkpoint for the [UFcompressor](https://github.com/UFcompressor) CAESAR model registry (UFL_MODELS). **Workflow test, not for production use.**

| | |
|---|---|
| File | `rahul_isabel_tc_v1.pt` |
| SHA-256 | `833ba620e37e64a9bff669fb9bcf2dc7105f9e653f577321f8045d5ec0e7e820` |
| Base model | `caesar_v2` (CAESAR 503513a) |
| Fine-tuning | `pyCAESAR/train_vae3d.py`, 3,000 steps on Hurricane Isabel `TCf48` frames 0–79, batch 4, lr 4e-4, beta 1e-5 → 3e-5 |
| Held-out score | frames 80–99, network-only NRMSE 0.00623 (caesar_v2: 0.00832) |

The checkpoint is a PyTorch `state_dict`, loadable with `torch.load(..., weights_only=True)`.
