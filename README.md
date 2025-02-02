1. Вывести имена всех людей, которые есть в базе данных
   авиакомпаний [(сайт)](https://sql-academy.org/ru/trainer/tasks/1)

<details>
  <summary>Решение</summary>

```postgres
SELECT name
FROM passenger;
```

</details>

2. Вывести названия всеx авиакомпаний [(сайт)](https://sql-academy.org/ru/trainer/tasks/2)

<details>
  <summary>Решение</summary>

```postgres
SELECT name
FROM Company;
```

</details>

3. Вывести все рейсы, совершенные из Москвы [(сайт)](https://sql-academy.org/ru/trainer/tasks/3)

<details>
 <summary>Решение</summary>

```postgres
SELECT *
FROM trip
WHERE town_from  = "Moscow";
```

</details>

4. Вывести имена людей, которые заканчиваются на "man" [(сайт)](https://sql-academy.org/ru/trainer/tasks/4)

<details>
 <summary>Решение</summary>

```postgres
SELECT name
FROM Passenger
WHERE name LIKE  '%man';
```

5.  Вывести количество рейсов, совершенных на TU-134 [(сайт)](https://sql-academy.org/ru/trainer/tasks/5)

<details>
 <summary>Решение</summary>

```postgres
SELECT COUNT(*) AS count  
FROM trip
WHERE plane = 'TU-134';
```

6.Какие компании совершали перелеты на Boeing  [(сайт)](https://sql-academy.org/ru/trainer/tasks/6)

<details>
<summary>Решение</summary>

```postgres
 SELECT DISTINCT cp.name
FROM company cp
JOIN trip tr ON cp.id = tr.company
WHERE plane = 'Boeing';
```

7.Вывести все названия самолётов, на которых можно улететь в Москву (Moscow) [(сайт)](https://sql-academy.org/ru/trainer/tasks/7)

<details>
<summary>Решение</summary>

```postgres
SELECT DISTINCT plane
FROM trip
WHERE town_to = 'Moscow';
```

8.



