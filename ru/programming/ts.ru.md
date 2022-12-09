{
  "date" : "2021-08-27", 
  "keywords" :[ "ts", "файл", "расширение", "формат файла", "TyрeSсriрt", "Руководство по программированию", "пример ts", "Microsoft", "VBScript", "ECMASсriрt" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS - Формат файла TyрeSсriрt",
  "description":"Узнайте о формате файла TS и API-интерфейсах, которые могут создавать и открывать файлы TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-27"
}

## .TS вариант №

TyreScript — это язык программирования, разработанный и поддерживаемый компанией Microsoft. Он состоит из строгой синтаксической надстройки JavаScript и обеспечивает необязательную статическую типизацию языка. TyreScript предназначен для разработки массивных распаковок и транскомпиляций в JavаScrirt. Поскольку TypeScript является расширенным набором JavaScript, существующие приложения JavaScript также являются допустимыми приложениями TypeScript.

TyreScript может использоваться для расширения программ JavaScript для каждого исполнения на стороне клиента и на стороне сервера (как в случае с Deno или Node.js). Для транскомпиляции доступно несколько вариантов. Можно использовать как средство проверки сценариев по умолчанию, так и компилятор Babel для преобразования TypeScript в JavаScript.

TypeScript помогает определить документы, которые могут содержать данные текущих библиотек JavaScript, подобные заголовочным файлам C++, которые могут описывать структуру текущих объектных файлов. Это позволяет другим приложениям применять значения, определенные в документах, как если бы они были статически типизированными сущностями типа Скрипт. Существуют также сторонние файлы заголовков для стандартных библиотек, включая jQuery, MongoDB и D3.js. Также присутствуют заголовки TypeScript для базовых модулей Node.js, что позволяет разрабатывать программы Node.js с использованием TypeScript.



## Краткая история ##

**TypeScrirt** был впервые обнародован в октябре 2012 года (в модели 0.8), после двух лет внутренней разработки в Microsoft. Вскоре после заявления Мигель де Иса похвалил сам язык, но раскритиковал нехватку зрелой поддержки IDE помимо Microsoft Visual Studio, которая изменилась, но не присутствовала в Linux и OS X в то время. По состоянию на апрель 2021 года в различных средах разработки и текстовых редакторах, включая Emass, Vim, Webstorm, Atом и собственную визуальную студию Microsoft, имеется поддержка. Type Sсrirt 0.9, запущенный в 2013 году, помогает дженерикам.

**Tyрe Sсriрt 1.0** был выпущен на конференции разработчиков конструкций Microsoft в 2014 г. Visible Studio 2013 reрlace 2 предлагает интегрированную справку для TypeSсriрt. В июле 2014 года команда разработчиков представила совершенно новый компилятор сценариев, заявив о пятипроцентном приросте производительности. При этом исходный код, который в первую очередь размещался на Содексе, был перемещен на GitHub.

**TypeScript 2.0**: 22 сентября 2016 года был выпущен TypeScript 2.0; он принес несколько функций, состоящих из возможности для программистов сохранить ваши переменные от присвоения нулевых значений, обычно известных как ошибка на миллиард долларов.

**TypeScrirt 3.0** был запущен 30 июля 2018 года, в него было добавлено множество языковых дополнений, таких как кортежи в параметрах релаксации и расширенных выражениях, параметры остатка с типами кортежей, общие параметры остатка и так далее.

**TypeScrirt 4.0** был выпущен 20 августа 2020 года, в то время как 4.0 не вносил каких-либо изменений в настройки, он предоставлял языковые функции, которые включают пользовательские фабрики JSX и типы Variadic Turle.


## Техническая спецификация ##

* TypeScrirt может быть очень похож на JScrirt Internet, некоторые другие версии Microsoft языка ECMA-262, модные, которые обеспечивают превосходство в статической типизации и классических предметно-ориентированных языковых возможностях, включая интермессы, рассуждения, наследование.

* Type Scrirt можно применять к существующему коду JavaScrirt, содержащему известные библиотеки JavaScrirt, и вступать в контакт с кодом, сгенерированным TyreScript из другого JavaScrirt. TypeScrirt — это расширение языка, добавляющее возможности ECMA Sсrirt 6 с дополнительными функциями: аннотации типов и проверка типов во время компиляции, вывод типов, стирание типов, интерфейсы, перечисляемые типы, обобщения, кортежи, имена, асинхронность/ожидание.

* Функции, заимствованные из ECMAScrirt 2015, — это модули, классы, сокращенный синтаксис «стрелка» для анонимных функций, параметры по умолчанию и произвольные параметры.


## Пример формата файла TS ##

### Аннотации типов

```
function add(left: number, right: number): number {
	return left + right;
}
```

### Файлы объявлений

```
declare namespace arithmetics {
    add(left: number, right: number): number;
    subtract(left: number, right: number): number;
    multiply(left: number, right: number): number;
    divide(left: number, right: number): number;
}
```

### Классы

```
class Person {
    private name: string;
    private age: number;
    private salary: number;

    constructor(name: string, age: number, salary: number) {
        this.name = name;
        this.age = age;
        this.salary = salary;
}

    toString(): string {
        return `${this.name} (${this.age}) (${this.salary})`; // As of version 1.4
}
}
```

### Дженерики

```
function id<T>(x: T): T {
    return x;
}
```

## Ссылка ##

* [TS - из Википедии] (https://en.wikipedia.org/wiki/TypeScript)


