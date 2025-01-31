{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "расширение", "файл", "формат файла", "Тип файла базы данных", "Формат файла базы данных", "Файлы базы данных" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла ACCDW и API-интерфейсах, которые могут создавать и открывать файлы ACCDW.",
  "title" :"ACCDW — файл ссылки на базу данных Microsoft Access",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## .ACCDW вариант №

Файл с расширением .accdw представляет собой файл ссылки, созданный с помощью Microsoft Access, и содержит информацию о ссылке для загрузки файла базы данных Access, т.е. [ACCDB](/ru/database/accdb/) с сервера SharePoint. Это позволяет пользователям совместно использовать файлы базы данных, размещенные удаленно. При открытии файла ACCDW связанный файл ACCDB загружается как локальная копия на компьютер пользователя. Загруженный файл сохраняется в папке загрузки по умолчанию, и доступ к нему можно получить, перейдя к нему. Обычно эти файлы загружаются и сохраняются под именем «SiteServer.accdb», которое относится к клиентским базам данных.

## Формат файла ACCDW — дополнительная информация

Файл ACCDW — это XML-файл, содержащий ссылку на сайт SharePoint, на котором размещены службы Access. Это только ярлык, и для их запуска требуется подключение к Интернету. В случае подключения к сети SharePoint кэшируется локально, чтобы предоставить возможность перевести его в автономный режим позже.

## использованная литература

* [Спецификации Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Загрузка файла .accdw](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file)
* [Какой формат файла Access следует использовать?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
