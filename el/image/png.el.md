{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο png", "μορφή αρχείου png", "τι είναι αρχείο png", "αρχείο", "παράδειγμα png", "επέκταση αρχείου png", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου PNG - Αρχείο εικόνας ράστερ",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PNG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο PNG;

Ένα αρχείο **PNG** (Portable Network Graphics) είναι μια μορφή αρχείου εικόνας ράστερ που χρησιμοποιεί συμπίεση χωρίς απώλειες. Αυτή η μορφή αρχείου δημιουργήθηκε ως αντικατάσταση του Graphics Interchange Format ([GIF](/el/image/gif/)) και δεν έχει περιορισμούς πνευματικών δικαιωμάτων. Ωστόσο, η μορφή αρχείου PNG δεν υποστηρίζει κινούμενα σχέδια. Η μορφή αρχείου PNG υποστηρίζει συμπίεση εικόνας χωρίς απώλειες που το καθιστά δημοφιλές στους χρήστες του. Με το πέρασμα του χρόνου, το PNG έχει εξελιχθεί ως μία από τις ευρέως χρησιμοποιούμενες μορφές αρχείων εικόνας.

## Σύντομο ιστορικό της μορφής αρχείου PNG

Ο κύριος λόγος πίσω από τη δημιουργία της μορφής αρχείου PNG ήταν ο πατενταρισμένος αλγόριθμος συμπίεσης, Lempel-Ziv-Welch, που χρησιμοποιήθηκε στη μορφή αρχείου GIF. Αυτό μαζί με άλλους περιορισμούς GIF δημιούργησε την ανάγκη αντικατάστασης της μορφής αρχείου [**GIF**](/el/image/gif/). Η πρώτη πρόταση και το όνομα για τη μορφή αρχείου PNG ήρθε τον Ιανουάριο του 1995. Βασικά συμβάντα σχετικά με τις μορφές αρχείων PNG παρατίθενται παρακάτω:

* Οκτώβριος 1996: Οι προδιαγραφές PNG Έκδοση 1.0 κυκλοφόρησαν και αργότερα εμφανίστηκαν ως [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Το ίδιο έγινε Σύσταση του W3C τον Οκτώβριο του 1996.
* Δεκέμβριος 1998: Κυκλοφόρησε η έκδοση 1.1, με κάποιες μικρές αλλαγές και την προσθήκη τριών νέων κομματιών.
* Αύγουστος 1999: Κυκλοφόρησε η έκδοση 1.2, προσθέτοντας ένα επιπλέον κομμάτι.
* Νοέμβριος 2003: Το PNG έγινε Διεθνές Πρότυπο (ISO/IEC 15948:2003). Αυτή η έκδοση του PNG διαφέρει ελάχιστα από την έκδοση 1.2 και δεν προσθέτει νέα κομμάτια.
* Μάρτιος 2004: ISO/IEC 15948:2004

## Λειτουργική σύγκριση GIF και PNG

Η μορφή αρχείου PNG σχεδιάστηκε για να είναι απλή και φορητή, νομικά απεριόριστη, εναλλάξιμη, ευέλικτη και ισχυρή. Ο παρακάτω πίνακας παραθέτει τις δυνατότητες GIF που κληρονομούνται από τη μορφή αρχείου PNG εκτός από τις νέες δυνατότητες.

|Δυνατότητα|GIF|PNG|
---|---|---|
|Εικόνες με ευρετήριο έως 256 χρώματα|Ναι|Ναι|
|Υποστήριξη για ροή|Ναι|Ναι|
|Διαφάνεια|Ναι|Ναι|
|Βοηθητικές πληροφορίες|Ναι|Ναι|
|Ανεξαρτησία υλικού και πλατφόρμας|Ναι|Ναι|
|Αποτελεσματικό|Ναι|Ναι|
|Εικόνες Truecolor έως 48 bit ανά pixel|Όχι|Ναι|
|Εικόνες σε κλίμακα του γκρι έως και 16 bit ανά pixel|Όχι|Ναι|
|Πλήρες κανάλι άλφα (μάσκες γενικής διαφάνειας)|Όχι|Ναι|
|Πληροφορίες γάμμα εικόνας|Όχι|Ναι|
|Αξιοπιστία|Όχι|Ναι|
|Ταχύτερη αρχική παρουσίαση|Όχι|Ναι|

## Δομή αρχείου PNG

Σχεδόν όλα τα λειτουργικά συστήματα έχουν υποστήριξη για το άνοιγμα αρχείων PNG. Για παράδειγμα, το πρόγραμμα προβολής Microsoft Windows έχει τη δυνατότητα να ανοίγει αρχεία PNG καθώς το λειτουργικό σύστημα έχει από προεπιλογή την υποστήριξη που είναι διαθέσιμη ως μέρος της εγκατάστασης. Ένα αρχείο PNG αποτελείται από μια «υπογραφή» PNG ακολουθούμενη από μια σειρά από //κομμάτια//.

### Κεφαλίδα αρχείου PNG

Τα πρώτα οκτώ byte ενός αρχείου PNG περιέχουν πάντα τις ακόλουθες (δεκαδικές) τιμές:

{{{137 80 78 71 13 10 26 10 }}}

Αυτή η υπογραφή υποδηλώνει ότι το υπόλοιπο αρχείο περιέχει μια μεμονωμένη εικόνα PNG, που αποτελείται από μια σειρά από κομμάτια που ξεκινούν με ένα κομμάτι IHDR και τελειώνουν με ένα κομμάτι IEND.

### Κομμάτια ###

Κάθε κομμάτι αποτελείται από τέσσερα μέρη:

**Μήκος:** Ένας ακέραιος χωρίς υπογραφή 4 byte που δίνει τον αριθμό των byte στο πεδίο δεδομένων του κομματιού. Το μήκος μετράει μόνο το πεδίο δεδομένων, όχι το ίδιο, τον κωδικό τύπου τεμαχίου ή το CRC. Το μηδέν είναι έγκυρο μήκος. Αν και οι κωδικοποιητές και οι αποκωδικοποιητές θα πρέπει να αντιμετωπίζουν το μήκος ως μη υπογεγραμμένο, η τιμή του δεν πρέπει να υπερβαίνει τα 231 byte.

**Τύπος κομματιού:** Κωδικός τύπου τεμαχίου 4 byte. Για ευκολία στην περιγραφή και στην εξέταση αρχείων PNG, οι κωδικοί τύπου περιορίζονται να αποτελούνται από κεφαλαία και πεζά γράμματα ASCII (AZ και az, ή 65-90 και 97-122 δεκαδικά). Ωστόσο, οι κωδικοποιητές και οι αποκωδικοποιητές πρέπει να αντιμετωπίζουν τους κωδικούς ως σταθερές δυαδικές τιμές και όχι ως συμβολοσειρές χαρακτήρων. Για παράδειγμα, δεν θα ήταν σωστό να αντιπροσωπεύσουμε τον κωδικό τύπου IDAT με τα ισοδύναμα EBCDIC αυτών των γραμμάτων. Πρόσθετες συμβάσεις ονομασίας για τύπους κομματιών συζητούνται στην επόμενη ενότητα.

**Δεδομένα τεμαχίων:** Τα byte δεδομένων που είναι κατάλληλα για τον τύπο τεμαχίου, εάν υπάρχουν. Αυτό το πεδίο μπορεί να έχει μηδενικό μήκος.

**CRC:** Ένας 4-byte CRC (Cyclic Redundancy Check) που υπολογίζεται στα προηγούμενα byte του τεμαχίου, συμπεριλαμβανομένων των πεδίων κωδικού τύπου τεμαχίου και δεδομένων τεμαχίου, αλλά χωρίς το πεδίο μήκους. Το CRC είναι πάντα παρόν, ακόμη και για κομμάτια που δεν περιέχουν δεδομένα.

Το μήκος του κομματιού δεδομένων μπορεί να είναι οποιοσδήποτε αριθμός byte μέχρι το μέγιστο. Επομένως, οι υλοποιητές δεν μπορούν να υποθέσουν ότι τα κομμάτια είναι ευθυγραμμισμένα σε όρια μεγαλύτερα από byte.

Τα κομμάτια μπορούν να εμφανιστούν με οποιαδήποτε σειρά, με την επιφύλαξη των περιορισμών που τίθενται σε κάθε τύπο κομματιού. (Ένας αξιοσημείωτος περιορισμός είναι ότι το IHDR πρέπει να εμφανίζεται πρώτο και το IEND πρέπει να εμφανίζεται τελευταίο· επομένως το κομμάτι IEND χρησιμεύει ως δείκτης τέλους αρχείου.) Μπορούν να εμφανιστούν πολλά κομμάτια του ίδιου τύπου, αλλά μόνο εάν επιτρέπονται ειδικά για αυτόν τον τύπο.

#### Τύποι κομματιών

Οι Τύποι τεμαχίων κατηγοριοποιούνται σε **Κρίσιμα** και **Βοηθητικά** κομμάτια με βάση την τιμή ASCII με διάκριση πεζών-κεφαλαίων 4 byte που έχει εκχωρηθεί στον Τύπο τμημάτων. Όλες οι υλοποιήσεις πρέπει να κατανοούν και να αποδίδουν με επιτυχία τα τυπικά κρίσιμα κομμάτια. Μια έγκυρη εικόνα PNG πρέπει να περιέχει ένα κομμάτι IHDR, ένα ή περισσότερα κομμάτια IDAT και ένα κομμάτι IEND.

### Συμπίεση

Η μέθοδος συμπίεσης PNG 0 (η μόνη μέθοδος συμπίεσης που ορίζεται επί του παρόντος για το PNG) καθορίζει τη συμπίεση ξεφουσκώματος/φουσκώματος με ένα συρόμενο παράθυρο το πολύ 32768 byte. Η συμπίεση Deflate είναι ένα παράγωγο LZ77 που χρησιμοποιείται σε zip, gzip, pkzip και σχετικά προγράμματα. Έχει γίνει εκτεταμένη έρευνα για την υποστήριξη του καθεστώτος του χωρίς διπλώματα ευρεσιτεχνίας. Τα συμπιεσμένα δεδομένα στη ροή δεδομένων zlib αποθηκεύονται ως μια σειρά μπλοκ, καθένα από τα οποία μπορεί να αντιπροσωπεύει ακατέργαστα (ασυμπίεστα) δεδομένα, συμπιεσμένα με LZ77 δεδομένα κωδικοποιημένα με σταθερούς κωδικούς Huffman ή συμπιεσμένα δεδομένα LZ77 κωδικοποιημένα με προσαρμοσμένους κώδικες Huffman. Ένα bit δείκτη στο τελικό μπλοκ το προσδιορίζει ως το τελευταίο μπλοκ, επιτρέποντας στον αποκωδικοποιητή να αναγνωρίσει το τέλος της συμπιεσμένης ροής δεδομένων.

#### Φιλτράρισμα προ-συμπίεσης

Εφαρμόζονται φίλτρα προσυμπίεσης για την προετοιμασία των δεδομένων εικόνας για τη βέλτιστη συμπίεση. Η μέθοδος φίλτρου PNG ορίζει πέντε βασικούς τύπους φίλτρων ως εξής:

|Τύπος φίλτρου|Όνομα|Προβλεπόμενη τιμή|
---|---|---|
|0|Καμία|Η γραμμή σάρωσης μεταδίδεται χωρίς τροποποίηση|
|1|Sub|Μεταδίδει τη διαφορά μεταξύ κάθε byte και της τιμής του αντίστοιχου byte του προηγούμενου pixel.|
|2|Up|Το φίλτρο Up() είναι ακριβώς όπως το φίλτρο Sub() με τη διαφορά ότι το εικονοστοιχείο ακριβώς πάνω από το τρέχον εικονοστοιχείο, και όχι ακριβώς στα αριστερά του, χρησιμοποιείται ως πρόβλεψη.|
|3|Average|Το φίλτρο Average() χρησιμοποιεί τον μέσο όρο των δύο γειτονικών pixel (αριστερά και πάνω) για να προβλέψει την τιμή ενός pixel.|
|4|Paeth|Το φίλτρο Paeth() υπολογίζει μια απλή γραμμική συνάρτηση των τριών γειτονικών εικονοστοιχείων (αριστερά, πάνω, επάνω αριστερά), και στη συνέχεια επιλέγει ως πρόβλεψη το γειτονικό εικονοστοιχείο που βρίσκεται πιο κοντά στην υπολογισμένη τιμή.|

Οι αλγόριθμοι φιλτραρίσματος εφαρμόζονται σε «byte» και όχι σε pixel, ανεξάρτητα από το βάθος bit ή τον τύπο χρώματος της εικόνας. Οι αλγόριθμοι φιλτραρίσματος λειτουργούν στην ακολουθία byte που σχηματίζεται από μια γραμμή σάρωσης. Εάν η εικόνα περιλαμβάνει ένα κανάλι άλφα, τα δεδομένα άλφα φιλτράρονται με τον ίδιο τρόπο όπως τα δεδομένα εικόνας.

Όταν η εικόνα συμπλέκεται, κάθε πέρασμα του μοτίβου διεπαφής αντιμετωπίζεται ως ανεξάρτητη εικόνα για σκοπούς φιλτραρίσματος. Τα φίλτρα λειτουργούν στις ακολουθίες byte που σχηματίζονται από τα εικονοστοιχεία που μεταδίδονται πραγματικά κατά τη διάρκεια μιας διέλευσης και η "προηγούμενη γραμμή σάρωσης" είναι αυτή που μεταδόθηκε προηγουμένως στο ίδιο πέρασμα, όχι αυτή που βρίσκεται δίπλα στην πλήρη εικόνα. Σημειώστε ότι η δευτερεύουσα εικόνα που μεταδίδεται σε οποιοδήποτε πέρασμα είναι πάντα ορθογώνια, αλλά έχει μικρότερο πλάτος ή/και ύψος από την πλήρη εικόνα. Το φιλτράρισμα δεν εφαρμόζεται όταν αυτή η δευτερεύουσα εικόνα είναι κενή.

## Βιβλιογραφικές αναφορές ##

* [PNG - Αρχική σελίδα](http://www.libpng.org/pub/png/)
