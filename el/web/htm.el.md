{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "αρχείο htm", "μορφή αρχείου htm", "τύπος αρχείου htm", "αρχείο", "τύπος", "τι είναι ένα αρχείο htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου HTM",
  "description" :"Ο οδηγός μορφής αρχείου σας για να μάθετε τι είναι ένα αρχείο HTM και API που μπορούν να τα δημιουργήσουν και να τα ανοίξουν.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο HTM;

Τα αρχεία με επέκταση **.htm** αντιπροσωπεύουν τη γλώσσα σήμανσης υπερκειμένου για τη δημιουργία ιστοσελίδων για εμφάνιση σε προγράμματα περιήγησης ιστού όπως το Google Chrome, ο Internet Explorer, ο Firefox και πολλά άλλα. Καθορίζει τις σημάνσεις για τη δημιουργία στατικών σελίδων που θα δημοσιευτούν στον Παγκόσμιο Ιστό (WWW) για πρόσβαση από άλλους. Αυτές οι σημάνσεις λένε στα προγράμματα περιήγησης πώς να εμφανίζουν τα περιεχόμενα μιας ιστοσελίδας. Τέτοιες σελίδες μπορεί να περιέχουν απλό κείμενο, εικόνες, υπερσυνδέσμους προς άλλες σελίδες, βίντεο και άλλες πληροφορίες πολυμέσων. Όταν δημοσιεύεται μια ιστοσελίδα, μπορείτε να ρίξετε μια ματιά στον κώδικα σήμανσης πίσω από αυτήν, προβάλλοντας την πηγή της σελίδας της. Τα σύγχρονα προγράμματα περιήγησης επιτρέπουν την επιθεώρηση κάθε ενότητας μιας ιστοσελίδας όπου έχει επεξεργαστεί κάθε υποδιαίρεση ή στοιχείο σήμανσης στην πηγή HTM.

## Σύντομη ιστορία της HTM

Από την έναρξή του και τον πρώτο του ρόλο, οι προδιαγραφές HTML διατηρήθηκαν από την Κοινοπραξία Παγκόσμιου Ιστού (W3C) από το 1996. Το 2000, έγινε επίσης διεθνές πρότυπο (ISO/IEC 15445:2000). Το 1999 δημοσιεύτηκε η HTML 4.01. Το 2004, η Ομάδα Εργασίας Τεχνολογίας Εφαρμογών Web Hypertext (WHATWG) άρχισε να εργάζεται για την έκδοση HTML5 που έγινε κοινό παραδοτέο με το W3C το 2008. Ολοκληρώθηκε και τυποποιήθηκε στις 28 Οκτωβρίου 2014.

## Μορφή αρχείου HTML

Ένα έγγραφο HTML 4 αποτελείται από τρία μέρη:

1. μια γραμμή που περιέχει πληροφορίες έκδοσης HTML
1. μια δηλωτική ενότητα κεφαλίδας
1. ένα σώμα, το οποίο περιέχει το πραγματικό περιεχόμενο του εγγράφου. Το σώμα μπορεί να υλοποιηθεί από το στοιχείο BODY ή το στοιχείο FRAMESET για να περιέχει το σώμα σε πλαίσια

Κάθε ενότητα μπορεί να οδηγείται ή να ακολουθείται από λευκά κενά, νέες γραμμές, καρτέλες και σχόλια. Ένα παράδειγμα απλού εγγράφου HTML είναι όπως φαίνεται παρακάτω:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Πληροφορίες έκδοσης

Η πρώτη γραμμή κώδικα,<!DOCTYPE html> , ονομάζεται δήλωση doctype και λέει στο πρόγραμμα περιήγησης σε ποια έκδοση HTML είναι γραμμένη η σελίδα. Ανάλογα με την έκδοση της HTML, υπάρχει ένας αριθμός διαφορετικών δηλώσεων doctype που ονομάζουν τον ορισμό τύπου εγγράφου (DTD) που χρησιμοποιείται για το έγγραφο. Κάθε DTD διαφέρει από τα άλλα ως προς τα στοιχεία που υποστηρίζει και διαφέρει ως εξής:

* HTML 4.01 Strict - περιλαμβάνει όλα τα στοιχεία και τα χαρακτηριστικά που δεν έχουν [καταργηθεί](https://www.w3.org/TR/html401/conform.html#deprecated) ή δεν εμφανίζονται σε έγγραφα σετ πλαισίων
* HTML 4.01 Transitional - περιλαμβάνει τα πάντα στο αυστηρό DTD συν καταργημένα στοιχεία και χαρακτηριστικά (τα περισσότερα από τα οποία αφορούν την οπτική παρουσίαση
* Σύνολο πλαισίων HTML 4.01 - περιλαμβάνει επίσης τα πάντα στα μεταβατικά πλαίσια DTD συν

Για **HTML5**, οι πληροφορίες έκδοσης είναι απλώς όπως αναφέρονται παρακάτω.

```
<!DOCTYPE html>
```

### Πληροφορίες κεφαλίδας

Η κεφαλίδα ενός εγγράφου HTML μπορεί να περιλαμβάνει έναν αριθμό στοιχείων HTML που δεν αποδίδονται από το πρόγραμμα περιήγησης. Τέτοια στοιχεία είναι είτε μεταδεδομένα που περιγράφουν πληροφορίες σχετικά με τη σελίδα είτε περιλαμβάνουν ενότητες που χρησιμοποιούνται για την ανάκτηση πληροφοριών από εξωτερικούς πόρους όπως φύλλα στυλ CSS ή αρχεία JavaScript. Η κεφαλίδα μιας σελίδας αντιπροσωπεύεται από το \<head> ετικέτα και τελειώνει με \</head> ετικέτα.

<html>Για να ορίσετε τον τίτλο της σελίδας, το \<title> Το στοιχείο είναι το μόνο που απαιτείται στις ετικέτες \<head>. Το ίδιο χρησιμοποιείται από τις μηχανές αναζήτησης για τον προσδιορισμό του τίτλου μιας σελίδας. </html>

### Πληροφορίες σώματος

Αυτή είναι η κύρια ενότητα του αρχείου που περιέχει όλα τα περιεχόμενα του αρχείου που αποδίδονται από προγράμματα περιήγησης. Το σώμα HTML μπορεί να περιέχει σημάνσεις που μπορούν να αναφέρονται σε διάφορα δομικά στοιχεία σε σχήμα ετικετών. Μπορεί να περιέχει πολλούς διαφορετικούς τύπους πληροφοριών όπως κείμενο, εικόνες, χρώματα, γραφικά κ.λπ. Επιπλέον, στοιχεία ήχου και βίντεο μπορούν επίσης να ενσωματωθούν στο σώμα html για απόδοση από προγράμματα περιήγησης. Παρουσία εφαρμογής μοντέρνων φύλλων στυλ για οπτική αναπαράσταση, τα χαρακτηριστικά παρουσίασης του BODY όπως το χρώμα φόντου, το χρώμα συνδέσμου, το χρώμα κειμένου κ.λπ. έχουν καταργηθεί. Έτσι, τα ίδια εφέ μπορούν να επιτευχθούν χρησιμοποιώντας φύλλα στυλ όπως φαίνεται παρακάτω:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Τα ενσωματωμένα φύλλα στυλ είναι εύκολο να ενσωματωθούν και για γρήγορες εφαρμογές στα οπτικά εφέ, τα εξωτερικά φύλλα στυλ καθιστούν πιο εύκολη την ανάπτυξη μία φορά και την πρόσβαση σε πολλά σημεία.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Στοιχεία HTML

Όπως αναφέρθηκε προηγουμένως, τα περιεχόμενα μέσα στο σώμα HTML αντιπροσωπεύονται από ετικέτες, γνωστές και ως στοιχεία Html. Κάθε ετικέτα μπορεί να έχει πρόσθετες πληροφορίες με τη μορφή χαρακτηριστικών που γράφονται ως
```
<tag attribute1#"value1" attribute2#"value2">
```
αν και δεν είναι απαραίτητο να υπάρχουν χαρακτηριστικά με κάθε ετικέτα. Εάν δεν αναφέρονται χαρακτηριστικά, χρησιμοποιούνται προεπιλεγμένες τιμές σε κάθε περίπτωση. Ακολουθούν μερικά από τα παραδείγματα του Στοιχείου:

#### Κεφαλίδα

```
<head>
  <title>The Title</title>
</head>
```

#### Επικεφαλίδες

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Παράγραφοι

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## βιβλιογραφικές αναφορές

* [The Global Structure of HTML document](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

