{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл CON — формат исходного файла концептуального приложения",
  "description" :"Узнайте, что такое файл CON и API, которые могут создавать и открывать файлы CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
"идентификатор":"веб-кон",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## .CON вариант №

Файл CON — это файл исходного кода для приложения, разработанного для **Concept Application Server**. Используется для написания приложений для обмена данными между сервером и пользователем. Файлы CON, размещенные на сервере, доступны через веб-браузер при условии, что на стороне пользователя установлен концептуальный клиент. Концептуальный сервер приложений — это веб-сервер с небольшим языком программирования, который может иметь механизм базы данных подмножества [SQL](/ru/database/sql/) (TinDB).

Файлы CON можно открывать/запускать с сервером приложений RadGs Concept Application Server.

## Формат файла CON — дополнительная информация

Файлы CON размещаются на сервере и доступны через веб-браузер на компьютере пользователя. Концептуальные [URL](/ru/web/url/) отличаются от обычных URL-адресов HTTP и начинаются с **concept://**.

### Пример URL файла CON

Доступ к файлу CON, размещенному на сервере приложений Concept, можно получить через веб-браузер, используя такие URL-адреса, как:

```
concept://domain.server.com/web_application/main.con.
```
## использованная литература

* [Сервер концептуальных приложений](https://github.com/Devronium/ConceptApplicationServer)

