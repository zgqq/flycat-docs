# Flycat
设计这个框架为了快速开发一个项目用于市场验证，如果后续流量上来了，能够快速修改成分布式应用

# Features
- 报警器 <br>
在 application.properties 加入邮箱配置
```
flycat.alarm.mail.sender.smtp=smtp.163.com
flycat.alarm.mail.sender.smtp.port=25
flycat.alarm.mail.sender.user=heijiw@163.com
flycat.alarm.mail.sender.password=13334
flycat.alarm.mail.receiver=heijiw@163.com
```

```
         AlarmUtils.sendNotify("Send notify");
```

- 事件管理器 <br>

*内置事件管理器，可以很方便监听认证失败，日志报错等事件，支持自定义事件*


- 友好的API接口 <br>
*清晰的错误码设计方便定位问题, 支持自定义各种错误返回结果.*

# Design
- 框架整合了Spring Boot常用starter，提供一站式技术栈
- 重复造轮子是没有意义的，框架本身依赖其他生产级别的类库，比如
guava, apache common等

# Best practices
- 排查线上问题 https://alibaba.github.io/arthas/


