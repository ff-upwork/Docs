---
date: 2020-11-11
keywords: myi, .myi, файлов формат myi, как да отваряте myi файлове, разширение .myi, разширение myi
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI файлов формат
linktitle: MYI
description: "Научете за файловия формат MYI и API, които могат да създават и отварят MYI файлове."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Какво е MYI файл? ##

MYI е известен също като MySQL MyISAM Index файл. Използва се за съхраняване на индекси за таблицата MyISAM от MySQL. Индексът на MySQL базата данни определя структурата на таблицата и съдържа контролния механизъм за проверка на целостта на таблиците.

## MYI файлов формат ##

MYI файлът има две части, заглавката и ключовите стойности.

### MYI Header ###

Заглавката съдържа информация за опции, размери на файлове и ключове. Ключовете в MySQL се създават с команда като

```sql
CREATE [UNIQUE] INDEX.
```

Файловете, които четат и записват MYI файлове, са в директорията ./myisam. Има следните файлове:

- mi_open.c: Този файл съдържа рутинните процедури, които записват всеки раздел на заглавката.
- mi_create.c: Този файл съдържа рутинните процедури, които извикват mi_open.c рутинни процедури.
- myisamdef.h: Този файл има дефинициите на структурата.

Заглавката има следните секции:

- състояние: Състоянието се записва от mi_open.c, mi_state_info_write(). Тази структура се появява веднъж във файла.
- база: Базата е написана от mi_open.c, mi_base_info_write(). MI_BASE_INFO е съответната структура за базата в myisamdef.h. Тази структура се появява веднъж във файла.
- keydef: Keydef е написан от mi_open.c, mi_keydef_write(). MI_KEYDEF е съответната структура за keydef в myisamdef.h. Това е многократна структура, която се появява за всеки индекс.
- recinfo: recinfo се записва от mi_open.c, mi_recinfo_write(). MI_COLUMNDEF е съответната структура за recinfo в myisamdef.h. Това е многократна структура, която се появява веднъж за всяко поле, което се появява в ключ.

### Ключови стойности ###

Страниците в MySQL се наричат блокове. Ключовите стойности са в блокове. Един блок съдържа информация само от един индекс. Всеки ключ съдържа цялото съдържание на всички колони. Нормалната дължина на блока е 0x0400 (1024) байта. Указателят има номер с фиксиран размер (4 байта) за таблици с фиксиран ред, който съдържа пореден номер на ред. Ако ключът е нула, тогава байтът е 0x00. Нормалният блок е пълен поне 65% и обикновено е пълен 80%.

Файлът myisamdef.h съдържа следната информация, изразена в константи. Максималният брой ключове е 32 (MI_MAX_KEY), а максималният брой сегменти в един ключ е 16 (MI_MAX_KEY_SEG). Максималната дължина на ключа е 500 (MI_MAX_KEY_LENGTH). Максималната дължина на блока е 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Препратки ##

- [Файлът .MYI](https://dev.mysql.com/doc/internals/en/the-myi-file.html)
