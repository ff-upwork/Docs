{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML файлов формат – Bean Markup Language File",
  "description":"Научете за BML файловия формат и API, които могат да създават и отварят BML файлове.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Какво е BML файл?

Файл с разширение .bml е файл на Bean Markup Language, който съхранява Java класове за поддръжка на Java приложения. Това позволява достъп до Java обекти и методи и не е необходимо да се създава нова функционалност с помощта на Java класове. Той определя как компонентите са свързани един с друг за изпълнение на полезни задачи. BML е разработен от IBM alphaWorks, за да опише връзките между структурите и компонентите. BML файловете могат да се отварят и преглеждат с помощта на всеки текстов редактор като уеб браузъри, Microsoft Notepad и Notepad++.

## BML файлов формат

Уебсайтът на IBM alphaworks предостави две реализации на BML. Първата имплементация е интерпретатор, който „възпроизвежда“ BML скрипт за генериране на желаната йерархия на компонентите. Второто изпълнение е компилатор, който компилира всеки BML скрипт в Java код без отражение. Това е предимство в смисъл, че позволява улавяне на междукомпонентната структура на приложението с помощта на език, който е предназначен за тази конкретна цел с добавена възможност за компилирането му в „обикновен“ Java код.

## BML етикети

Следното е обяснение на някои от таговете, използвани в езика BML:

### The<bean> таг:

The<bean> елемент се използва за създаване на нови зърна или за търсене на зърна по име. The<bean> етикетът е във формат:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
„ID“ в етикета е свързан с регистъра на обекта за JavaBean.

### The<string> етикет

Има два начина, по които тагът за низ може да се използва:

1. За да създадете непразен низ:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. За да създадете празен низ:

```
<string/>
```
## Препратки

* [Обектно-ориентирано изпращане на съобщения с XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Езикът за физическо маркиране](http://web.mit.edu/mecheng/pml/standards.htm)


