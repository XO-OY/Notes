# TOMCAT

## 指定字符集

    <Connector   URIEncoding="UTF-8"/> --tomcat/conf/server.xml

## EL表达式

    ${}在TOMCAT可以直接解析后台方法，在WebSphere不行

## illegal cyclic inheritance dependencies

    出现类循环继承导致内存溢出启动失败，jar包冲突导致，在项目目录下移除冲突包，重新编译运行

## 启动前看project facets中java版本是否正确
