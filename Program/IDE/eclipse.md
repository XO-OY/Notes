# ECLIPSE

## 从资源库导出项目转为web项目

* tomcat deploy_path：webApp
  * project-Properties-
    * Project Facets-DynamicWebModule和Java 勾上，并选择合适版本
    * Java Compiler-Building-Build path problems 去掉Abort...选项
    * Deployment Assembly 配置路径映射/webApp /
    * Java Bulid Path 中 Default output folder 设为.../webApp/WEB-INF/classes

## Ant打war包变小，查看是否有代码未编译成功，或者未编译到发布路径

## 编译找不到监听器或者类文件

  1. 看build path Source-Default output folder是否正确
  2. 看web.xml监听器配置
  3. 看Project Facets Java版本是否正确

## 配置VM参数

  preferences>Java>Installed JREs 选择jdk-edit
