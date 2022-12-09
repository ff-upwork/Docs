{
  "date" : "2021-06-09",
  "keywords" :[ "метка", "файл", "расширение", "формат", "что такое файл метки", "музыка", "формат файла метки", "спецификация формата файла метки", "лист метки", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла CUE и API-интерфейсах, которые могут создавать, конвертировать и открывать файлы CUE.",
  "title" :"CUE - Файл Cue Sheet",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## .CUE вариант №

Файл с расширением .cue, также известный как файл cue sheet, представляет собой файл метаданных, содержащий информацию о расположении дорожек на компакт-диске или DVD-диске. Они поддерживаются медиаплеерами и приложениями для создания оптических дисков. На основные аудиоданные, хранящиеся на компакт-диске, ссылается файл метки вместе со спецификациями длины дорожек, названиями дисков и исполнителями. Таким образом, если один аудиофайл содержит несколько дорожек, файл метки можно использовать для разделения аудио на несколько файлов или ссылки на разные дорожки.

## Формат файла CUE

Файлы CUE или Cue Sheet хранятся в текстовом формате, удобочитаемом для человека. Информация в cue-файле — это команды с одним или несколькими параметрами. Эти команды применяются либо ко всему файлу, либо к отдельной дорожке, в зависимости от конкретной команды и контекста. Руководство пользователя CDRWIN описывает спецификации синтаксиса и семантики Cue Sheet.

## Основные команды листа CUE

|Команда|Описание|
---|---|
|ФАЙЛ| Относится к файлу, содержащему данные и их формат, например [MP3](/ru/audio/mp3/), [WAV](/ru/audio/wav/) или обычный двоичный образ диска)|
|ТРЕК| Определяет информацию о контексте дорожки, такую как ее номер и тип или режим.|
|ИНДЕКС| Представляет позицию в виде индекса в ФАЙЛЕ. Формат: mm:ss:ff (минута-секунда-кадр).|
|PREGAP и POSTGAP|Это указывает на предварительный или последующий интервал дорожки, который не сохраняется ни в одном файле данных. Длина указывается в том же формате минуты-секунды-кадра, что и для ИНДЕКС.|

### Пример листа CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## использованная литература

* [Файл .cda - По Википедии] (https://en.wikipedia.org/wiki/.cda_file)
