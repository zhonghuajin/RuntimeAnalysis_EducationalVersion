# RuntimeAnalysis_EducationalVersion

本项目用于展示本人研发的跨语言插桩工具套件分析源码的效果。

> 对插桩技术感兴趣可以加QQ群：732447253

## 一、使用方法：

1. 执行call_logs.sql文件；

2. 启动程序：java -jar logs-analysis-1.0.jar

3. 访问 http://localhost:8087

## 二、插桩工具套件架构图

![ ](https://raw.githubusercontent.com/zhonghuajin/RuntimeAnalysis_EducationalVersion/master/%E6%8F%92%E6%A1%A9%E5%A5%97%E4%BB%B6%E6%9E%B6%E6%9E%84.jpg)

本项目是上述架构中“日志分析系统”部分的简化版，只保留了前端展示部分。

## 三、语言支持

套件目前支持以下语言：

1. java

2. python

3. go

4. js/ts

5. c/c++/objective-c

6. c#

目前call_logs.sql只包含java(activiti)、c(redis)、c++(mysql)的例子，其它示例正在梳理中。