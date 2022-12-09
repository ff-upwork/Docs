---
date: 2019-10-11
keywords: prc, .prc, формат файла prc, как открыть файлы prc, расширение .prc, расширение prc
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файла PRC
linktitle: PRC
description: "Узнайте о формате файла PRC и API-интерфейсах, которые могут создавать и открывать файлы PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Форматы файлов PRC
Расширения «.prc» используются для формата файла Product Representation Compact 3D и формата файла электронной книги от MobiPocket.

## Что такое файл Product Representation Compact (PRC)?

PRC (Product Representation Compact) — это формат файла 3D, оптимизированный для хранения, загрузки и отображения 3D-данных, особенно поступающих из систем CAD (автоматизированного проектирования). Это последовательный двоичный файл, написанный переносимым способом. PRC можно использовать для встраивания 3D-данных в файл PDF. PRC поддерживает большинство основных конструкций САПР, таких как сборки и детали, деревья трехмерных объектов, точное геометрическое представление, триангулированное представление и разметку. PRC использует расширение .prc, а используемый тип интернет-носителя — *model/prc*.

PRC — это многоцелевой формат файла, который в зависимости от его использования может либо храниться с использованием обычного сжатия для непосредственного представления данных САПР, либо храниться с использованием высокой степени сжатия для уменьшения размера файла. Трехмерные данные, хранящиеся в формате PDF в формате PRC, совместимы с приложениями CAM и CAE.

### Спецификация формата файла Product Representation Compact (PRC)

Файл PRC имеет один основной раздел заголовка, за которым следует одна или несколько файловых структур, за которыми в конце следует один файл модели. Файловая структура имеет один заголовок, за которым следуют следующие разделы данных:

- **Globals**: он содержит указанные файловые структуры и цвета, стили линий и системы координат для каждого древовидного объекта файловой структуры.
- **Дерево**: содержит описание дерева элементов, таких как экземпляры продукта, определения деталей, элементы представления и разметка.
- **Тесселяция**: содержит все мозаичные (триангулированные) данные в конечных объектах дерева (элементы представления и разметки).
- **Геометрия**: содержит все точные данные геометрии и топологии листовых объектов дерева (элементов представления).
- **Дополнительная геометрия**: содержит сводные данные геометрии. Это позволяет частично загрузить файл без загрузки всей геометрии.

Ниже приведена структура типичного файла PRC.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Что такое файл электронной книги MobiPocket с расширением PRC
Формат файлов электронных книг, представленный французской компанией **Mobipocket**, также использует расширение «.prc». Первоначально Mobipocket запустил бесплатное приложение для нескольких интеллектуальных устройств, таких как планшеты, КПК и смартфоны. Расширение «.prc» на самом деле идентично .mobi, но используется, в частности, для КПК, которые поддерживают только расширения **.prc** или **.pdb**.

### Спецификации формата файла Mobipocket PRC
Формат файла MobiPocket PRC основан на стандарте Open eBook с использованием XHTML, а также может включать JavaScript и фреймы. Также доступна поддержка собственных SQL-запросов для использования со встроенными базами данных.

Mobipocket Reader имеет библиотеку домашних страниц. Читатели могут вставлять пустые страницы в любую часть книги и добавлять различные рисунки. Такими объектами, как аннотации, закладки, исправления, заметки и рисунки, можно управлять из одного места. Изображения конвертируются в формат GIF и имеют максимальный размер 64K, что достаточно для мобильных телефонов с маленькими экранами. Mobipocket Reader имеет электронные закладки и встроенный словарь.

Ридер имеет полноэкранный режим чтения и поддержку многих КПК, Коммуникаторов и Смартфонов. Продукты Mobipocket поддерживают большинство операционных систем Palm, Windows, Symbian, BlackBerry, но не Android. Читалка работает под Linux или Mac OS X с использованием WINE.

## использованная литература

- [КНР - Википедия](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Спецификация формата PRC] (https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Сравнение форматов электронных книг - По Википедии] (https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)
