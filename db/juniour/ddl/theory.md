# DDL

Имя Атрибута, Тип PG, Ограничения (Constraints).
Все эти данные хранятся как данные специальных встроенных таблиц Postgres.

##

Значения по умолчанию

```
CREATE TABLE "Table" (t int default 1);


```


## Constraints
```
create table test (
  value numeric(1) check (value >= 1)
);

create table test (
  value numeric(1),
  constraint valid check (value >= 1)	
);

```

```sql

CREATE table baz ( value int NOT NULL);

```

## Unique

Ограничения, например, номер паспорта

```
CREATE TABLE FOO ( VALUE INT UNIQUE (FOO) ); 

```
## Primary Key

Первичный ключ -- определяет уникальность строки. 

Можно сделать его составным.

```
Create table foo ( k int primary k );

Create table baz ( k int, primary key (k) )
```

## Alter

Изменение таблицы

```

Alter table foo drop column t;
Alter table "baz" alter column type varchar;
Drop table foo;
alter table foo add constraint check_positive check (val > 0);
AlTeR TaBlE fOo REnAme column t to v; 


```

## Представления

Сохраненные запросы. Это удобно, когда запрос очень сложный, чтобы не писать в программе.
Существуют материализованные представления, данные там хранятся. Однако существует проблема, что данные исходных таблиц не обновляются.

```
Create view v_t as select 1;
DROP view v_t;
```


## Связи -- следующий Урок @TODO


Проверка через триггер *. Пока не будем брать, т.к. будем

 
