---
date: 2022-05-09
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Формат файлу PYI – визначення інтерфейсу Python
linktitle: PYI
description: "Дізнайтеся про формат файлу PYI та API, які можуть створювати та відкривати файли PYI."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Що таке файл PYI?

Файл PYI — це файл визначення інтерфейсу Python, який містить посилання на заглушку коду для реалізації інтерфейсу. Кожен модуль Python представлений як заглушка .pyi, яка є звичайним файлом Python, але з порожніми методами. Синтаксис файлів PYI такий самий, як і звичайного модуля Python. Реалізація порожніх методів залишається для кінцевого користувача для досягнення конкретної мети, для якої написаний модуль. Саме тут файли PYI відрізняються від файлів [PY](/uk/programming/py/), які містять повну реалізацію програми. Файли PYI можна відкривати за допомогою текстових редакторів, таких як Notepad, Notepad++, Microsoft Visual Studio Code та JetBrains PyCharm.

## Формат файлу PYI

Файли PYI зберігаються як звичайні текстові файли, які можна відкрити в будь-якому текстовому редакторі. Python — це мова інтерпретатора, яка виконує перевірку типу під час виконання коду. У такому випадку файли PYI корисні тим, що розробники можуть вручну визначати та перевіряти типи модуля під час написання програми.

## Посилання ##

* [Інтерфейси - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [Інтерпретатори PYM](https://github.com/interpreters/pym)

