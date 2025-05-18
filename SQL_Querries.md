# Restarant Data Analysis


**Selecting Database**


````SQL
USE restaurant;
````

**Checking Dataset**

````sql
SELECT * FROM orders;
````

**Result :**


| Order_id     | Customer_code      | Placed_at           | Restaurant_id | Cuisine  | Order_status | Promo_code_Name |
|--------------|--------------------|---------------------|---------------|----------|--------------|-----------------|
| OF1900191801 | UFDDN1991918XUY1   | 2025-01-01 15:30:20 | KMKMH6787     | Lebanese | Delivered    | Tasty50         |
| OF1900191802 | UFDDN1991918XUY1   | 2025-01-02 12:15:45 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191803 | UFDDN1991918XUY1   | 2025-01-10 18:45:30 | PIZZA123      | Italian  | Cancelled    | HUNGRY20        |
| OF1900191804 | UFDDN1991918XUY1   | 2025-01-15 19:20:15 | ITALIAN2      | Italian  | Delivered    | NULL            |
| OF1900191805 | UFDDN1991918XUY1   | 2025-01-20 11:30:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191806 | ABC1234567890XYZ   | 2025-01-01 08:45:00 | AMERICAN2     | American | Delivered    | NEWUSER         |
| OF1900191807 | ABC1234567890XYZ   | 2025-01-05 13:20:00 | TACO789       | Mexican  | Delivered    | NULL            |
| OF1900191808 | DEF9876543210XYZ   | 2025-01-02 09:15:00 | MEXICAN2      | Mexican  | Delivered    | FIRSTORDER      |
| OF1900191809 | GHI5678901234XYZ   | 2025-01-03 14:30:00 | SUSHI456      | Japanese | Delivered    | NEWUSER         |
| OF1900191810 | JKL3456789012XYZ   | 2025-01-04 12:00:00 | JAPANESE2     | Japanese | Delivered    | FIRSTORDER      |
| OF1900191811 | MNO7890123456XYZ   | 2025-01-05 19:45:00 | KMKMH6787     | Lebanese | Delivered    | NULL            |
| OF1900191812 | PQR1234567890ABC   | 2025-01-06 11:30:00 | LEBANESE2     | Lebanese | Delivered    | NEWUSER         |
| OF1900191813 | STU9876543210ABC   | 2025-01-07 13:15:00 | PIZZA123      | Italian  | Delivered    | NULL            |
| OF1900191814 | VWX5678901234ABC   | 2025-01-08 18:00:00 | ITALIAN2      | Italian  | Delivered    | FIRSTORDER      |
| OF1900191815 | YZA3456789012ABC   | 2025-01-09 12:45:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191816 | BCD7890123456ABC   | 2025-01-10 20:15:00 | AMERICAN2     | American | Delivered    | NEWUSER         |
| OF1900191817 | EFG1234567890DEF   | 2025-01-11 09:30:00 | TACO789       | Mexican  | Delivered    | NULL            |
| OF1900191818 | HIJ9876543210DEF   | 2025-01-12 14:45:00 | MEXICAN2      | Mexican  | Delivered    | FIRSTORDER      |
| OF1900191819 | KLM5678901234DEF   | 2025-01-13 17:30:00 | SUSHI456      | Japanese | Delivered    | NULL            |
| OF1900191820 | NOP3456789012DEF   | 2025-01-14 12:15:00 | JAPANESE2     | Japanese | Delivered    | NULL            |
| OF1900191821 | QRS7890123456DEF   | 2025-01-15 19:00:00 | KMKMH6787     | Lebanese | Delivered    | NEWUSER         |
| OF1900191822 | TUV1234567890GHI   | 2025-01-16 10:45:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191823 | WXY9876543210GHI   | 2025-01-17 15:30:00 | PIZZA123      | Italian  | Delivered    | FIRSTORDER      |
| OF1900191824 | ZAB5678901234GHI   | 2025-01-18 18:15:00 | ITALIAN2      | Italian  | Delivered    | NULL            |
| OF1900191825 | CDE3456789012GHI   | 2025-01-19 11:00:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191826 | FGH7890123456GHI   | 2025-01-20 20:45:00 | AMERICAN2     | American | Delivered    | NEWUSER         |
| OF1900191827 | IJK1234567890JKL   | 2025-01-21 09:15:00 | TACO789       | Mexican  | Delivered    | NULL            |
| OF1900191828 | LMN9876543210JKL   | 2025-01-22 14:30:00 | MEXICAN2      | Mexican  | Delivered    | FIRSTORDER      |
| OF1900191829 | OPQ5678901234JKL   | 2025-01-23 17:45:00 | SUSHI456      | Japanese | Delivered    | NULL            |
| OF1900191830 | RST3456789012JKL   | 2025-01-24 12:30:00 | JAPANESE2     | Japanese | Delivered    | NULL            |
| OF1900191831 | UVW7890123456JKL   | 2025-01-25 19:15:00 | KMKMH6787     | Lebanese | Delivered    | NEWUSER         |
| OF1900191832 | XYZ1234567890MNO   | 2025-01-26 10:00:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191833 | ABC9876543210MNO   | 2025-01-27 15:15:00 | PIZZA123      | Italian  | Delivered    | FIRSTORDER      |
| OF1900191834 | DEF5678901234MNO   | 2025-01-28 18:30:00 | ITALIAN2      | Italian  | Delivered    | NULL            |
| OF1900191835 | GHI3456789012MNO   | 2025-01-29 11:45:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191836 | JKL7890123456MNO   | 2025-01-30 20:00:00 | AMERICAN2     | American | Delivered    | NEWUSER         |
| OF1900191837 | MNO1234567890PQR   | 2025-01-31 09:45:00 | TACO789       | Mexican  | Delivered    | NULL            |
| OF1900191838 | PQR9876543210PQR   | 2025-01-31 14:00:00 | MEXICAN2      | Mexican  | Delivered    | FIRSTORDER      |
| OF1900191839 | STU5678901234PQR   | 2025-01-31 17:15:00 | SUSHI456      | Japanese | Delivered    | NULL            |
| OF1900191840 | VWX3456789012PQR   | 2025-01-31 12:00:00 | JAPANESE2     | Japanese | Delivered    | NULL            |
| OF1900191841 | JAN_ONLY_ORDER1    | 2025-01-15 13:30:00 | KMKMH6787     | Lebanese | Delivered    | NEWUSER         |
| OF1900191842 | JAN_ONLY_ORDER2    | 2025-01-20 18:45:00 | LEBANESE2     | Lebanese | Delivered    | FIRSTORDER      |
| OF1900191843 | NO_ORDER_LAST7_1   | 2025-02-01 12:15:00 | PIZZA123      | Italian  | Delivered    | NEWUSER         |
| OF1900191844 | NO_ORDER_LAST7_2   | 2025-02-05 19:30:00 | ITALIAN2      | Italian  | Delivered    | FIRSTORDER      |
| OF1900191845 | THIRD_ORDER_CUST1  | 2025-01-05 11:45:00 | BURGER99      | American | Delivered    | NEWUSER         |
| OF1900191846 | THIRD_ORDER_CUST1  | 2025-01-10 14:15:00 | AMERICAN2     | American | Delivered    | NULL            |
| OF1900191847 | THIRD_ORDER_CUST1  | 2025-01-15 17:45:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191848 | THIRD_ORDER_CUST2  | 2025-01-10 10:30:00 | TACO789       | Mexican  | Delivered    | FIRSTORDER      |
| OF1900191849 | THIRD_ORDER_CUST2  | 2025-01-15 13:45:00 | MEXICAN2      | Mexican  | Delivered    | NULL            |
| OF1900191850 | THIRD_ORDER_CUST2  | 2025-01-20 16:30:00 | TACO789       | Mexican  | Delivered    | NULL            |
| OF1900191851 | MULTI_CUISINE_CUST | 2025-01-05 12:00:00 | KMKMH6787     | Lebanese | Delivered    | NEWUSER         |
| OF1900191852 | MULTI_CUISINE_CUST | 2025-01-10 15:30:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191853 | MULTI_CUISINE_CUST | 2025-01-15 18:45:00 | PIZZA123      | Italian  | Delivered    | NULL            |
| OF1900191854 | MULTI_CUISINE_CUST | 2025-01-20 11:15:00 | ITALIAN2      | Italian  | Delivered    | NULL            |
| OF1900191855 | MULTI_CUISINE_CUST | 2025-01-25 14:45:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191856 | SINGLE_ORDER_JAN   | 2025-01-10 19:00:00 | AMERICAN2     | American | Delivered    | FIRSTORDER      |
| OF1900191857 | NO_ORDER_RECENT    | 2025-02-10 12:30:00 | TACO789       | Mexican  | Delivered    | NEWUSER         |
| OF1900191858 | NO_ORDER_RECENT    | 2025-02-15 18:00:00 | MEXICAN2      | Mexican  | Delivered    | NULL            |
| OF1900191859 | PROMO_FIRST_ONLY   | 2025-02-01 11:45:00 | SUSHI456      | Japanese | Delivered    | WELCOME50       |
| OF1900191860 | PROMO_FIRST_ONLY   | 2025-02-05 14:15:00 | JAPANESE2     | Japanese | Delivered    | NULL            |
| OF1900191861 | PROMO_FIRST_ONLY   | 2025-02-10 17:30:00 | SUSHI456      | Japanese | Delivered    | NULL            |
| OF1900191862 | LAST_ORDER_7DAYS   | 2025-03-20 10:00:00 | KMKMH6787     | Lebanese | Delivered    | FIRSTORDER      |
| OF1900191863 | LAST_ORDER_7DAYS   | 2025-03-25 13:15:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191864 | LAST_ORDER_7DAYS   | 2025-03-31 16:30:00 | KMKMH6787     | Lebanese | Delivered    | NULL            |
| OF1900191865 | ABC9876543210MNO   | 2025-02-27 15:15:00 | PIZZA123      | Italian  | Delivered    | NULL            |
| OF1900191866 | CDE3456789012GHI   | 2025-03-27 15:15:00 | PIZZA123      | Italian  | Delivered    | NULL            |
| OF1900191867 | ABC9876543210MNO   | 2025-03-15 15:15:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |
| OF1900191868 | ZZZ9876543210MNO   | 2025-03-20 15:15:00 | LEBANESE2     | Lebanese | Delivered    | NEWUSER         |
| OF1900191869 | UFDDN1991918XUY1   | 2025-03-28 11:30:00 | BURGER99      | American | Delivered    | NULL            |
| OF1900191870 | MULTI_CUISINE_CUST | 2025-03-31 14:45:00 | PIZZA123      | Italian  | Delivered    | NULL            |
| OF1900191871 | DEF9876543210XYZ   | 2025-03-02 09:15:00 | KMKMH6787     | Lebanese | Delivered    | TASTY50         |
| OF1900191872 | UVW7890123456JKL   | 2025-02-25 19:15:00 | KMKMH6787     | Lebanese | Delivered    | TASTY25         |
| OF1900191873 | UVW7890123456JKL   | 2025-03-25 19:15:00 | PIZZA123      | Italian  | Delivered    | TASTY50         |





