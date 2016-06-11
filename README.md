# LightFramework
轻量级javaweb框架
#入门
#1. 创建一个 Maven Web 工程
整个工程的目录结构如下：
light-sample/
　　┗ src/
　　　　┗ main/
　　　　　　┗ java/
　　　　　　┗ resources/
　　　　　　┗ webapp/
　　┗ pom.xml
在 java 目录下，创建以下包名目录结构：
org/
　　┗ light4j/
　　　　┗ sample/
　　　　　　┗ action/
　　　　　　┗ entity/
　　　　　　┗ service/
可见，基础包名为：org.light4j.sample，下面的配置中会用到它。
#2. 配置 Maven 依赖
由于light-framework还没有发布到中央仓库，也没有发布到别的第三方仓库(后期会做这个工作)，所以需要把light-framework下载到本地，打包到本地仓库，编辑pom.xml 文件，添加 light-framework 依赖：
<dependency>
    <groupId>org.light4j</groupId>
    <artifactId>light-framework</artifactId>
    <version>1.0.0</version>
</dependency>
#3. 编写 Light 配置
在 resources 目录下，创建一个名为 light.properties 的文件，内容如下：
light.framework.app.base_package=org.light4j.sample
light.framework.app.home_page=/users

light.framework.jdbc.driver=com.mysql.jdbc.Driver
light.framework.jdbc.url=jdbc:mysql://localhost:3306/light-sample
light.framework.jdbc.username=root
light.framework.jdbc.password=123456
提示：需根据实际情况修改以上配置。
