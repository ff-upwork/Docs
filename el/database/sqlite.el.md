{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "αρχεία βάσης δεδομένων" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου SQLITE και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SQLITE.",
  "title" :"Μορφή αρχείου SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Τι είναι ένα αρχείο SQLite;

Ένα αρχείο με επέκταση .sqlite είναι ένα ελαφρύ αρχείο βάσης δεδομένων SQL που δημιουργήθηκε με το λογισμικό [SQLite](https://www.sqlite.org/index.html). Είναι μια βάση δεδομένων σε ένα αρχείο και υλοποιεί μια αυτόνομη, πλήρως εξοπλισμένη, εξαιρετικά αξιόπιστη μηχανή βάσης δεδομένων [SQL](/el/database/sql/). Τα αρχεία βάσης δεδομένων SQLite μπορούν να χρησιμοποιηθούν για την κοινή χρήση πλούσιου περιεχομένου μεταξύ συστημάτων με απλή ανταλλαγή αυτών των αρχείων μέσω του δικτύου. Σχεδόν όλα τα κινητά και οι υπολογιστές χρησιμοποιούν το SQLite για αποθήκευση και κοινή χρήση δεδομένων και είναι η επιλογή μορφής αρχείου για εφαρμογές πολλαπλών πλατφορμών. Λόγω της συμπαγούς χρήσης και της εύκολης χρηστικότητάς του, διατίθεται σε πακέτο σε άλλες εφαρμογές. Οι δεσμεύσεις SQLite υπάρχουν για γλώσσες προγραμματισμού όπως C, [C#](/el/programming/cs), [C++](/el/programming/cpp), [Java](/el/programming/java/), [PHP](/el/programming/php/ ), και πολλοί άλλοι.

## Μορφή αρχείου SQLite

Το SQLite στην πραγματικότητα είναι μια βιβλιοθήκη C-Language που υλοποιεί το SQLite RDBMS χρησιμοποιώντας τη μορφή αρχείου SQLite. Με την εξέλιξη των νέων συσκευών κάθε μέρα, η μορφή του αρχείου του διατηρείται συμβατή προς τα πίσω για να φιλοξενεί παλαιότερες συσκευές. Η μορφή αρχείου SQLite θεωρείται ως μακροπρόθεσμη μορφή αρχείου για τα δεδομένα.

### Το αρχείο της βάσης δεδομένων

Μια βάση δεδομένων SQLite διατηρείται πλήρως μέσω δύο αρχείων.
* Αρχείο κύριας βάσης δεδομένων - Περιέχει την πλήρη κατάσταση της βάσης δεδομένων SQLite
* Περιοδικό επαναφοράς - Αποθηκεύει πρόσθετες πληροφορίες σε ένα δεύτερο αρχείο και χρησιμοποιείται κατά την εκτέλεση συναλλαγών. Σε περίπτωση που το SQLite βρίσκεται σε λειτουργία WAL, διατηρείται ένα αρχείο καταγραφής κεφαλής εγγραφής.

#### Αρχείο περιοδικού

Αυτό το αρχείο προορίζεται να διατηρήσει όλες τις πληροφορίες που διατηρούνται σε περίπτωση που η τελευταία συναλλαγή δεν μπορούσε να ολοκληρωθεί σε περιπτώσεις όπως ένα σφάλμα υπολογιστή. Αυτό το αρχείο χρησιμοποιείται για την επαναφορά του αρχείου της βάσης δεδομένων σε συνεπή κατάσταση.

#### Σελίδες

Το κύριο αρχείο βάσης δεδομένων SQLite αποτελείται από μία ή περισσότερες σελίδες. Σε οποιαδήποτε χρονική στιγμή, κάθε σελίδα στην κύρια βάση δεδομένων έχει μία μόνο χρήση που είναι μία από τις ακόλουθες:

* Η σελίδα κλειδώματος byte
* Μια σελίδα freelist
* Μια σελίδα κορμού freelist
* Μια σελίδα φύλλου freelist
* Μια σελίδα β-δέντρου
* Εσωτερική σελίδα πίνακα b-tree
* Σελίδα φύλλου πίνακα β-δέντρου
* Μια εσωτερική σελίδα ευρετηρίου b-tree
* Μια σελίδα φύλλου ευρετηρίου β-δέντρου
* Μια σελίδα υπερχείλισης ωφέλιμου φορτίου
* Μια σελίδα χάρτη δείκτη

Το μέγεθος των αρχείων βάσης δεδομένων SQLite μπορεί να κυμαίνεται από λίγα kilobyte έως λίγα gigabyte.

### Κεφαλίδα SQLite

Η κεφαλίδα της βάσης δεδομένων SQLite βρίσκεται στα πρώτα 100 byte του αρχείου βάσης δεδομένων. Κάθε έγκυρο αρχείο βάσης δεδομένων SQLite ξεκινά με 16 byte (σε hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Οι λεπτομέρειες των πεδίων κεφαλίδας είναι όπως στον παρακάτω πίνακα.

|Μετατόπιση|Μέγεθος|Περιγραφή|
---|---|---|
|0|16|Η συμβολοσειρά κεφαλίδας: "SQLite format 3\000"|
|16|2|Το μέγεθος της σελίδας της βάσης δεδομένων σε byte. Πρέπει να είναι δύναμη δύο μεταξύ 512 και 32768 ή η τιμή 1 να αντιπροσωπεύει μέγεθος σελίδας 65536.|
|18|1|Έκδοση εγγραφής μορφής αρχείου. 1 για κληρονομιά? 2 για WAL.|
|19|1|Μορφή αρχείου αναγνωσμένη έκδοση. 1 για κληρονομιά? 2 για WAL.|
|20|1|Byte αχρησιμοποίητου "δεσμευμένου" χώρου στο τέλος κάθε σελίδας. Συνήθως 0.|
|21|1|Μέγιστο κλάσμα ενσωματωμένου ωφέλιμου φορτίου. Πρέπει να είναι 64.|
|22|1|Ελάχιστο κλάσμα ενσωματωμένου ωφέλιμου φορτίου. Πρέπει να είναι 32.|
|23|1|Κλάσμα ωφέλιμου φορτίου φύλλου. Πρέπει να είναι 32.|
|24|4|Μετρητής αλλαγής αρχείου.|
|28|4|Μέγεθος αρχείου βάσης δεδομένων σε σελίδες. Το "μέγεθος βάσης δεδομένων στην κεφαλίδα".|
|32|4|Αριθμός σελίδας της πρώτης σελίδας κορμού freelist.|
|36|4|Συνολικός αριθμός σελίδων freelist.|
|40|4|Το cookie σχήματος.|
|44|4|Ο αριθμός μορφής σχήματος. Οι υποστηριζόμενες μορφές σχήματος είναι 1, 2, 3 και 4.|
|48|4|Προεπιλεγμένο μέγεθος προσωρινής μνήμης σελίδας.|
|52|4|Ο αριθμός σελίδας της μεγαλύτερης σελίδας ρίζας β-δέντρου όταν βρίσκεται σε λειτουργία αυτόματης κενού ή αυξητικής κενού, ή μηδέν διαφορετικά.|
|56|4|Η κωδικοποίηση κειμένου της βάσης δεδομένων. Η τιμή 1 σημαίνει UTF-8. Η τιμή 2 σημαίνει UTF-16le. Η τιμή 3 σημαίνει UTF-16be.|
|60|4|Η "έκδοση χρήστη" όπως διαβάζεται και ορίζεται από το user_version pragma.|
|64|4|True (μη μηδενικό) για τη λειτουργία αυξητικής κενού. Λάθος (μηδέν) αλλιώς.|
|68|4|Το "Αναγνωριστικό εφαρμογής" που ορίστηκε από το PRAGMA application_id.|
|72|20|Διατίθεται για επέκταση. Πρέπει να είναι μηδέν.|
|92|4|Η έκδοση-ισχύει-για τον αριθμό.|
|96|4|SQLITE_VERSION_NUMBER|

## Βιβλιογραφικές αναφορές ##

* [Μορφή αρχείου SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - C Language Specs](https://www.sqlite.org/c3ref/intro.html)
