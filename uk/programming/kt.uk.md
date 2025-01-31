---
date: 2019-10-11
keywords: kt, .kt, формат файлу kotlin, як відкрити файли kotlin, як запустити файли kotlin, формат файлу .kt, файл kt, розширення файлу kotlin, розширення .kt, kotlin проти java
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу KT
linktitle: KT
description: "Дізнайтеся про формат файлів KT та API, які можуть створювати та відкривати файли KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Що таке файл KT? ##

Вихідний код, написаний у Kotlin, зберігається з розширенням .kt, яке широко відоме як **розширення файлу Kotlin**. Kotlin — це універсальна крос-платформна мова програмування, розроблена JetBrains для повної взаємодії з [Java](/uk/programming/java/). Торгова марка Kotlin захищена Фондом Котліна.

7 травня 2019 року компанія Google оголосила Kotlin як мову програмування, якій надається перевага для розробки додатків Android. У жовтні 2017 року Android Studio 3.0 почала підтримувати Kotlin як альтернативу для розробки додатків Android.

## Коротка історія формату файлів Kotlin KT##

Kotlin був представлений JetBrains у липні 2011 року як нова мова програмування для JVM. Керівник JetBrains Дмитро Джемеров сказав, що в більшості мов відсутні функції, які вони шукали, крім Scala, але повільна компіляція Scala була недоліком. Однією з головних цілей Kotlin була компіляція так само швидко, як Java. Проект Kotlin був відкритий за ліцензією Apache 2 у лютому 2012 року.

Версія 1.0 Kotlin була випущена 15 лютого 2015 року. Android оголосила про першокласну підтримку Kotlin на Android на Google I/O 2017. Kotlin 1.2 було випущено 28 листопада 2017 року з можливістю спільного використання коду між платформами JVM і JavaScript. Kotlin 1.3 було випущено 29 жовтня 2018 року з підтримкою асинхронного програмування. 7 травня 2019 року Google оголосив Kotlin як мову програмування, якій надається перевага для розробки додатків Android. Kotlin 1.4 було випущено в серпні 2020 року з деякими незначними змінами для підтримки взаємодії з Swift/Objective-C.

## Синтаксис Kotlin ##

Kotlin було розроблено, щоб бути кращим за Java, але все ще бути сумісним із кодом Java, щоб забезпечити поступовий перехід від Java до Kotlin.

* Крапка з комою необов’язкова в Kotlin. Щоб вказати кінець висловлювання, достатньо нового рядка.
* Kotlin підтримує два типи змінних: лише для читання, визначені ключовим словом *val*, і змінні, визначені ключовим словом *var*.
* За замовчуванням заняття приватні та остаточні. Щоб походити від класу, базовий клас має бути оголошений за допомогою ключового слова *open*.
* Kotlin також підтримує процедурне програмування.
* Точкою входу в програму Kotlin є «основна» функція, подібна до Java, C# тощо.

### Приклад синтаксису ###

Нижче наведено приклад синтаксису Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

У наведеному вище коді ключове слово **fun** визначає функцію під назвою main. Усередині функції оголошується змінна "audience", доступна лише для читання, за допомогою ключового слова **val**. За допомогою методу **println** на консолі друкується «Hello World from Kotlin». Значення змінної аудиторії вводиться в рядок зі знаком **$**.

## Kotlin проти Java
Kotlin є офіційною мовою для написання програм для Android із багатьма розширеними функціями, але багато досвідчених Java-розробників досі не виявляють інтересу переходити на Kotlin. Вони думають, що можуть зробити все лише за допомогою Java. Отже, нижче наведено порівняння між двома технологіями, які можуть переконати розробників Java змінити:

| Параметр | Java | Котлін |
|--------------------|-----------|---------------- -|
| Об'єкти Singletons | √ | √ |
| Типи підстановок | √ | Χ |
| Компіляція | Байт-коди | Віртуальна машина |
| Лямбда-вираз | Χ | √ |
| Інваріантний масив | Χ | √ |
| Неприватні поля | √ | Χ |
| Smart Casts | Χ | √ |
| Null Safety | Χ | √ |
| Статичні члени | √ | Χ |

## Посилання ##

- [Kotlin (мова програмування) - Вікіпедія](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

