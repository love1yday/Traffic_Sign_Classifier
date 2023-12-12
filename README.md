## 交通标志识别分类器

这是一个用 TensorFlow 构建的卷积神经网络，经过训练可以识别交通标志。使用的数据集是 [德国交通标志识别基准](http://benchmark.ini.rub.de/?section=gtsrb) 数据集.

### 训练和实验结果

最终模型在官方 GTSRB 测试数据集上的准确率达到 95.23% .

该模型包括我自己使用总体矩的运行平均估计器实现的批量归一化，以及一些测试和可视化，以了解批量归一化的作用。

所有代码、训练结果以及相关解释和注释都包含在该目录下的 iPython Notebook 中。

### 使用说明

1. 克隆或分叉此存储库。
2. 启动Jupyter笔记本：`jupyter笔记本traffic_sign_classifier.ipynb`
3. 执行您感兴趣的代码单元格。请注意，单元格可能依赖于之前的单元格和/或需要下面链接的数据集。 该笔记本清楚地解释了每个代码单元的作用。

### 数据集

用于该项目的官方 GTSRB 训练和测试数据集的调整大小和腌制版本可以在 [此处](https://blog.csdn.net/li_xiaolaji/article/details/108369873) 下载。

### 依赖关系

1. Python 3.x
2. TensorFlow 0.1x
3. Numpy
4. Matplotlib

