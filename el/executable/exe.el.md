{
  "date" : "2021-06-30",
  "keywords" :[ "αρχείο exe", "μορφή αρχείου exe", "τι είναι αρχείο exe", "αρχείο", "παράδειγμα exe", "επέκταση αρχείου exe", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ένα αρχείο .exe είναι ένα εκτελέσιμο αρχείο της Microsoft που εκτελείται σε λειτουργικό σύστημα Windows. Μάθετε περισσότερα για τη μορφή αρχείου EXE.",
  "title" :"Τι είναι ένα εκτελέσιμο αρχείο EXE;",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Τι είναι ένα αρχείο EXE;

Η λέξη EXE είναι σύντομη για το **εκτελέσιμο**. Ένα αρχείο .exe είναι ένα πρόγραμμα που μπορεί να εκτελεστεί σε λειτουργικό σύστημα Microsoft Windows. Οι προγραμματιστές εφαρμογών δημοσιεύουν κυρίως τα προγράμματά τους για λειτουργικό σύστημα Windows σε εκτελέσιμη μορφή ως αρχεία exe. Είναι η τυπική μορφή αρχείου για την εκτέλεση εφαρμογών στα Windows. Τα **Setup.exe**, **Install.exe** και **cmd.exe** είναι μερικά κοινά και γνωστά ονόματα αρχείων EXE.

## Μορφή αρχείου EXE

Οι μεταγλωττιστές MS-DOS εισήχθησαν με τα μοντέλα μνήμης να έχουν περιορισμό μνήμης 64K. Η γενική ιδέα είναι να ορίσετε διαφορετικούς καταχωρητές τμημάτων στη CPU x86 (CS, DS, ES, SS) ώστε να δείχνουν στα διαφορετικά ή ίδια τμήματα, επιτρέποντας επομένως διάφορους βαθμούς πρόσβασης στη μνήμη. Μερικά συγκεκριμένα μοντέλα μνήμης ήταν:

- **Tiny**: Όλες οι προσβάσεις στη μνήμη είναι 16-bit (οι καταχωρητές τμημάτων δεν έχουν αλλάξει). Παράγει ένα αρχείο .COM αντί για ένα αρχείο .EXE.
- **Μικρό**: Όλες οι προσβάσεις στη μνήμη είναι 16-bit (οι καταχωρητές τμημάτων δεν έχουν αλλάξει).
- **Συμπαγής**: Οι διευθύνσεις δεδομένων περιλαμβάνουν τμήμα και μετατόπιση, επαναφόρτωση των καταχωρητών DS ή ES κατά την πρόσβαση και επιτρέποντας έως και 1M δεδομένων. Οι προσβάσεις κώδικα δεν αλλάζουν τον καταχωρητή CS, επιτρέποντας 64K κώδικα.
- **Μεσαίο**: Οι διευθύνσεις κώδικα περιλαμβάνουν τη διεύθυνση τμήματος, επαναφόρτωση CS κατά την πρόσβαση και επιτρέποντας έως και 1M κώδικα. Οι προσβάσεις δεδομένων δεν αλλάζουν τους καταχωρητές DS και ES, επιτρέποντας 64K δεδομένων.
- **Μεγάλο**: Τόσο οι διευθύνσεις κώδικα όσο και οι διευθύνσεις δεδομένων είναι ζεύγη (τμήμα, μετατόπιση), πάντα φορτώνοντας ξανά τις διευθύνσεις τμημάτων. Ολόκληρος ο χώρος μνήμης 1M byte είναι διαθέσιμος τόσο για κώδικα όσο και για δεδομένα.
- **Τεράστιο**: Το ίδιο με το μεγάλο μοντέλο, με πρόσθετη αριθμητική που δημιουργείται από τον μεταγλωττιστή για να επιτρέπεται η πρόσβαση σε πίνακες μεγαλύτερους από 64K.

Οι προγραμματιστές πρέπει να αποφασίσουν ποιο μοντέλο θα επιλεγεί κατά τη δημιουργία ενός αρχείου exe.

### Φορητή μορφή αρχείου EXE

Η φορητή μορφή εκτελέσιμου αρχείου (PE) περιέχει έναν αριθμό ενημερωτικών κεφαλίδων, η ακόλουθη είναι η λίστα των κεφαλίδων:

- **Κεφαλίδα DOS**: Η κεφαλίδα MS-DOS διασφαλίζει είτε συμβατότητα προς τα πίσω είτε χαριτωμένη μείωση των νέων τύπων αρχείων.
- **Κεφαλίδα PE**: Σε μετατόπιση 60 (0x3C) από την αρχή της κεφαλίδας DOS είναι ένας δείκτης προς την κεφαλίδα αρχείου PE
- **COFF Header**: Η κεφαλίδα COFF έχει κάποιες πληροφορίες που είναι χρήσιμες σε ένα εκτελέσιμο αρχείο και κάποιες πληροφορίες που είναι πιο χρήσιμες σε ένα αρχείο αντικειμένου.
- **Προαιρετική κεφαλίδα PE**: Η προαιρετική κεφαλίδα PE εμφανίζεται αμέσως μετά την κεφαλίδα COFF και ορισμένες πηγές εμφανίζουν ακόμη και τις δύο κεφαλίδες ως μέρος της ίδιας δομής.
- **Πίνακας Ενοτήτων**: Αμέσως μετά το PE Optional Header βρίσκουμε έναν πίνακα ενοτήτων. Ο πίνακας ενοτήτων αποτελείται από έναν πίνακα δομών IMAGE_SECTION_HEADER.
- **Ενότητες με δυνατότητα χαρτογράφησης**: Μπορεί να εξοικονομήσει χώρο στη μνήμη αντιστοιχίζοντας τον κώδικα μιας βιβλιοθήκης σε περισσότερες από μία διεργασίες.

## Μπορείτε να εκτελέσετε ένα αρχείο EXE σε Mac;

Τα αρχεία exe δεν χρησιμοποιούνται ως εκτελέσιμα στο Mac OS. Ωστόσο, εάν θέλετε να εκτελέσετε ένα αρχείο exe σε Mac OS, μπορούν να χρησιμοποιηθούν οι ακόλουθες μέθοδοι.

1. **Wine** - Το κρασί είναι η τέλεια λύση για άτομα που θέλουν να χρησιμοποιήσουν τις εφαρμογές υπολογιστή τους σε συστήματα Mac. Είναι ένα αρκτικόλεξο που σημαίνει "Wine Is Not A Emulator", που σημαίνει. Το Wine δημιουργεί το ίδιο περιβάλλον καταλόγων που χρησιμοποιεί η Microsoft, ώστε να μπορείτε να εκτελέσετε την εφαρμογή Windows χρησιμοποιώντας το.
2. **Virtual Machines** - Δημιουργήστε μια εικονική μηχανή Windows χρησιμοποιώντας Parallel Desktop ή VM Virtual Box και εκτελέστε την εφαρμογή σας μέσα στην εικονική μηχανή.
3. **Boot Camp** - Η εγκατάσταση και η διαμόρφωση των Windows Boot Camp σε Mac OS σάς επιτρέπει να εκτελείτε το λειτουργικό σύστημα Windows σε μηχάνημα Mac.

## βιβλιογραφικές αναφορές

* [.exe- από τη Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

