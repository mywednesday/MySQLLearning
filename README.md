# MySQLLearning

#### Day 1
1. 安装MySQL

#### Day 2
1. 复习SQL语句的增、删、改、查;
2. sql 中unique与distinct的区别， distinct用在select， 而unique是列的属性；
3. [MYSQL的安全模式：sql_safe_updates介绍](https://www.cnblogs.com/fengff/p/10774145.html)；用来限制update和delete操作，防止误操作； 关键字： where、索引字段、limit；
4. 自增长的Key
  * insert即可以指定也可以不指定Key值，但是不能指定已存在的Key；
  * insert时不指定key的值，新增记录的Key从表中最大的Key值开始自增长；
  * 不能删除数据库中有自动增长的主键的表，其原因是这个表与其它表之间建立有“关系”。必须将“关系”删除后才能删除表；
