{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Метафайл компьютерной графики", "Файл", "Расширение", "Формат файла", "Векторная графика", "Дескриптор метафайла"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла CGM",
  "description":"Узнайте о формате файла CGM и API-интерфейсах, которые могут создавать и открывать файлы CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## .CGM вариант № ##

Метафайл компьютерной графики (CGM) — это бесплатный, независимый от платформы, международный стандартный формат метафайла для хранения и обмена векторной графикой (2D), растровой графикой и текстом. CGM использует объектно-ориентированный подход и множество функциональных возможностей для создания изображений. CGM использует эти объектно-ориентированные характеристики для преобразования графических элементов в изображение. Метафайл содержит необходимую информацию, которая определяет другие файлы. В CGM текстовый исходный файл содержит все графические элементы, которые впоследствии могут быть скомпилированы в двоичный файл. По сути, CGM — это способ облегчить обмен 2D-графическими данными, не зависящий от какой-либо конкретной платформы или устройства.

Формат CGM предоставляет различные элементы для выполнения функций и обозначения объектов для корректировки геометрических примитивов и графической информации. Хотя CGM был вытеснен другими форматами для отображения графики на веб-страницах, поскольку он не очень хорошо поддерживается веб-страницами, он по-прежнему очень популярен среди промышленных, авиационных и других технических приложений. Хотя Консорциум World Wide Web разработал WebCGM, альтернативный подход к использованию CGM в Интернете. Первичная реализация CGM была иллюстрацией последовательности основных операций системы графического ядра (GKS). Он не получил широкого распространения в профессиональном дизайне, но в значительной степени вытеснил другие форматы, такие как DXF и SVG.

## История ##

CGM стал международным стандартом в 1987 году (ISO 8632-1987), а также был принят BSI в качестве национального стандарта в Великобритании и ANSI в США. После ряда поправок в 1991 г. в 1992 г. был выпущен пересмотренный стандарт CGM (ISO 8632:1992). В 2001 году консорциум World Wide Web разработал WebCGM с расширенными возможностями для использования с веб-страницами. В 2007 г. была выпущена вторая версия WebCGM, а в 2010 г. — третья версия с расширенными возможностями.

## Формат файла CGM ##

Метафайлы компьютерной графики в основном представляют собой базу данных для графической информации и предоставляют средства для захвата, хранения и передачи графических данных. Следовательно, должен быть графический компонент системы для создания базы данных одновременно с выполнением приложения в формате метафайла. В большинстве случаев этим компонентом является генератор метафайлов. Наряду с этим необходим еще один компонент, который может извлекать, интерпретировать и отображать графические данные в метафайле. Эта потребность удовлетворяется наличием интерпретатора метафайлов. На следующем рисунке представлена графическая рабочая среда метафайла.

Связь CGM с другими компонентами типичной графической системы показана на рисунке выше. Из рисунка также видно, что функциональность метафайла не зависит от конечного вывода устройства.

Как правило, существует две категории метафайлов: **захват раздела** и **захват изображения**. Основной функцией метафайла захвата изображения является захват аппаратно-независимых множественных определений изображений. В то время как метафайлы захвата сеанса используют системный интерфейс для захвата выходного диалога в графической системе. CGM относится к категории метафайлов захвата статических изображений. CGM обеспечивает хорошо организованное расположение компонентов с двухуровневой структурой.

1. Дескриптор метафайла
1. Пул логически независимых изображений

Каждое изображение представляет собой набор дескрипторов изображения и тело изображения, включающее определение изображения. Дескриптор метафайла определяет описательную информацию, которая в равной степени относится ко всем изображениям этого метафайла. Эта информация помогает интерпретатору правильно анализировать метафайл и распознавать ресурсы, необходимые для правильного рендеринга изображения. Хотя дескриптор изображения также содержит описательную информацию, он может распознавать только изображение, в котором находится дескриптор. В этом формате файла каждое определение изображения является автономным и логически независимым. Они не зависят от всех других определений изображений в файле. Сразу после интерпретации мета-дескриптора изображения могут быть доступны и интерпретированы случайным образом. Изменение состояния предыдущих изображений не влияет на их последователей. Эта независимость от изображения является еще одной важной особенностью CGM. CGM состоит из пространства координат, которое представляет собой двумерные декартовы координаты, называемые координатами виртуального устройства, и может быть представлено числом или точностью, представляющей диапазон и степень детализации. CGM определяет как прямой выбор цветов, так и выбор на основе индекса. В первом случае спецификатор цвета состоит из тройки RGB, а позже спецификатор цвета указывает индекс в таблице цветов.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.