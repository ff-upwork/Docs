{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "файл", "расширение", "формат", "что такое файл amr", "музыка", "формат файла amr", "файл amr", "преобразовать файл amr в mp3", "воспроизвести файл amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла AMR и API-интерфейсах, которые могут создавать, конвертировать и открывать файлы AMR.",
  "title" :"AMR — файл адаптивного многоскоростного кодека",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## .AMR вариант №
Файл с расширением .amr представляет собой формат аудиоданных, соответствующий аудиокодеку **Adaptive Multi-Rate**; состоит из многоскоростного узкополосного речевого кодека, который кодирует узкополосные сигналы со скоростью передачи 4,75–12,2 кбит/с с речью междугородного качества, начиная с 7,4 кбит/с; использует адаптацию канала для выбора одной из восьми различных скоростей передачи данных.

## Формат файла AMR
Формат файла AMR использует множество методов кодирования, алгоритм ACELP (алгебраическое линейное предсказание с возбуждением кода) является одним из лучших методов; предназначен для более эффективного сжатия человеческого голоса. AMR был установлен 3GPP в качестве стандартного голосового или речевого кодека в 1999 году. Формат файла AMR также используется для хранения разговорного звука с помощью аудиокодека **Adaptive Multi-Rate**, который используется многими смартфонами для хранения записанных данных. речи.

### Структура формата файла
AMR (Adaptive Multi-Rate) — это аудиоформат; широко используется в различных мобильных приложениях и устройствах, обычно в аудиоплеерах/рекордерах или в приложениях типа VoIP. УПП можно дополнительно классифицировать как:

1. AMR-NB (узкополосный)
2. AMR-WB (широкополосный)

Обычно AMR относится к AMR-NB. Формат файла AMR имеет следующую структуру:

Каждый файл AMR содержит 6-байтовый заголовок, который распознает файл как аудио AMR. Этот заголовок всегда имеет значение:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Обычно это одинаково для всех файлов AMR-NB. Если заголовок соответствует стандарту, вполне вероятно, что файл поврежден и не должен использоваться. файл AMR состоит из целого числа упакованных аудиокадров. Каждый из этих кадров составляет 20 мс аудио. Каждый кадр может быть закодирован с использованием любого из допустимых режимов AMR-NB (0-7, 8 SID в режиме DTX). Поскольку кадры могут быть закодированы с разной скоростью передачи данных, этот типичный метод называется Adaptive Multi-Rate (AMR).
#### Режимы AMR
Ниже приведены различные режимы AMR и соответствующие им битрейты:

|РЕЖИМ| СКОРОСТЬ БИТ|
---|---|
|0| AMR 4.75 — кодирует со скоростью 4,75 кбит/с |
|1 | AMR 5.15 — кодирует со скоростью 5,15 кбит/с |
|2 | AMR 5.9 — кодирует со скоростью 5,9 кбит/с |
|3 | AMR 6.7 — кодирует со скоростью 6,7 кбит/с |
|4 | AMR 7.4 — кодирует со скоростью 7,4 кбит/с |
|5 | AMR 7.95 — кодирует со скоростью 7,95 кбит/с |
|6 | AMR 10.2 — кодирует со скоростью 10,2 кбит/с |
|7 | AMR 12.2 — кодирует со скоростью 12,2 кбит/с |

Размер кадра режимов AMR в байтах (включая байт заголовка) указан ниже:

|CMR |РЕЖИМ |РАЗМЕР КАДРА(в байтах)|
---|---|---|
|0 |4,75 AMR |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |7,95 AMR |21|

## Использованная литература ##

* [Адаптивный многоскоростной аудиокодек — Википедия] (https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Формат полезной нагрузки RTP и формат хранения файлов для аудиокодеков AMR и AMR-WB] (https://tools.ietf.org/html/rfc4867#page-35)