**Top 1 outlet by each cuisine type**


````sql
with cte as (select cuisine, restaurant_id, count(*) as cnt 
from orders 
group by cuisine, restaurant_id	)

select * from (select *, row_number() over(partition by cuisine order by cnt desc) as rn 
from cte) A 
where rn = 1  
order by cnt desc;
````

**Result :**

| cuisine  | restaurant_id | cnt | rn |
|----------|---------------|-----|----|
| Italian  | PIZZA123      |  10 |  1 |
| Lebanese | KMKMH6787     |  10 |  1 |
| American | BURGER99      |   8 |  1 |
| Mexican  | TACO789       |   7 |  1 |
| Japanese | SUSHI456      |   6 |  1 |





**Number of customers joining each day.**

````SQL
with cte as (select Customer_code, min(date(Placed_at)) as date_order 
from orders 
group by customer_code) 

select date_order, count(*) as new_customers 
from cte 
group by date_order 
order by date_order;
````

**Result :**

| date_order | new_customers |
|------------|---------------|
| 2025-01-01 |             2 |
| 2025-01-02 |             1 |
| 2025-01-03 |             1 |
| 2025-01-04 |             1 |
| 2025-01-05 |             3 |
| 2025-01-06 |             1 |
| 2025-01-07 |             1 |
| 2025-01-08 |             1 |
| 2025-01-09 |             1 |
| 2025-01-10 |             3 |
| 2025-01-11 |             1 |
| 2025-01-12 |             1 |
| 2025-01-13 |             1 |
| 2025-01-14 |             1 |
| 2025-01-15 |             2 |
| 2025-01-16 |             1 |
| 2025-01-17 |             1 |
| 2025-01-18 |             1 |
| 2025-01-19 |             1 |
| 2025-01-20 |             2 |
| 2025-01-21 |             1 |
| 2025-01-22 |             1 |
| 2025-01-23 |             1 |
| 2025-01-24 |             1 |
| 2025-01-25 |             1 |
| 2025-01-26 |             1 |
| 2025-01-27 |             1 |
| 2025-01-28 |             1 |
| 2025-01-29 |             1 |
| 2025-01-30 |             1 |
| 2025-01-31 |             4 |
| 2025-02-01 |             2 |
| 2025-02-05 |             1 |
| 2025-02-10 |             1 |
| 2025-03-20 |             2 |





