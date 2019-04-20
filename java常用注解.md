## lombook的注解
##### @EqualsAndHashCode(callSuper=true)
> 使生成的方法中调用父类方法
##### @NoArgsConstructor
> 生成一个无参数的构造方法
##### @AllArgsContructor
> 生成一个包含所有变量的构造放噶
## mybatis-plus的注解
#### @TableId(type = IdType.参数)
> 指定一张表的id
> IdType是指定这张表的生成策略

|Java|描述|
|:----|:----:|
|IdType.AUTO|数据库自增|
|IdType.INPUT|自行输入|
|IdType.ID_WORKER|分布式全局唯一ID 长整型类型|
|IdType.UUID|32 位UUID字符串|
|IdType.NONE|无状态|
|IdType.ID_WORKER_STR|分布式全局唯一ID 字符串类型|

#### @TableField
>例如：@TableField(.. , update="%s+1") 其中 %s 会填充为字段
>输出 SQL 为：update 表 set 字段=字段+1 where ...
>例如：@TableField(.. , update="now()") 使用数据库时间
>输出 SQL 为：update 表 set 字段=now() where ...





