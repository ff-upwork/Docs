{
  "date" : "2021-09-08", 
  "keywords" :[ "LUA", "файл", "расширение", "формат файла", "мультипарадигма", "Руководство по программированию", "пример LUA", "Luа 5", "Luа VM", "Luа версия", " Luа байт-код", "Lu виртуальная машина", "Luа программы", "Lu файл" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LUA — файл языка программирования",
  "description":"Узнайте о формате файлов LUA и API, которые могут создавать и открывать файлы LUA.",
  "linktitle" : "LUA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-08"
}

## .LUA вариант №

Файл с расширением .lua принадлежит языку программирования **Luа**. Luа — это легкий, высокоуровневый, мультипарадигменный язык программирования, разработанный в первую очередь для встроенного использования в приложениях. Он кроссплатформенный, так как написан интерпретатор скомпилированного байт-кода, а у Luа есть относительно простой [C](/ru/programming/c/) АРI для встраивания его в приложения.

Первоначально Lua был разработан в 1993 году как язык для расширения приложений программного обеспечения для удовлетворения растущего спроса на настройку в то время. Он предоставлял базовые возможности большинства процедурных языков программирования, но не включал более сложные или предметно-ориентированные функции:

* Включены механизмы расширения языка
* Разрешение программистам реализовывать такие функции


## Краткая история ##

Luа был создан в 1993 году Роберто Иерусалимским, Луисом Энрике де Фигейредо и Вальдемаром Селесом, членами группы компьютерных графических технологий, также известной как Teсgraf, в Университете Ронтификал Католис в Рио-де-Жанейрсил.

С 1977 по 1992 год в Бразилии существовала политика сильных торговых барьеров, называемая рыночным резервом для компьютерного оборудования и программного обеспечения. В такой атмосфере клиенты Teсgraf не могли ни политически, ни финансово позволить себе покупать специализированное программное обеспечение за границей. Эти причины побудили Teсgraf реализовать базовые инструменты, которые ей были нужны, с нуля. Предшественниками Luа были языки описания/конфигурации данных SOL (Simple Object Language) и DEL (Dat Entry Language).


## Техническая спецификация ##

Lua обычно называют «мультипарадигмальным» языком, предоставляющим небольшой набор общих функций, которые можно расширить для решения различных типов задач. Lua не содержит явного запроса на наследование, но позволяет реализовать его с помощью метатаблиц. Точно так же Lua позволяет программистам реализовывать имена, классы и другие связанные функции, используя его единственную табличную реализацию:

* Первоклассные функции позволяют использовать многие приемы функционального программирования
* Полная лексическая сортировка позволяет скрывать детализированную информацию для обеспечения соблюдения принципа наименьших привилегий

В целом, Lua стремится предоставлять простые, гибкие мета-функции, которые можно расширять по мере необходимости, а не предоставлять набор функций, специфичный для одной парадигмы программирования. В результате базовый язык является легким, так как интерпретатор полной ссылки занимает всего около 247 КБ и легко адаптируется к широкому диапазону приложений.

Язык с динамической типизацией, предназначенный для использования в качестве языка расширений или языка сценариев, Lua достаточно удобен, чтобы соответствовать различным хост-платформам. Он поддерживает только небольшое количество атомарных структур данных, таких как логические значения, числа (по умолчанию с плавающей запятой двойной точности и 64-битные целые числа) и строки.

Типичные структуры данных, такие как массивы, наборы, списки и записи, могут быть представлены с помощью единственной родной структуры данных Luа, таблицы, которая по существу является гетерогенным ассоциативным массивом.

Поскольку Lua задумывался как универсальный язык встраиваемых расширений, разработчики этого языка сосредоточились на улучшении его скорости, переносимости, расширяемости и простоты использования при разработке. Luа-программы не интерпретируются непосредственно из текстового Luа-файла, а компилируются в байт-код, который затем запускается на виртуальной машине Luа.

Процесс компиляции, как правило, невидим для пользователя и выполняется во время выполнения, особенно при использовании JIT-компилятора, но его можно выполнять и в автономном режиме, чтобы повысить производительность загрузки или уменьшить объем памяти, загружаемой в среде хоста. компилятор.

Байт-код Lu также может быть сгенерирован и выполнен изнутри Luа, используя функцию дампа из библиотеки строк и функции load/loadstring/loadfile. Luа версии 5.3.4 реализован примерно в 24 000 строк кода на С.

Как и большинство СRU, и в отличие от большинства виртуальных машин, основанных на стеке, виртуальная машина Luа основана на регистрах и, следовательно, более похожа на реальное аппаратное обеспечение. Архитектура реестра позволяет избежать чрезмерной сортировки значений и сокращает общее количество инструкций на функцию. Виртуальная машина Luа 5 является одной из первых чистых виртуальных машин на основе регистров, получивших широкое распространение.

Этот язык реализует небольшой набор расширенных функций, таких как первоклассные функции, сборка мусора, замыкания, правильные вызовы хвоста, автоматическое преобразование между строковыми и числовыми значениями во время выполнения, сопрограммы (сопрограммирование многозадачности).


## Пример формата файла LUA ##

### Синтаксис ###

```
print("Hello, World!")

--or

print 'Hello, World!'
```

### Функции ###

```
do
  local oldprint = print
  -- Store current print function as oldprint
  function print(s)
    oldprint(s == "foo" and "bar" or s)
  end
end
```

```
function addto(x)
  -- Return a new function that adds x to the argument
  return function(y)
    return x + y
  end
end
```

### Поток управления ###

```
while condition do
  --statements
end

repeat
  --statements
until condition

for i = first, last, delta do
  --statements
  --example: print(i)
end
```

```
for key, value in pairs(_G) do
  print(key, value)
end
```

```
local grid = {
  { 11, 12, 13 },
  { 21, 22, 23 },
  { 31, 32, 33 }
}

for y, row in ipairs(grid) do
  for x, value in ipairs(row) do
    print(x, y, value)
  end
end
```
	


### Таблицы ###

```
ExampleTable =
{
  {1, 2, 3, 4},
  {5, 6, 7, 8}
}
print(ExampleTable[1][3]) -- Prints "3"
print(ExampleTable[2][4]) -- Prints "8"
```

### Метатаблицы ###

```
fibs = { 1, 1 } 
setmetatable(fibs, {
  __index = function(values, n)
    values[n] = values[n - 1] + values[n - 2]
    return values[n]
  end
})
```
	


### Наследование ###

```
local Vector = {}
Vector.__index = Vector

function Vector:new(x, y, z)
	return setmetatable({x = x, y = y, z = z}, self)
end

function Vector:magnitude()
	return math.sqrt(self.x^2 + self.y^2 + self.z^2)
end

local VectorMult = {}
VectorMult.__index = VectorMult
setmetatable(VectorMult, Vector)

function VectorMult:multiply(value) 
  self.x = self.x * value
  self.y = self.y * value
  self.z = self.z * value
  return self
end

local vec = VectorMult:new(0, 1, 0)
print(vec:magnitude())
print(vec.y)
vec:multiply(2)
print(vec.y)  
```

## Ссылка ##

* [LUA - из Википедии](https://en.wikipedia.org/wiki/Lua_(programming_language))