**Number of repeat orders each month**

````SQL
with cte as (select month(placed_at)as month_order,customer_code, row_number() over(partition by customer_code) as rn 
from orders)

select month_order, count(*) as cnt_repeat_customers
from cte
where rn <= 2
group by month_order
order by month_order;
````


**Result :**

| month_order | cnt_repeat_customers |
|-------------|----------------------|
|           1 |                   46 |
|           2 |                    6 |
|           3 |                    7 |





**All users those were acquired in Jan and only placed orders in jan and not after that.**


````SQL
with cte as (select placed_at,Customer_code 
from orders
where month(placed_at) = 1)

select distinct Customer_code from cte 
where Customer_code not in (select Customer_code 
from orders
where month(placed_at) > 1) ;
````


**Result :**

| Customer_code     |
|-------------------|
| ABC1234567890XYZ  |
| GHI5678901234XYZ  |
| JKL3456789012XYZ  |
| MNO7890123456XYZ  |
| PQR1234567890ABC  |
| STU9876543210ABC  |
| VWX5678901234ABC  |
| YZA3456789012ABC  |
| BCD7890123456ABC  |
| EFG1234567890DEF  |
| HIJ9876543210DEF  |
| KLM5678901234DEF  |
| NOP3456789012DEF  |
| QRS7890123456DEF  |
| TUV1234567890GHI  |
| WXY9876543210GHI  |
| ZAB5678901234GHI  |
| FGH7890123456GHI  |
| IJK1234567890JKL  |
| LMN9876543210JKL  |
| OPQ5678901234JKL  |
| RST3456789012JKL  |
| XYZ1234567890MNO  |
| DEF5678901234MNO  |
| GHI3456789012MNO  |
| JKL7890123456MNO  |
| MNO1234567890PQR  |
| PQR9876543210PQR  |
| STU5678901234PQR  |
| VWX3456789012PQR  |
| JAN_ONLY_ORDER1   |
| JAN_ONLY_ORDER2   |
| THIRD_ORDER_CUST1 |
| THIRD_ORDER_CUST2 |
| SINGLE_ORDER_JAN  |




