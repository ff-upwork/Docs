{
  "date" : "2021-10-20",
  "keywords" :[ "bns файл", "bns файлов формат", "какво е bns файл", "файл", "bns пример", "разширение на файла на скрипта за бонус карта на портала", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете повече за BNS файловия формат на ortal Bonus Map Script и API, които могат да създават и отварят BNS файлове.",
  "title" :"BNS – Скрипт файл с бонус карта на портала",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Какво е BNS файл?

Файл с разширение .bns е файл със скрипт на игра, създаден с игра за решаване на пъзели Portal Map, разработена от Valve. Той съдържа текстов скрипт за дефиниране на информация за карта на портал, която се съхранява като .bsp файл. BNS файловете се използват като препратка към този действителен файл с карта и съдържа списък с предизвикателства, които трябва да бъдат изпълнени. В допълнение, той съдържа име на картата, коментари за картата и препратки към файлове с миниатюрни изображения. BNS файл може да бъде отворен във всеки текстов редактор като Notepad++, textEdit и Notepad.

## BNS файлов формат

BNS файловете се записват като обикновени текстови файлове, които могат да се четат от хора. Те могат да се отварят в текстови редактори и също така да се редактират. Те обаче трябва да бъдат внимателно редактирани, за да се избегнат грешки в скрипта.

## Пример за файлов формат на BNS

BNS файл може да изглежда по следния начин, когато се отвори в текстов редактор като Notepad++.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## Части от BNS файл

В горния пример,

* `#Bonus_Map_Challenges` - Представлява името на картата.
* `map` - Представлява името на картата, която да бъде поставена в папката с карти на играта
* `chapter` - Представлява главата, към която принадлежи картата. Всички файлове с глави се намират във VPK файла чрез добавяне на името на картата във формат `map your_map_name`
* `Изображение` - Съдържа миниатюрата на картата и се съхранява в основния път steam\steamapps\common\portal\portal\materials\VGUI.
* `Коментар` - Описателен текст за създадената карта.

## Препратки

* [Скрипт за предизвикателство на портала](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

