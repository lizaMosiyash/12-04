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
 select date_format(p.payment_date, '%Y-%m') month, count(r.rental_id) rentCount from payment p inner join rental r on p.rental_id=r.rental_id group by date_format(p.payment_date, '%Y-%m') order by rentCount desc limit 1;
```

![3](https://github.com/lizaMosiyash/12-04/blob/master/screenshots/3.PNG)


