{
  "date" : "2021-05-24",
  "keywords" :["xht", "Αρχείο", "Επέκταση", "Μορφή αρχείου", "Επέκταση αρχείου", "εκτεταμένη γλώσσα σήμανσης υπερκειμένου"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XHT και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XHT.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Τι είναι ένα αρχείο XHT;

Ένα αρχείο με επέκταση .xht είναι ένα αρχείο ιστού που σχετίζεται με τον τύπο αρχείου [XHTML](/el/web/xhtml/) (Extended Hypertext Markup Language), ο οποίος είναι ένα αρχείο σήμανσης που βασίζεται σε [XML](/el/web/xml/). Και τα δύο αυτά αρχεία είναι παρόμοια με την HTML, αλλά έχουν μια πιο αυστηρή σύνταξη που μοιάζει με XML. Τα αρχεία XHT έχουν σχεδιαστεί με τρόπο ώστε να είναι πιο δομημένα, περιλαμβάνουν λιγότερα σενάρια και είναι γενικά εκτός από τη χρήση των υπαρχουσών εγκαταστάσεων της XML.

## Μορφή αρχείου XHT

Ένα αρχείο XHT δημιουργείται και αποθηκεύεται ως αρχείο απλού κειμένου με κωδικοποίηση UTF-8 από προεπιλογή. Περιέχει τον πλήρη πηγαίο κώδικα ενός εγγράφου XHTML που μπορεί να ανοίξει και να επεξεργαστεί με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου που υποστηρίζει κωδικοποίηση Unicode. Εκτός από τους επεξεργαστές κειμένου, η μορφή αρχείου XHT είναι κατανοητή από τα περισσότερα από τα σύγχρονα προγράμματα περιήγησης ιστού και μπορεί να ανοίξει χρησιμοποιώντας αυτά.

## Παράδειγμα XHT

Το ακόλουθο παράδειγμα ενός εγγράφου XHT ορίζει τις δηλώσεις XML.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Βιβλιογραφικές αναφορές ##

* [A History of XHTML: From the 1990 to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)
