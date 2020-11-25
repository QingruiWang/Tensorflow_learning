# Tensorflow 2.0 Learning
## 环境准备

**1. Anaconda环境搭建**

下载Anaconda
[下载地址](https://www.anaconda.com/products/individual)，按步骤正常安装即可

**2. 安装CUDA和cuDNN**

CUDA版本：10.0 [下载地址](https://developer.nvidia.com/cuda-10.0-download-archive)

cuDNN版本：7.6.5 [下载地址](https://developer.nvidia.com/rdp/cudnn-archive)

*配置cuDNN: 将下载的cuDNN解压后改名为cudnn并复制到CUDA安装路径（一般为C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0）*

*配置环境变量：检查环境变量中是否有：(路径可能会略有出入)*

*C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\bin*

*C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\libnvvp*

*C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\cudnn\bin*

**3. 配置anaconda虚拟环境**

conda create -n tensorflow_2.0 python=3.7 (创建python版本为3.7的名字为tensorflow_2.0的虚拟环境)

---
备注：

Conda 国内源设置：

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main

conda config --set show_channel_urls yes

---

**4. 安装tensorflow 2.0**

在anaconda中激活创建的虚拟环境： conda activate tensorflow_2.0

pip install tensorflow-gpu==2.0.0 (注意，如果不指定2.0.0，可能会导致tensorflow版本和cuda版本不兼容)

---

备注：

pip 国内源：

清华：https://pypi.tuna.tsinghua.edu.cn/simple

阿里云：http://mirrors.aliyun.com/pypi/simple/

中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/

华中理工大学：http://pypi.hustunique.com/

山东理工大学：http://pypi.sdutlinux.org/ 

豆瓣：http://pypi.douban.com/simple/

---

在python环境检查tensorflow是否安装成功

``` python
import tensorflow as tf
tf.test.is_gpu_available()
```

## 
