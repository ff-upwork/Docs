{
  "date" : "2019-12-09",
  "keywords" :[ "файл 3mf", "формат файла 3mf", "что такое файл 3mf", "файл", "пример 3mf", "расширение файла 3mf", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3МФ",
  "description":"Узнайте о формате файлов 3MF и API, которые могут открывать и создавать файлы 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## .3MF вариант №

3MF, формат 3D-производства, используется приложениями для рендеринга 3D-моделей объектов для множества других приложений, платформ, сервисов и принтеров. Он был создан, чтобы избежать ограничений и проблем в других форматах 3D-файлов, таких как [STL](/ru/cad/stl/), для работы с последними версиями 3D-принтеров. 3MF — относительно новый формат файлов, разработанный и опубликованный консорциумом 3MF. Он достаточно богат, чтобы полностью описать модель, сохраняя внутреннюю информацию, цвет и другие характеристики, что делает его расширяемым для поддержки новых инноваций в 3D-печати. Этот формат является расширяемым, может широко применяться и не имеет проблем, характерных для других широко используемых форматов файлов.

## Краткая история формата файлов 3MF

Существующие ограничения в доступных форматах файлов описания моделей, таких как STL и другие, вынуждают ведущие бренды собираться вместе и разрабатывать более расширяемый формат файлов для 3D-печати. Важным соображением было то, как приложения должны передавать данные модели на 3D-принтеры. Таким образом, был создан консорциум 3MF для поддержки нового формата 3D-файлов под названием 3MF с целью сделать его достаточно расширяемым для удовлетворения потребностей 3D-печати. В этот консорциум входили несколько компаний, включая Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP и другие. Microsoft предоставила свой незавершенный формат файла 3D в качестве отправной точки для совместной дальнейшей разработки спецификации консорциумом 3MF.

## Формат файла 3MF — дополнительная информация

3MF – это формат данных на основе XML — удобочитаемый сжатый XML, который включает в себя определения данных, связанных с трехмерным производством, в том числе сторонние возможности расширения для пользовательских данных. Формат файла 3MF был разработан с учетом ограничений и проблем, с которыми сталкиваются другие форматы файлов 3D. Это привело к формулировке формата файла 3MF:

* **Complete:** Содержит всю необходимую информацию о модели, материалах и свойствах в одном архиве.
* **Удобочитаемый:** использование общих структур, таких как OPC, [ZIP](/ru/compression/zip/) и XML, для упрощения разработки.
* **Просто:** Короткая и четкая спецификация, упрощающая разработку и ускоряющая проверку.
* **Расширяемость:** Использование пространств имен XML позволяет использовать как общедоступные, так и частные расширения при сохранении совместимости.
* **Однозначность:** Четкий язык и тесты на соответствие гарантируют, что файл всегда будет согласован как в цифровом, так и в физическом виде.
* **Бесплатно:** Доступ к спецификации 3MF и ее реализация всегда будут свободны от роялти, патентов и лицензий.

Спецификации формата файлов 3MF размещены на [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) для общего доступа и постоянного обновления. Текущая опубликованная версия — 1.2.3, которая описывает набор соглашений по использованию XML и других широко доступных технологий для описания содержимого и внешнего вида одной или нескольких 3D-моделей. Разработчики, которые хотят создавать системы для обработки файлов формата 3MF, могут обратиться к этим спецификациям для реализации.

## Спецификации формата файла 3MF

Формат файла 3MF использует спецификации Open Packaging в виде ZIP-архива для своей физической модели. Он включает в себя четко определенный набор частей и взаимосвязей, которые выполняют определенную цель в документе. Это также заставляет формат соответствовать функции пакета, включая цифровые подписи и эскизы.

### Документ 3MF — обзор

Типичный документ 3MF выглядит следующим образом:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Полезная нагрузка включает в себя полный набор деталей, необходимых для обработки части 3D-модели. Весь контент, который будет использоваться для изготовления объекта, описанного в полезной нагрузке 3D, ДОЛЖЕН содержаться в документе 3MF. Описание каждой части документа, а также ее статус в зависимости от необходимости или опции приведены в следующей таблице.


|**Имя**|**Описание**|**Источник отношений**|**Обязательный/необязательный**
--- | --- | --- | ---
|3D-модель|Содержит описание одного или нескольких 3D-объектов для производства.|Пакет|ОБЯЗАТЕЛЬНО
|Основные свойства|Часть OPC, которая содержит различные свойства документа.|Пакет|ДОПОЛНИТЕЛЬНО
|Происхождение цифровой подписи|Часть OPC, являющаяся корнем цифровых подписей в пакете.|Пакет|ДОПОЛНИТЕЛЬНО
|Цифровая подпись|Части OPC, каждая из которых содержит цифровую подпись.|Происхождение цифровой подписи|ДОПОЛНИТЕЛЬНО
|Сертификат цифровой подписи|Части OPC, содержащие сертификат цифровой подписи.|Цифровая подпись|ДОПОЛНИТЕЛЬНО
|PrintTicket|Предоставляет настройки, используемые при выводе 3D-объектов в детали 3D-модели.|3D-модель|ДОПОЛНИТЕЛЬНО
|Миниатюра|Содержит небольшое изображение в формате JPEG или PNG, представляющее 3D-объекты в пакете или пакет в целом.|Пакет|НЕОБЯЗАТЕЛЬНЫЙ
|3D-текстура|Содержит текстуру, используемую для применения цвета к 3D-объекту в части 3D-модели (доступно для расширений)|3D-модель|ДОПОЛНИТЕЛЬНО
|Пользовательские части|Части OPC, связанные с метаданными|Пакет|ДОПОЛНИТЕЛЬНО

[Части и отношения](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D-модели](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [ресурсы объектов](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Материальные ресурсы](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) и разделы [Возможности пакета](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) спецификаций. документ дает подробную информацию о документе 3MF.

## Использованная литература ##

* [Спецификации формата файла 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF — Википедия](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

