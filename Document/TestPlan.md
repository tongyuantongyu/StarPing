# 测试计划

## 引言

## 任务概述

## 测试策略

### 测试人员需求、分工

单元测试理论由代码实现者一并实现，其他人在发现问题后亦可以补充测试用例。

其他测试由组长进行。

### 测试方法

本项目测试分为三种类型，单元测试、压力测试与稳定性测试。

单元测试使用自动测试方法，Planet端使用go test工具，Star后端使用unittest模块，Star前端采用Vue Test Utils进行测试，要求每一项实现的需求都有对应单元测试。 

压力测试采用手动方法，模仿高负载运行情形对各个模块进行测试，保证程序不崩溃。

稳定性测试采用手动方法，在实际环境中运行系统一周时间，要求保证整个系统工作正常。

## 测试资源

### 硬件资源

运行于amd64架构的linux计算机一台（要求长期开机，拥有公网IP）；运行于amd64架构的Windows计算机一台（要求有网络接入）。

### 软件需求

linux计算机：Python3.7+，PostgreSQL。

Windows计算机：Chrome浏览器，Firefox浏览器。

### 测试环境

linux计算机：长期开机，拥有公网IP，拥有root权限。

Windows计算机：管理员权限。

<hr>

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。