### 指定字符集编译
    javac -encoding utf-8 *.java
### 编译文件夹下所有Java文件
    dir /s/B * java > sources.txt
    javac @sources.txt
### 打jar包
    jar cvf name.jar [source.class | file/*]