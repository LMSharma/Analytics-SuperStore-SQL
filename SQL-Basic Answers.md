1. 604
```SQL
select count(*) from city;
```
2. 531 
```SQL
select distinct(name) from city limit 10;
```
3.
```SQL
select name as duplicate_city_name, count(name)
from city
group by name
having count(name) >1;
```
4.
```SQL
select extract(year from order_date) as year,count(id) as orders
from orders
group by 1
```
5.
```SQL
select extract(month from order_date) as month, sum(sales) as sales
from orders
where extract(year from order_date) = 2017
group by 1
```
6.
```SQL
select extract(month from order_date) as month, sum(sales) as sales
from orders
where extract(year from order_date) = 2016
group by 1
order by 2 desc
limit 2;
```
7.
```SQL
select extract(month from order_date) as month, sum(sales) as sales
from orders
where extract(year from order_date) = 2017
group by 1
order by 2 asc
limit 2;
```
8.
```SQL
select split_part(id, '-',1) 
from orders

-- Checking distinct
select distinct(split_part(id, '-',1) )
from orders
```
9.
```SQL
select distinct(split_part(product_id, '-',1) )
from orders
```
10. 
```SQL
select split_part(product_id, '-',1) as category,
	count(id)
from orders
group by 1

-- Give full name to categories
select split_part(product_id, '-',1) as category,
		(case 
		when split_part(product_id, '-',1) = 'FUR' then 'FURNITURE'
		when split_part(product_id, '-',1) = 'OFF' then 'OFFICE'
		when split_part(product_id, '-',1) = 'TEC' then 'TECHNOLOGY'
		end) as Category_Full_Name, 
	count(id)
from orders
group by 1,2
```



