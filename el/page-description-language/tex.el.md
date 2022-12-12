{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου TEX",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου TEX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο TEX; ##

Η **TeX** είναι μια γλώσσα που περιλαμβάνει προγραμματισμό καθώς και δυνατότητες σήμανσης, που χρησιμοποιούνται για τη στοιχειοθεσία εγγράφων. Ο Donald Knuth από το Πανεπιστήμιο του Στάνφορντ, είναι ο δημιουργός αυτού του πολυμήχανου συστήματος στοιχειοθεσίας. Σε όλο τον κόσμο, το TeX είναι η απόλυτη επιλογή συγγραφέων και εκδοτών για την παραγωγή τεχνικών εγγράφων υψηλής ποιότητας. Το TeX εκτελεί μια εξαιρετική δουλειά στη μορφοποίηση σύνθετων μαθηματικών παραστάσεων. Σε συνδυασμό με έναν υψηλής ποιότητας φωτοστοιχειοθέτη, το TeX ανταγωνίζεται τα αποτελέσματα που παράγονται από τα καλύτερα παραδοσιακά συστήματα στοιχειοθέτησης. Ως εκ τούτου θεωρείται ως τα πιο κλασικά ψηφιακά τυπογραφικά συστήματα.

Τα αρχεία εισόδου TeX βασίζονται σε κώδικα ASCII, επιτρέποντας έτσι την κοινή χρήση χειρογράφων μεταξύ συγγραφέων, διαχειριστών εκδόσεων και κριτικών. Μια μεγάλη ποικιλία υπολογιστικών περιβαλλόντων, σχεδόν κάθε σύγχρονη πλατφόρμα και πολλές παλαιότερες πλατφόρμες υποστηρίζουν το TeX. Επιπλέον, το TeX είναι ένα δωρεάν λογισμικό, διαθέσιμο σε ένα ευρύ φάσμα καταναλωτών. Πολλές εγκαταστάσεις UNIX χρησιμοποιούν και το UNIX troff και το TeX ως σύστημα μορφοποίησης για διαφορετικούς σκοπούς. Άλλες εργασίες στοιχειοθεσίας εκτελούνται εξαιρετικά με τη μορφή LaTeX, ConTeXt και άλλων πακέτων μακροεντολών.

## Σύντομη Ιστορία ##

Το TeX σχεδιάστηκε και γράφτηκε από τον Donald Knuth το 1978. Ο Guy Steele από το Τεχνολογικό Ινστιτούτο της Μασαχουσέτης αναθεώρησε την είσοδο/έξοδο του TeX για να το κάνει να λειτουργεί κάτω από το Μη συμβατό λειτουργικό σύστημα όπως το Timesharing System (ITS). Η πρώτη έκδοση του TeX αναπτύχθηκε με το λειτουργικό σύστημα WAITS του Stanford στη γλώσσα προγραμματισμού (SAIL) και δοκιμάστηκε για εκτέλεση σε PDP-10. Ο Knuth εισήγαγε την ιδέα του εγγράμματου προγραμματισμού για προηγμένες εκδόσεις. Ο εγγράμματος προγραμματισμός είναι ένας τρόπος δημιουργίας μεταγλωττιζόμενου πηγαίου κώδικα και στοιχειοθέτησης (σε TeX) για διασυνδεδεμένη τεκμηρίωση χρησιμοποιώντας το αρχικό αρχείο. Η γλώσσα που χρησιμοποιείται για την ανάπτυξη αυτών των προηγμένων εκδόσεων του TeX ονομάζεται WEB, ένα μείγμα προγραμμάτων DEC PDP-10 Pascal για τη διασφάλιση της φορητότητας.

Μια αναθεωρημένη νέα έκδοση του TeX που δημοσιεύτηκε το 1982 και ονομάστηκε TeX82. Η κύρια αλλαγή είναι η αντικατάσταση του αρχικού αλγόριθμου συλλαβισμού με τον πρόσφατα γραμμένο αλγόριθμο του Frank Liang. Για να διασφαλιστεί η φορητότητα σε διαφορετικές πλατφόρμες, αντί να χρησιμοποιεί κινητή υποδιαστολή, το TeX82 χρησιμοποιεί αριθμητική σταθερού σημείου μαζί με μια πραγματική, πλήρη γλώσσα προγραμματισμού. Το 1989, κυκλοφόρησε μια νέα έκδοση του TeX και του Metafont. Έτσι, η έκδοση 3.0 του TeX διευκολύνει τις εισόδους 8-bit, επιτρέποντας 256 διαφορετικούς χαρακτήρες στο κείμενο. Μετά την έκδοση 3, οι ενημερώσεις σημειώνονται με την προσθήκη ενός επιπλέον ψηφίου στο τέλος του δεκαδικού, π.χ. η τρέχουσα έκδοση του TeX υποδεικνύεται ως 3.14159265. Αυτή η έκδοση ενημερώθηκε τελευταία φορά στις 12-1-2014.

## Είσοδος TeX ##

Ένα αρχείο εισόδου στο TEX μπορεί να προετοιμαστεί με ένα πρόγραμμα επεξεργασίας κειμένου χρησιμοποιώντας συνηθισμένο κείμενο. Σε αντίθεση με έναν τυπικό επεξεργαστή κειμένου, αυτό το αρχείο εισόδου δεν επιτρέπει αόρατους χαρακτήρες ελέγχου. Ένα αρχείο μπορεί να ενσωματωθεί σε ένα άλλο αρχείο, που περιέχει ορισμούς μακροεντολών και βοηθητικούς ορισμούς που ενισχύουν τις δυνατότητες του TeX. Εάν μια εγκατάσταση TeX συνοδεύεται από αρχεία μακροεντολών, οι τοπικές πληροφορίες σχετικά με το TeX δείχνουν τη χρήση αρχείων μακροεντολών. Η τυπική μορφή του TeX, ενσωματώνει έναν συνδυασμό μακροεντολών και άλλους ορισμούς γνωστούς ως απλό TEX.

Με βάση την ακριβή γνώση των μεγεθών όλων των χαρακτήρων και συμβόλων, υπολογίζει τη βέλτιστη οργάνωση των γραμμάτων ανά γραμμή και των γραμμών ανά σελίδα. Κατά τη στιγμή της επεξεργασίας του εγγράφου, παράγεται ένα αρχείο .dvi, όπου το "dvi" σημαίνει "ανεξάρτητη συσκευή". Απαιτούνται προγράμματα οδήγησης συσκευής για την εκτύπωση ή την προεπισκόπηση του εγγράφου με επέκταση dvi. Σήμερα, η παραγωγή dvi παρακάμπτεται από ένα ευρέως χρησιμοποιούμενο pdf-TeX. Δεν υπάρχει προηγούμενη γνώση των γραμματοσειρών κατά την εγκατάσταση TeX, επομένως τα εξωτερικά αρχεία γραμματοσειρών, που αποτελούν μέρος του τοπικού περιβάλλοντος TeX, χρησιμοποιούνται για τη λήψη πληροφοριών για έγγραφα.

## Σύστημα στοιχειοθέτησης ##

Περίπου 300 αρχέγονοι (εντολές) μπορούν να γίνουν κατανοητοί από το βασικό σύστημα TeX. Οι πρωτόγονες είναι εντολές χαμηλού επιπέδου, επομένως ένας κοινός χρήστης σπάνια τις χρησιμοποιούσε απευθείας και οι περισσότερες λειτουργίες εκτελούνται από αρχεία μορφής. Αυτά τα αρχεία μορφής είναι προφορτωμένες εικόνες μνήμης του TeX, οι οποίες ακολουθούνται από τη φόρτωση μεγάλων συλλογών μακροεντολών. Η αρχική προεπιλεγμένη μορφή της γλώσσας, δηλαδή το απλό TeX προσθέτει περίπου 600 εντολές.

Μια ανάστροφη κάθετο ομαδοποιημένη με σγουρά άγκιστρα υποδηλώνει την έναρξη των εντολών TeX. Δεδομένου ότι η TeX είναι μια γλώσσα που βασίζεται σε μακροεντολές και διακριτικά, σχεδόν όλα τα συντακτικά χαρακτηριστικά του TeX μπορούν να αλλάξουν κατά το χρόνο εκτέλεσης, συμπεριλαμβανομένων εκείνων που ορίζονται από τον χρήστη, εκτός από τα μη επεκτάσιμα διακριτικά που στη συνέχεια εκτελούνται. Η ίδια η επέκταση είναι πρακτικά χωρίς προβλήματα. Ορισμένες εντολές πρέπει να έρχονται μετά από ορίσματα που βοηθούν στην εξήγηση της λειτουργίας μιας εντολής. Για παράδειγμα, η εντολή \vskip κατευθύνει το TEX να παρακάμψει προς τα κάτω/επάνω τη σελίδα ακολουθούμενο από ένα όρισμα που καθορίζει πόσο χώρο θα παραλείψει.

## Εκδόσεις ##

Το LaTeX είναι η πιο συχνά χρησιμοποιούμενη μορφή που αναπτύχθηκε αρχικά από τον Leslie Lamport. Το LaTeX ενσωματώνει διαφορετικά στυλ εγγράφων για αρχεία, γράμματα, βιβλία και διαφάνειες και προσφέρει αναφορά και αυτόματη αρίθμηση για διαφορετικές ενότητες και μαθηματικές εκφράσεις. Το AMS-TeX είναι μια άλλη δημοφιλής μορφή, που αναπτύχθηκε από την American Mathematical Society.

Το AMS-TeX προσφέρει πολύ πιο φιλικές προς το χρήστη εντολές, οι οποίες μπορούν να επαναπροσδιοριστούν από περιοδικά για να ταιριάζουν στο τοπικό τους στυλ. Το LaTeX μπορεί να επωφεληθεί από τα πλεονεκτήματα του AMS-TeX χρησιμοποιώντας τα "πακέτα" AMS τα οποία στη συνέχεια ονομάζονται AMS-LaTeX. Το ConTeXt είναι μια άλλη μορφή γραμμένη από τον Hans Hagen που χρησιμοποιείται κυρίως για επιτραπέζιες εκδόσεις.

Το λογισμικό TeX προσφέρει πολλά χαρακτηριστικά που δεν ήταν διαθέσιμα ή χαμηλότερης ποιότητας σε άλλα συστήματα στοιχειοθεσίας κατά τη στιγμή της δημιουργίας του. Ορισμένα από τα καινοτόμα χαρακτηριστικά αυτής της γλώσσας βασίζονται σε ενδιαφέροντες αλγόριθμους που προέρχονται από τις διατριβές των μαθητών του Knuth. Ενώ άλλα προγράμματα στοιχειοθεσίας ενσωματώνουν πλέον χρήσιμες δυνατότητες του TeX στα προγράμματά τους.

## Βιβλιογραφικές αναφορές ##

* [TeX Typesetting system](https://en.wikipedia.org/wiki/TeX)
