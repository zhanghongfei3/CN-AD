# 创建只读实例
在对数据库有少量写请求，但有大量读请求的应用场景下，单个实例可能无法抵抗读取压力，甚至对主业务产生影响。为了实现读取能力的弹性扩展，分担数据库压力，您可以在某个地域中创建一个或多个只读实例，利用只读实例满足大量的数据库读取需求，以此增加应用的吞吐量。

云数据库 MySQL/Percona/MariaDB 只读实例为单节点的架构，采用原生复制功能将主实例的更改同步到所有只读实例。

## 限制条件
* 单个实例下只读实例个数不能超过 8 个
* 只读实例所在的网络的可用 IP 数需要大于 购买量
* 只读实例只支持 ***按配置*** 计费类型，不支持 ***包年包月***

## 操作步骤
1. 登录 [云数据库 RDS 控制台](https://rds-console.jdcloud.com/database)。
2. 选择需要进行添加只读实例的目标实例，点击目标实例的名称，进入到实例详情页。
3. 选择 ***只读实例管理*** 标签，打开只读实例管理页面，点击 ***新增只读实例*** 按钮，创建只读实例。
4. 创建只读实例的界面参数说明
    * 地域：地域不可修改，默认就是和主实例所处同一个地域。
    * 可用区：不同地域，可用区的数量不同，具体以控制台为准，关于地域的详细说明，请参考 [地域与可用区](https://www.jdcloud.com/help/detail/1844/isCatalog/1)。
    * 规格：新建的只读实例规格选择，建议只读实例规格不小于主实例。
    * 存储空间：新建的只读实例存储空间，请确保存储空间不小于主实例，否则有可能会导致数据不一致。
    * 网络：网络不可修改，默认就是和主实例所处同一个网络。
    * 购买量：购买相同配置的只读实例个数。
    
    ![image2018-3-2 13_58_33.png](https://img1.jcloudcs.com/cms/e13a1926-043c-49e1-a94c-c27f1491f3bc20180302140739.png)

5. 点击 ***立即购买*** 按钮，进入订单确认页。
6. 阅读完云数据库 RDS 服务条款，点击立即开通，开始创建只读实例。