{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο P7S - Μήνυμα ηλεκτρονικού ταχυδρομείου με ψηφιακή υπογραφή",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου P7S και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Τι είναι ένα αρχείο P7S;

Ένα αρχείο P7S είναι μια ψηφιακή υπογραφή που λαμβάνεται με ένα ψηφιακά υπογεγραμμένο email. Η παρουσία αυτού του αρχείου ως συνημμένου με το email επαληθεύει ότι το email έχει σταλεί από αυθεντική πηγή. Αυτό διασφαλίζει ότι ο αποστολέας έχει εγκατεστημένο στον υπολογιστή του ένα πιστοποιητικό υπογραφής email. Όταν αποστέλλεται ένα τέτοιο υπογεγραμμένο email από τον υπολογιστή του χρήστη, επισυνάπτεται το αρχείο P7S που περιέχει το όνομα του αποστολέα. Οι πελάτες ηλεκτρονικού ταχυδρομείου που υποστηρίζουν υπογεγραμμένα email μπορούν να δουν τις πληροφορίες του αποστολέα.

## Μορφή αρχείου P7S - Περισσότερες πληροφορίες

S/MIME (Ασφαλείς/Πολλαπλές Επεκτάσεις αλληλογραφίας Διαδικτύου) Τα αρχεία P7S περιέχουν τις πληροφορίες σε μορφή απλού κειμένου που είναι αναγνώσιμη από τον άνθρωπο. Τα προγράμματα-πελάτες ηλεκτρονικού ταχυδρομείου όπως το Microsoft Outlook, το Apple Mail και το Mozilla Thunderbird υποστηρίζουν την ανάγνωση των ψηφιακά υπογεγραμμένων πληροφοριών από ένα μήνυμα ηλεκτρονικού ταχυδρομείου S/MIME. Η υπογραφή ενός email επαληθεύει την ταυτότητα του αποστολέα και ενημερώνει τον παραλήπτη ότι το μήνυμα είναι αυθεντικό. Όταν γίνεται λήψη μηνυμάτων ηλεκτρονικού ταχυδρομείου από προγράμματα-πελάτες ηλεκτρονικού ταχυδρομείου (είτε ως [EML](/el/email/eml/) είτε ως [MSG](/el/email/msg/)), αυτά τα αρχεία P7S βρίσκονται συνημμένα με αυτά τα μηνύματα ηλεκτρονικού ταχυδρομείου.

Ένα αρχείο P7S περιέχει τις ακόλουθες πληροφορίες:

* Πηγή προέλευσης του email
* Ημερομηνία και ώρα αποστολής,
* Εάν έχει τροποποιηθεί κατά τη μετάδοση

Αυτές οι πληροφορίες ενσωματώνονται χρησιμοποιώντας την τεχνολογία Δημοσίου Κλειδιού Κρυπτογραφίας Standard #7 (PKCS7) για την ψηφιακή επισύναψη των κρυπτογραφημένων υπογραφών στο email.

## Βιβλιογραφικές αναφορές ##

* [Εργαλείο υπογραφής Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

