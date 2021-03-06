# 第一章 操作系统引论

## 操作系统的目的和作用

### 操作系统的目标

* 方便性
* 有效性
* 可扩充性
* 开发性

### 操作系统的作用

* OS作为用户与计算机硬件系统之间的接口
* OS作为计算机系统资源的管理者
* OS实现了对计算机资源的抽象

### 推动操作系统发展的主要动力

* 不断提高计算机资源利用率
* 方便用户
* 器件的不断更新迭代
* 计算机体系结构的不断发展
* 不断提出新的应用需求

## 操作系统的发展过程

### 未配置操作系统的计算机系统

1. 人工操作方式

   缺点： 1. 用户独占全机 2. CPU等待人工操作

2. 脱机输入/输出 `Off-Line I/O` 方式

   优点： 1. 减少了CPU的空闲时间 2. 提高了I/O速度

### 单道批处理系统 `Simple Batch Processing System`

1. 单道批处理系统的处理过程

   内存中始终只保持一道作业

2. 单道批处理系统的缺点

   系统中的资源得不到充分的利用

### 多道批处理系统 `Multiprogrammed Batch Processing System`

1. 多道程序设计的基本理念

   保持CPU处于忙碌状态

2. 多道批处理系统的优缺点

   优点： 1. 系统利用率高 2. 系统吞吐量大

   缺点： 1. 平均周转时间长 2. 无交互能力

3. 多道批处理系统需要解决的问题 1. 处理机争用问题 2. 内存分配和保护问题 3. I/O设备分配问题 4. 文件大组织和管理问题 5. 作业管理问题 6. 用户与系统的接口问题

> 操作系统定义： 操作系统是一组能有效地组织和管理计算机硬件和软件资源，合理地对 各类作业进行调度，以及方便用户使用的程序的集合。

### 分时系统 `Time Sharing System`

1. 分时系统的引入
   1. 人-机交互
   2. 共享主机
2. 分时系统实现重大关键问题
   1. 及时接收
   2. 及时处理
      1. 作业直接进入内存
      2. 采用轮转运行方式
   3. 分时系统的特征
      1. 多路性
      2. 独立性
      3. 交互性

### 实时系统 `Real Time System`

1. 实时系统的类型
   1. 工业（武器）控制系统
   2. 信息查询系统
   3. 多媒体系统
   4. 嵌入式系统
2. 实时任务的类型
   1. 周期性实时任务和非周期性实时任务
   2. 硬实时任务和软实时任务
3. 实时系统与分时系统特征的比较
   1. 多路性
   2. 独立性
   3. 及时性
   4. 交互性
   5. 可靠性

### 微机操作系统的发展

1. 单用户单任务操作系统
   * CP/M `Control Program/Monitor`
     * 8位
     * Digital Research 
   * MS/DOS
     * IBM-PC
2. 单用户多任务操作系统
   * Windows
3. 多用户多任务操作系统
   * Unix OS
     * Solaris OS
     * Linux OS

## 操作系统的基本特性

### 并发 `Consurrence`

1. 并行与并发

   并行：两个或多个事件在同一时刻发生

   并发：两个或多个事件在同一时间间隔内发生（宏观上）

2. 引入进程

   进程 `Process`：在系统中能独立运行并作为资源分配的基本单位，由一组机器指令、数据和堆栈等组成的，是一个能独立运行的活动实体。

### 共享 `Sharing`

1. 互斥共享方式

   打印机、磁带机、大多数物理设备，以及栈、变量和表格

   临界资源（独占资源）：一段时间内只允许一个进程访问的资源

2. 同时访问方式

   磁盘设备（宏观）

> 并发和共享是多用户（多任务）OS的两个最基本的特征。它们也是互为存在的条件。

### 虚拟 `Virtual`

在OS中，把通过某种技术将一个物理实体变为若干个逻辑上的对应物的功能称为“虚拟”。

与通讯系统一样，在OS中也是利用时分复用和空分复用技术来实现“虚拟”的。

1. 时分复用技术
   1. 虚拟处理机技术
   2. 虚拟设备技术
2. 空分复用技术

   提高存储空间的利用率

   虚拟存储技术（时分复用）

### 异步 `Asynchronism`

进程是以人们不可与之的速度向前推进的，此即进程的异步性。

## 操作系统的主要功能

### 处理机管理功能

1. 进程控制
2. 进程同步
3. 进程通讯
4. 调度
   1. 作业调度
   2. 进程调度

### 存储器管理功能

1. 内存分配
2. 内存保护
3. 地址映射
4. 内存扩充

### 设备管理功能

1. 缓冲管理
2. 设备分配
3. 设备处理

### 文件管理功能

1. 文件存储空间的管理
2. 目录管理
3. 文件的读/写管理和保护

### 操作系统与用户之间的接口

1. 用户接口 1. 联机用户接口 2. 脱机用户接口 3. 图形用户接口
2. 程序接口

### 现代操作系统的新功能

1. 系统安全
   1. 认证技术
   2. 密码技术
   3. 访问控制技术
   4. 反病毒技术
2. 网络的功能和服务
   1. 网络通信
   2. 资源管理
   3. 应用互操作
3. 支持多媒体
   1. 接纳控制功能
   2. 实时调度
   3. 多媒体文件的存储

## OS结构设计

1. 无结构操作系统
2. 模块化结构OS
3. 分层式结构OS

   优点： 1. 易保证系统的正确性 2. 易扩充和易维护性

### 客服/服务器模式 `Client/Server Model` 简介

1. 客户/服务器模式的由来、组成和类型
   1. 客户机
   2. 服务器
   3. 网络系统
2. 客户/服务器之间的交互
   1. 客户发送请求消息
   2. 服务器接收消息
   3. 服务器回送消息
   4. 客户机接收消息
3. 客户/服务器模式的优点
   1. 数据的分布处理和存储
   2. 便于集中管理
   3. 灵活性和可扩充性
   4. 易于改编应用软件

### 面向对象的程序设计 `Object-Orientated Programming` 技术简介

优点： 1. 通过“重用”提高产品质量和生产率 2. 使系统具有更好的易修改性和易扩展性 3. 更易于保证系统的“正确性”和“可靠性”

### 微内核 `MicroKernel` OS结构

1. 微内核操作系统的基本概念
   1. 足够小的内核
   2. 基于客户/服务器模式
   3. 应用“机制与策略分离”远离
   4. 采用面向对象技术
2. 微内核的基本功能
   1. 进程（线程）管理
   2. 低级存储器管理
   3. 中断和陷入处理
3. 微内核操作系统的优点
   1. 提高了系统的可扩展性
   2. 增强了系统的可靠性
   3. 可移植性强
   4. 提供了对分布式系统的支持
   5. 融入了面向对象技术
4. 微内核操作系统存在的问题

   运行效率有所降低

