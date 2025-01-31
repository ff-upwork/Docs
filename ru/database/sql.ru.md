{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "расширение", "файл", "формат файла", "Тип файла базы данных", "Формат файла базы данных", "Файлы базы данных" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файлов SQL и API, которые могут создавать и открывать файлы SQL.",
  "title" :"Формат файла SQL — файл данных языка структурированных запросов",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## .SQL вариант №

Файл с расширением .sql представляет собой файл языка структурированных запросов (SQL), который содержит код для работы с реляционными базами данных. Он используется для написания операторов SQL для операций CRUD (создание, чтение, обновление и удаление) в базах данных. Файлы SQL распространены при работе с настольными и веб-базами данных. Существует несколько альтернатив SQL, таких как Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL и некоторые другие. Файлы SQL можно открывать с помощью редакторов запросов Microsoft SQL Server, MySQL и других текстовых редакторов, таких как Блокнот в ОС Windows.

## Краткая история

* Разработан и представлен Доналом Д. Чемберлином и Рэймондом Ф. Бойсом в IBM в начале 1970-х гг.
* Используется для хранения и извлечения данных из исходной квазиреляционной системы управления базами данных IBM, System R.
* Начали использоваться в коммерческих продуктах на базе своего прототипа System R, включая System/38, SQL/DS и DB2, которые были коммерчески доступны в 1979, 1981 и 1983 годах соответственно.
* Официально принят группами стандартов ANSI и ISO в качестве стандарта «Язык базы данных SQL» для систем управления реляционными базами данных (RDBMS) к 1986 г.

## Формат файла SQL

Файлы SQL имеют обычный текстовый формат и могут содержать несколько языковых элементов. В один файл SQL можно добавить несколько операторов, если их выполнение возможно независимо друг от друга. Эти команды SQL могут выполняться редакторами запросов для выполнения операций CRUD.

### Элементы языка SQL

Элементы языка SQL перечислены ниже.

|Элемент|Описание|
---|---|
|Положения| Составные компоненты операторов и запросов.|
|Выражения| Может создавать либо скалярные значения, либо таблицы, состоящие из столбцов и строк данных|
|Предикаты| Укажите условия, которые могут быть оценены для трехзначной логики SQL (3VL) (истина/ложь/неизвестно) или логические значения истинности и используются для ограничения эффектов операторов и запросов или для изменения потока программы.|
|Запросы| Получить данные на основе определенных критериев. Это важный элемент SQL.|
|Утверждения| Может оказывать постоянное влияние на схемы и данные или может управлять транзакциями, потоком программ, соединениями, сеансами или диагностикой.|

### Пример SQL
Следующая инструкция SQL создает таблицу с именем **DATA**, за которой следуют дополнительные команды `INSERT` для вставки записей в эту таблицу.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Использованная литература ##

* [SQL из Википедии](https://en.wikipedia.org/wiki/SQL)
* [Синтаксис SQL](https://en.wikipedia.org/wiki/SQL_syntax)

