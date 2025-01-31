{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "extension", "file format", "CSharp", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Αρχείο κώδικα CSharp",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο CS;

Τα αρχεία με επέκταση .cs είναι αρχεία πηγαίου κώδικα για τη γλώσσα προγραμματισμού C#. Παρουσιάστηκε από τη Microsoft για χρήση με το .NET Framework, η μορφή αρχείου παρέχει τη γλώσσα προγραμματισμού χαμηλού επιπέδου για τη σύνταξη κώδικα που μεταγλωττίζεται για τη δημιουργία του τελικού αρχείου εξόδου με τη μορφή EXE ή DLL. Αυτά μπορούν να δημιουργηθούν και να μεταγλωττιστούν με το Microsoft Visual Studio. Το Microsoft Visual Studio Express μπορεί επίσης να χρησιμοποιηθεί για τη δημιουργία και ενημέρωση τέτοιων αρχείων που είναι δωρεάν IDE. Τα αρχεία CS χρησιμοποιούνται για την ανάπτυξη εφαρμογών που μπορεί να κυμαίνονται από απλές εφαρμογές επιφάνειας εργασίας έως πιο σύνθετα προγράμματα. Ένα απλό έργο Visual Studio [λύση](/el/programming/sln/) που δημιουργήθηκε με γλώσσα C# μπορεί να αποτελείται από ένα ή περισσότερα τέτοια αρχεία. Τα αρχεία που έχουν επισημανθεί για συμπερίληψη στη μεταγλώττιση παρατίθενται στο αρχείο [CSPROJ](/el/programming/csproj/) που αποτελεί μέρος του έργου και λέει στον μεταγλωττιστή να χρησιμοποιήσει τα επισημασμένα αρχεία.

## Μορφή αρχείου CS ##

Τα αρχεία CS είναι μορφές αρχείων που βασίζονται σε κείμενο και μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου για επεξεργασία. Ωστόσο, όταν ανοίγεται σε ένα υποστηριζόμενο IDE με σωστή επισήμανση σύνταξης, ο κώδικας είναι εύκολο να διαβαστεί και να τακτοποιηθεί. Ένα απλό αρχείο CS περιέχει:

* Δήλωση χώρων ονομάτων - Για αναφορά σε μια συγκεκριμένη λειτουργία που ορίζεται από τον συγκεκριμένο χώρο ονομάτων
* Δήλωση μεταβλητών - Για να δηλώσετε μεταβλητές επιπέδου κλάσης για τη συγκεκριμένη υλοποίηση
* Δήλωση μεθόδων - Για να δηλώσετε δήλωση μεθόδων για τη συγκεκριμένη λειτουργικότητα

### Σύνταξη ###

* Τα ερωτηματικά χρησιμοποιούνται για να δηλώσουν το τέλος μιας πρότασης.
* Οι σγουρές αγκύλες χρησιμοποιούνται για την ομαδοποίηση δηλώσεων. Οι δηλώσεις συνήθως ομαδοποιούνται σε μεθόδους (συναρτήσεις), μεθόδους σε κλάσεις και κλάσεις σε χώρους ονομάτων.
* Οι μεταβλητές εκχωρούνται χρησιμοποιώντας ένα σύμβολο ίσου, αλλά συγκρίνονται χρησιμοποιώντας δύο διαδοχικά σύμβολα ίσου.
* Οι αγκύλες χρησιμοποιούνται με πίνακες, τόσο για τη δήλωση τους όσο και για τη λήψη μιας τιμής σε έναν δεδομένο δείκτη σε έναν από αυτούς.

### Παράδειγμα ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

