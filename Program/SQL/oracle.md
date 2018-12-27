### 生成ID函数
    select sys_guid() from dual;

### 选择数据不足5位补零
    select lpad('123',5,'0') from dual;

### 查询跨库查询账号
    select * from dba_db_links;

### 替换文本
    select replace (id,'1','2') from dual;

### 截取前两位
    select substr(col_name,1,2) from dual;

### 查找某个字段属于哪个表
    select table_name from dba_tab_columns where column_name='字段名（大写）'

### 拼接字段
    select LISTAGG(id,',') WITHIN GROUP( ORDER BY column_name1),column_name1 
        from table_name
        group by column_name1;

    select wm_concat(id)
        from table_name
        group by column_name1;

### 系统时间查询
    SELECT SYSDATE FROM dual;

### 建索引
    Create Index i_deptno_job on emp(deptno,job);

### 查建表时间
    SELECT t.* FROM user_objects t where t.OBJECT_NAME=table_name

### oracle 条件函数
    decode(exp，conq1,  exp1, conq2, exp2 );

### 截取字段
    Substr(col_name,start_index,length);

### 触发器
    alter table table_name disable all triggers;
    alter trigger trigger1_table_name enable; 

### 树遍历-从根节点向下
    select * from table_name
        start with identity=475
        connect by prior identity = pid;

### 树遍历-从叶节点向上
    select level ,identity,pid,yylevel from table_name
    　　start with identity=542
    　　connect by prior pid = identity;

### 修改字段长度
    ALTER TABLE tableName modify(columnName 类型);

### 杀锁表进程
    select * from v$locked_object; (查看锁表session_id)
    SELECT * FROM V$SESSION t WHERE 1=1 AND t.SID = session_id;
    alter system kill SESSION 'sid,serial#';

### 查对应的数据库语句
    SELECT * FROM V$SQL t;

### hints 强制走索引
    select /*+ index(table_name index_name) */ * from dual;