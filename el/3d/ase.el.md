{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","αρχείο", "μορφή", "τύπος αρχείου", "επέκταση","τι είναι ένα αρχείο ASE;" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ASE και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία ASE.",
  "title" :"ASE - Autodesk ASCII Scene Export File",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Τι είναι ένα αρχείο ASE;

Ένα αρχείο με επέκταση .ase είναι μια μορφή αρχείου Autodesk ASCII Scene Export που είναι μια αναπαράσταση ASCII μιας σκηνής, που περιέχει πληροφορίες 2D ή 3D κατά την εξαγωγή δεδομένων σκηνής χρησιμοποιώντας το Autodesk. Το Autodesk παρέχει επιλογές για τη συμπερίληψη στοιχείων σκηνής κατά την εξαγωγή δεδομένων σκηνής. Μπορείτε να συμπεριλάβετε ορισμό πλέγματος μαζί με πληροφορίες κορυφής και προσώπου, περιγραφή υλικού, δεδομένα κίνησης μετασχηματισμού για τα αντικείμενα, πλήρη ορισμό πλέγματος για κάθε n καρέ, δεδομένα κινούμενων εικόνων για κάμερες και φώτα και ρυθμίσεις αρμών IK.

## Μορφή αρχείου ASE - Περισσότερες πληροφορίες

Τα αρχεία ASE είναι αρχεία κειμένου που είναι αποθηκευμένα σε μορφή ASCII και μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Ένα αρχείο ASE μπορεί να περιέχει τους ακόλουθους τύπους πληροφοριών που παρέχονται από την Autodesk.

### Επιλογές εξόδου

* "Mesh Definition" - Εξάγει τον ορισμό κάθε πλέγματος, συμπεριλαμβανομένων των πληροφοριών κορυφής και προσώπου για γεωμετρικά αντικείμενα. Επιπλέον, η ενεργοποίηση αυτής της επιλογής ενεργοποιεί τα στοιχεία στο πλαίσιο ομάδας Επιλογών πλέγματος, που περιγράφεται παρακάτω.
* «Υλικά» - Περιλαμβάνει την περιγραφή του υλικού. Εάν ένα υλικό δεν έχει εκχωρηθεί σε ένα αντικείμενο, εξάγεται το χρώμα του καλωδίου. Περιλαμβάνονται όλα τα επίπεδα ενός δέντρου υλικού, επομένως αυτό μπορεί να παράγει πολύ κείμενο.
* "Transform Animation Keys" - Περιλαμβάνει τα δεδομένα κίνησης μετασχηματισμού για τα αντικείμενα. Εάν το αντικείμενο είναι μια κάμερα στόχος ή ένας προβολέας, αυτό θα περιλαμβάνει δεδομένα κινούμενης εικόνας στόχου.
* `Animated Mesh` - Εξάγει έναν πλήρη ορισμό πλέγματος για κάθε n καρέ. Η συχνότητα καθορίζεται από τον περιστρεφόμενο διακόπτη εξόδου ελεγκτή, που περιγράφεται παρακάτω. Κάθε μπλοκ περιέχει τις ίδιες πληροφορίες που καθορίζονται στο πλαίσιο της ομάδας Επιλογές πλέγματος, που περιγράφεται παρακάτω. Η ενεργοποίηση αυτού μπορεί να έχει ως αποτέλεσμα ένα τεράστιο αρχείο, ακόμη και για μικρές σκηνές.
* "Κινούμενη κάμερα/Ρυθμίσεις φωτός" - Εξάγει τα δεδομένα κινούμενων εικόνων για κάμερες και φώτα, όπως χρώμα, ένταση, πτώση, μεροληψία χάρτη και ούτω καθεξής. Εξάγει ένα μπλοκ κάθε n καρέ, όπως καθορίζεται από τον περιστρεφόμενο έλεγχο εξόδου ελεγκτή.
* `Αντίστροφες κινηματικές αρθρώσεις` - Εξάγει τις ρυθμίσεις άρθρωσης IK στον κλάδο Hierarchy.

### Τύποι αντικειμένων

Τα στοιχεία εδώ σάς επιτρέπουν να καθορίσετε ποια κατηγορία αντικειμένου θέλετε να συμπεριληφθεί στην έξοδο. Μπορείτε να συμπεριλάβετε γεωμετρικά αντικείμενα, σχήματα, κάμερες, φώτα και βοηθητικά αντικείμενα.

* Γεωμετρική
* Σχήματα
* Κάμερες
* Φώτα
* Βοηθοί

### Επιλογές πλέγματος

* "Mesh Normals" - Εξάγει τα κανονικά του προσώπου και των κορυφών. Το κανονικό του προσώπου παρατίθεται πρώτα, ακολουθούμενο από το κανονικό των τριών κορυφών που υποστηρίζουν το πρόσωπο. Η ενεργοποίηση αυτού έχει ως αποτέλεσμα ένα πολύ μεγαλύτερο αρχείο.
* «Συντεταγμένες αντιστοίχισης» - Εξάγει μια λίστα κορυφών και όψεων αντιστοίχισης, σύμφωνα με τις δομές TVert και TVFace που περιγράφονται στο κιτ ανάπτυξης λογισμικού 3ds Max. Εάν ένα αντικείμενο χρησιμοποιεί αντιστοίχιση προσώπων, εξάγεται μια λίστα χαρτών προσώπου που περιέχει συντεταγμένες UVW για κάθε πρόσωπο.
* `Vertex Colors` - Εξάγει χρώματα κορυφής.

### Έξοδος ελεγκτή

* «Χρήση κλειδιών» - Εξάγει τις τιμές κλειδιών. Εάν ο ελεγκτής δεν χρησιμοποιεί κλειδιά, τότε χρησιμοποιείται η μέθοδος Force Sample. Στην περίπτωση των ελεγκτών μετασχηματισμού, η επιλογή Χρήση πλήκτρων λειτουργεί μόνο εάν όλοι οι ελεγκτές μετασχηματισμού είναι είτε Linear/TCB είτε Bezier. Εάν ένα από τα ίχνη μετασχηματισμού χρησιμοποιεί διαφορετικό τύπο ελεγκτή, τότε η μέθοδος Force Sample χρησιμοποιείται για όλα τα ίχνη μετασχηματισμού.
* «Επιγκαστικά δείγματα» - Δείγματα τιμών ελεγκτή με βάση τη συχνότητα που καθορίζεται στα πλαίσια ανά ελεγκτή δείγματος.

## βιβλιογραφικές αναφορές

* [Autodesk - Exporting to ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-9D-98B23-A3A7-4096-8E81-888A3F9D6069-htm.html)