**List all customers with no orders in the last 7 days but were acquired one month ago with first order on promo code.**


````SQL
with cte as (select customer_code, min(placed_at) as first_order, max(placed_at) as latest_order
from orders
group by customer_code)

select c.customer_code, date(c.first_order) as first_order, date(c.latest_order) as latest_order, o.promo_code_name
from cte c 
inner join orders o
on c.first_order = o.placed_at and c.customer_code = o.customer_code
where latest_order < '2025-03-20' and
first_order < '2025-2-27' and
o.promo_code_name is not null ;
````


**Result :**

| customer_code     | first_order | latest_order | promo_code_name |
|-------------------|-------------|--------------|-----------------|
| ABC1234567890XYZ  | 2025-01-01  | 2025-01-05   | NEWUSER         |
| DEF9876543210XYZ  | 2025-01-02  | 2025-03-02   | FIRSTORDER      |
| GHI5678901234XYZ  | 2025-01-03  | 2025-01-03   | NEWUSER         |
| JKL3456789012XYZ  | 2025-01-04  | 2025-01-04   | FIRSTORDER      |
| PQR1234567890ABC  | 2025-01-06  | 2025-01-06   | NEWUSER         |
| VWX5678901234ABC  | 2025-01-08  | 2025-01-08   | FIRSTORDER      |
| BCD7890123456ABC  | 2025-01-10  | 2025-01-10   | NEWUSER         |
| HIJ9876543210DEF  | 2025-01-12  | 2025-01-12   | FIRSTORDER      |
| QRS7890123456DEF  | 2025-01-15  | 2025-01-15   | NEWUSER         |
| WXY9876543210GHI  | 2025-01-17  | 2025-01-17   | FIRSTORDER      |
| FGH7890123456GHI  | 2025-01-20  | 2025-01-20   | NEWUSER         |
| LMN9876543210JKL  | 2025-01-22  | 2025-01-22   | FIRSTORDER      |
| ABC9876543210MNO  | 2025-01-27  | 2025-03-15   | FIRSTORDER      |
| JKL7890123456MNO  | 2025-01-30  | 2025-01-30   | NEWUSER         |
| PQR9876543210PQR  | 2025-01-31  | 2025-01-31   | FIRSTORDER      |
| JAN_ONLY_ORDER1   | 2025-01-15  | 2025-01-15   | NEWUSER         |
| JAN_ONLY_ORDER2   | 2025-01-20  | 2025-01-20   | FIRSTORDER      |
| NO_ORDER_LAST7_1  | 2025-02-01  | 2025-02-01   | NEWUSER         |
| NO_ORDER_LAST7_2  | 2025-02-05  | 2025-02-05   | FIRSTORDER      |
| THIRD_ORDER_CUST1 | 2025-01-05  | 2025-01-15   | NEWUSER         |
| THIRD_ORDER_CUST2 | 2025-01-10  | 2025-01-20   | FIRSTORDER      |
| SINGLE_ORDER_JAN  | 2025-01-10  | 2025-01-10   | FIRSTORDER      |
| NO_ORDER_RECENT   | 2025-02-10  | 2025-02-15   | NEWUSER         |
| PROMO_FIRST_ONLY  | 2025-02-01  | 2025-02-10   | WELCOME50       |





