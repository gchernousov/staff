## Дополнительное задание на создание таблиц

Код:

```
CREATE TABLE departments(
	id SERIAL PRIMARY KEY,
	department VARCHAR(255) NOT NULL,
);

CREATE TABLE staff(
	id SERIAL PRIMARY KEY,
	employee VARCHAR(255) NOT NULL,
	department INTEGER REFERENCES departments(id),
	head INTEGER REFERENCES staff(id)
);
```

Схема:

![](/staff.jpg)