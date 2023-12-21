# 交通标志识别分类器

这是一个用 TensorFlow 构建的卷积神经网络，经过训练可以识别交通标志。使用的数据集是 [德国交通标志识别基准](http://benchmark.ini.rub.de/?section=gtsrb) 数据集.

## 训练和实验结果

最终模型在官方 GTSRB 测试数据集上的准确率达到 95.23% .

该模型包括我自己使用总体矩的运行平均估计器实现的批量归一化，以及一些测试和可视化，以了解批量归一化的作用。

所有代码、训练结果以及相关解释和注释都包含在该目录下的 iPython Notebook 中。

## 使用说明(TensorFlow)

### Docker使用
1、先拉取镜像

```sh
docker pull udacity/carnd-term1-starter-kit
```

2、创建容器

```sh
docker run -it --rm --entrypoint "/run.sh" -p 8888:8888 -v `pwd`:/src udacity/carnd-term1-starter-kit
```

3、使用浏览器访问 Jupyter 服务器
`http://10.120.16.130:8888/`

### 直接使用
1. 克隆此存储库。
2. 启动Jupyter笔记本：`jupyter notebook traffic_sign_classifier.ipynb`
3. 执行代码单元格。

## 使用说明(Pytorch)

### Docker使用

1、拉取镜像

```sh
docker pull lorenzopapa5/cuda11.3-python3.8-pytorch1.11
```

2、创建容器

```sh
docker run -itd --name zcg_pytorch --user root --runtime=nvidia lorenzopapa5/cuda11.3-python3.8-pytorch1.11 /bin/bash
```

3、进入容器

```sh
docker exec -it zcg_pytorch /bin/bash
```

4、将 Python3.8 注册为 Jupyter 内核：

```sh
python -m ipykernel install --user --name python3.8 --display-name "Python 3.8"
```

5、启动Jupyter笔记本

```sh
jupyter notebook --allow-root --port=8889
```

6、使用浏览器访问 Jupyter 服务器
`http://localhost:8889/`


## 数据集

用于该项目的官方 GTSRB 训练和测试数据集可以在 [此处](https://blog.csdn.net/li_xiaolaji/article/details/108369873) 下载，也可以直接下载 `traffic-signs-data.7z` 。

## 说明
`traffic.ipynb`文件是Pytorch版
`Traffic_Sign_Classifier.ipynb`文件是TensorFlow版
`images`文件夹里存放的是5张测试图片.

## 依赖关系
### TensorFlow版
1. Python 3.x
2. TensorFlow 1.x
3. Numpy
4. Matplotlib

### Pytorch版
1. Python3.8
2. Numpy
3. Matplotlib
4. Pytorch1.11