**Show the customer id of the customers after every second transaction, which team can use to send personalized email.**

````SQL
with cte as (
select *, row_number() over(partition by customer_code order by placed_at) as transaction_number
from orders)
select * from cte
where transaction_number%2=0 and date(placed_at) = '2025-03-31'
order by customer_code;
````

**Result :**


| Order_id     | Customer_code      | Placed_at           | Restaurant_id | Cuisine | Order_status | Promo_code_Name | transaction_number |
|--------------|--------------------|---------------------|---------------|---------|--------------|-----------------|--------------------|
| OF1900191870 | MULTI_CUISINE_CUST | 2025-03-31 14:45:00 | PIZZA123      | Italian | Delivered    | NULL            |                  6 |





**List of customer who has placed more than 1 order and all of them were with a promo code**

````SQL
select customer_code, count(customer_code) as no_of_orders, count(promo_code_name) as promocode_count
from orders
group by customer_code
having  no_of_orders > 1 and 
no_of_orders = promocode_count ;
````

**Result :**


| customer_code    | no_of_orders | promocode_count |
|------------------|--------------|-----------------|
| DEF9876543210XYZ |            2 |               2 |
| UVW7890123456JKL |            3 |               3 |




**list of customers which were acquired organically in Jan 2025, without any promo code**

