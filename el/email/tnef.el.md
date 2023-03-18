{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου TNEF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο TNEF;

Το Transport Neutral Encapsulation Format (TNEF) είναι ιδιόκτητο της Microsoft, για την ενθυλάκωση συνημμένων email με βάση τη διεπαφή προγραμματισμού εφαρμογής μηνυμάτων (**MAPI**). Το Microsoft Outlook και ο Microsoft Exchange Server, υποστηρίζουν πλήρως το TNEF, ενώ αργότερα αποκωδικοποιεί το TNEF σε MAPI και εμφανίζει τα μορφοποιημένα μηνύματα αλληλογραφίας. Ένα συνημμένο email με κωδικοποίηση TNEF έχει τύπο MIME MS-TNEF και αποθηκεύεται ως winmail/win.dat. Το συνημμένο στο winmail .dat περιλαμβάνει τις ακόλουθες πληροφορίες:


|Μήνυμα|Αντικείμενα OLE|Δυνατότητες του Outlook
---|---|---|
|<ul><li> Αρχικά συνημμένα μηνυμάτων</li><li> Αρχική μορφοποιημένη έκδοση</li><li> γραμματοσειρές, μεγέθη κειμένου και χρώματα κειμένου</li></ul> |<ul><li> ενσωματωμένες εικόνες</li><li> ενσωματωμένα έγγραφα του Office</li></ul> |<ul><li> προσαρμοσμένες φόρμες</li><li> κουμπιά ψηφοφορίας</li><li> αιτήματα συνάντησης</li></ul>


Άλλες υπηρεσίες email που δεν υποστηρίζουν το TNEF, παρουσιάζουν απλό κείμενο για μηνύματα με μορφή TNEF. Το Outlook ενσωματώνει μια πλούσια μορφή του μηνύματος σε αρχεία TNEF (OLE) ή σε συγκεκριμένες δυνατότητες του Outlook (φόρμες, κουμπιά δημοσκόπησης και αιτήματα συνδιάσκεψης). Η επιβολή κυρώσεων για ρητή κωδικοποίηση TNEF εντός του προγράμματος-πελάτη ηλεκτρονικού ταχυδρομείου του Outlook δεν είναι δυνατή, ωστόσο, η επιλογή μορφής RTF για την αποστολή ενός μηνύματος ηλεκτρονικού ταχυδρομείου διευκολύνει έμμεσα την κωδικοποίηση TNEF.

## Μορφή αρχείου TNEF

Ο αλγόριθμος δεδομένων TNEF δημιουργεί μια ισοπεδωμένη δομή από πλούσιες ιεραρχικές ιδιότητες μηνυμάτων. Αυτές οι ισοπεδωμένες δομές χρησιμοποιούνται στη συνέχεια για να αναπαραστήσουν μια σειριακή ροή δεδομένων που αποτελείται από συγκεκριμένες ιδιότητες.

Σε ορισμένες περιπτώσεις, όπου οι ιδιότητες εμφανίζονται σε ομάδες ή έχουν πολλαπλές τιμές, η ροή μπορεί να περιλαμβάνει μετρήσεις και συμπληρώσεις για την επιβολή συγκεκριμένων στοίχισης δεδομένων. Μια χαρακτηριστική κατάσταση όπου η χρήση αυτού του αλγορίθμου είναι πλεονεκτική είναι σε ένα μη υποστηρικτικό περιβάλλον μηνυμάτων. Σε τέτοια περιβάλλοντα, μια ιδιότητα εμπλουτισμένου μηνύματος κωδικοποιείται σε μια σειριακή ροή δεδομένων από έναν TNEF Writer. Επιπλέον, οι ιδιότητες που δεν ανήκουν στο υποκείμενο TNEF μπορούν να ενθυλακωθούν κατά τη μετάδοση. Αυτές οι ενθυλακωμένες ιδιότητες στη συνέχεια διατίθενται με αποκωδικοποίηση μέσω ενός TNEF για να διασφαλιστεί η διαθεσιμότητα όλων των ιδιοτήτων του αρχικού μηνύματος στην εφαρμογή πελάτη.

Στο TNEF όλοι οι τύποι αριθμητικών δεδομένων είναι ελάχιστα-ενδιάνικοι και το μέγεθός τους είναι μεγαλύτερο από ένα byte. Ο χειρισμός αυτών των αριθμητικών τιμών σε πλατφόρμες που δεν είναι μικροί endian απαιτεί την πραγματοποίηση των κατάλληλων μετασχηματισμών για να ληφθούν οι σωστές τιμές. Οι τιμές συμβολοσειράς αντιπροσωπεύονται σε μορφή Augmented Backus-Naur Form (ABNF) σύμφωνα με τις προδιαγραφές [RFC5234]. Όταν η συμβολοσειρά τελειώνει με μηδενικό χαρακτήρα, περιλαμβάνεται επίσης. για παράδειγμα, "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="Μορφή αρχείου TNEF" >}}

## Χαρακτηριστικά TNEF και κανόνες επεξεργασίας ##

Η ροή δεδομένων στο TNEF ξεκινά με έναν αριθμό έκδοσης παλαιού τύπου, μια υπογραφή, μια τιμή πρωταρχικού κλειδιού και ένα χαρακτηριστικό που αντιπροσωπεύει την κωδικοσελίδα. Αυτή η κωδικοσελίδα δημιουργείται όταν ο κωδικοποιητής καταγράφει χαρακτηριστικά και ιδιότητες ANSI. Μετά από αυτό, η ροή έγινε μια σειρά από χαρακτηριστικά στα οποία τα χαρακτηριστικά του μηνύματος ήταν αρχικά γραμμωμένα και μετά ακολουθήθηκαν από τα χαρακτηριστικά συνημμένου. Διαφορετικά χαρακτηριστικά μηνυμάτων και συνημμένων περιέχονται σε ειδικά χαρακτηριστικά όπως attMsgProps, attAttachment και attRecipTable. Τα χαρακτηριστικά που εμφανίζονται στη ροή TNEF περιέχουν τη δομή, τις ιδιότητες του μηνύματος και τις μετατροπές που είναι απαραίτητες για την αλληλεπίδρασή τους με τις ιδιότητες μηνύματος. Κάθε χαρακτηριστικό αποτελείται από ένα αναγνωριστικό, μέγεθος και δεδομένα του χαρακτηριστικού, ένα άθροισμα ελέγχου και ένα επίπεδο ανάλογα με την εφαρμογή του.

## Σχέση με πρωτόκολλα και άλλους αλγόριθμους ##

Τα συστήματα που έχουν κακό μηχανισμό για την εμφάνιση εμπλουτισμένης μορφής μηνύματος εγγενώς χρειάζονται αλγόριθμο δεδομένων TNEF για μεταφορά. Χρησιμοποιώντας τον τύπο μέσου ms-TNEF, η έξοδος του αλγορίθμου αποτελείται από ένα αρχείο συνημμένου (winmail.dat) και ένα τμήμα σώματος του MIME που καθορίζεται στο [RFC2045]. Το σώμα απλού μηνύματος κειμένου μεταδίδεται με χρήση UUENCODE σύμφωνα με την προδιαγραφή [MSDN-UAF] και αυτό το σώμα μηνύματος ή ισοδύναμη μέθοδος αποκωδικοποιείται στο τέλος του παραλήπτη. Επιπλέον, το TNEF μπορεί να μεταδίδει δεδομένα μηνυμάτων χρησιμοποιώντας διαφορετικά πρωτόκολλα Διαδικτύου όπως SMTP, POP3, IMAP4 και αυτά που ενσωματώνουν το MIME σύμφωνα με το πρότυπο RFC2045.

## Δήλωση εφαρμογής ##

Εκτός από την απλή μετάδοση μηνυμάτων, η αρχική εφαρμογή του TNEF επρόκειτο να δημιουργηθεί για να χρησιμοποιεί κλάσεις μηνυμάτων και να υποστηρίζει πρόσθετες λειτουργίες που δεν έχουν αρχική υποστήριξη στο πρωτόκολλο μεταφοράς. Αυτή η εφαρμογή βελτιώθηκε περαιτέρω για τη μετάδοση ιδιοτήτων εμπλουτισμένων μηνυμάτων και επώνυμων ιδιοτήτων που χρησιμοποιούν σήμερα οι σύγχρονοι πελάτες ανταλλαγής μηνυμάτων. Για συμμόρφωση με την αρχική υλοποίηση, διατηρείται η αρχική σύνταξη χαρακτηριστικών και ένα ειδικό χαρακτηριστικό διατηρεί τις νέες ιδιότητες του μηνύματος ξεχωριστά.

## βιβλιογραφικές αναφορές

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Διευθύνσεις ηλεκτρονικού ταχυδρομείου και βιβλία διευθύνσεων στον Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Μεταφορά ουδέτερη μορφή ενθυλάκωσης (TNEF) Αλγόριθμος δεδομένων](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)
