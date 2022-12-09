{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл APPCACHE — формат файла манифеста кэша HTML5",
  "description" :"Узнайте, что такое файл APPCACHE и API, которые могут создавать и открывать файлы APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## .APPCACHE вариант №

Файл APPCACHE — это текстовый файл, содержащий список ресурсов, которые браузеры должны кэшировать для автономного доступа к веб-приложениям. Это полезно, когда нет подключения к Интернету. В такой ситуации браузер использует ресурсы автономного кэша для обеспечения доступа к веб-содержимому. Файл APPCACHE содержит веб-ресурсы, такие как изображения (например, **[PNG](/ru/image/png/)**, **[WEBP](/ru/image/webp/)** и т. д.), таблицы стилей **([ CSS])(/ru/web/css/)** и файлы сценариев (например, файлы Javascript **[JS](/ru/web/js/)**).

Приложения, которые могут **открывать файлы APPCACHE**, включают веб-браузеры, такие как Google Chrome, Safari и Firefox.

## Формат файла APPCACHE — дополнительная информация

Файлы APPCACHE представляют собой простые текстовые файлы, обеспечивающие автономный доступ к веб-страницам для работы без подключения к Интернету. Наличие APPCACHE означает, что страница доступна в автономном режиме.

### Как сослаться на файл APPCACHE?

На вашей HTML-странице файл APPCACHE упоминается следующим образом.

```
<html manifest="example.appcache">
  ...
</html>
```

## Структура файла манифеста APPCACHE

Простой файл манифеста APPCACHE выглядит следующим образом.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Это самый простой пример, но могут быть и более сложные конструкции.

## Преимущества манифеста APPCACHE

Использование интерфейса кэширования дает веб-приложениям следующие преимущества.

1. Просмотр в автономном режиме. Интерфейс кеша позволяет конечным пользователям просматривать ваш сайт полностью, когда они находятся в автономном режиме.
1. Скорость — кеш-память обеспечивает высокоскоростной доступ к офлайн-контенту прямо с диска.
1. Постоянная доступность. Если ваш сайт выйдет из строя, пользователи по-прежнему будут иметь доступ к веб-содержимому и смогут работать в автономном режиме.

## использованная литература

* [Руководство для начинающих по манифесту AppCache] (https://web.dev/appcache-beginner/)
