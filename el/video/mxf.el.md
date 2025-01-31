{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Μορφή ανταλλαγής υλικού",
  "keywords" :[ "MXF", "matroska βίντεο", "μορφή mkv", "πώς παίζω αρχεία MXF", "SMPTE", "multimedia", "video" ],
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MXF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Τι είναι ένα αρχείο MXF;

Ένα αρχείο με επέκταση .mxf είναι μια μορφή κοντέινερ πολυμέσων που περιέχει ψηφιακά μέσα βίντεο και ήχου μαζί με πληροφορίες μεταδεδομένων για το αρχείο. Ακολουθεί το πρότυπο SMPTE (Society of Motion Picture and Television Engineers) που είναι μια παγκόσμια ένωση επαγγελματιών από τη μηχανική, την τεχνολογία και τα στελέχη που εργάζονται στον κλάδο των μέσων ενημέρωσης και της ψυχαγωγίας. Τα αρχεία MXF μπορούν να μετατραπούν σε άλλες μορφές αρχείων όπως [AVI](/el/video/avi/) ή [MOV](/el/video/mov/).

## Μορφή αρχείου MXF

Τα αρχεία MXF είναι στην πραγματικότητα δυαδικά αρχεία που αποτελούνται από μια ακολουθία byte σε συγκεκριμένη μορφή. Οι εφαρμογές αποκωδικοποίησης πρέπει να συμμορφώνονται με αυτήν τη μορφή προκειμένου να την κατανοήσουν και να εξάγουν πληροφορίες από αυτήν. Η μορφή επιτρέπει την προσθήκη νέων στοιχείων χωρίς διακοπή της συμβατότητας προς τα πίσω χρησιμοποιώντας την κωδικοποίηση KLV που περιγράφεται παρακάτω.

* Κλειδί – το αναγνωριστικό του στοιχείου, μια καθολική ετικέτα SMPTE (UL)
* Μήκος – το μήκος των δεδομένων που είναι η κωδικοποίηση μεταβλητού μήκους που χρησιμοποιείται για τη μείωση του χώρου που απαιτείται για αυτό το στοιχείο
* Τιμή – η πραγματική τιμή του στοιχείου.

### Προδιαγραφές μορφής SMPTE

Η μορφή αρχείου MXF έχει οριστεί από τις ακόλουθες προδιαγραφές SMPTE.

* SMPTE ST 377-1:2011. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Προδιαγραφή μορφής αρχείου
* SMPTE ST 377-2 (εργασίες σε εξέλιξη από τον Ιανουάριο του 2012). Κωδικοποιημένη σύνταξη επέκτασης KLV για MXF.
* SMPTE ST 378:2004 (Αρχειοθετήθηκε 2010). Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Λειτουργικό μοτίβο 1a (μεμονωμένο αντικείμενο, μεμονωμένο πακέτο)
* SMPTE ST 379-1:2009. Μορφή ανταλλαγής υλικού (MXF) — Γενικό κοντέινερ MXF
* SMPTE ST 379-2:2010. Μορφή ανταλλαγής υλικού (MXF) -- Περιορισμένο γενικό κοντέινερ MXF
* SMPTE ST 380:2004. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Περιγραφικό σχήμα μεταδεδομένων-1 (Τυπικό, Δυναμικό)
* SMPTE ST 381-1:2005. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση ροών MPEG στο γενικό κοντέινερ MXF (Δυναμικό)
* SMPTE ST 381-2:2011. Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση ροών MPEG στο περιορισμένο γενικό κοντέινερ MXF
* SMPTE ST 382:2007. Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση ροών AES3 και ήχου εκπομπής κυμάτων στο γενικό κοντέινερ MXF
* SMPTE ST 383:2008. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση δεδομένων DV-DIF στο γενικό κοντέινερ MXF
* SMPTE ST 384:2005. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση μη συμπιεσμένων εικόνων στο γενικό κοντέινερ MXF
* SMPTE ST 385:2004. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση ουσίας SDTI-CP και μεταδεδομένων στο γενικό κοντέινερ MXF
* SMPTE ST 386:2004 (Αρχειοθετήθηκε 2010). Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση τύπου D-10 Essence Data στο Γενικό κοντέινερ MXF
* SMPTE ST 387:2004 (Αρχειοθετήθηκε 2010). Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση τύπου D-11 Essence Data στο Γενικό κοντέινερ MXF
* SMPTE ST 388:2004 (Αρχειοθετήθηκε 2010). Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Αντιστοίχιση κωδικοποιημένου ήχου A-law στο γενικό κοντέινερ MXF
* SMPTE ST 389:2005. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Στοιχείο συστήματος αντίστροφης αναπαραγωγής γενικού κοντέινερ MXF
* SMPTE ST 390:2011. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Εξειδικευμένο λειτουργικό πρότυπο "Atom" (Απλοποιημένη αναπαράσταση ενός μεμονωμένου αντικειμένου)
* SMPTE ST 391:2004 (Αρχειοθετήθηκε 2010). Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Λειτουργικό μοτίβο 1β (μεμονωμένο αντικείμενο, ομαδικά πακέτα)
* SMPTE ST 392:2004. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Λειτουργικό μοτίβο 2a (Στοιχεία λίστας αναπαραγωγής, μεμονωμένο πακέτο)
* SMPTE ST 393:2004. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Λειτουργικό μοτίβο 2β (Στοιχεία λίστας αναπαραγωγής, ομαδικά πακέτα)
* SMPTE ST 394:2006. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Σχήμα συστήματος 1 για το γενικό κοντέινερ MXF
* SMPTE ST 405:2006. Τηλεόραση — Μορφή ανταλλαγής υλικού (MXF) — Στοιχεία και μεμονωμένα στοιχεία δεδομένων για το Γενικό Σύστημα Εμπορευματοκιβωτίων MXF 1
* SMPTE ST 407:2006. Τηλεόραση — MXF — Λειτουργικά Μοτίβα 3α και 3β
* SMPTE ST 408:2006. Τηλεόραση — MXF — Λειτουργικά μοτίβα 1c, 2c και 3c
* SMPTE ST 410: 2008. Material Exchange Format - Generic Stream Partition.
* SMPTE ST 422:2006. Μορφή ανταλλαγής υλικού — Αντιστοίχιση ροών κώδικα JPEG2000 στο γενικό κοντέινερ MXF
* SMPTE ST 429.4:2006. Συσκευασία D-Cinema — Εφαρμογή MXF JPEG 2000
* SMPTE ST 429.5:2006. Συσκευασία D-Cinema — Αρχείο κομματιού κειμένου χρονισμένου χρόνου
* SMPTE ST 429.6:2006. Συσκευασία D-Cinema — Κρυπτογράφηση ουσίας αρχείου κομματιού MXF
* SMPTE ST 434:2006. Μορφή ανταλλαγής υλικού — Κωδικοποίηση XML για πληροφορίες μεταδεδομένων και δομής αρχείων
* SMPTE ST 436:2006. Τηλεόραση — Αντιστοιχίσεις MXF για γραμμές VBI και βοηθητικά πακέτα δεδομένων
* SMPTE ST 2019-4:2009. Αντιστοίχιση μονάδων κωδικοποίησης VC-3 στο γενικό κοντέινερ MXF
* SMPTE ST 2037:2009. Αντιστοίχιση του VC-1 στο γενικό κοντέινερ MXF
* SMPTE RP 2008:2008. Μορφή ανταλλαγής υλικού — Αντιστοίχιση ροών AVC στο γενικό κοντέινερ MXF
* SMPTE RP 2057:2011. Μεταφορά μεταδεδομένων βάσει κειμένου σε MXF
* SMPTE EG 41:2004. Μορφή ανταλλαγής υλικού (MXF) — Οδηγία μηχανικής. Σημείωση: Αυτό το έγγραφο δεν περιλαμβανόταν πλέον στον ιστότοπο SMPTE όταν συμβουλευόταν τον Ιανουάριο του 2012.
* SMPTE EG 42:2004. Μορφή ανταλλαγής υλικού (MXF) — Περιγραφικά μεταδεδομένα MXF
* SMPTE RDD 3:2008. Προδιαγραφές διαλειτουργικότητας e-VTR MXF
* SMPTE RDD 9-2009. Προδιαγραφές διαλειτουργικότητας MXF των προϊόντων Sony MPEG Long GOP
* Μενού υπολογιστικού φύλλου μητρώου μεταδεδομένων SMPTE.

### Δομικά Μεταδεδομένα MXF

Τα δομικά μεταδεδομένα είναι θεμελιώδη σε ένα αρχείο MXF καθώς περιέχουν χρήσιμες πληροφορίες σχετικά με τα περιεχόμενα του αρχείου. Τα μεταδεδομένα MXF περιέχουν πληροφορίες όπως ρυθμός καρέ, μέγεθος καρέ, ημερομηνία δημιουργίας αρχείου και προσαρμοσμένη ημερομηνία τροποποίησης. Τα δομικά μεταδεδομένα περιγράφουν τη δομή και τις δυνατότητες ενός αρχείου MXF που περιλαμβάνει την τεχνική περιγραφή των διαφόρων βασικών στοιχείων και τη μετάδοση του τρόπου σύνθεσης του χρονοδιαγράμματος εξόδου.

## βιβλιογραφικές αναφορές

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Αναφορά προόδου](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Βιβλιοθήκη OpenSource C++ για MXF](http://www.freemxf.org/)

