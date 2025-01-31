{
  "date" : "2019-10-11",
  "keywords" :[ "файл gbr", "формат файла gbr", "что такое файл gbr", "файл", "пример gbr", "расширение файла gbr", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла GBR - формат файла Gerber для печатной платы",
  "description":"Узнайте о формате файла GBR и API-интерфейсах, которые могут создавать и открывать файлы GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .GBR вариант №

Файл с расширением .gbr представляет собой формат файла изображения Gerber для обмена проектными данными печатной платы (PCB). Он был разработан компанией Ucamco. Данные проектирования печатных плат являются основным компонентом, требуемым для обработки в производственной отрасли. Файл GRB содержит данные печатной платы, такие как медные слои, паяльная маска, легенда, а также данные сверления и трассировки. Его можно использовать для передачи данных, таких как характеристики изготовления печатных плат, включая толщину или отделку, в стандартном формате. Все системы проектирования печатных плат выводят файлы Gerber, которые могут обрабатываться системами изготовления печатных плат. Файлы GBR теперь стали стандартом де-факто для передачи данных проектирования печатных плат (PCB). Ucamco предоставила [бесплатную онлайн-программу просмотра](https://gerber-viewer.ucamco.com/) для открытия и просмотра форматов файлов GBR.

## Формат файла GBR

GBR — это удобочитаемый формат UTF-8, состоящий всего из 27 команд. Благодаря этому короткому списку команд и компактности GBR легко отлаживать. Gerber по своей сути является открытым векторным форматом для двумерных бинарных изображений. Метаинформация передается вместе с изображениями через атрибуты. Один файл GRB определяет одно изображение и не требует интерпретации каких-либо сопутствующих файлов или внешних параметров. Для одного изображения нужен только один файл. Он использует 7-битные символы ASCII для всех команд и имен, определенных в спецификации, которые можно распечатать. Это полностью охватывает полное создание изображения.

### Пример файла GBR

Ниже приведен пример файла Gerber, который создает круг диаметром 1,5 мм с центром в исходной точке. В каждой строке одна команда.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## использованная литература

* [Формат Gerber](https://www.ucamco.com/en/gerber)

