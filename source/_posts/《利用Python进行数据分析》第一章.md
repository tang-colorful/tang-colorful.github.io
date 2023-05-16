---
title: 《利用Python进行数据分析》第一章
date: 2022-03-20 16:31:20
tags: 读书笔记
---

# 第一章 准备工作

## 1.1 本书内容

**常见数据形式**

- 表格型的数据，每一列可能会包含不同的类型（字符串、数值、日期或其他）。
- 多维数组（矩阵）。
- 由键位列关联的多张表数据（对于SQL用户来说就是主键或外键）。
- 均匀或非均匀的时间序列。

## 1.2 为何利用Python进行数据分析

- Python作为胶水，整合C、C++等语言的代码
- 解决“双语言”难题：使用相同程序工具集来兼顾研究人员和软件工程师的好处越发明显。
- 当搭建高并发、多线程应用，尤其是多CPU绑定线程时，使用Python则会成为一项挑战。原因在于Python拥有全局解释器锁（GIL），这是一种防止解释器同时执行多个Python指令的机制。当搭建高并发、多线程应用，尤其是多CPU绑定线程时，使用Python则会成为一项挑战。原因在于Python拥有全局解释器锁（GIL），这是一种防止解释器同时执行多个Python指令的机制。

## 1.3 重要的Python库

<!--more-->

**Numpy**

- NumPy（http://numpy.org）是Numerical Python的简写，是Python数值计算的基石。
- NumPy赋予Python的快速数组处理能力。
- 对于数值数据，NumPy数组能够比Python内建数据结构更为高效地存储和操作数据。
- 用底层语言编写的库可以在NumPy数组存储的数据上直接操作，而无须将数据复制到其他内存中后再操作。

**Pandas**

- pandas（http://pandas.pyda ta.org）提供了高级数据结构和函数
- 在本书中主要使用的pandas对象是DataFrame，它是用于实现表格化、面向列、使用行列标签的数据结构；以及Series，一种一维标签数组对象。
- pandas尤其擅长深度时间序列和处理商业进程中产生的时间索引数据

**matplotlib**

- matplotlib（http://matplotlib.org）是最流行的用于制图及其他二维数据可视化的Python库

**IPython与Jupyter**

- IPython使用**执行-探索**工作流来替代其他语言典型的**编辑-编译-运行**工作流
- 本书所有章节代码：http://github.com/wesm/pydata-book

**SciPy**

- SciPy（http://scipy.org）是科学计算领域针对不同标准问题域的包集合，SciPy与NumPy一起为很多传统科学计算应用提供了一个合理、完整、成熟的计算基础。

- 
```
  scipy.integrate  #数值积分例程和微分方程求解器
  scipy.linalg  #线性代数例程和基于numpy.linalg的矩阵分解
  scipy.optimize  #函数优化器（最小化器）和求根算法
  scipy.signal  #信号处理工具
  scipy.sparse  #稀疏矩阵与稀疏线性系统求解器
  scipy.special  #SPECFUN的包装器。SPECFUN是Fortran语言下实现通用数据函数的包，例如gamma函数。
  scipy.stats  #标准的连续和离散概率分布（密度函数、采样器、连续分布函数）、各类统计测试、各类描述性统计。

```



**scikit-learn**

- http://scikit-learn.org：机器学习工具包
- 分类：SVM、最近邻、随机森林、逻辑回归等
- 回归：Lasso、岭回归等
- 聚类：k-means、谱聚类等·
- 降维：PCA、特征选择、矩阵分解等
- 模型选择：网格搜索、交叉验证、指标矩阵
- 预处理：特征提取、正态化

**statsmodels**

- statsmodels（http://statsmodels.org）是一个统计分析包，为R语言公式系统所驱动的statsmodels包提供公式、模型规范框架。
- 与scikit-learn相比，statsmodels包含经典的（高频词汇）统计学、经济学算法。
  - 方差分析（ANOVA）
  - 时间序列分析：AR、ARMA、ARIMA、VAR等模型
  - 非参数方法：核密度估计、核回归
  - 统计模型结果可视化
- statsmodels更专注于统计推理，提供不确定性评价和p值参数。相反，scikit-learn更专注于预测。

## 1.4 安装与配置

**Windows**

- 下载安装Anaconda：http://anaconda.com/downloads
- 查看设置是否正确，在命令行中输入python启动python解释器，应该可以看到符合你下载的Anaconda版本的信息。
- 退出命令行：Ctrl-D（Linux或macOS）/ Ctrl-Z（Windows），或者输入exit()

**Apple（OS X和macOS）**

- 略

**GNU/Linux**

- 略

**安装及更新Python包**

- 通常通过以下命令进行安装：

  ```
  conda install package_name
  ```

- 使用pip包管理工具进行安装:

  ```
  pip install package_name
  ```

- 使用conda update命令来更新包:

  ```
  conda update package_name
  ```

- pip还支持通过--upgrade标识升级：

  ```
  pip install --upgrade package_name
  ```


> 同时使用conda和pip进行包安装时，请不要尝试使用pip更新conda安装的包，否则可能会导致环境问题。
>
> 当使用Anaconda或者Miniconda时，最好还是使用conda进行更新。

## 1.5 社区和会议

## 1.6 快速浏览本书

**示例数据**

- 每章的示例数据托管在GitHub仓库：http://github.com/wesm/pydata-book
- 关于如何获得本书资料的最新指引：http://wesmckinney.com

**导入约定**

- 一次性从像NumPy这样的大包中引入所有内容（from numpyimport *）在Python软件开发中被认为是拙劣实践。

- ```
  import numpy as np
  import matplotlib.pyplot as plt
  import pandas as pd
  import seaborn as sns
  import statsmodels as sm
  ```

**术语**

- 处理/处置/规整（munge/munging/wrangling）
  - 将非结构化或者同时又很凌乱的数据整理成结构化、清晰形式的整个过程。
- 伪代码
  - 将非结构化或者同时又很凌乱的数据整理成结构化、清晰形式的整个过程。
- 语法糖
  - 并不增加新特性，但便利于代码编写的编程语法。
