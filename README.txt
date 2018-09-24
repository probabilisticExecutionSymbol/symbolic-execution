JPF符号执行框架

文件结构：
项目一目前有三个工程构和一个配置文件成：JPF-core, JPF-symbc, z3以及配置文件site.properties
JPF-core: 用于符号执行的总框架，是基于Java 二进制码的可扩展的软件分析框架，后面的工具都是以其作为基础的
JPF-symbc: 专门用于符号执行的工具
z3：解释器，用于测试，后面会换成greenSolver
site.properties 格式如下：
# 注意将user.home改成当前jpf文件夹保存目录
# JPF site configuration

jpf-core = ${user.home}/jpf/jpf-core

# numeric extension
jpf-numeric = ${user.home}/jpf/jpf-numeric

# annotation-based program properties extension
jpf-aprop = ${user.home}/jpf/jpf-aprop

extensions=${jpf-core},${jpf-aprop}

#... and all your other installed projects

操作步骤如下：
在eclipse中运行
1.运行jpf-core 的example
使用eclipse 安装插件 网址：http://babelfish.arc.nasa.gov/trac/jpf/raw-attachment/wiki/projects/eclipse-jpf/update
在src/examples 中选择后缀为jpf的文件右键选择 Verify... 就可以运行了
2.运行jpf-syboc的example
开始时会报错找不到libz3java.dll,在java的classpath中加入目录jpf/z3/build
在src/examples 中选择后缀为jpf的文件右键选择 Verify... 就可以运行了

在命令行中执行
> <jpf-core-dir>/bin/jpf +classpath=. <application-main-class>
或者
> <jpf-core-dir>/bin/jpf <application-property-file>.jpf
或者
> java -jar <jpf-core-dir>/build/RunJPF.jar +classpath=. <application-main-class>



