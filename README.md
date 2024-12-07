# Домашнее задание к занятию "`SQL. Часть 2`" - `Солдатенкова Елизавета`

---

### Задание 1

```
select concat(st.first_name, ' ', st.last_name) as stuff_name, city, count(c.customer_id) as count_of_customers  from store s inner join customer c inner join staff st on s.store_id=c.store_id=st.store_id inner join address ad on ad.address_id=s.address_id inner join city ci on ci.city_id=ad.city_id group by st.first_name, st.last_name having count(c.customer_id) > 300;
```

![1](https://github.com/lizaMosiyash/12-04/blob/master/screenshots/1.PNG)


---

### Задание 2

```
select count(*) from film where length > (select AVG(length) from film);
```

![2](https://github.com/lizaMosiyash/12-04/blob/master/screenshots/2.PNG)


---

### Задание 3

```
 select top 1 * from (select date_format(payment_date, '%Y-%m') month as month, sum(amount) sumPerMonth from payment group by date_format(payment_date, '%Y-%m') order by sumPerMonth desc) s order by s.month desc;
```

![3](https://github.com/lizaMosiyash/12-04/blob/master/screenshots/3.PNG)

