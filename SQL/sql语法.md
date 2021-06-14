### SQL语法学习

###### sql 执行顺序

 SQL Select语句完整的执行顺序： 
> 1. FROM 子句组装来自不同数据源的数据;
> 2. ON 对笛卡尔积的虚表进行筛选;
> 3. JOIN 用于添加数据到on之后的虚表中;
> 4. WHERE 对虚表中的数据进行筛选;
> 5. GROUP BY 对数据进行分组;
> 6. HAVING 对分组后的数据进行筛选（尽量减少 HAVING 的使用）;
> 7. SELECT 处理SELECT列表;
> 8. DISTINCT 将重复的行删除;
> 9. ORDER BY 按ORDER BY子句中的列列表顺序
