{
  "date" : "2019-10-11",
  "keywords" :[ "ott fájl", "ott fájlformátum", "mi az ott fájl", "fájl", "ott példa", "ott fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - OpenDocument sablonfájl",
  "description":"További információ az OTT fájlformátumról és az API-król, amelyek OTT-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az OTT fájl?

Az OTT kiterjesztésű fájlok az OASIS OpenDocument szabvány formátumának megfelelő alkalmazások által generált sablondokumentumok. Ezeket szövegszerkesztő alkalmazásokkal, például ingyenes OpenOffice Writer-rel hozzák létre, és olyan beállításokat tartalmazhatnak, amelyek segítségével új dokumentumokat lehet létrehozni ezekből a sablonfájlokból. Ezek a beállítások közé tartoznak az oldalmargók, szegélyek, fejlécek, láblécek és egyéb oldalbeállítások. Az ilyen sablonokat olyan hivatalos dokumentumokban használják, mint a vállalati levélpapírok és szabványosított űrlapok.

## Rövid története ##

Az ODP fájlformátum specifikációi az ODF specifikációként kifejlesztett szabványon alapulnak. Ezek a specifikációk az elmúlt időszakban az OASIS által kifejlesztett és közzétett három változat formájában fejlődtek, az alábbiak szerint:

**2005:** Az 1.0-s verzió 2005 májusában jelent meg

**2007:** Az 1.1-es verzió 2007 februárjában jelent meg

**2011:** Az 1.2-es verzió 2011 szeptemberében jelent meg

Elég apró változások történtek az ODF 1.0-ról az 1.1-es verziókra való áttéréskor. Az [ODF 1.2-es verzió](https://www.oasis-open.org/standards#opendocumentv1.2) az ODF-specifikációk legújabb verziója, és a fejlesztőknek konzultálniuk kell vele az ODS-olvasáshoz/íráshoz kapcsolódó alkalmazások fejlesztésekor.

## A fájlformátum specifikációi

Az OpenDocument formátum támogatja a dokumentumok egyetlen XML-dokumentumként való megjelenítését, valamint több aldokumentum gyűjteményét egy csomagon belül [ZIP](/hu/compression/zip/) archívumként. A ZIP archívumból származó fájlok mindegyike a teljes dokumentum egy részét tárolja. Minden aldokumentum a dokumentum egy bizonyos aspektusát tárolja. Például egy aldokumentum tartalmazza a stílusinformációkat, egy másik pedig a dokumentum tartalmát. Egy tipikus ODF dokumentum a következő összetevőket tartalmazza:

* content.xml – Dokumentumtartalom és a tartalomban használt automatikus stílusok.
* styles.xml – A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
* meta.xml – A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
* settings.xml – Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

Ezeken kívül a csomagban sok más aldokumentum is lehet, mint a dokumentum bélyegképe, képek stb. A dokumentumfájlok az ODF fájlok azon részhalmaza, ahol a tartalom (lapok) a //content.xml// aldokumentumban tárolódnak.

## Referenciák ##

* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

