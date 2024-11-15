# ViT vs. Baseline Algorithms for EEG-based Gaze Prediction

## 概述
本项目探讨了在EEGEyeNet数据集的基于EEG的注视预测任务中，使用基础视觉Transformer (ViT)模型的表现。我们使用两个基准算法进行比较：**平均基准方法**和**线性回归**。使用的具体任务是EEGEyeNet数据集中的`Position_task_with_dots_synchronised_min`。由于对超参数的调整还不熟练，三个模型的表现都不理想，我还会继续进行修改和优化。

## 数据集下载
要下载数据集，请使用以下命令：
```bash
wget -O "./dataset/Position_task_with_dots_synchronised_min.npz" "https://osf.io/download/ge87t/"
