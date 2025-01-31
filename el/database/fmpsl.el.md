{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου FMPSL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FMPSL.",
  "title" :"Μορφή αρχείου FMPSL - FileMaker Pro 12 Snapshot Link File",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Τι είναι ένα αρχείο FMPSL;

Ένα αρχείο FMPSL είναι ένα αρχείο στιγμιότυπου της βάσης δεδομένων που δημιουργήθηκε με το FileMaker Pro 12. Αποθηκεύει τα ερωτούμενα αποτελέσματα από τη βάση δεδομένων μαζί με άλλες πληροφορίες, όπως οπτική διάταξη και ορατές πληροφορίες. Το αρχείο FMPSL μπορεί να χρησιμοποιηθεί για την επαναφορά όλων αυτών των δεδομένων σε μια άλλη παρουσία της βάσης δεδομένων FileMaker Pro. Αυτή η μορφή αρχείου εισήχθη με την κυκλοφορία του FileMaker Pro v 12. Πριν από αυτήν την έκδοση, οι σύνδεσμοι στιγμιότυπου εισήχθησαν ως μορφή αρχείου FPSL στο FileMaker Pro v 11. Τα αρχεία FMPSL μπορούν να ανοίξουν με το λογισμικό FileMaker Pro Advanced. Άλλες μορφές αρχείων που υποστηρίζονται από το FileMaker Pro περιλαμβάνουν τα [FP5](/el/database/fp5/), [FP7](/el/database/fp7/) και [FMP12](/el/database/fmp12/).

## Μορφή αρχείου FMPSL

Οι λεπτομέρειες της εσωτερικής μορφής αρχείου των αρχείων FMPSL δεν είναι διαθέσιμες δημόσια για αναφορά του προγραμματιστή.

### Πώς να αποθηκεύσετε εγγραφές ως αρχείο FMPSL;

Τα δεδομένα από τη βάση δεδομένων FileMaker Pro μπορούν να αποθηκευτούν ως αρχείο συνδέσμου στιγμιότυπου χρησιμοποιώντας τα ακόλουθα βήματα.

1. Αναζητήστε τις εγγραφές από τη βάση δεδομένων που απαιτείται να αποθηκευτούν ως αρχείο συνδέσμου στιγμιότυπου.
1. Χρησιμοποιώντας την επιλογή Send Record As Snapshot Link από το μενού, αποθηκεύστε το αρχείο εισάγοντας ένα όνομα αρχείου.
1. Χρησιμοποιήστε τις Εγγραφές που περιηγούνται για να αποθηκεύσετε ολόκληρο το σύνολο εγγραφών που βρέθηκαν.

Το αρχείο στιγμιότυπου που δημιουργήθηκε θα αποθηκευτεί στο δίσκο με το καθορισμένο όνομα.

## βιβλιογραφικές αναφορές

* [Μετατροπή προηγούμενων εκδόσεων των μορφών αρχείων FileMaker Pro σε μορφή αρχείου FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Αποθήκευση εγγραφών ως αρχείο συνδέσμου στιγμιότυπου](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

