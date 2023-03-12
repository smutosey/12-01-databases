# Домашнее задание к занятию "`12.1. Базы данных`" - `Александр Недорезов`

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

> #### Ответ:
> Поднял базу MySQL (для выполнения следующих заданий в курсе)
> [Vagrantfile](https://github.com/smutosey/12-01-databases/blob/main/vagrant/Vagrantfile) + [config.sh](https://github.com/smutosey/12-01-databases/blob/main/vagrant/config.sh) для создания ВМ, установки Docker и запуска БД в контейнере  
> [docker-compose.yml](https://github.com/smutosey/12-01-databases/blob/main/docker-compose.yml) - инструкции для запуска MySQL и инициализации БД  

> Диаграмма БД:  
> ![img](https://github.com/smutosey/12-01-databases/blob/main/img/1-01.png)  
> 
> Сотрудники (  
> - идентификатор сотрудника, первичный ключ, integer
> - фамилия varchar(30)
> - имя varchar(30)
> - отчество varchar(30)
> - дата приёма date
> - дата увольнения date
> - оклад numeric
> - идентификатор должности, внешний ключ, smallint
> - идентификатор филиала, внешний ключ, smallint
> - идентификатор структурного подразделения, внешний ключ, smallint
> )
> 
> Должности (  
> - идентификатор должности, первичный ключ, smallint
> - наименование должности varchar(100)
> )
> 
> Филиалы (  
> - идентификатор филиала, первичный ключ, smallint
> - наименование филиала, varchar(100)
> - директор, внешний ключ (сотрудники), integer
> - КПП, smallint
> - адрес филиала, внешний ключ, smallint
> )
> 
> Подразделения (  
> - идентификатор структурного подразделения, первичный ключ, smallint
> - идентификатор типа подразделения, внешний ключ, smallint
> - наименование подразделения varchar(100)
> - вышестоящее подразделение, внешний ключ, smallint
> )  
> 
> Типы подразделений (  
> - идентификатор типа подразделения, первичный ключ, smallint
> - наименование типа подразделения, varchar(50)
> )  
> 
> Адреса (
> - идентификатор адреса, первичный ключ, smallint
> - идентификатор региона, внешний ключ, smallint
> - идентификатор населенного пункта, внешний ключ, smallint
> - идентификатор улицы, внешний ключ, smallint
> - номер дома, varchar(20)
> )
> 
> Регионы (
> - идентификатор региона, первичный ключ, smallint
> - наименование региона, varchar(50)
> )
> 
> Населенные пункты (
> - идентификатор населенного пункта, первичный ключ, smallint
> - наименование населенного пункта, varchar(50)
> )
> 
> Улицы (
> - идентификатор улицы, первичный ключ, smallint
> - наименование улицы, varchar(100)
> )
> 
> Проекты (  
> - идентификатор проекта, первичный ключ, integer
> - наименование проекта, varchar(200)
> - описание, text
> - менеджер проекта, внешний ключ, integer
> )

