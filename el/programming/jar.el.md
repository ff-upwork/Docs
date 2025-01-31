{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","τι είναι ένα αρχείο jar", "πώς να ανοίξετε ένα αρχείο jar", "επέκταση", "αρχείο", "αρχείο jar", "μορφή αρχείου jar", "επέκταση .jar"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Μορφή αρχείου αρχείου Java",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου JAR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχείο JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Τι είναι ένα αρχείο JAR;

Ένα αρχείο με επέκταση .jar είναι ένα αρχείο Java Archive που περιέχει πολλά διαφορετικά αρχεία που σχετίζονται με εφαρμογές ως ένα μόνο αρχείο. Αυτή η μορφή αρχείου δημιουργήθηκε για να μειώσει την ταχύτητα φόρτωσης μιας ληφθείσας Java Applet στο πρόγραμμα περιήγησης μέσω συναλλαγής HTTP, αποφεύγοντας τη δημιουργία πολλαπλών συνδέσεων HTTP. Ένα μόνο αρχείο JAR μπορεί να περιέχει αρχεία κλάσης Java ([.class](/el/programming/class/)), [images](/el/image/) και [sounds](/el/audio/). Τα μεμονωμένα στοιχεία μέσα σε ένα αρχείο JAR μπορούν να υπογραφούν ψηφιακά από τον προγραμματιστή της εφαρμογής για τον έλεγχο ταυτότητας της προέλευσής τους. Τα αρχεία JAR χρησιμοποιούνται τακτικά για τη δημιουργία λειτουργικών API που περιέχουν συγκεκριμένες λειτουργίες που σχετίζονται με αυτό το API.

## Μορφή αρχείου JAR

Τα αρχεία JAR βασίζονται στη δημοφιλή [μορφή αρχείου ZIP](/el/compression/zip/) που αρχειοθετεί τα μεμονωμένα αρχεία περιεχομένου σε ένα μόνο αρχείο. Η μορφή αρχείου JAR υποστηρίζει συμπιέσεις, με αποτέλεσμα μικρότερο μέγεθος αρχείου για λήψη και ως εκ τούτου βελτιώνει περαιτέρω τον χρόνο λήψης. Το άρθρο [Προδιαγραφές αρχείου JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) της Oracle παρέχει πλήρεις λεπτομέρειες σχετικά με τις εσωτερικές προδιαγραφές των αρχείων JAR.

### Το αρχείο Manifest

Όταν δημιουργείται ένα αρχείο JAR, δημιουργείται αυτόματα ένα αρχείο δήλωσης μέσα σε αυτό που περιέχει τις πληροφορίες μεταδεδομένων σχετικά με τα περιεχόμενα του αρχείου JAR. Αυτό το αρχείο εμφανίζει τα περιεχόμενα που είναι συσκευασμένα μέσα στο αρχείο JAR. Ένα τυπικό αρχείο Manifest έχει την εξής εμφάνιση που δείχνει τους φακέλους και τις κλάσεις που περιλαμβάνονται στο αρχείο JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Προδιαγραφές Manifest

Οι προδιαγραφές του Manifest ορίζονται από την Oracle ως εξής.

`manifest-file`: νέα γραμμή κύριας ενότητας \*individual-section

`main-section`: έκδοση-πληροφορίες νέας γραμμής \*main-attribute

`version-info`: Manifest-Version : version-number

`version-number` : ψηφίο+{.ψηφίο+}*

`main-attribute`: (οποιοδήποτε νόμιμο κύριο χαρακτηριστικό) νέα γραμμή

`individual-section`: Όνομα : τιμή newline \*perentry-attribute

`perentry-attribute`: (οποιοδήποτε νόμιμο χαρακτηριστικό perentry) νέα γραμμή

`νέα γραμμή` : CR LF | LF | CR (δεν ακολουθείται από LF)

`digit`: {0-9}

### Εκτελέσιμο JAR

Τα αρχεία JAR μπορούν επίσης να αποτελούνται από μια εφαρμογή που μπορεί να εκτελεστεί από Java Virtual Machine (JVM) παρόμοια με οποιαδήποτε άλλη εφαρμογή στο λειτουργικό σύστημα Microsoft Windows. Σε αυτήν την περίπτωση, το JVM πρέπει να γνωρίζει για το σημείο εισόδου της εφαρμογής που είναι οποιαδήποτε κλάση με μια δημόσια μέθοδο static void main. Το αρχείο δήλωσης προσδιορίζει μια τέτοια κλάση με την κεφαλίδα "Main-Class" στην ακόλουθη μορφή:

```
Main-Class: com.example.MyClassName
```



## βιβλιογραφικές αναφορές

* [Επισκόπηση αρχείου JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Μορφή αρχείου JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

