

# Eclipse

## 基本设置

**设置文本文件编码**  Preferences -> General -> Workspace -> Text file encoding  (UTF-8)  
**设置JSP文件编码**  Preferences -> Web -> JSP Files -> Encoding  (ISO 10646/Unicode(UTF-8))  
**设置properties文件编码**  Preferences -> General -> Content Types -> Text -> Java Properties File缺省编码改为UTF-8  
**设置JDK本地源码的JavaDOC API路径**  Preferences -> Java -> Installed JREs -> Edit -> 全选所有jar包 -> Source Attachment Configuration -> External location -> External File(C:/Program Files/Java/jdk1.8.0_131/src.zip)  
**设置JavaScript文件代码自动提示**  Preferences -> JavaScript -> Editor -> Content Assist -> Auto-Activation  
**设置HTML文件代码自动提示**  Preferences -> Web -> HTML Files -> Editor -> Content Assist -> Auto-Activation  
**设置**

## 其他

### rt.jar调试支持查看类变量

- 创建rt_debug目录(D:\rt_debug)，将 `%JAVA_HOME%\jre\lib\rt.jar` `%JAVA_HOME%\src.zip` 复制到该目录解压
- 解压后的src目录保留java、javax、org三个目录，其余删除
- src目录中打开cmd命令行窗口，执行 `dir /B /S /X jdk_src\*.java > filelist.txt`
- 创建D:\rt_debug\classes目录
- cmd中执行 `javac -J-Xms16m -J-Xmx1024m -sourcepath D:\rt_debug\src -cp D:\rt_debug\rt.jar  -d D:\rt_debug\classes -g @filelist.txt`
- 进入D:\rt_debug\classes目录执行 `jar cf0 rt_debug.jar *`
- 将生成的rt_debug.jar复制到 `%JAVA_HOME%\jre\lib`
- eclipse中Preferences -> Java -> Installed JREs -> Add External JARs添加该jar并Up至rt.jar之上

### 反编译插件

- http://jd.benow.ca/ 下载jdeclipse安装包
- eclipse dropins文件夹下新建jdeclipse文件夹，将安装包中features、plugins文件夹复制到新建的文件夹中，重启eclipse
- Preferences -> General -> Editors -> File Associations中*.class类型的文件，选择JD Class File Viewer作为默认编辑器

### Maven插件

- 安装Maven
- 添加外部Maven安装目录 Preferences -> Maven -> Installations -> Add
- 使用外部Maven的全局设置 Preferences -> Maven -> User Settings -> Global Settings

### Tomcat插件

- 安装Tomcat
- 添加外部Tomcat安装目录 Preferences -> Tomcat -> Tomcat home
- 添加服务器运行环境 Preferences -> Server -> Runtime Environments -> Add

### HttpServlet not found问题

jsp文件中报该错误 The superclass "javax.servlet.http.HttpServlet" was not found on the Java Build Path
- 项目上单击鼠标右键，添加tomcat库 Build Path -> Configure Build Path -> Libraries -> Add Library -> Server Runtime
- Build Path -> Configure Build Path -> Order and Export 勾选tomcat库
