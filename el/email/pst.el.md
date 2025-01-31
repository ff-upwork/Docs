{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Μορφή αρχείου αποθήκευσης προσωπικών πληροφοριών του Outlook",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PST και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο PST;

Τα αρχεία με επέκταση .pst αντιπροσωπεύουν τα Προσωπικά αρχεία αποθήκευσης του Outlook (ονομάζονται επίσης Personal Storage Table) που αποθηκεύουν ποικιλία πληροφοριών χρήστη. Οι πληροφορίες χρήστη αποθηκεύονται σε φακέλους διαφορετικών τύπων που περιλαμβάνουν email, στοιχεία ημερολογίου, σημειώσεις, επαφές και πολλές άλλες μορφές αρχείων. Τα αρχεία PST χρησιμοποιούνται για την αρχειοθέτηση δεδομένων αποστολής email εκτός σύνδεσης, τα οποία μπορούν αργότερα να φορτωθούν και να προβληθούν σε διάφορες εφαρμογές.

## Προδιαγραφές μορφής αρχείου PST

Μορφή αρχείου PST [προδιαγραφές](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) είναι διαθέσιμα από τη Microsoft ως δωρεάν και αμετάκλητη δωρεάν άδεια χρήσης διπλωμάτων ευρεσιτεχνίας μέσω της υπόσχεσης Open Specification Promise .

### Τύπος μορφών PST

Οι μορφές αρχείων PST κατηγοριοποιούνται σε δύο τύπους με βάση την κωδικοποίηση του τύπου αρχείου. Τα αρχεία PST με κωδικοποίηση ANSI είναι παλαιότερες μορφές αρχείων και υποστηρίζονται μόνο από το Outlook 2002 και παλαιότερες εκδόσεις. Τέτοια αρχεία έχουν μέγιστο όριο μεγέθους 2 GB (2^^31^^ Byte) και δεν υποστηρίζουν Unicode. Ένας πιο σύγχρονος τύπος μορφής αρχείου, που βασίζεται στην κωδικοποίηση Unicode, καταργεί τον περιορισμό μεγέθους αρχείου και μπορεί να φτάσει το μέγιστο μέγεθος δεδομένων των 50 GB.

### Λογική οργάνωση της μορφής αρχείου PST

Στη βάση της μορφής αρχείου PST βρίσκεται το B-Tree που διατηρεί τα δεδομένα ταξινομημένα και επιτρέπει αναζητήσεις, διαδοχική πρόσβαση, εισαγωγές, διαγραφές κ.λπ. σε λογαριθμικό χρόνο. Η συνολική δομή ενός αρχείου PST είναι οργανωμένη σε τρία επίπεδα.

![Logical layers of a PST file](/el/email/PST-1.png "Logical layers of a PST file")

«Επίπεδο βάσης δεδομένων κόμβου (NDB)» - Το επίπεδο βάσης δεδομένων κόμβου βρίσκεται στο κατώτερο επίπεδο ενός αρχείου PST και περιλαμβάνει βάση δεδομένων κόμβων. Αυτοί οι κόμβοι αντιπροσωπεύουν στην πραγματικότητα εγκαταστάσεις αποθήκευσης χαμηλότερου επιπέδου της μορφής αρχείου PST. Το επίπεδο NDB αποτελείται από κεφαλίδες, πληροφορίες κατανομής αρχείων, μπλοκ και BTrees (Node BTree και BTree BTree) από την άποψη αποθήκευσης. Οι κόμβοι και τα μπλοκ του επιπέδου NDB συνδέονται μέσω Data BID που είναι μία από τις τέσσερις ιδιότητες της αναφοράς κόμβου, δηλαδή NID (Node ID), Parent NID, Data BID (Block BID) και SubNode BID.

Επίπεδο "Λίστες, Πίνακες και Ιδιότητες" - Το επίπεδο LTP παρέχει τη λογική κατανόηση των εννοιών υψηλότερου επιπέδου πάνω από το NDB. Εκτός από άλλα στοιχεία, το επίπεδο LTP αποτελείται κυρίως από Περιβάλλον Ιδιοτήτων (PC) και Πλαίσιο Πίνακα (TC). Το PC είναι μια συλλογή ιδιοτήτων, ενώ η TC αντιπροσωπεύει μια δισδιάστατη μήτρα συλλογής ιδιοτήτων έναντι της παρουσίας αυτών. Αποτελεσματική υλοποίηση υπολογιστών και TC, το επίπεδο LTP χρησιμοποιεί τους ακόλουθους δύο τύπους δομών δεδομένων πάνω από τον κόμβο NDB:

* Heap On Node (HN) - επιτρέπει την υποκατανομή της ροής δεδομένων ενός κόμβου σε μικρά τμήματα μεταβλητού μεγέθους.
* BTree on Heap (BTH) - Το BTH παρέχει έναν βολικό και πρακτικό τρόπο αναζήτησης μέσω δεδομένων Οι υπολογιστές που περιγράφηκαν παραπάνω, υλοποιούνται ως BTH και γι' αυτό υλοποιείται με την κατασκευή μέσα σε μια δομή HN.

`Επίπεδο μηνυμάτων -` Κανόνες υψηλότερου επιπέδου και επιχειρηματική λογική για την εργασία με αρχεία PST εφαρμόζονται σε αυτό το επίπεδο. Η λογική έξοδος αυτού του επιπέδου έχει ως αποτέλεσμα αντικείμενα φακέλου, αντικείμενα μηνύματος, αντικείμενα συνημμένου και ιδιότητες, τα οποία καθίστανται δυνατά με το συνδυασμό επιπέδων LTP και NDB. Σε αυτό το επίπεδο ορίζονται επίσης κανόνες και απαιτήσεις, που πρέπει να τηρούνται κατά την τροποποίηση των περιεχομένων του PST.

### Φυσική οργάνωση μορφής αρχείου PST

Το υψηλό επίπεδο οργάνωσης αρχείων του αρχείου PST φαίνεται στο παρακάτω σχήμα. Αυτή είναι απλώς μια επισκόπηση διαφορετικών εννοιών από λογικά στοιχεία του αρχείου PST.

![Physical organization of the PST file format](/el/email/PST-2.png "Physical organization of the PST file format")


#### Πληροφορίες κεφαλίδας PST

Η δομή HEADER του αρχείου PST βρίσκεται στην αρχή του αρχείου με μετατόπιση 0. Περιέχει πληροφορίες μεταδεδομένων σχετικά με το αρχείο PST και πληροφορίες ROOT για πρόσβαση στις δομές δεδομένων του επιπέδου NDB που περιγράφονται παραπάνω. Η δομή HEADER διαφέρει για τις εκδόσεις Unicode και ANSI της μορφής αρχείου PST.

Η κεφαλίδα ξεκινά με μια μαγική λέξη 4 byte **!BDN** που αντιπροσωπεύεται από byte (0x21, 0x42, 0x44, 0x4E). Ένας άλλος μαγικός αριθμός 2 byte, **SM** (0x53, 0x4D), βρίσκεται στη μετατόπιση 8 από την αρχή του αρχείου. Οι πληροφορίες έκδοσης (ANSI ή Unicode) βρίσκονται σε μετατόπιση 10 από την αρχή του αρχείου. Η τιμή Hex (0x17) καθορίζει το αρχείο Unicode PST ενώ το 0x0E ή το 0x0F αντιπροσωπεύει τη μορφή αρχείου ANSI.

|Πεδίο|Περιγραφή
---|---|
|dwMagic (4 byte)|ΠΡΕΠΕΙ να είναι "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPpartial (4 byte)|Η τιμή CRC 32-bit των 471 byte δεδομένων ξεκινώντας από το wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|ΠΡΕΠΕΙ να είναι "{ 0x53, 0x4D }".
|wVer (2 byte)|Έκδοση μορφής αρχείου. Αυτή η τιμή ΠΡΕΠΕΙ να είναι 14 ή 15 εάν το αρχείο είναι αρχείο ANSI PST και ΠΡΕΠΕΙ να είναι 23 εάν το αρχείο είναι αρχείο Unicode PST.
|wVerClient (2 byte)|Έκδοση μορφής αρχείου πελάτη. Η έκδοση που αντιστοιχεί στη μορφή που περιγράφεται σε αυτό το έγγραφο είναι 19. Οι δημιουργοί ενός νέου αρχείου PST που βασίζεται σε αυτό το έγγραφο ΠΡΕΠΕΙ να αρχικοποιήσουν αυτήν την τιμή σε 19.
|bPlatformCreate (1 byte)|Αυτή η τιμή ΠΡΕΠΕΙ να οριστεί σε 0x01.
|bPlatformAccess (1 byte)|Αυτή η τιμή ΠΡΕΠΕΙ να οριστεί σε 0x01.
|dwReserved (8 byte)|
|bidUnused (8 byte μόνο Unicode)|Προστέθηκε μη χρησιμοποιημένο padding όταν δημιουργήθηκε η μορφή αρχείου Unicode PST.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|BID επόμενης σελίδας. Οι σελίδες διαθέτουν ειδικό μετρητή για την εκχώρηση τιμών bidIndex. Η τιμή του bidIndex για BID για σελίδες εκχωρείται από αυτόν τον μετρητή.
|bidNextB (μόνο 4 byte ANSI): |Επόμενη BID. Αυτή η τιμή είναι ο μονοτονικός μετρητής που υποδεικνύει το BID που θα εκχωρηθεί για το επόμενο εκχωρημένο μπλοκ. Οι τιμές BID προχωρούν σε προσαυξήσεις των 4. Για περισσότερες λεπτομέρειες, δείτε την ενότητα 2.2.2.2.
|dwUnique (4 byte)|Πρόκειται για μια μονότονα αυξανόμενη τιμή που τροποποιείται κάθε φορά που τροποποιείται η δομή HEADER του αρχείου PST. Η λειτουργία αυτής της τιμής είναι να παρέχει μια μοναδική τιμή και να διασφαλίζει ότι τα HEADER CRC είναι διαφορετικά μετά από κάθε τροποποίηση κεφαλίδας.
|rgnid[]   (128 byte)|Μια σταθερή συστοιχία 32 NID, το καθένα αντιστοιχεί σε ένα από τα 32 πιθανά NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE_MESSAGE_MESSAGE,NID_TYPE)
|qwUnused (8 byte)|Χώρος που δεν χρησιμοποιείται; ΠΡΕΠΕΙ να οριστεί στο μηδέν. Μόνο μορφή αρχείου Unicode PST.
|root (Unicode: 72 byte; ANSI: 40 bytes)|Δομή ROOT (ενότητα 2.2.2.5).
|dwAlign (4 byte)|Αχρησιμοποίητα byte στοίχισης. ΠΡΕΠΕΙ να οριστεί στο μηδέν. Μόνο μορφή αρχείου Unicode PST.
|rgbFM (128 byte)|Καταργήθηκε το FMap. Αυτό δεν χρησιμοποιείται πλέον και ΠΡΕΠΕΙ να συμπληρωθεί με 0xFF. Οι αναγνώστες ΠΡΕΠΕΙ να αγνοούν την τιμή αυτών των byte.
|rgbFP (128 byte)|Καταργήθηκε το FPMap. Αυτό δεν χρησιμοποιείται πλέον και ΠΡΕΠΕΙ να συμπληρωθεί με 0xFF. Οι αναγνώστες ΠΡΕΠΕΙ να αγνοούν την τιμή αυτών των byte.
|bSentinel (1 byte)|ΠΡΕΠΕΙ να οριστεί σε 0x80.
|bCryptMethod (1 byte)|Δηλώνει πώς κωδικοποιούνται τα δεδομένα μέσα στο αρχείο PST. ΠΡΕΠΕΙ να οριστεί σε μία από τις προκαθορισμένες τιμές (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbΔέσμευση (2 byte)| Κατοχυρωμένα; ΠΡΕΠΕΙ να οριστεί στο μηδέν.
|bidNextB (8 byte)|Δηλώνει την επόμενη διαθέσιμη τιμή BID. Μόνο μορφή αρχείου Unicode PST.
|bidNextB (ΜΟΝΟ Unicode: 8 byte)|Επόμενη ΠΡΟΣΦΟΡΑ. Αυτή η τιμή είναι ο μονοτονικός μετρητής που υποδεικνύει το BID που θα εκχωρηθεί για το επόμενο εκχωρημένο μπλοκ. Οι τιμές BID προχωρούν σε προσαυξήσεις των 4. Για περισσότερες λεπτομέρειες, δείτε την ενότητα 2.2.2.2.
|dwCRCFull (4 byte)|Η τιμή CRC 32-bit των 516 byte δεδομένων ξεκινώντας από το wMagicClient έως το bidNextB, συμπεριλαμβανομένου. Μόνο μορφή αρχείου Unicode PST.
|ullReserved (8 byte)|Δεσμευμένο; ΠΡΕΠΕΙ να οριστεί στο μηδέν. Μόνο μορφή αρχείου ANSI PST.
|dwReserved (4 byte)|Δεσμευμένο; ΠΡΕΠΕΙ να οριστεί στο μηδέν. Μόνο μορφή αρχείου ANSI PST.
|rgbReserved2 (3 byte)|
|bΔέσμευση (1 byte) |
|rgbReserved3 (32 byte) |

### Προστασία δεδομένων ###

Για ασφάλεια, τα αρχεία PST μπορούν επίσης να προστατεύονται με κωδικό πρόσβασης, κάτι που απαιτεί από την εφαρμογή φόρτωσης να εφαρμόσει κωδικό πρόσβασης για να είναι δυνατή η προβολή τους. Ο κωδικός πρόσβασης που εφαρμόζεται στο αρχείο PST αποθηκεύεται στον χώρο αποθήκευσης μηνυμάτων. Ωστόσο, αυτό δεν παρέχει ισχυρή προστασία δεδομένων, καθώς ο κωδικός πρόσβασης μπορεί να αφαιρεθεί με διαθέσιμα εργαλεία. Επίσης, ο κωδικός πρόσβασης που καθορίζεται από το χρήστη δεν χρησιμοποιείται ως μέρος του κλειδιού για την κωδικοποίηση και την αποκωδικοποίηση αλγορίθμων κρυπτογράφησης. Έτσι, δεν υπάρχει κανένα όφελος από την προστασία των δεδομένων στα οποία έχουν πρόσβαση μη εξουσιοδοτημένα μέρη. Η αποθήκευση του κωδικού πρόσβασης ως κατακερματισμός CRC-32 της αρχικής συμβολοσειράς την καθιστά επίσης μια αδύναμη μέθοδο για την ασφάλεια των δεδομένων έναντι της προσέγγισης ωμής βίας.

## Βιβλιογραφικές αναφορές ##

* [Μορφή αρχείου Outlook Personal Folders (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Προδιαγραφές μορφής αρχείου προσωπικού φακέλου](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

