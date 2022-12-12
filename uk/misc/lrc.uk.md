{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу LRC - що таке файл LRC?",
  "description":"Дізнайтеся про файл LRC Lyric та API, які можуть створювати та відкривати файли LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Що таке файл LRC?

Файл LRC — це текстовий файл із текстом пісень, який містить текст аудіопісні. Коли аудіопісня відтворюється за допомогою музичного плеєра або програмного забезпечення аудіопрогравача на комп’ютері, файл LRC зчитується паралельно та відображається з часом. Файли LRC містять контрольні точки для відображення тексту під час відтворення пісні. Загалом, файли LRC мають таку саму назву, що й відповідний аудіофайл, наприклад audio.mp3 та audio.lrc. Файли LRC схожі на файли субтитрів, наприклад [SRT](/uk/video/srt/).

## Формат файлу LRC - Додаткова інформація

Файли формату лірики LRC зберігаються як звичайні текстові файли, їх можна відкривати та редагувати в текстовому файлі. Вміст файлу LRC містить інформацію про колір для відображення тексту пісень.

## Формати LRC

Існує кілька форматів файлів LRC, які були розроблені з часом. Ці

### Простий формат LRC

Теги часу рядка мають формат [mm:ss.xx], де mm — хвилини, ss — секунди, xx — соті частки секунди.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Розширений простий формат

Він включає в себе можливість змінювати та вказувати стать тексту пісень за допомогою M: чоловічий, F: жіночий, D: дует.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Розширений формат LRC

Розширений формат LRC є розширеною версією простого формату LRC. Він додає тег часу Word у форматі<mm:ss.xx> в кінці попереднього слова.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Список літератури

* [Формат файлу пісень LRC – Вікіпедія](https://en.wikipedia.org/wiki/LRC_(file_format))