````SQL
create view jan_null_promocode as (
select *, row_number() over(partition by customer_code order by placed_at) as rn
from orders
where month(placed_at) = 1);

select * 
from jan_null_promocode
where rn = 1 and promo_code_name is null;
````


**Result :**


| Order_id     | Customer_code    | Placed_at           | Restaurant_id | Cuisine  | Order_status | Promo_code_Name | rn |
|--------------|------------------|---------------------|---------------|----------|--------------|-----------------|----|
| OF1900191825 | CDE3456789012GHI | 2025-01-19 11:00:00 | BURGER99      | American | Delivered    | NULL            |  1 |
| OF1900191834 | DEF5678901234MNO | 2025-01-28 18:30:00 | ITALIAN2      | Italian  | Delivered    | NULL            |  1 |
| OF1900191817 | EFG1234567890DEF | 2025-01-11 09:30:00 | TACO789       | Mexican  | Delivered    | NULL            |  1 |
| OF1900191835 | GHI3456789012MNO | 2025-01-29 11:45:00 | BURGER99      | American | Delivered    | NULL            |  1 |
| OF1900191827 | IJK1234567890JKL | 2025-01-21 09:15:00 | TACO789       | Mexican  | Delivered    | NULL            |  1 |
| OF1900191819 | KLM5678901234DEF | 2025-01-13 17:30:00 | SUSHI456      | Japanese | Delivered    | NULL            |  1 |
| OF1900191837 | MNO1234567890PQR | 2025-01-31 09:45:00 | TACO789       | Mexican  | Delivered    | NULL            |  1 |
| OF1900191811 | MNO7890123456XYZ | 2025-01-05 19:45:00 | KMKMH6787     | Lebanese | Delivered    | NULL            |  1 |
| OF1900191820 | NOP3456789012DEF | 2025-01-14 12:15:00 | JAPANESE2     | Japanese | Delivered    | NULL            |  1 |
| OF1900191829 | OPQ5678901234JKL | 2025-01-23 17:45:00 | SUSHI456      | Japanese | Delivered    | NULL            |  1 |
| OF1900191830 | RST3456789012JKL | 2025-01-24 12:30:00 | JAPANESE2     | Japanese | Delivered    | NULL            |  1 |
| OF1900191839 | STU5678901234PQR | 2025-01-31 17:15:00 | SUSHI456      | Japanese | Delivered    | NULL            |  1 |
| OF1900191813 | STU9876543210ABC | 2025-01-07 13:15:00 | PIZZA123      | Italian  | Delivered    | NULL            |  1 |
| OF1900191822 | TUV1234567890GHI | 2025-01-16 10:45:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |  1 |
| OF1900191840 | VWX3456789012PQR | 2025-01-31 12:00:00 | JAPANESE2     | Japanese | Delivered    | NULL            |  1 |
| OF1900191832 | XYZ1234567890MNO | 2025-01-26 10:00:00 | LEBANESE2     | Lebanese | Delivered    | NULL            |  1 |
| OF1900191815 | YZA3456789012ABC | 2025-01-09 12:45:00 | BURGER99      | American | Delivered    | NULL            |  1 |
| OF1900191824 | ZAB5678901234GHI | 2025-01-18 18:15:00 | ITALIAN2      | Italian  | Delivered    | NULL            |  1 |




**Percentage of customers which were acquired organically in Jan 2025, without any promo code.**

````SQL
select count(case when rn = 1 and promo_code_name is null then customer_code end)*100 / count(distinct customer_code) as organic_percentage  
from jan_null_promocode;
````


**Result :**

| organic_percentage |
|--------------------|
|            43.9024 |






