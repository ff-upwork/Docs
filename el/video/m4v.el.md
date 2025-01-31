{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "αρχείο", "επέκταση", "μορφή", "MPEG-4", "Διαχείριση ψηφιακών δικαιωμάτων", "DRM", "Apple", "βίντεο"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου M4V και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Τι είναι ένα αρχείο M4V;

Η μορφή αρχείου **M4V**, που αναπτύχθηκε από την Apple, είναι ένα κοντέινερ βίντεο που προστατεύεται προαιρετικά με προστασία αντιγραφής της Διαχείρισης ψηφιακών δικαιωμάτων (DRM) για προστασία του απορρήτου ή της αντιγραφής. Τα βίντεο και τα κομμάτια ήχου τυλίγονται από αρχεία κοντέινερ για την ευρετηρίαση και την οργάνωση των ροών αναπαραγωγής. Επιπλέον, τα κοντέινερ παρέχουν επίσης τη δυνατότητα κεφαλαίων παρόμοιων με αυτά των DVD. Η Apple χρησιμοποιεί το M4V για την κωδικοποίηση βίντεο στο iTunes Store της. Προστατεύει τη μη εξουσιοδοτημένη αναπαραγωγή μέσω της προστασίας αντιγραφής FairPlay της Apple, επιτρέποντας την αναπαραγωγή αρχείων M4V μόνο σε εξουσιοδοτημένους υπολογιστές που έχουν τους λογαριασμούς που χρησιμοποιούνται για την αγορά του βίντεο. Ωστόσο, εάν αφαιρεθεί η προστασία DRM από αρχεία M4V, αυτά τα αρχεία μπορούν να αναπαραχθούν σε άλλα προγράμματα αναπαραγωγής βίντεο αλλάζοντας την επέκταση από .m4v σε .mp4, γι' αυτό τα αρχεία M4V συσχετίζονται με το MPEG-4. Το M4V χρησιμοποιεί H.264 για βίντεο και **[AAC](/el/audio/aac/)** και Dolby Digital για κωδικοποίηση και αποκωδικοποίηση ήχου.

## Δομή αρχείου M4V ##

Τα αρχεία M4V έχουν συνεχή κομμάτια με κεφαλίδα 8 byte, μέγεθος τεμαχίου 4 byte και τύπο τεμαχίου 4 byte σε κάθε κομμάτι. Το πρώτο κομμάτι είναι "ftype" και έχει έναν δευτερεύοντα τύπο σε μετατόπιση 8. M4V που ορίζεται από τον δευτερεύοντα τύπο που πρέπει να είναι "M4V_". Περαιτέρω τύποι τμημάτων είναι προκαθορισμένες υπογραφές: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " ΕΙΚΟΝΑ». Επαναλαμβάνοντας κομμάτια, μέχρι να εντοπιστεί άγνωστος τύπος, συνθέτουμε αρχείο M4V.

Ακολουθεί μια εξέταση ενός δείγματος: Τα δυαδικά δεδομένα ενός δείγματος αρχείου m4v ελέγχονται μέσω του Hex Viewer και μπορεί να παρατηρηθεί ότι ξεκινά με μια υπογραφή **ftyp** (hex: 66 74 79 70) στη μετατόπιση 4, η οποία ορίζει το QuickTime Τύπος αρχείου κοντέινερ. Ο δευτερεύων τύπος αρχείου είναι **M4V_** (hex: 4D 34 56 20) που δείχνει τον τύπο αρχείου M4V (MPEG-4). Το μέγεθος του πρώτου μπλοκ είναι 32 (δεκαεξαδικό: 00 00 00 20, big-endian, υψηλό byte πρώτα), το μέγεθος βρίσκεται σε μετατόπιση 0. Στη μετατόπιση 32 (δεκαεξαδικό: 20) βρίσκεται το δεύτερο κομμάτι, το οποίο έχει μέγεθος 30.322 (δεκαεξαδικό : 00 00 76 72, big-endian, low-byte πρώτα) και πληκτρολογήστε **moov** (hex: 6D 6F 6F 76). Το επόμενο κομμάτι βρίσκεται στο offset 32+30,322#30,354 (hex: 00 00 76 92) και έχει μέγεθος 8 (hex: 00 00 00 08) και τύπο **free** (hex: 66 72 65 65).
### Κωδικοποιητές που χρησιμοποιούνται στο M4V ###

#### Video Codec H.264 ####

Το H.264 είναι ένα πρότυπο συμπίεσης βίντεο που μετατρέπει το ψηφιακό βίντεο σε μορφή που απαιτεί λιγότερο χώρο όταν απαιτείται μετάδοση ή αποθήκευση. Το M4V χρησιμοποιεί H.264 για συμπίεση βίντεο. Η εφαρμογή του κυμαίνεται από DVD, τηλεόραση, τηλεδιάσκεψη και ροή βίντεο μέσω Διαδικτύου. Το H.264 αποτελείται από δύο κύρια μέρη: Κωδικοποιητής – Ο οποίος συμπιέζει το βίντεο, Αποκωδικοποιητής – Αποσυμπιέζει το συμπιεσμένο βίντεο προς τα πίσω. Στο παρακάτω σχήμα, επισημαίνονται οι διαδικασίες κωδικοποίησης και αποκωδικοποίησης και άλλες διεργασίες καλύπτονται στο πρότυπο H.264.

##### Διαδικασία κωδικοποίησης και αποκωδικοποίησης βίντεο στο H.264 #####

Για τη συμπιεσμένη ροή bit H.264, ο κωδικοποιητής βίντεο διεξάγει τη διαδικασία πρόβλεψης, μετασχηματισμού και κωδικοποίησης. Ταυτόχρονα, ο αποκωδικοποιητής πραγματοποιεί την αντίστροφη διαδικασία αποκωδικοποίησης, αντίστροφου μετασχηματισμού και ανακατασκευής για την παραγωγή του αρχείου βίντεο. Το H.264 παίρνει το μισό μέγεθος του MPEG.

#### Κωδικοποιητής ήχου ####

Το Advanced Audio Coding (AAC) είναι ένας κωδικοποιητής ήχου για συμπίεση ψηφιακού ήχου με απώλειες και χρησιμοποιείται σε κοντέινερ M4V. Το AAC είναι ο διάδοχος της μορφής [MP3](/el/audio/mp3/) και επιτυγχάνει καλύτερη ποιότητα από το MP3 με τον ίδιο ρυθμό bit. Η μορφή AAC απορρίπτει κάποιες πληροφορίες κατά τη διαδικασία συμπίεσης, η οποία είναι λιγότερο σημαντική. Το AAC είναι ένας κωδικοποιητής μεταβλητού bitrate (VBR) που βασίζεται σε μπλοκ, όπου κάθε μπλοκ αποκωδικοποιείται σε 1024 δείγματα χρονικού τομέα.

### Βιβλιογραφικές αναφορές ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

