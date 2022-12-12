{
  "date" : "2021-08-11",
  "keywords" :[ "αρχείο vdi", "μορφή αρχείου vdi", "τι είναι αρχείο vdi", "αρχείο", "παράδειγμα vdi", "επέκταση αρχείου vdi", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου VDI και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VDI.",
  "title" :"VDI - Αρχείο εικόνας εικονικού δίσκου VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Τι είναι ένα αρχείο VDI;
Ένα αρχείο με επέκταση .vdi είναι μια εικόνα εικονικού δίσκου. ειδικά για το πρόγραμμα εικονικοποίησης επιφάνειας εργασίας ανοιχτού κώδικα της Oracle που ονομάζεται VirtualBox. Τα αρχεία VDI χρησιμοποιούνται για την εκκίνηση της εικονικής μηχανής VirtualBox. Τα VM επιτρέπουν στους χρήστες να εκτελούν επιπλέον λειτουργικά συστήματα ή προγράμματα σε έναν μόνο υπολογιστή. Ως εκ τούτου, το πλεονέκτημα των αρχείων VDI είναι ότι οι χρήστες μπορούν να αποθηκεύουν αυτά τα αρχεία εικόνας δίσκου στον σκληρό τους δίσκο και μπορούν να τα εκτελούν χρησιμοποιώντας εξομοιωτές όποτε χρειάζονται.

## Μορφή αρχείου VDI
Το Virtual Disk Image (VDI) είναι η κύρια μορφή αρχείου δίσκου για ένα ενεργά αναπτυγμένο Oracle VM ανοιχτού κώδικα, γνωστό ως VirtualBox, το οποίο είναι ένα προϊόν εικονικοποίησης εταιρικής κλάσης. Η μορφή αρχείου VDI έχει σχεδιαστεί για να δημιουργεί μια φορητή εικόνα δίσκου η οποία μπορεί να εκτελεστεί εύκολα χρησιμοποιώντας άλλα προγράμματα εικονικοποίησης. Υποστηρίζει τόσο δυναμικά εκχωρημένο όσο και σταθερό μέγεθος αποθήκευσης. Σας επιτρέπει να επεκτείνετε ένα αρχείο εικόνας μετά τη δημιουργία του, ακόμα κι αν περιέχει ήδη δεδομένα.

### Εικονικοποίηση δίσκου
Το σύστημα προσομοιώνει σκληρούς δίσκους σε μορφή εικόνας δίσκου VDI. Ένα VirtualBox VM μπορεί να χρησιμοποιήσει προηγούμενους δίσκους που δημιουργήθηκαν σε Microsoft Virtual PC ή VMware, καθώς και τη δική του εγγενή μορφή. Το VirtualBox έχει επίσης τη δυνατότητα σύνδεσης με στόχους iSCSI και ακατέργαστη κατάτμηση στον κεντρικό υπολογιστή, χρησιμοποιώντας είτε ως εικονικούς σκληρούς δίσκους. Το VirtualBox προσομοιώνει IDE (ελεγκτές PIIX4 και ICH6), SATA (ελεγκτής ICH8M), ελεγκτές SAS στους οποίους μπορούν να προσαρτηθούν σκληροί δίσκοι και SCSI.

Η υποστήριξη είναι διαθέσιμη για Open Virtualization Format (OVF) από την έκδοση 2.2.0 του VirtualBox. Τόσο οι φυσικές συσκευές που είναι συνδεδεμένες στον κεντρικό υπολογιστή όσο και οι εικόνες ISO μπορούν να τοποθετηθούν ως μονάδες CD ή DVD.
Από προεπιλογή το VirtualBox υποστηρίζει γραφικά μέσω προσαρμοσμένης εικονικής κάρτας γραφικών συμβατή με VESA.

### Υποστήριξη εικονικοποίησης για Ethernet
Το VirtualBox εικονικοποιεί τις ακόλουθες κάρτες διεπαφής δικτύου για έναν προσαρμογέα δικτύου Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Επιτραπέζιος υπολογιστής Intel Pro/1000 MT (82540EM)
- Διακομιστής Intel Pro/1000 MT (82545EM)
- Διακομιστής Intel Pro/1000 T (82543GC)
- Παραεικονικός προσαρμογέας δικτύου (virtio-net)

Οι προσομοιωμένες κάρτες δικτύου επιτρέπουν στα λειτουργικά συστήματα φιλοξενούμενων να εκτελούνται χωρίς την ανάγκη αναζήτησης και εγκατάστασης προγραμμάτων οδήγησης για υλικό δικτύωσης, καθώς είναι διαθέσιμα ως μέρος του λειτουργικού συστήματος επισκέπτη. Ένας ειδικός παραεικονικός προσαρμογέας δικτύου βελτιώνει την απόδοση του δικτύου περιορίζοντας την ανάγκη αντιστοίχισης μιας συγκεκριμένης διεπαφής υλικού. Επομένως, απαιτεί ειδική υποστήριξη προγράμματος οδήγησης στον επισκέπτη.


## βιβλιογραφικές αναφορές

* [VirtualBox - από τη Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)

