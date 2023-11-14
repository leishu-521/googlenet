# <center> DataWhale & 趋动云任务四</center>

<center>**通过免费的GPU算力，线上训练深度学习模型。**</center>



[TOC]



### 创建项目

#### 1. 填写项目名称

输入“花瓣分类”，也可以自定义名称

![image-20231114211305367](/home/zhurenzhang/.config/Typora/typora-user-images/image-20231114211305367.png)

#### 2. 选择镜像

官方镜像中，选择pytorch1.9.1和conda3.8的镜像即可。（结合镜像的创建时间，别选错了）

![image-20231114211533653](/home/zhurenzhang/.config/Typora/typora-user-images/image-20231114211533653.png)

#### 3. 添加数据

选择“公开”，同时搜索“flower”，找到这个218.21MB的数据集，选择并确定。

![image-20231114211702542](/home/zhurenzhang/.config/Typora/typora-user-images/image-20231114211702542.png)

#### 4. 创建

点击“确定”之后，弹出窗口，选择“代码暂不上传”。

![image-20231114212001374](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114212001374.png)

### 训练

1. 先“运行环境 ”，选择资源“B1.small”：GPU：6GB，内存：12GB够用了

![image-20231114215510655](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114215510655.png)

![image-20231114215549688](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114215549688.png)

2. 进入开发环境，拉取代码。（由于网络原因，如果拉取失败，多试几次即可）

```
git clone https://github.com/leishu-521/googlenet.git
```

![image-20231114215813078](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114215813078.png)

![image-20231114215938028](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114215938028.png)

3. 开始训练，等待一段时间，让它训练

```
#进入根目录

cd googlenet

#开始训练

python train.py
```

![img](file:////home/zhurenzhang/.config/QQ/nt_qq_7364ac65dc26c138252e07f740479548/nt_data/Pic/2023-11/Ori/08739f8b6fd2d4e4bfea74e07cf146bc.png)

### 预测

1. 在网上找一张花的图片，可以用截图工具截取一张240*240的花瓣图片，修改名称：img01.jpg , 拖动到代码目录中，如图：

![image-20231114221750771](/home/zhurenzhang/bypy/00每日问题/趋动云任务四.assets/image-20231114221750771.png)

2. 预测，得到结果

```
python predict.py
```

![img](file:////home/zhurenzhang/.config/QQ/nt_qq_7364ac65dc26c138252e07f740479548/nt_data/Pic/2023-11/Ori/105bfc2ed6b942d11b0ac3e3abbfba60.png)