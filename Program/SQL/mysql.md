### 查询mysql安装位置
    select @@basedir as basePath from dual
### 查询sql_mode
    SELECT @@GLOBAL.sql_mode;
    SELECT @@SESSION.sql_mode;