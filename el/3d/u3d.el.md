{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο u3d", "μορφή αρχείου u3d", "τι είναι αρχείο u3d", "αρχείο", "παράδειγμα u3d", "επέκταση αρχείου u3d", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Universal 3D μορφή αρχείου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου U3D και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο U3D;

Το **U3D** (Universal 3D) είναι μια συμπιεσμένη μορφή αρχείου και δομή δεδομένων για τρισδιάστατα γραφικά υπολογιστή. Περιέχει πληροφορίες τρισδιάστατων μοντέλων, όπως τρίγωνα πλέγματα, φωτισμό, σκίαση, δεδομένα κίνησης, γραμμές και σημεία με χρώμα και δομή. Η μορφή έγινε αποδεκτή ως πρότυπο[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) τον Αύγουστο του 2005. 3D [PDF](/el/pdf/) έγγραφα υποστηρίζουν U3D αντικείμενα ενσωματώνονται και μπορούν να προβληθούν στο Adobe Reader (έκδοση 7 και μετά).

Η μορφή U3D αναπτύχθηκε λαμβάνοντας υπόψη τον στόχο να καθιερωθεί ένα παγκόσμιο πρότυπο για την τρισδιάστατη αποθήκευση και ανταλλαγή δεδομένων. Ωστόσο, η μορφή βρίσκει την κύρια χρήση της στην κωδικοποίηση για 3D PDF αντί να χρησιμοποιείται ως μορφή ανταλλαγής. Το Acrobat 3D μετατρέπει έναν υποστηριζόμενο τύπο αρχείου 3D σε U3D ή PRC κατά τη μετατροπή σε PDF.

## Μορφή αρχείου U3D

Τα αρχεία U3D είναι σε δυαδική μορφή αρχείου που υποβλήθηκαν σε τέσσερις εκδόσεις, όπως περιγράφεται από το έγγραφο αναφοράς [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), με αποτέλεσμα την ενημέρωση προδιαγραφών με κάθε έκδοση. Το πρότυπο αρχείου PDF ISO-32000 δέχεται το U3D ως επιτρεπόμενο σχολιασμό και τύπο πολυμέσων.

Η πρώτη έκδοση του U3D επικεντρώθηκε στις βασικές αναπαραστάσεις των ιδιοτήτων των τρισδιάστατων γραφικών, όπως η γεωμετρία, το χρώμα, οι υφές, ο φωτισμός, τα οστά και τα κινούμενα σχέδια που βασίζονται σε μετασχηματισμούς. Η δεύτερη και η τρίτη έκδοση διόρθωσαν κάποια σφάλματα στην πρώτη έκδοση, με την τρίτη έκδοση να είναι ο πιο συχνά χρησιμοποιούμενος τύπος στο βιομηχανικό λογισμικό. Η τέταρτη έκδοση παρέχει ορισμούς για πρωτόγονα υψηλότερης τάξης (καμπύλες επιφάνειες). Οι [προδιαγραφές U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) είναι διαθέσιμες στο διαδίκτυο για αναφορά χρήστη στον ιστότοπο της ECMA.

### Τύποι δεδομένων σε αρχεία U3D

Το δυαδικό αρχείο θα περιέχει τους ακόλουθους τύπους: U8, U16, U32, U64, I16, I32, F32, F64 και String.

* U8 : Ένας ανυπόγραφος ακέραιος αριθμός 8 bit
* U16 : Ένας ακέραιος αριθμός 16 bit χωρίς υπογραφή
* U32: Ένας ανυπόγραφος ακέραιος αριθμός 32 bit
* U64: Ένας ανυπόγραφος ακέραιος αριθμός 64 bit
* I16: Ένας υπογεγραμμένος ακέραιος αριθμός 16 bit
* F32: Ένας απλός πλωτήρας ακριβείας IEEE.
* F64: Πλωτήρας διπλής ακρίβειας IEEE.
* Συμβολοσειρά: Οι συμβολοσειρές σε ένα αρχείο U3D ξεκινούν με έναν ανυπόγραφο ακέραιο αριθμό 16 bit που ορίζει το συνολικό μήκος των χαρακτήρων στη συμβολοσειρά. Οι συμβολοσειρές επεξεργάζονται πάντα ως διάκριση πεζών-κεφαλαίων.

## Δομή αρχείου U3D

Ένα αρχείο U3D περιέχει μια ακολουθία μπλοκ. Υπάρχουν 3 διαφορετικοί τύποι μπλοκ σε κάθε αρχείο U3D.

* Μπλοκ κεφαλίδας αρχείου
* Μπλοκ Διακήρυξης
* Μπλοκ Συνέχειας

Ο φορτωτής καθορίζει το τέλος ενός μπλοκ εάν τα δεδομένα σε αυτό το μπλοκ δεν απαιτούνται ή εάν δεν υπάρχει διαθέσιμος αποκωδικοποιητής για αυτόν τον τύπο μπλοκ.

{{< figure src="../u3d.png" alt="Μορφή αρχείου U3D" >}}

### Μπλοκ κεφαλίδας αρχείου
Ένα μπλοκ κεφαλίδας αρχείου περιέχει πληροφορίες αρχείου που χρησιμοποιούνται από το φορτωμένο για να καθορίσει τον τρόπο ανάγνωσης του αρχείου.

### Μπλοκ δήλωσης

Τα μπλοκ δήλωσης περιέχουν πληροφορίες για τα αντικείμενα του αρχείου. Τα αντικείμενα σε ένα μπλοκ δηλώσεων πρέπει να οριστούν.

### Μπλοκ συνέχισης

Πρόσθετες πληροφορίες για αντικείμενα που δηλώνονται σε ένα μπλοκ δήλωσης παρέχονται στο μπλοκ συνέχισης. Κάθε μπλοκ συνέχισης πρέπει να συσχετίζεται με ένα μπλοκ δήλωσης.


## Βιβλιογραφικές αναφορές ##

* [Μορφή αρχείου U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Προδιαγραφές μορφής αρχείου ECMA U3D](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

