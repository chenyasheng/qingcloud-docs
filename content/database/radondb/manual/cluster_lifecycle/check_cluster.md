---
title: "查看集群信息"
description: 本小节主要介绍如何查看 RadonDB 集群信息。 
keywords: RadonDB 集群信息
weight: 10
collapsible: false
draft: false
---


RadonDB 集群创建成功后，可在 AppCenter 查看集群信息，包括集群基本属性、服务端口信息、租赁信息、节点信息、配置参数、告警配置、备份列表、存储节点信息、监控节点信息、数据库账号等。

本小节主要介绍如何查看集群信息。

## 前提条件

- 已获取 QingCloud 管理控制台登录账号和密码，且已获取集群查看权限。

## 操作步骤

1. 登录 QingCloud 管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **分布式数据库 RadonDB**，进入集群管理页面。

   可查看当前区域集群列表，以及集群基本信息。

    <img src="../../../_images/cluster.png" alt="集群列表" style="zoom:100%;" />

3. 选择目标集群，点击目标集群 ID，进入集群详情页面。

    可查看集群各详细信息，以及执行集群的各项功能管理操作。

4. 当在对集群执行操作后，可在集群详情页面左下侧，查看集群操作日志。

   <img src="../../../_images/operate_log.png" alt="操作日志" style="zoom:50%;" />

### 基本属性

在集群详情页面左侧**基本属性**区域，可查看集群基本状态、版本信息、节点数量、网络信息等。

点击下拉栏图标，展开集群操作列表，可查看集群服务功能。

<img src="../../../_images/basic_info.png" alt="基本属性" style="zoom:50%;" />

### 服务端口信息

在集群详情页面左侧**服务端口信息**区域，可查看集群服务端口、高可用读写 IP。

- 高可用读 IP：内网访问高可用读 IP。可将请求在 SQL 节点及其副本之间进行负载分担，提高读取性能，消除单点故障。

- 高可用写 IP：内网访问高可用写 IP。始终指向 SQL 节点。

> **注意**
> 
> -务必使用高可用的读写 IP 来访问集群。由于连接到读 IP 的请求会在所有 SQL 节点及其副本（包括当前的 SQL 主节点）之间负载。故当某个连接请求被分配到当前主节点时，也是可写的。
> 
> -反之，若分配到非主节点，则必然是只读的。

<img src="../../../_images/check_access_info.png" alt="连接信息" style="zoom:50%;" />

### 节点列表

在**节点**页面，可查看集群各节点的 ID、服务状态、监控信息、资源配置等。

![节点](../../../_images/check_node.png)

### 配置参数

在**配置参数**页面，可查看集群性能优化配置参数项。

> **说明**
> 
> 修改后将导致自动重启集群的参数，请在业务低峰时进行修改。

![配置参数](../../../_images/config_list.png)

### 监控告警

在**告警**页面，可以查看集群告警配置信息，及时掌握集群的资源和服务状况。

![监控告警](../../../_images/alarm_list.png)

### 备份

在**备份**页面，可以查看集群备份列表信息，可查看集群列表和**备份链**结构示意图，以及可从备份创建新集群。

![备份信息](../../../_images/backup.png)

### 存储节点信息

在**存储节点信息**页面，可以查看集群存储节点角色、节点读写 VIP 等信息。

![存储节点](../../../_images/storage_nodeinfo.png)

### 监控节点信息

在**监控节点信息**页面，可以查看集群监控节点账号访问地址、账号权限等。

<img src="../../../_images/monitoring_addr.png" alt="监控访问地址" style="zoom:50%;" />

### 账号列表

在**账号**页面，可以查看集群账号。

![账号](../../../_images/check_user.png)

### 租赁信息

在集群详情页面左侧**租赁信息**区域，可以查看集群当前计费信息。

<img src="../../../_images/payment_info.png" alt="租赁信息" style="zoom:50%;" />
