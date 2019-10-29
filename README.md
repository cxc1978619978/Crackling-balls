# 学习汇总
纯笔记，供学习和工作使用
----------------------------------------------------------------------------------------------------------------------------
## 目录

### 一、大汇总

### 二、ssm框架

----------------------------------------------------------------------------------------------------------------------------
#### 一、大汇总
1.Markdown格式
[.md(markdown)文件的基本编写语法](https://www.jianshu.com/p/7b1f94d7b5a6）

----------------------------------------------------------------------------------------------------------------------------
#### 二、ssm框架
+ 右键选择 “ Mark Directory as ” ，分别将 java 目录和 resource 目录设置为 “ 源码根目录 ” 和 “ 配置文件目录 ”

java 目录下新建代码目录：
controller ——控制层目录
dao        ——dao层目录
entity     ——实体层目录
service    ——业务层目录
utiles     ——工具类目录
resources 目录下新建 mappers 目录用来存放 MyBatis 的 mapper 文件

**框架结构如下：**
ssm-demo                                ——项目名称
     ├── src/main/java                  ——Java 源码根目录
            ├── controller              ——控制层目录
            ├── dao                     ——dao层目录
            ├── entity                  ——实体层目录
            ├── service                 ——业务层目录
                └── impl                ——业务实现类目录
            └── utiles                  ——工具类目录
     ├── src/main/resources             ——配置文件根目录
            └── mappers                 ——mapper文件目录
     ├── src/main/webapp                ——网站 Web 资源
     └── pom.xml                        ——pom文件
	 
+ applicationContext.xml
Spring 的核心默认配置文件的名字叫做 applicationContext.xml，如有需要也可以自行修改此名称，此文件是用于指导 Spring 工厂进行 Bean 生产、依赖关系注入（装配）及 Bean 实例分发的 “ 图纸 ” ，在常见的 Java Web 开发中，Spring 配置文件通常有一套万能的流程模板，如下所示：

—— 注解驱动的依赖性注入，自动扫描； —— 存储数据库信息； —— 加载数据源； —— 装配 sessionFactory； —— 整合 ORM 框架，如 MyBatis； —— 配置事务； —— 配置事务通知属性； —— 配置事务切面； —— 整合 MVC 框架，如 Spring MVC 。

+ mybatis-config.xml 
mybatis-config.xml 是 MyBatis 的核心配置文件，MyBatis 的相关配置都写在这个文件里

+ spring-mvc.xml

+ web.xml 
关于三大框架的配置文件已创建且配置完成，想使得这些配置生效的话还需要一步操作，就是在 web.xml 中加入框架的设置语句， web.xml 文件是 Java web 项目中的一个配置文件，主要用于配置欢迎页、Filter 、Listener 、Servlet 等

此配置文件主要定义了：

—— 工程基本信息：名字、描述（ display-name 和 description 标签)； —— 声明应用范围内的初始化参数（ context-param 标签)； —— 过滤器配置（ Filter 标签，如编码过滤器）； —— 监听器配置（ Listener 标签）； —— servlet配置（ servlet 标签，如 Spring MVC ）； —— 欢迎页面（ welcome-file-list 标签，index.jsp 页面）。

以上即是一些通用的文件配置，当然还有诸如错误页面配置（ error-page 标签）、安全限制配置（ security-constraint 标签）




----------------------------------------------------------------------------------------------------------------------------