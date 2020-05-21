# hibernate

## hbm.xml配置

    数据库字段名不宜太长，会导致映射失败。

    字段配置与映射配置不会冲突。

## 多对一映射

    <many-to-one name="属性名" class="关联类" fetch="select" insert="false" update="false" property-ref="关联类类关联属性">
        <column name="本类关联数据库列名" />
    </many-to-one>

## 一对多映射

    <set name="属性名">
        <key column="关联类对应数据库列名" property-ref="本类关联属性名"/>
        <one-to-many class="关联类"/>
	</set>

## 直接执行sql语句的，数值赋值不要带引号，前台直接取值时会无法识别成数字