# 刷卡器配置

```
整个流程的前提是需要设置好刷卡器，比如完美的就可以使用安装ISO自带的工具设置
开启账号类型:IC卡号
update sys_accounttype set state=1 where atypeID=5;

```

## 1.服务端操作

```mermaid
flowchart TB
    服务端创建任意账号 --> 服务端开启漫游打印 --> 服务端添加刷卡器-添加时绑定打印机
```

## 2.输出端口操作

```mermaid
flowchart TB
    安装客户端 --> 登录任意账号提交终端信息 --> 
    登录sysadm开启刷卡刻录 -->
    退出账号
```

## 3.提交端口操作

```mermaid
flowchart TB
    安装客户端 --> 登录任意账号提交终端设备信息 --> 
    登录账号完成打印提交流程-打印机选择漫游 -->
    管理端状态为待输出
```

## 4.刷卡器绑定

```mermaid
flowchart TB
    输出端sysadm开启打印显号 -->
    退出账号 -->
    去刷卡 -->
    输出端客户端账号栏显示卡号 -->
    管理端添加用户IC卡账号 -->
    输出端sysadm改回刷卡打印
```

## 5.流程

```mermaid
flowchart TB
    提交端提交漫游任务 -->
    去刷卡 -->
    任务输出
```

    