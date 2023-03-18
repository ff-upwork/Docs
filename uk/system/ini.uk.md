{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "розширення", "файл", "формат", "система", "ініціація", "розширення каталогу", "програми", "комп'ютер", "програма"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - формат початкового файлу",
  "description":"Дізнайтеся про формат файлу INI та API, які можуть створювати та відкривати файли INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Що таке файл INI? ##

INI-файл — це документ конфігурації повідомлення для комп’ютерних програм, який містить відкриті ключі для характеристик і розділів, які організовують атрибути в структурі та граматиці. Ці документи конфігурації формату системного файлу отримали свою назву від розширення каталогу INI операційної системи MS-DOS, що означає ініціацію. Це популяризувало цю форму налаштування програмного забезпечення. Багато програм в інших прикладних програмах використовують різноманітні доповнення до імен файлів, наприклад CONF і [CFG](/uk/system/cfg), хоча цей формат є неофіційним стандартом у багатьох ситуаціях налаштування.

## Коротка історія файлів INI##

Спочатку основною технікою конфігурації програм Windows був формат текстового файлу, який складався з рядків тексту з однією ключовою парою на рядок, розділених на розділи. У цьому форматі зберігалися драйвери пристроїв, шрифти та засоби запуску. Програми також зазвичай зберігали індивідуальні налаштування у файлах INI.
До Windows 3.1x цей формат підтримувався на 16-розрядних платформах Microsoft Windows. Починаючи з Windows 95, Microsoft почала заохочувати розробників використовувати для конфігурації реєстр Windows замість файлів INI.

## Файл INI – специфікації формату файлу

### Ключі/Властивості ###

Ключ/властивість є основним елементом файлу INI. Символ рівності (=) відокремлює назву та значення кожного ключа. Ліворуч від знака рівності відображається ім’я. Символ рівності та крапка з комою є дискретними літерами в системі Windows, тому їх не можна використовувати в ключі. У значенні можна використовувати будь-який символ.

```
name=value
```

### Розділи ###

Коментар розділу відображається в квадратних дужках ([]) у окремому рядку. Після визначення розділу всі ключі пов’язані з цим розділом. Розділи закінчуються на наступному позначенні розділу або в кінці документа; немає спеціального роздільника "кінець розділу". Розділи не можна складати в стопку; їх можна назвати лише один раз, і зв’язувати їх не потрібно.

```
[section]
a=a
b=b
```

### Зміна функцій ###

Формат файлу INI не має загальноприйнятого визначення. Багато комп’ютерних програм містять функції на додаток до вже згаданих. Наведений нижче список містить деякі загальні характеристики, які можуть бути або не включені в будь-яку окрему програму.

* Коментарі
* Екранування символів
* Повторювані імена


## Приклад INI ##

Зразок INI-файлу виглядає так:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Посилання ##

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)
