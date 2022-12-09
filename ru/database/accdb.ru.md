{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "расширение", "файл", "формат файла", "Тип файла базы данных", "Формат файла базы данных", "Файлы базы данных" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла ACCDB и API-интерфейсах, которые могут создавать и открывать файлы ACCDB.",
  "title" :"Формат файла ACCDB — файл базы данных Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## .ACCDB вариант №

Файл с расширением .accdb представляет собой файл базы данных Microsoft Access 2007, в котором данные пользователей хранятся в таблицах. Он поддерживает хранение
настраиваемые формы, SQL-запросы и другие данные. Файлы ACCDB заменили файлы [MDB](/ru/database/mdb/) после того, как Microsoft перешла на файловую структуру на основе XML. Файлы ACCDB все еще могут быть преобразованы в MDB со старой совместимостью. Однако в настоящее время ACCDB является широко используемым форматом файла базы данных Access. Microsoft также поддерживала дополнительные функции в формате ACCDB, такие как возможность хранения файловых вложений, двоичных данных и поддержка многозначных полей.

## Формат файла ACCDB

Как и в случае с MDB, для формата файла ACCDB нет общедоступных спецификаций. Microsoft поддерживает программный доступ к этим файлам через стандарт Open Database Connectivity (ODBC) и Visual Basic для приложений (VBA).

### Инсайт

Шестнадцатеричный дамп простого файла ACCDB предполагает наличие общего сходства в структуре с последними версиями предшествующего семейства форматов MDB. Оба формата файлов используют фиксированный размер страницы 4096 байт. Еще одно сходство между ACCDB и MDB заключается в форме магического числа, которое включает в себя строку «Стандартная база данных ACE» для ACCDB. Код версии или совместимости находится в одном и том же месте в обоих форматах. Инструменты mdb | В файле HACKING указано: «Смещение 0x14 содержит Jet-версию этой базы данных», и неофициальное руководство MDB соглашается. Информация в этих источниках в сочетании с записью Википедии для [Microsoft Jet Database Engine] (https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) предполагает, что значение 0x02 указывает на ACE 12 (Access 2007), а 0x03 указывает на ACE. 14 (Доступ 2010). Однако минимальная база данных, созданная в Access 2010, и аналогичная база данных, созданная в Access 2016, имеют в этом расположении 0x02. Минимальная база данных, созданная в Access 2016, но определяющая столбец с недавно введенным типом данных «большое целое», имела значение 0x05. В файлах ACCDB этот индикатор отражает совместимость файла, а не версию механизма ACE, использованного для его создания.

## использованная литература

* [Формат файла доступа] (https://support.microsoft.com/en-us/office/what-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Спецификации Access 2016] (https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Ядро базы данных Microsoft Jet] (https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Какой формат файла Access следует использовать?] (https://support.microsoft.com/en-us/office/what-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)
