{
  "date" : "2019-11-25",
  "keywords" :[ "файл jpeg", "формат файла jpeg", "что такое файл jpeg", "файл", "пример jpeg", "расширение файла jpeg", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG — формат файла изображения",
  "description":"Узнайте о формате файла JPEG и API-интерфейсах, которые могут создавать и открывать файлы JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## .JPEG вариант № ##

JPEG — это тип формата изображения, который сохраняется с использованием метода сжатия с потерями. Выходное изображение в результате сжатия представляет собой компромисс между размером хранилища и качеством изображения. Пользователи могут настроить уровень сжатия для достижения желаемого уровня качества и в то же время уменьшить размер хранилища. Качество изображения незначительно ухудшается, если к изображению применяется сжатие 10:1. Чем выше значение сжатия, тем выше ухудшение качества изображения.

## Спецификации формата файла ##

Формат файла изображения JPEG был стандартизирован Объединенной группой экспертов по фотографии, отсюда и название JPEG. Формат был выбран для хранения и передачи фотографических изображений в Интернете. Почти все операционные системы теперь имеют средства просмотра, поддерживающие визуализацию изображений JPEG, которые также часто хранятся с расширением JPG. Даже веб-браузеры поддерживают визуализацию изображений JPEG. Прежде чем перейти к спецификациям формата файла JPEG, необходимо упомянуть общий процесс, связанный с созданием JPEG.

### Шаги сжатия JPEG ###

**Преобразование:** цветные изображения преобразуются из RGB в изображение яркости/цветности (глаз чувствителен к яркости, а не к цветности, так что часть цветности может потерять много данных и, следовательно, может быть сильно сжата.

**Понижающая выборка:** Понижающая выборка выполняется для цветного компонента, а не для яркостной составляющей. Понижающая выборка выполняется в соотношении 2:1 по горизонтали и 1:1 по вертикали (2 ч 1 В). Таким образом, изображение уменьшается в размере, так как компонент 'y' не затрагивается, нет заметной потери качества изображения.

** Организация в группы: ** Пиксели каждого цветового компонента организованы в группы 8 × 2 пикселей, называемые «единицами данных», если количество строк или столбцов не кратно 8, нижняя строка и крайний правый столбец дублируются.

**Дискретное косинусное преобразование.** Затем к каждой единице данных применяется дискретное косинусное преобразование (DCT) для создания карты преобразованных компонентов размером 8×8. DCT приводит к некоторой потере информации из-за ограниченной точности компьютерной арифметики. Это означает, что даже без карты будет некоторая потеря качества изображения, но обычно она невелика.

**Квантование:** Каждый из 64 преобразованных компонентов в единице данных делится на отдельное число, называемое его «Коэффициентом квантования (КК)», а затем округляется до целого числа. Здесь информация теряется безвозвратно, большой контроль качества приводит к большим потерям. В целом, большинство реализаций JPEG позволяют использовать таблицы контроля качества, рекомендованные стандартом JPEG.

**Кодирование:** 64 квантованных преобразованных коэффициента (которые теперь являются целыми числами) каждого блока данных кодируются с использованием комбинации RLE и кодирования Хаффмана.

**Добавление заголовка:** Последний шаг добавляет заголовок и все используемые параметры JPEG и выводит результат.

Декодер JPEG использует шаги в обратном порядке для создания исходного изображения из сжатого.

### Структура файла ###

Изображение JPEG представлено в виде последовательности сегментов, где каждый сегмент начинается с маркера. Каждый маркер начинается с байта 0xFF, за которым следует флаг маркера, представляющий тип маркера. Полезная нагрузка, за которой следует маркер, зависит от типа маркера. Общие типы маркеров JPEG перечислены ниже:

|Короткое имя|Байты|Полезная нагрузка|Имя|Комментарии
---|---|---|---|---|
|SOI|0xFF, 0xD8|нет|Начало изображения|
|S0F0|0xFF, 0xC0|переменный размер|Начало кадра|
|S0F2|0xFF, 0xC2|переменный размер|Начало кадра|
|DHT|0xFF, 0xC4|переменный размер|Определить таблицы Хаффмана|
|DQT|0xFF, 0xDB|переменный размер|Определить таблицу(ы) квантования|
|DRI|0xFF, 0xDD|4 байта|Определить интервал перезапуска|
|SOS|0xFF, 0xDA|переменный размер|Начало сканирования|
|RSTn|0xFF, 0xD//n//(/ru//n//#0..7)|нет|Перезагрузка|
|APPn|0xFF, 0xE//n//|размер переменной|Зависит от приложения|
|COM|0xFF, 0xFE|переменный размер|Комментарий|
|EOI|0xFF, 0xD9|нет|Конец изображения|

В данных с энтропийным кодированием после любого байта 0xFF кодировщик вставляет байт 0x00 перед следующим байтом, чтобы не было маркера там, где он не предназначен, что предотвращает ошибки кадрирования. Декодеры должны пропустить этот байт 0x00. Этот метод, называемый [заполнение байтами] (https://en.wikipedia.org/wiki/Byte_stuffing) (см. раздел F.1.2.3 спецификации JPEG), применяется только к данным с энтропийным кодированием, а не к данным полезной нагрузки маркера. . Обратите внимание, однако, что данные с энтропийным кодированием имеют несколько собственных маркеров; в частности, маркеры сброса (от 0xD0 до 0xD7), которые используются для изоляции независимых фрагментов данных с энтропийным кодированием, чтобы обеспечить параллельное декодирование, и кодировщики могут свободно вставлять эти маркеры сброса через равные промежутки времени (хотя не все кодеры делают это).
