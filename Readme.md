# 项目介绍

  从0到1开始部署[CVPR2020] BiFuse: Monocular 360 Depth Estimation via Bi-Projection Fusion：介绍，配置，测试（大一开源作业）

## 项目介绍

### 简介

​	该项目选自[CVPR2020] BiFuse: Monocular 360 Depth Estimation via Bi-Projection Fusion（基于双投影融合的单目360度深度估计） 可以根据2D图像进行深度估计，首先生成一张图片，以黑白程度表示距离远近，然后利用3D点云可视化，将2D图转换为一个3D模型，最终以一个GUI（Graphics User Interface）图形用户界面展示出来。

### 可行度

日常生活：目前在各个领域上，深度估计起到了重要作用例如在日常生活上，房地产商可以利用图片对房屋进行3D模型展示，让买家更直观的了解房屋大小，样式，从而既节省了销售的人力，又节约了买家的时间，让彼此实现双赢。

汽车领域：在目前汽车上也用到了深度估计，例如Benz在倒车时，倒车雷达除了显示实时画面同时还会出现3D模型，从空中俯瞰汽车情况，多角度的让驾驶员了解当前汽车情况，从而提高了驾驶的安全性。

医学领域：不仅如此，在医学领域同样也使用了深度估计技术。随着5G的出现，让远程手术成为可能，在医生进行手术中也会使用到深度估计技术，为医生判断位置，让安全性更高，让这项技术更加成熟。

### 前景

根据以上方面，前景是十分可观的。

汽车领域：各个汽车品牌为了自己的利益，开始推出各种配套技术，例如在车里加装自动停车，甚至是无人驾驶技术，那么深度估计在此方面可以起到很大作用，无论是对环境的判断还是路线的情况以及距离的把控都将更上一层楼，提高了无人驾驶的安全性，那么无人驾驶的落地速度会更快。

医学领域：想请好的主治医师手术，那么很多人很难预约到，通过该项目的应用那么机器人手术的风险降低，安全性也相应的提高了，从而实现全民能够获得优良的医学技术。

### 环境要求：

- Python（在3.7.4上测试）

- PyTorch（在1.4.0上测试）

- 其他依赖项

- pip install requirements.txt

  

### 作者环境如下：

- Windows11
- python3.7.4
- Pytorch1.12.1
- cuda11.3
- GeForce GTX 3050 Laptop GPU

# 配置项目：

## 克隆项目：

首先创建一个项目文件夹，然后git bash here (https://github.com/yuhsuanyeh/BiFuse)

## 安装必要的库：

### 首先创建虚拟环境：

在anaconda中使用命令`conda create -n de python==3.7.4`

创建一个名为de的虚拟环境 

然后此时我们使用命令`conda activate de`激活虚拟环境

使用命令 `Pip install -r requirements.txt`下载所需要的库

还需单独下载一个vispy的库 `conda install vispy`

和一个窗口控件PyQt5 `pip install PyQt5`和 `pip install PyQt5-tools`

# 下载训练模型

首先创建一个叫save的文件夹，然后在 https://drive.google.com/file/d/1EOEfyVuaJC1k5xAtqG37yXHxN-LnxA2n/view  中下载pkl后缀的文件，将该文接放在save文件夹中

# 运行模型

激活我们创建的虚拟环境，然后进入BiFuse文件夹。将你自己准备好的rpg图片放在My_Test_Data的文件夹 运行`python main.py --path ”./My_Test_Data“`

然后其结果会保存在My_Test_Result中

然后此时虚拟环境进入到tools文件夹 再运行`python vis3D.py ../My_Test_Result/Data000.npy`就能生成点云可视化的3d模型





