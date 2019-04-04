# 命令

## 查看系统运行中的端口

    netstat -an

## 查特定端口（可查到对应的pid）

    netstat   -ano|findstr  8080  

## 终止线程

    taskkill  /pid  11600  /f
