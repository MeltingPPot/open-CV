# 代码复现

## 推荐复现顺序

1. CIFAR-10 图像分类 baseline
2. ResNet 训练与迁移学习
3. YOLO / Faster R-CNN 小数据集检测
4. U-Net 图像分割
5. ViT 或 MAE 轻量实验
6. CLIP 图文检索小实验

## 每个复现项目建议包含

- `README.md`：任务说明、数据、运行方式、结果。
- `train.py`：训练入口。
- `eval.py`：评估入口。
- `infer.py`：推理入口。
- `configs/`：参数配置。
- `notebooks/`：探索性分析。
