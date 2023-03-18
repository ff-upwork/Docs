{
  "date" : "2019-10-11",
  "keywords" :[ "asp", "αρχείο asp", "μορφή αρχείου asp", "τύπος αρχείου asp", "αρχείο", "τύπος", "τι είναι αρχείο asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Μορφή αρχείου ενεργών σελίδων διακομιστή",
  "description" :"Μάθετε τι είναι ένα αρχείο ASP και τα API που μπορούν να τα δημιουργήσουν και να τα ανοίξουν.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο ASP;

Το ASP σημαίνει Active Server Pages που είναι ένα πλαίσιο ανάπτυξης για τη δημιουργία ιστοσελίδων. Επιτρέπει την εκτέλεση κώδικα υπολογιστή από έναν εσωτερικό διακομιστή για την εξυπηρέτηση των αιτημάτων Ιστού. Όταν δημιουργείται ένα αίτημα για ένα αρχείο ASP από το πρόγραμμα περιήγησης ιστού, ο διακομιστής διαβάζει το αρχείο και εκτελεί οποιονδήποτε κώδικα/script μέσα σε αυτό για να δημιουργήσει το **[HTML](/el/web/html/)** αποτέλεσμα το οποίο επιστρέφεται στο πρόγραμμα περιήγησης για προβολή.

Σε αντίθεση με τις σελίδες HTML, οι οποίες είναι στατικές σελίδες που εξυπηρετούνται από τον διακομιστή, τα αρχεία ASP δημιουργούν δυναμικό περιεχόμενο κατά το χρόνο εκτέλεσης που μπορεί να περιλαμβάνει αιτήματα για δεδομένα από μια βάση δεδομένων. Οι σελίδες ASP χρησιμοποιούν συνήθως την επέκταση .asp αντί για .html. Δεδομένου ότι ο κώδικας/δέσμη ενεργειών μέσα σε ένα αρχείο ASP εκτελείται από την πλευρά του διακομιστή, το πρόγραμμα περιήγησης που ζητά δεν μπορεί να δει τον κώδικα που χρησιμοποιήθηκε για τη δημιουργία της σελίδας που εμφανίζεται. Όλα τα σύγχρονα προγράμματα περιήγησης έχουν τη δυνατότητα να εμφανίζουν σελίδες που δημιουργούνται ως αποτέλεσμα. Με βάση την τεχνολογία της Microsoft, οι σελίδες που έχουν δημιουργηθεί με ASP φιλοξενούνται σε διακομιστές Microsoft Internet Information Services (IIS).

## Σύντομο ιστορικό της μορφής αρχείου ASP
Το ASP έχει υποστεί λίγες μόνο αναθεωρήσεις, αλλά αντικαταστάθηκε από το ASP.NET, το οποίο είναι ένας πιο σύγχρονος και πιο αποτελεσματικός τρόπος ανάπτυξης και διαχείρισης σελίδων διακομιστή. Η υποστήριξη για ASP περιλαμβάνεται από προεπιλογή μαζί με τις Υπηρεσίες Πληροφοριών Διαδικτύου (IIS). Το ASP δημοσιεύτηκε σε τρεις διαφορετικές εκδόσεις με βελτιώσεις σε κάθε μία.

* Το ASP 1.0 κυκλοφόρησε τον Δεκέμβριο του 1996 ως μέρος του IIS 3.0
* Το ASP 2.0 κυκλοφόρησε τον Σεπτέμβριο του 1997 ως μέρος του IIS 4.0
* Το ASP 3.0 κυκλοφόρησε τον Νοέμβριο του 2000 ως μέρος του IIS 5.0

## Λειτουργικά Αντικείμενα ASP

Τα αρχεία ASP χρησιμοποιούν αντικείμενα από την πλευρά του διακομιστή για την επεξεργασία αιτημάτων χρήστη και τη δημιουργία σελίδων εξόδου που θα προβληθούν στους χρήστες. Κάθε αντικείμενο έχει ένα σύνολο συλλογών, ιδιοτήτων και μεθόδων για την επεξεργασία αιτημάτων και απαντήσεων. Αυτά τα αντικείμενα περιλαμβάνουν:

### Αίτημα αντικειμένου

Όταν ένα πρόγραμμα περιήγησης ζητά μια σελίδα από έναν διακομιστή, ονομάζεται αίτημα. Το αντικείμενο Request χρησιμοποιείται για τη λήψη πληροφοριών από έναν επισκέπτη.

### Αντικείμενο απόκρισης

Το αντικείμενο ASP Response χρησιμοποιείται για την αποστολή εξόδου στον χρήστη από τον διακομιστή.

### Αντικείμενο διακομιστή

Το αντικείμενο ASP Server χρησιμοποιείται για πρόσβαση σε ιδιότητες και μεθόδους στο διακομιστή. Επιτρέπει συνδέσεις με βάσεις δεδομένων (ADO), σύστημα αρχείων και χρήση στοιχείων που είναι εγκατεστημένα στον διακομιστή.

### Αντικείμενο συνεδρίας

Ένα αντικείμενο περιόδου λειτουργίας είναι σαν ένας σύνδεσμος μεταξύ του προγράμματος περιήγησης του χρήστη που ζητά μια σελίδα από τον διακομιστή και του ίδιου του διακομιστή. Αυτό επιτυγχάνεται με ένα cookie που δημιουργείται από την ASP και αποστέλλεται στον υπολογιστή του χρήστη. Το αντικείμενο Session αποθηκεύει πληροφορίες σχετικά με ή αλλάζει τις ρυθμίσεις για μια περίοδο λειτουργίας χρήστη. Οι πληροφορίες που αποθηκεύονται σε ένα αντικείμενο περιόδου λειτουργίας μοιράζονται σε όλες τις σελίδες μιας εφαρμογής. Οι κοινές πληροφορίες που αποθηκεύονται στις μεταβλητές περιόδου λειτουργίας είναι το όνομα, το αναγνωριστικό και οι προτιμήσεις. Ο διακομιστής δημιουργεί ένα νέο αντικείμενο Session για κάθε νέο χρήστη και καταστρέφει το αντικείμενο Session όταν λήξει η περίοδος λειτουργίας.

### Αντικείμενο εφαρμογής

Το αντικείμενο Application περιέχει πληροφορίες που θα χρησιμοποιηθούν από πολλές σελίδες στην εφαρμογή (όπως πληροφορίες σύνδεσης βάσης δεδομένων). Οι πληροφορίες είναι προσβάσιμες από οποιαδήποτε σελίδα. Οι πληροφορίες μπορούν επίσης να αλλάξουν σε ένα μέρος και οι αλλαγές θα αντικατοπτρίζονται αυτόματα σε όλες τις σελίδες. Το αντικείμενο Application χρησιμοποιείται για την αποθήκευση και την πρόσβαση σε μεταβλητές από οποιαδήποτε σελίδα, όπως ακριβώς και το αντικείμενο Session.

### Αντικείμενο ASPError

Το αντικείμενο ASPError υλοποιήθηκε στο ASP 3.0 και είναι διαθέσιμο σε IIS5 και μεταγενέστεραΤο αντικείμενο ASPError χρησιμοποιείται για την εμφάνιση λεπτομερών πληροφοριών οποιουδήποτε σφάλματος εμφανίζεται σε δέσμες ενεργειών σε μια σελίδα ASP.

**Σημείωση:** Το αντικείμενο ASPError δημιουργείται όταν καλείται το Server.GetLastError, επομένως η πρόσβαση στις πληροφορίες σφάλματος είναι δυνατή μόνο χρησιμοποιώντας τη μέθοδο Server.GetLastError.

## βιβλιογραφικές αναφορές

* [ASP - By W3C](https://www.w3schools.com/asp/default.asp)
* [Δημιουργία απλών σελίδων ASP](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))
