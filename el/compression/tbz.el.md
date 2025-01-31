{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο tbz", "μορφή αρχείου tbz", "τι είναι ένα αρχείο tbz", "αρχείο", "παράδειγμα tbz", "επέκταση αρχείου tbz", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip Compressed Tar Archive",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου TBZ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Τι είναι ένα αρχείο TBZ;

Ένα αρχείο με επέκταση .tbz είναι ένα συμπιεσμένο αρχείο που χρησιμοποιεί συμπίεση BZIP για τη μείωση του μεγέθους των αρχείων περιεχομένου. Τα αρχεία TBZ είναι στην πραγματικότητα αρχειοθετημένα αρχεία UNIX [TAR](/el/compression/tar/) που συμπιέζονται με BZIP. Η πιο πρόσφατη συμπίεση δεύτερου επιπέδου είναι το [BZIP2](/el/compression/bz2/) που αντικατέστησε το BZIP. Η μορφή αρχείου TBZ είναι κατάλληλη για τη μεταφορά μεγάλων αρχείων. Τα αρχεία TBZ μπορούν να ανοίξουν/εξαχθούν χρησιμοποιώντας εφαρμογές λογισμικού όπως 7-Zip, PeaZip και jZip. Οι χρήστες Linux και macOS μπορούν επίσης να ανοίξουν ένα TBZ με την εντολή BZIP2 από ένα παράθυρο τερματικού.

## Μορφή αρχείου TBZ

Τα αρχεία TBZ είναι στην πραγματικότητα συμπιεσμένα αρχεία που δημιουργούνται με συμπίεση BZIP/[BZIP2](/el/compression/bz2/). Δεν υπάρχουν διαθέσιμες επίσημες προδιαγραφές για αυτήν τη μορφή αρχείου. Ωστόσο, μια ανεπίσημη [αντίστροφη μηχανική προδιαγραφές](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) δείχνει ότι μια ροή .bz2 αποτελείται από μια κεφαλίδα 4 byte που ακολουθείται με μηδέν ή περισσότερα συμπιεσμένα μπλοκ.

## Βιβλιογραφικές αναφορές ##

* [Προδιαγραφές μορφής BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

