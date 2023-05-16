---

title: 安装R语言环境和生物信息学包
date: 2022-04-23 
tags: bioinformatics
---



# 下载

进入R语言官网：[R: The R Project for Statistical Computing (r-project.org)](https://www.r-project.org/)

点击download R

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423094715316.png" alt="image-20220423094715316" style="zoom:50%;" />

<!--more-->

向下滚动找到中文版，选择清华镜像进行下载

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423094906772.png" alt="image-20220423094906772" style="zoom: 33%;" />

进行一系列适合自己电脑系统的选择

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/%E4%B8%8B%E8%BD%BDR%E8%AF%AD%E8%A8%80.png" alt="下载R语言" style="zoom: 50%;" />

# 安装R

将下载得到的文件移动到相应文件夹下，我的路径为：D:\Application\R

> 安装路径最好为全英文，且中间不要用空格存在，这可能会影响到后续编程
>
> 最好不要安装在C盘下

双击文件进行安装

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423101352724.png" alt="image-20220423101352724" style="zoom: 67%;" />

需要注意安装文件路径的问题

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/Snipaste_2022-04-23_10-11-08.png" alt="Snipaste_2022-04-23_10-11-08" style="zoom: 67%;" />

安装成功后桌面会出现R语言快捷方式图标<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423104231373.png" alt="image-20220423104231373" style="zoom:50%;" />

# 安装生物信息学包

> 不需要本部分功能直接跳过



## 一般包的安装方法

安装pheatmap包：输入语句：`install.packages("pheatmap")`

选择兰州大学镜像，速度较快

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/%E9%95%9C%E5%83%8F.png" alt="镜像" style="zoom:50%;" />

安装成功界面

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/%E5%AE%89%E8%A3%85%E6%88%90%E5%8A%9F.png" alt="安装成功" style="zoom: 50%;" />

## 安装bioconductor包

有一些使用普通方法找不到的包，它可能包含在bioconductor中，可以利用bioconductor来安装，例如:limma

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423105154194.png" alt="image-20220423105154194" style="zoom: 67%;" />

搜索安装方式

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423105441126.png" alt="image-20220423105441126" style="zoom: 50%;" />

下滑网页，会给出对应的安装方式，复制代码到R中安装即可

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423105620116.png" alt="image-20220423105620116" style="zoom: 50%;" />

在安装过程中会询问是否更新一些包，有些包更新时间会很长，选择n不更新一样可以使用；也可以按照自己需求进行选择性更新

<img src="https://cdn.jsdelivr.net/gh/tang-colorful/Images/Images/image-20220423110156044.png" alt="image-20220423110156044" style="zoom:50%;" />

其他包在使用过程中采用上述方式安装即可