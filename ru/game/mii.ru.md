{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла MGX для повтора расширения Age of Empires 2 и API, которые могут создавать и открывать файлы MGX.",
  "title" :"Файл MII — формат файла виртуального аватара Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## .MII вариант №

Файл MII — это формат файла виртуального аватара, используемый для хранения виртуальных аватаров на игровой консоли Nintendo Wii. Эти файлы содержат такую информацию, как внешний вид, движения и анимация аватара. Их можно использовать в играх, приложениях для социальных сетей и другом программном обеспечении на Wii. Файл MII также содержит другие характеристики аватара, такие как пол, цвет волос, цвет кожи, черты лица и тип глаз.

Вы можете открыть файл MII с помощью [Редактора моего аватара](https://rc24.xyz/goodies/mii/).

## Формат файла MII

Формат файла MII подробно описан на [Wii Brew](https://wiibrew.org/wiki/Mii_data). Строки в файле MII хранятся в формате Unicode (UTF-16), с прямым порядком байтов.

### Блок МИ

Данные файла MII хранятся на Wiimote в двух блоках. Каждый блок имеет длину 750 байт с 2 байтами CRC, что в сумме дает 752 байта. Каждый блок начинается с 4-байтового значения («RNCD»), которое кажется магическим числом для формата файла MII.

## Как создать файлы MII?

Есть несколько разных способов создания аватаров для Nintendo Wii:

1. «Использование встроенного канала Mii на Wii». Этот канал позволяет создавать собственные аватары с использованием различных инструментов, включая черты лица, форму тела и одежду. Создав свой аватар, вы можете сохранить его в виде файла Mii и использовать в играх и других программах на Wii.

1. «Использование приложения Mii Maker на Nintendo 3DS». Приложение Mii Maker позволяет создавать собственные аватары с помощью сенсорного экрана и камеры на Nintendo 3DS. После того, как вы создали свой аватар, вы можете сохранить его как файл Mii и перенести на Wii через беспроводное соединение.

1. «Использование стороннего программного обеспечения». Некоторые разработчики создали программное обеспечение, позволяющее создавать собственные аватары для Wii. Это программное обеспечение обычно предназначено для использования на компьютере и может потребовать дополнительных действий для переноса аватара на вашу Wii.

1. «Использование готовых аватаров»: некоторые игры и другое программное обеспечение для Wii могут поставляться с готовыми аватарами, которые вы можете использовать.

Во всех случаях вам необходимо иметь учетную запись Nintendo, чтобы создать и сохранить свой аватар на Wii.

## использованная литература

* [Мой редактор аватаров](https://rc24.xyz/goodies/mii/)
* [Wii Brew](https://wiibrew.org/wiki/Mii_data)
