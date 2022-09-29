# SQL学习笔记
Author: 丁宇宬
Date: 2022/09/30

**Tips 1**: SQL命令对大小写不敏感。  
**Tips 2**: 分号用于分隔不同的语句。某些数据库系统要求在每条 SQL 语句的末端使用分号。    
### **Select语句**   
从*table_name*表中选取*column_name_1*列，*column_name_2*列，... ：
```
SELECT <column_name_1>, <column_name_2>, ...
FROM <table_name>;
```
**Tips 3**: 同一语句中的不同要素间（如FROM前）可不换行，但换行可读性更佳。   
从*table_name*表中选取所有列：   
```
SELECT *
FROM <table_name>;
```
#### select where   
从*table_name*表中选取满足条件*condition*的*column_name_1*列，... ：   
```
SELECT <column_name_1>, ...
FROM <table_name>
WHERE <condition>;
```
例题1：[leetcode 595: 大的国家](https://leetcode.cn/problems/big-countries/)   
```
select name, population, area 
from world
where population >= 25000000 or area >= 3000000;
```
