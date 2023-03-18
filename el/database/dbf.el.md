{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "επέκταση", "αρχείο dbf", "μορφή αρχείου dbf", "Τύπος αρχείου βάσης δεδομένων", "μορφή αρχείου βάσης δεδομένων", "τι είναι αρχείο dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου DBF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DBF.",
  "title" :"DBF - Αρχείο βάσης δεδομένων dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Τι είναι ένα αρχείο DBF;
Το αρχείο με επέκταση .dbf είναι ένα αρχείο βάσης δεδομένων που χρησιμοποιείται από μια εφαρμογή συστήματος διαχείρισης βάσης δεδομένων που ονομάζεται **dBASE**. Αρχικά, η βάση δεδομένων dBASE ονομάστηκε Project Vulcan. ξεκίνησε από τον **Wayne Ratliff** το 1978. Ο τύπος αρχείου DBF εισήχθη με το dBASE II το 1983. Τακτοποιεί πολλαπλές εγγραφές δεδομένων με πεδία τύπου Array. Το λογισμικό βάσης δεδομένων **xBase** που είναι δημοφιλές λόγω της συμβατότητάς του με ένα ευρύ φάσμα μορφών αρχείων. υποστηρίζει επίσης τα αρχεία DBF.

## Μορφή αρχείου DBF
Η μορφή αρχείου DBF ανήκει στο σύστημα διαχείρισης βάσεων δεδομένων dBASE, αλλά μπορεί να είναι συμβατό με το xBase ή άλλα λογισμικά DBMS. Η αρχική έκδοση του αρχείου dbf αποτελούνταν από έναν απλό πίνακα που θα μπορούσε να έχει δεδομένα προσθήκης, τροποποίησης, διαγραφής ή εκτύπωσης χρησιμοποιώντας το σύνολο χαρακτήρων ASCII. Με το πέρασμα του χρόνου βελτιώθηκε το .dbf και προστέθηκαν πρόσθετα αρχεία για να αυξηθούν οι δυνατότητες και οι δυνατότητες του συστήματος βάσης δεδομένων.

Στο σύγχρονο dBASE ένα αρχείο DBF αποτελείται από μια κεφαλίδα, τις εγγραφές δεδομένων και τον δείκτη EOF (Τέλος αρχείου).

- Η κεφαλίδα περιέχει πληροφορίες σχετικά με το αρχείο, όπως τον αριθμό των εγγραφών και τον αριθμό των τύπων πεδίων που χρησιμοποιούνται στις εγγραφές.
- Οι εγγραφές περιέχουν τα πραγματικά δεδομένα.
- Το τέλος του αρχείου επισημαίνεται με ένα μόνο byte, με τιμή 0x1A.

### Κεφαλίδα αρχείου
Η διάταξη της κεφαλίδας αρχείου στο dBase δίνεται στον παρακάτω πίνακα:

| Byte | Περιεχόμενα | Σημασία |
---|---|---|
| 0 | 1 byte | Έγκυρο αρχείο dBASE για DOS. τα bit 0–2 υποδηλώνουν τον αριθμό έκδοσης, το bit 3 υποδηλώνει την παρουσία ενός αρχείου υπομνήματος dBASE για DOS, τα bit 4–6 υποδηλώνουν την παρουσία ενός πίνακα SQL, το bit 7 υποδηλώνει την παρουσία οποιουδήποτε αρχείου σημείωσης (είτε dBASE m PLUS είτε dBASE για DOS) |
| 1–3 | 3 byte | Ημερομηνία τελευταίας ενημέρωσης. μορφοποιημένο ως YYMMDD |
| 4–7 | Αριθμός 32 bit | Αριθμός εγγραφών στο αρχείο βάσης δεδομένων |
| 8–9 | Αριθμός 16 bit | Αριθμός byte στην κεφαλίδα |
| 10–11 | Αριθμός 16 bit | Αριθμός byte στην εγγραφή |
| 12–13 | 2 byte | Κατοχυρωμένα; γεμίζω με 0 |
| 14 | 1 byte | Σημαία που υποδεικνύει μη ολοκληρωμένη συναλλαγή[σημείωση 1] |
| 15 | 1 byte | Σημαία κρυπτογράφησης[σημείωση 2] |
| 16–27 | 12 byte | Με κράτηση για dBASE για DOS σε περιβάλλον πολλών χρηστών |
| 28 | 1 byte | Σημαία αρχείου παραγωγής .mdx. 1 εάν υπάρχει αρχείο παραγωγής .mdx, 0 εάν όχι |
| 29 | 1 byte | Αναγνωριστικό προγράμματος οδήγησης γλώσσας |
| 30–31 | 2 byte | Κατοχυρωμένα; γεμίζω με 0 |
| 32–n [σημείωση 3][σημείωση 4] | 32 byte το καθένα | πίνακας περιγραφέων πεδίων (δείτε παρακάτω για διάταξη περιγραφέων) |
| n + 1 | 1 byte | 0x0D ως τερματιστής πίνακα περιγραφής πεδίου |

- Η συνάρτηση ISMARKEDO ελέγχει αυτήν τη σημαία (Η ΕΝΑΡΞΗ ΣΥΝΑΛΛΑΓΗΣ την ορίζει σε 1, ΤΕΛΕΙΩΣΗ ΣΥΝΑΛΛΑΓΗΣ και ROLLBACK την επαναφέρει στο 0).
- Εάν αυτή η σημαία έχει οριστεί σε 1, εμφανίζεται το μήνυμα Database encrypted.
- Ο μέγιστος αριθμός πεδίων είναι 255.
- n σημαίνει το τελευταίο byte στον πίνακα περιγραφών πεδίου.

### Πίνακας περιγραφέων πεδίων
Διάταξη περιγραφέων πεδίων σε dBASE:

| Byte | Περιεχόμενα | Σημασία |
---|---|---|
| 0–10 | 11 byte | Όνομα πεδίου σε ASCII (μηδενικό) |
| 11 | 1 byte | Τύπος πεδίου. Επιτρεπόμενες τιμές: C, D, F, L, M, ή N (δείτε τον επόμενο πίνακα για τις έννοιες) |
| 12–15 | 4 byte | Με κράτηση |
| 16 | 1 byte | Μήκος πεδίου σε δυαδικό (μέγιστο 254 (0xFE)). |
| 17 | 1 byte | Δεκαδικός αριθμός πεδίου σε δυαδικό |
| 18–19 | 2 byte | Ταυτότητα χώρου εργασίας |
| 20 | 1 byte | Παράδειγμα |
| 21–30 | 10 byte | Με κράτηση |
| 31 | 1 byte | Σημαία πεδίου παραγωγής MDX. 1 εάν το πεδίο έχει μια ετικέτα ευρετηρίου στο αρχείο MDX παραγωγής, 0 εάν όχι |

### Εγγραφές βάσης δεδομένων
Κάθε εγγραφή ξεκινά με μια σημαία διαγραφής (1 byte). Τα πεδία είναι τυλιγμένα σε εγγραφές χωρίς διαχωριστικά πεδίων. Όλα τα δεδομένα πεδίου είναι ASCII. Ανάλογα με τον τύπο του πεδίου, η εφαρμογή επιβάλλει περαιτέρω περιορισμούς. Ακολουθούν οι τύποι πεδίων στο dBase:

| Τύπος πεδίου | Μνημονική | Τι δέχεται |
-------|-----|----|
| C | Χαρακτήρας | Οποιοδήποτε κείμενο ASCII (συμπληρωμένο με κενά μέχρι το μήκος του πεδίου) |
| D | Ημερομηνία | Αριθμοί και χαρακτήρας για διαχωρισμό του μήνα, της ημέρας και του έτους (αποθηκευμένα εσωτερικά ως 8 ψηφία σε μορφή ΕΕΕΕΜΜΗΔ) |
| F | Πλωτό σημείο | -, ., 0–9 (δεξιά δικαιολογημένα, συμπληρωμένα με κενά) |
| L | Λογικό | Y, y, N, n, T, t, F, f, ή ? (όταν δεν έχει αρχικοποιηθεί) |
| M | Υπόμνημα | Οποιοδήποτε κείμενο ASCII (αποθηκευμένο εσωτερικά ως 10 ψηφία που αντιπροσωπεύουν έναν αριθμό μπλοκ .dbt, αιτιολογημένος δεξιά, συμπληρώνεται με κενά) |
| N | Αριθμητικό | -, ., 0–9 (δεξιά δικαιολογημένα, συμπληρωμένα με κενά) |









## Βιβλιογραφικές αναφορές ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)
