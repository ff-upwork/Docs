{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "файл asmx", "формат файлу asmx", "тип файлу asmx", "файл", "тип", "що таке файл asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - файл веб-служби ASP.NET",
  "description" :"Дізнайтеся, що таке файл ASMX та API, які можуть створювати та відкривати файли ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Що таке файл ASMX?

Файл із розширенням .asmx — це файл веб-служби ASP.NET, який забезпечує зв’язок між двома об’єктами через Інтернет за допомогою простого протоколу доступу до об’єктів (SOAP). Він розгортається як служба на веб-сервері Windows для обробки вхідного запиту та повернення відповіді. На відміну від файлів [ASPX](/uk/web/aspx/), які містять код для візуального відображення веб-сторінок ASP.NET, файли ASMX працюють на сервері у фоновому режимі та виконують різні завдання, як-от підключення до бази даних, отримання даних і повернення їх у формат, у якому було зроблено запит. Вони використовуються спеціально для веб-служб XML.

## Формат файлу ASMX

Файли ASMX мають звичайний текстовий формат і їх можна відкривати або редагувати в таких програмах, як Microsoft Visual Studio або текстових редакторах. Це власний формат файлів Microsoft і має чітко визначений синтаксис для створення веб-служб. Відповідь файлу ASMX у формі SOAP XML містить такі елементи.

* `Envelop` - кореневий елемент, який ідентифікує XML-документ як повідомлення SOAP.
* `Header` – необов'язковий елемент, який містить інформацію про програму, наприклад дані автентифікації. Якщо присутній елемент Header, він має бути першим дочірнім елементом елемента Envelope.
* `Тіло` - містить повідомлення SOAP, призначене для одержувача.
* `Fault` - додатковий елемент, який використовується для вказівки повідомлень про помилки. Якщо присутній елемент Fault, він має бути дочірнім елементом елемента Body.

Файли ASMX можна писати такими мовами .NET, як [C#](/uk/programming/cs/), [Visual Basic](/uk/programming/vb/) або JScript.

## Чим ASMX відрізняється від ASPX і ASCX?

Файли ASMX відрізняються від файлів ASPX і ASCX.

* ASPX, Active Server Pages, файли – це файли програмування, створені за допомогою Microsoft ASP.NET framework, що працює на веб-серверах. Вони відображаються у веб-браузері клієнта, коли користувач запитує доступ до такої сторінки.
* ASCX, Active Server User Control, визначає елементи керування користувачами, які використовуються для визначення повторно використовуваних елементів керування на веб-сторінках ASP.NET або на всьому веб-сайті.

## Список літератури

* [Використання служби ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Керування користувача ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

