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
```
insert education.school (name)value("衡水中学");
insert education.school (id, name)value(1, "衡水中学");
insert education.school (id, name)value(5, "衡水中学");


delete from education.school where id=5;

select id from education.school where name="衡水中学";

update education.school set name="sadfsf" where id = 2;

update education.school set name="衡水中学" where id = (select id from education.school where name="sadfsf");		-- 安全模式的问题 

SELECT * FROM education.school;
```
5. Advanced   top、limit、in、between、like
```
SELECT * FROM education.school;
SELECT * FROM education.school limit 3;
SELECT * FROM education.school order by name limit 3;

SELECT * FROM education.school where id in (1,3);
SELECT * FROM education.school where id between 1 and 101;
SELECT * FROM education.school where id > 1 and id < 101;

SELECT * FROM education.school where name like "%学";
SELECT * FROM education.school where name like "%水%";
```
