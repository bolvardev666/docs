# 故障处理

## 1.zookeeper组件挂掉(适用于大部分症状)
> <span style="color:red"> 端口扫描服务千万不要开,他会让后端zookeeper挂掉!</span>
当碰到大量客户端无法注册,查看审计日志统计信息缓慢(可能要等待十多分钟)等情况时,应该检查zookeeper是不是死掉了
