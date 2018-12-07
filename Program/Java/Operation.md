### 指定字符集编译
    javac [-g(生成调试信息)] [-encoding utf-8(编码格式)] [-cp xxx.jar(指定依赖)[;xxx.jar]] *.java
### 编译文件夹下所有Java文件
    dir /s/B *.java > sources.txt
    javac @sources.txt
### 打jar包
    jar cvf name.jar [source.class | file/*]
### 编译报(非法字符：\65279)错误
    修改为gbk编码，修改乱码字段，再重新改回utf-8