{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "розширення", "файл", "формат", "система", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet File",
  "description":"Дізнайтеся про формат файлу CAB та API, які можуть створювати та відкривати файли CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Що таке файл CAB? ##

Файл із розширенням .cab належить до CAB-файлу Windows, який відноситься до категорії системних файлів. Це файл, який зберігається у форматі архівного файлу у версіях Microsoft Windows, які підтримують алгоритми стиснених даних, наприклад [LZX](/uk/compression/lzx/), Quantum і [ZIP](/uk/compression/zip/ ). Цей файл має життєво важливе значення, коли користувач або розробник хоче містити та ділитися даними та файлами встановлення програмного забезпечення. Функції стиснення даних без втрат і цифрова сертифікація, включені в ці файли, роблять цей файл ідеальним для зберігання та спільного використання таких файлів. Він підтримує різні інсталятори Microsoft, такі як Device Installer, SetUp API та AdvPak.

## Коротка історія ##

Файл CAB – це тип файлу стиснення даних, розроблений Microsoft. Спочатку він називався «Diamond», але потім його стали називати файлом CAB, скорочення від слова «Cabinet».

## Технічна специфікація ##

CAB-файл зазвичай може містити максимум 65535 папок, які, у свою чергу, можуть містити максимум 65536 файлів кожна. Механізм зберігання файлів CAB економить час і місце, оскільки він зберігає кожну папку як стиснутий блок замість того, щоб стискати та зберігати кожен файл окремо. Порожні папки не можна зберігати в архівних папках CAB. Файл CAB спочатку був розроблений Microsoft і використовується в різних інсталяторах, таких як InstallShield, у дещо іншому форматі. CAB-файли зазвичай пов’язані з програмами, що саморозпаковуються. Файли Microsoft CAB легко впізнати завдяки унікальному маркеру, який допомагає визначити формат. Унікальним маркером для всіх CAB-файлів Microsoft є префікс із чотирьох слів, MSCF. Побачивши цей код, користувач може легко відрізнити CAB-файл Microsoft від інших файлів і відповідно використовувати його в компресорах або версіях. Файли можна стиснути з додатковими даними про інсталяцію програмного забезпечення або поточні дані можна розпакувати за допомогою відповідного програмного забезпечення.


## Приклад CAB ##

Наступний приклад ілюструє зв’язок між файлами та папками у файловій структурі CAB:

{{< figure src="../cab.png" alt="Формат файлу CAB" >}}

## Посилання ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))