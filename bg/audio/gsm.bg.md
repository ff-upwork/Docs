{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "файл", "разширение", "формат", "аудио", "глобална система за мобилно аудио", "gsm разширение", "gsm файлове"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за GSM файловия формат и API, които могат да създават и отварят GSM файлове.",
  "title" :"GSM – Глобална система за мобилен аудио файлов формат",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Какво е GSM файл?

GSM е файлово разширение, което е свързано с Global System for Mobile Audio Format Files. Файлове, съдържащи GSM разширения, могат да се отварят на платформи Linux, Windows и Mac OS. GSM файловият формат принадлежи към категорията аудио файлове.

GSM файл е кодиран с кодек за компресиране на звук CBR (постоянен битрейт) със загуби. Честотата на дискретизация в GSM аудио файл е 8000 проби/секунда, докато скоростта на данни е около 13 kbps. Битрейтът в рамките на GSM файловете гарантира качество по време на запис на глас. Освен това GSM файловият формат е известен също като глобален стандартен формат, който се използва в мобилни телефони, а WAV файловете също могат лесно да бъдат кодирани с помощта на GSM файлов формат. Всички проблеми с GSM файл могат лесно да бъдат разрешени от самия потребител, без да се обръща към експерт.

Потребителите могат също да конвертират GSM файлове във формати [MP3](/bg/audio/mp3/) и [MP4](/bg/video/mp4/).

## Кратка история на GSM файловия формат

GSM е формат на аудио файл, създаден за интернет телефония в Европа. Той е разработен от Европейския институт за телекомуникационни стандарти (ETSI), за да се използва като 2G цифрова клетъчна мрежа, използвана в мобилни телефони и таблети. Днес се използва за съхраняване на записи на телефонни разговори и гласови съобщения.

## Спецификации на GSM файлов формат ##

GSM работят в структурирана мрежа, която се състои от следните секции:

- **Модулация** : Това е процес на трансформиране на входните данни във формат, който може лесно да се предава. Предадените данни се демодулират в приемащия край
- **Скорост на предаване**: GSM е цифрова система, която има над битова скорост от 270 kbps
- **Честотен обхват на връзката нагоре**: 933-960 MHz
- **Честотен обхват на връзката надолу**: 890 – 915 MHz
- **Разстояние между каналите**: Означава разстоянието между съседни бариери, което трябва да бъде около 200 kHz
- **Дуплексно разстояние**: Това е пространството между честотите на връзката нагоре и надолу, което трябва да бъде 80 MHz
- **Кодиране на речта**: GSM използва линейно предсказващо кодиране (LPC). LPC компресира битрейта. Когато аудио сигналът преминава през филтър и имитира гласовия тракт. GSM кодира реч при 13kbps

| Формат за аудио компресия | Алгоритъм | Процент | Преобразуване на побитова скорост | Латентност | CBR | VBR | Стерео | Многоканален |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Да | Не | Не | Не |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Да | Не | Не | Не |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Да | Не | Не | Не |

## Препратки ##

* [GSM – От Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

