{
  "date" : "2019-10-11",
  "keywords" :[ "file odt", "formato file odt", "cos'è un file odt", "file", "esempio odt", "estensione file odt", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - File di testo OpenDocument",
  "description":"Scopri il formato di file ODT e le API che possono creare e aprire file ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ODT?

I file ODT sono tipi di documenti creati con applicazioni di elaborazione testi basati sul formato OpenDocument Text File. Questi sono creati con applicazioni di elaborazione testi come OpenOffice Writer gratuito e possono contenere contenuti come testo, immagini, oggetti e stili. Il file ODT è per il word processor di Writer quello che il [DOCX](/it/word-processing/docx/) è per Microsoft Word. Diverse applicazioni, tra cui Google Docs e l'elaboratore di testi basato sul Web di Google incluso in Google Drive, possono aprire i file ODT per la modifica. Microsoft Word può anche aprire file ODT e salvarli in altri formati come [DOC](/it/word-processing/doc/) e DOCX.

## Breve storia ##

Le specifiche del formato di file ODP si basano sullo standard sviluppato come specifiche ODF. Queste specifiche si sono evolute in passato sotto forma di tre versioni sviluppate e pubblicate da OASIS come segue:

**2005** La versione 1.0 è stata pubblicata nel maggio 2005

**2007:** La versione 1.1 è stata pubblicata nel febbraio 2007

**2011:** La versione 1.2 è stata pubblicata a settembre 2011

Ci sono stati cambiamenti piuttosto minori nella transizione dalle versioni ODF 1.0 alla 1.1. La [versione ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) è l'ultima versione per le specifiche ODF e dovrebbe essere consultata dagli sviluppatori per lo sviluppo di applicazioni relative alla lettura/scrittura ODS.

## Specifiche del formato file ##

Il formato OpenDocument supporta la rappresentazione del documento come un singolo documento XML, nonché una raccolta di diversi documenti secondari all'interno di un pacchetto come archivio [ZIP](/it/compression/zip/). Ciascuno dei file dell'archivio ZIP memorizza parte del documento completo. Ogni documento secondario memorizza un aspetto particolare del documento. Ad esempio, un documento secondario contiene le informazioni sullo stile e un altro documento secondario contiene il contenuto del documento. Un tipico documento ODF ha i seguenti componenti:

* content.xml – Contenuto del documento e stili automatici utilizzati nel contenuto.
* styles.xml – Stili utilizzati nel contenuto del documento e stili automatici utilizzati negli stili stessi.
* meta.xml – Le metainformazioni del documento, come l'autore o l'ora dell'ultima azione di salvataggio.
* settings.xml – Impostazioni specifiche dell'applicazione, come le dimensioni della finestra o le informazioni sulla stampante.

Oltre a questi, nel pacchetto possono essere presenti molti altri documenti secondari come miniature di documenti, immagini, ecc. I file di documento sono il sottoinsieme di file ODF in cui il contenuto (fogli) è archiviato in //content.xml// sottodocumento.

## Riferimenti ##

* [OpenDocument - Di Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

