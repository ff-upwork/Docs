{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "файл", "расширение", "формат", "3D", "Хронос Групп 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о файлах GLTF и API, которые могут создавать и открывать файлы GLTF.",
  "title" :"GLTF — формат файла передачи GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .GLTF вариант №

glTF (формат передачи GL) — это формат файла 3D, в котором информация о 3D-модели хранится в формате JSON. Использование JSON минимизирует как размер 3D-ресурсов, так и время выполнения, необходимое для распаковки и использования этих ресурсов. Он был адаптирован для эффективной передачи и загрузки 3D-сцен и моделей приложениями. glTF был разработан рабочей группой Khronos Group по 3D-форматам и также описывается его создателями как [JPEG](/ru/image/jpeg/) 3D.

Формат файла GLTF определяет расширяемый общий формат публикации для инструментов и сервисов 3D-контента, который оптимизирует рабочие процессы разработки и обеспечивает функциональное взаимодействие использования контента в отрасли. Цель создания формата файлов glTF состояла в том, чтобы определить расширяемый общий формат публикации для инструментов и сервисов 3D-контента, который должен упростить рабочие процессы разработки и обеспечить возможность функционального использования контента в отрасли. Это сводит к минимуму обработку во время выполнения приложениями, использующими WebGL и другие API.

## Краткая история файла GLTF

Первые спецификации для формата файла glTF 1.0 были объявлены в октябре 2015 года. Это стало серией усилий, начатых Khronos в марте 2012 года. Цель этих усилий состояла в том, чтобы оценить возможности, связанные с распространением WebGL. В результате первая демонстрация формата glTF, основанная на формате JSON, была представлена на встрече WebGl в 2012 году. Формат время от времени применялся несколькими компаниями, включая Cesium, 3D Tiles, Oculus, Microsoft, Archilogic и другие.

glTF 2.0 был опубликован 5 июня 2017 года на конференции Web3D 2017. После этого существует длинный список компаний, которые приняли формат файла glTF.

## Формат файла GLTF

Спецификации формата файла для glTF 2.0 доступны [онлайн] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) для справки, и с ними следует обращаться в любой реализации, связанной с чтением/записью, для поддержки формат файла glTF.

glTF определяет активы как файлы JSON с вспомогательными внешними данными. Он представляет 3D-модели с помощью:

* Полное описание сцены, содержащееся в файле .glTF в формате JSON, которое включает информацию об иерархии узлов, материалах, камерах, а также информацию о дескрипторах для сеток, анимаций и других конструкций.
* Двоичные файлы (.bin), содержащие данные геометрии и анимации, а также другие данные на основе буфера.
* Файлы изображений ([.jpg](/ru/image/jpeg/), [.png](/ru/image/png/)) для текстур

Любые внешние активы, такие как изображения, хранятся во внешних файлах, на которые ссылаются через URI. Эти URI хранятся вместе с контейнером GLB или встроены непосредственно в JSON с использованием URI данных. Каждый допустимый glTF должен указывать свою версию.

glTF был разработан для достижения небольшого размера файла, быстрой загрузки, полного представления трехмерной сцены и расширяемости. Эти уникальные цели дизайна являются основными причинами популярности формата файла glTF в 3D-области. Ниже приведены типы mime, поддерживаемые форматом файла glTF для различных типов файлов:

* В файлах .gltf используется модель/gltf+json
* .bin файлы используют application/octet-stream
* Файлы текстур используют официальный тип image/*, основанный на конкретном формате изображения. Для совместимости с современными веб-браузерами поддерживаются следующие форматы изображений: image/jpeg, image/png.

### Кодировка JSON

glTF накладывает следующие дополнительные ограничения на формат файла JSON.

Чтобы упростить реализацию на стороне клиента, glTF имеет дополнительные ограничения на формат и кодировку JSON.

1. JSON должен использовать кодировку UTF-8 без спецификации.
1. Все строки, определенные в этой спецификации (имена свойств, перечисления), используют только кодировку ASCII и должны быть записаны как обычный текст, например, «буфер» вместо `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Имена (ключи) внутри объектов JSON должны быть уникальными, т. е. не допускаются дубликаты ключей.

### URI

На буферы и ресурсы изображений ссылаются через URI. Следующие два типа URI должны поддерживаться клиентами.

**URI данных:** URI данных определены в RFC 2397 и используются glTF для встраивания ресурсов в JSON.

**Относительные пути URI:** или схема пути, как определено в RFC 3986, [раздел 4.2] (https://tools.ietf.org/html/rfc3986#section-4.2) — без схемы, полномочий или параметров. Зарезервированные символы должны быть закодированы в процентах в соответствии с RFC 3986, [раздел 2.2] (https://tools.ietf.org/html/rfc3986#section-2.2).

## Использованная литература ##

* [Спецификации glTF 2.0 — Khronos] (https://github.com/KhronosGroup/glTF)
* [Формат файла glTF — по Википедии] (https://en.wikipedia.org/wiki/GlTF)
