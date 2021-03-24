# ali-天池
记录阿里天池学习的过程，共勉~
## python训练营
1. 完成python训练营task01打卡
   比较特别的地方：
   1. 元组推导式生成的是生成器对象
   2. 通过位操作实现整数的运算
   3. 负数的二进制是原码加负号
2. python训练营task02打卡
   1. 各种内置方法比较多，需要更多的练习来记忆
3. python训练营task03打卡
   1. 魔法方法比较多，需要多用一用才能掌握
   2. 斐波那契数列被玩坏了2333
4. python训练营task04打卡
   1. 要学的东西还很多，加油~
   2. 对pandas和绘图的使用熟练了许多
## sql训练营
1. 完成sql训练营task01打卡，完成课后练习
   1. CREATE TABLE Addressbook
   (regist_no INTEGER NOT NULL,
   name VARCHAR(128) NOT NULL,
   adress VARCHAR(256) NOT NULL,
   tel_no CHAR(10),
   mail_address CHAR(20),
   PRIMARY KEY (regist_no));
   2. ALTER TABLE `addressbook` ADD COLUMN postal_code CHAR(8) NOT NULL;
   3. DROP TABLE `addressbook` 
2. 完成sql训练营task02打卡，完成课后练习
   1. SELECT product_name, regist_date FROM `product` WHERE `regist_date` > '2009-04-28'  
   2. /* 
   ans1：查询不到结果
   ans2：查询不到结果
   ans3：查询不到结果
      */  
   3. SELECT `product_name` ,`sale_price` , `purchase_price` FROM `product` WHERE `sale_price` - `purchase_price` >= 500;
-- SELECT `product_name` ,`sale_price` , `purchase_price` FROM `product` WHERE `purchase_price` - `sale_price` <= -500  
   4. SELECT `product_name` , `product_type` , `sale_price` * 0.9 - `purchase_price` AS 'profit' FROM product
-- 	 WHERE `sale_price` * 0.9 - `purchase_price` > 100 AND ( `product_name`='办公用品' OR `product_name` = '厨房用具');   
   5. GROUP BY 条件没有包含在选择列中;product_sum不可以sum聚合;where语句的位置错误
   6. SELECT `product_type` , SUM( `sale_price`) , SUM( `purchase_price`)  FROM `product` GROUP BY `product_type` HAVING  SUM( `sale_price`) > SUM( `purchase_price`) *1.5  ;  
   7. 日期，降序；出售价格，升序
