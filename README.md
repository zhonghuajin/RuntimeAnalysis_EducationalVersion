# RuntimeAnalysis_EducationalVersion

---

RuntimeAnalysis是本人研发的一套高效的源码分析工具，可应用于源码阅读、系统重构、信创、二次开发、BUG定位等场景。

RuntimeAnalysis目前支持c\c++\js(ts\vue)\go\c#\java\go\python。

通过RuntimeAnalysis可以捕捉基于上述语言实现的系统、框架、第三方库在各种场景下做出的响应，也就是场景触发的核心源码，并对源码做出分析。

本项目（RuntimeAnalysis_EducationalVersion）源于RuntimeAnalysis的源码分析结果展示部分，提供了目前支持的语言的例子，用于展示RuntimeAnalysis分析源码的效果。

## 使用方法：

1. 执行call_logs.sql文件(<mark>不支持mysql 8，请使用mysql 5.7</mark>)
   
   ```sql
   mysql --max_allowed_packet=100M -u root -p database < call_logs.sql
   ```

2. 启动程序
   
   ```
   java -jar logs-analysis-1.0.jar访问 http://localhost:8087
   ```

3. 选择语言及场景查看各种场景触发的核心代码（**点击'函数名'列可查看函数源码**）
   
   

---

## 补充：

### 一、RuntimeAnalysis架构图

RuntimeAnalysis的核心技术路线是代码插桩。RuntimeAnalysis基于各种语言的生态中对插桩的支持，实现了各种语言的代码插桩以及源码分析相关的功能。以下是RuntimeAnalysis的架构图：

![ ](https://raw.githubusercontent.com/zhonghuajin/RuntimeAnalysis_EducationalVersion/master/%E6%8F%92%E6%A1%A9%E5%A5%97%E4%BB%B6%E6%9E%B6%E6%9E%84.jpg)

<mark>本项目截取了“日志分析系统”的前端部分用作效果展示。</mark>

### 二、github项目列表

以下是github私有空间RuntimeAnalysis相关项目的列表：

1. RuntimeAnalysis_JAVA_D
   
   java动态插桩；

2. RuntimeAnalysis_FRIDA
   
   andriod静态插桩；

3. RuntimeAnalysis_JAVA
   
   java静态插桩；

4. RuntimeAnalysis_LogsParser
   
   日志文件解析系统；

5. logs-analysis-backend
   
   后台日志分析系统；

6. logs-analysis-frontend
   
   日志分析前端展示系统；

7. RuntimeAnalysis_PYTHON
   
   python静态插桩；

8. RuntimeAnalysis_CSHARP
   
   c#静态插桩；

9. RuntimeAnalysis_C_CPP
   
   c、cpp、objective-c静态插桩  +  c、cpp动态插桩；

10. RuntimeAnalysis_GO
    
    go静态插桩

11. RuntimeAnalysis_JS
    
    js静态插桩。

**由于无法投入大量精力维护，所以RuntimeAnalysis不开源。**

### 三、示例列表

本项目中提供了目前支持的语言的例子：

1. **c语言**
   
   以redis 7.0.0 添加和读取一条字符串的场景为例子；

2. **c++**
   
   以mysql 8.0.26 innobase建表、innobase插入一条记录、innobase查询记录、innobase修改一条记录、innobase删除一条记录等场景为例子；

3. **js**
   
   以element-ui 2.13.0（vue）的Input-输入字符、Select-点击下拉菜单、Select-选中菜单、DatePicker-点击DatePicker、DatePicker-选择日期等场景为例子；

4. **ts**
   
   以nestjs 10.3.2 的内置sample中的mvc为例子，分析了mvc_sample-启动、mvc_sample-访问根url等场景；

5. **java**
   
   以activiti 6.0.0 的activiti-engine创建流程引擎、activiti-engine获取流程存储服务、activiti-engine获取运行时服务、activiti-engine获取流程任务、activiti-engine部署流程、activiti-engine启动流程、activiti-engine查询第一个任务、activiti-engine完成第一个任务、activiti-engine查询第二个任务、activiti-engine查询任务个数、activiti-engine关闭流程引擎等场景为例子；

6. **go语言**
   
   以k8s 1.28.2 的kubelet-启动、kubelet-空转等场景为例子；

7. **python**
   
   以jupyter_server 2.13.0 的notebook启动、创建新的notebook、执行单元格等场景为例子；

8. **c#**
   
   以ShareX截图工具的Sharex主项目-启动、ShareX主项目-截取矩形区域、ShareX主项目-截图活动窗口等场景为例子。
