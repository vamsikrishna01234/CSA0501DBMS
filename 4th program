mysql> use gb;
Database changed
mysql> select * from gb;
ERROR 1146 (42S02): Table 'gb.gb' doesn't exist
mysql> select * from student;
+----+--------+---------+--------+
| id | name   | city    | salary |
+----+--------+---------+--------+
| 11 | lokesh | chennai |   1234 |
| 12 | mani   | goa     |   6541 |
| 13 | sai    | ongole  |   9874 |
| 14 | venky  | araku   |    874 |
| 18 | loks   | chennai |    234 |
| 36 | swetha | chirala |  65743 |
| 45 | janu   | chirala |  65743 |
| 63 | venky  | chirala |  65743 |
| 64 | bsr    | 3652    |   NULL |
+----+--------+---------+--------+
9 rows in set (0.04 sec)

mysql> select name,salary,
    -> case
    -> when salary<5000 then'excellent'
    -> when salary=5000 then'good'
    -> else'average'
    -> end performance
    -> from student;
+--------+--------+-------------+
| name   | salary | performance |
+--------+--------+-------------+
| lokesh |   1234 | excellent   |
| mani   |   6541 | average     |
| sai    |   9874 | average     |
| venky  |    874 | excellent   |
| loks   |    234 | excellent   |
| swetha |  65743 | average     |
| janu   |  65743 | average     |
| venky  |  65743 | average     |
| bsr    |   NULL | average     |
+--------+--------+-------------+
9 rows in set (0.00 sec)


mysql> select name,salary,if(salary>7000,'good','bad') from student;
+--------+--------+------------------------------+
| name   | salary | if(salary>7000,'good','bad') |
+--------+--------+------------------------------+
| lokesh |   1234 | bad                          |
| mani   |   6541 | bad                          |
| sai    |   9874 | good                         |
| venky  |    874 | bad                          |
| loks   |    234 | bad                          |
| swetha |  65743 | good                         |
| janu   |  65743 | good                         |
| venky  |  65743 | good                         |
| bsr    |   NULL | bad                          |
+--------+--------+------------------------------+
9 rows in set (0.02 sec)

mysql> select name,salary,
    -> case
    -> when salary>6000 then'good'
    -> when salary=6000 then'better'
    -> else 'bad'
    -> end performance
    -> from student;
+--------+--------+-------------+
| name   | salary | performance |
+--------+--------+-------------+
| lokesh |   1234 | bad         |
| mani   |   6541 | good        |
| sai    |   9874 | good        |
| venky  |    874 | bad         |
| loks   |    234 | bad         |
| swetha |  65743 | good        |
| janu   |  65743 | good        |
| venky  |  65743 | good        |
| bsr    |   NULL | bad         |
+--------+--------+-------------+
9 rows in set (0.00 sec)

mysql> select id,city,salary,
    -> case
    -> when salary>60000 then'good'
    -> when salary=60000 then'better'
    -> else'excellent'
    -> end performance
    -> from student;
+----+---------+--------+-------------+
| id | city    | salary | performance |
+----+---------+--------+-------------+
| 11 | chennai |   1234 | excellent   |
| 12 | goa     |   6541 | excellent   |
| 13 | ongole  |   9874 | excellent   |
| 14 | araku   |    874 | excellent   |
| 18 | chennai |    234 | excellent   |
| 36 | chirala |  65743 | good        |
| 45 | chirala |  65743 | good        |
| 63 | chirala |  65743 | good        |
| 64 | 3652    |   NULL | excellent   |
+----+---------+--------+-------------+
9 rows in set (0.00 sec)

mysql> select id,name,salary,if(salary>70000,'good','better')from student;
+----+--------+--------+----------------------------------+
| id | name   | salary | if(salary>70000,'good','better') |
+----+--------+--------+----------------------------------+
| 11 | lokesh |   1234 | better                           |
| 12 | mani   |   6541 | better                           |
| 13 | sai    |   9874 | better                           |
| 14 | venky  |    874 | better                           |
| 18 | loks   |    234 | better                           |
| 36 | swetha |  65743 | better                           |
| 45 | janu   |  65743 | better                           |
| 63 | venky  |  65743 | better                           |
| 64 | bsr    |   NULL | better                           |
+----+--------+--------+----------------------------------+
9 rows in set (0.00 sec)

mysql> select id,name,salary,if(salary>700,'good','better')from student;
+----+--------+--------+--------------------------------+
| id | name   | salary | if(salary>700,'good','better') |
+----+--------+--------+--------------------------------+
| 11 | lokesh |   1234 | good                           |
| 12 | mani   |   6541 | good                           |
| 13 | sai    |   9874 | good                           |
| 14 | venky  |    874 | good                           |
| 18 | loks   |    234 | better                         |
| 36 | swetha |  65743 | good                           |
| 45 | janu   |  65743 | good                           |
| 63 | venky  |  65743 | good                           |
| 64 | bsr    |   NULL | better                         |
+----+--------+--------+--------------------------------+
9 rows in set (0.00 sec)
