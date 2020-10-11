# 某大学打卡自动签到

## Github Actions 部署指南

### 一、Fork 此仓库
![image-20200727142541791](https://i.loli.net/2020/07/27/jK5H8FLvt7aBeYX.png)



### 二、设置账号密码
前往 serverchan（http://sc.ftqq.com/ ） 按照要求绑定微信以便使用签到状态推送功能。

默认只推送 签到失败 的状态，如果想推送其他状态，请前往 checkin.py 自行修改。

添加名为 **USER**、**PWD**、**SCKEY** 的变量，值分别为 **学号**、**密码**、**从serverchan获得的SCKEY**

> Settings-->Secrets-->New secret

支持多账号，账号之间与密码之间用 ***#*** 分隔，账号、密码和SCKEY的个数要对应

示例：**USER:200806185946#201542356981**，**PWD:cxkjntm#jntmcxk**

若要使用多账号，请在SCKEY中同样以 **#** 隔开每个SCKEY，不论是否你只想使用一个微信账号接收推送。

![image-20201011202253175](https://i.loli.net/2020/10/11/g9ptbAYzEeQOKF5.png)

### 三、启用 Action
1. 点击 ***Actions***，再点击 **I understand my workflows, go ahead and enable them**

   ![](https://i.loli.net/2020/07/27/pyQmdMHrOIz4x2f.png)

2. 点击右上角的 ***Star***

   ![image-20201011202217087](https://i.loli.net/2020/07/27/3cXnHYIbOxfQDZh.png)

### 四、查看运行结果
> Actions --> 签到 --> build
>
> 能看到如下图所示，表示成功

![image-20201011202209081](https://i.loli.net/2020/10/11/pb5HyziBFCRt93c.png)


## 注意事项

1. 每天运行两次，在上午 8 点 和上午 10 点。

2. 可以通过 ***Star*** 手动启动一次。

   ![image-20201011202217807](https://i.loli.net/2020/07/27/87oQeLJOlZvU3Ep.png)
