{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CAB και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Τι είναι ένα αρχείο CAB; ##

Ένα αρχείο με επέκταση .cab ανήκει σε ένα αρχείο cabinet των Windows που ανήκει στην κατηγορία των αρχείων συστήματος. Είναι ένα αρχείο που αποθηκεύεται σε μορφή αρχείου αρχειοθέτησης στις εκδόσεις των Microsoft Windows που υποστηρίζουν αλγόριθμους συμπιεσμένων δεδομένων, όπως το [LZX](/el/compression/lzx/), το Quantum και το [ZIP](/el/compression/zip/ ). Το αρχείο χρησιμοποιείται ζωτικής σημασίας όταν ένας χρήστης ή προγραμματιστής θέλει να περιέχει και να μοιράζεται δεδομένα και αρχεία εγκατάστασης λογισμικού. Τα χαρακτηριστικά της συμπίεσης δεδομένων χωρίς απώλειες και η ψηφιακή πιστοποίηση που περιλαμβάνεται σε αυτά τα αρχεία καθιστούν αυτό το αρχείο ιδανικό για αποθήκευση και κοινή χρήση τέτοιων αρχείων. Υποστηρίζει διαφορετικά προγράμματα εγκατάστασης της Microsoft, όπως το Device Installer, το SetUp API και το AdvPak.

## Σύντομη Ιστορία ##

Το αρχείο CAB είναι ένας τύπος αρχείου συμπίεσης δεδομένων που αναπτύχθηκε από τη Microsoft. Αρχικά ονομαζόταν "Diamond", αλλά στη συνέχεια έγινε γνωστό ως αρχείο CAB, συντομογραφία της λέξης "Cabinet"

## Τεχνική προδιαγραφή ##

Ένα αρχείο CAB μπορεί συνήθως να περιέχει έως και 65535 φακέλους, οι οποίοι με τη σειρά τους μπορούν να περιέχουν έως και 65536 αρχεία ο καθένας. Ο μηχανισμός αποθήκευσης αρχείων CAB είναι αποδοτικός σε χρόνο και χώρο, καθώς αποθηκεύει κάθε φάκελο ως συμπιεσμένο μπλοκ αντί να συμπιέζεται και να αποθηκεύεται κάθε αρχείο ξεχωριστά. Οι άδειοι φάκελοι δεν μπορούν να αποθηκευτούν σε φακέλους αρχειοθέτησης CAB. Το αρχείο CAB αναπτύχθηκε για πρώτη φορά από τη Microsoft και χρησιμοποιείται σε διάφορα προγράμματα εγκατάστασης, όπως το InstallShield με ελαφρώς διαφορετική μορφή. Τα αρχεία CAB συνήθως συνδέονται με προγράμματα αυτοεξαγωγής. Τα αρχεία CAB της Microsoft είναι εύκολα αναγνωρίσιμα λόγω του μοναδικού δείκτη τους που βοηθά στον προσδιορισμό της μορφής. Ο μοναδικός δείκτης για όλα τα αρχεία CAB της Microsoft είναι ένα πρόθεμα τεσσάρων λέξεων, το MSCF. Βλέποντας αυτόν τον κώδικα, ένας χρήστης μπορεί εύκολα να διακρίνει ένα αρχείο Microsoft CAB από άλλα αρχεία και να το χρησιμοποιήσει ανάλογα σε συμπιεστές ή εκδόσεις. Τα αρχεία μπορούν να συμπιεστούν με περισσότερα δεδομένα εγκαταστάσεων λογισμικού ή τα τρέχοντα δεδομένα μπορούν να αποσυμπιεστούν χρησιμοποιώντας το κατάλληλο λογισμικό.


## Παράδειγμα CAB ##

Το ακόλουθο παράδειγμα επεξηγεί τη σχέση μεταξύ αρχείων και φακέλων σε μια δομή αρχείου CAB:

{{< figure src="../cab.png" alt="Μορφή αρχείου CAB" >}}

## Αναφορά ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
