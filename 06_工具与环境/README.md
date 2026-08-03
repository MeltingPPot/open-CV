# 工具与环境

## 推荐工具

- Python 3.10+
- PyTorch
- torchvision
- OpenCV
- Matplotlib / Seaborn
- JupyterLab
- scikit-learn
- tqdm
- wandb 或 TensorBoard

## 环境建议

先建立一个独立环境，避免不同项目依赖互相污染。

```bash
conda create -n cv-learning python=3.10
conda activate cv-learning
pip install torch torchvision opencv-python matplotlib scikit-learn jupyter tqdm
```

如果有 NVIDIA GPU，再根据本机 CUDA 版本安装对应 PyTorch。
