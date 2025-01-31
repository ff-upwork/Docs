{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου SLN και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι το αρχείο SLN;
Ένα αρχείο με επέκταση .SLN αντιπροσωπεύει μια λύση **Visual Studio** που διατηρεί πληροφορίες σχετικά με την οργάνωση των έργων σε ένα αρχείο λύσης. Τα περιεχόμενα ενός τέτοιου αρχείου λύσης γράφονται σε απλό κείμενο μέσα στο αρχείο και μπορούν να παρατηρηθούν/επεξεργασθούν ανοίγοντας το αρχείο σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Οι πληροφορίες που περιέχονται σε ένα αρχείο λύσης παραμένουν επίμονες και χρησιμοποιούνται για τη φόρτωση των πληροφοριών που σχετίζονται με τη λύση, όπως [projects ](/el/programming/csproj/)και οποιεσδήποτε άλλες απαιτούμενες πληροφορίες. Τα αρχεία έργου που αναφέρονται από το αρχείο λύσης περιέχουν πρόσθετες πληροφορίες για να ενεργοποιηθεί το περιβάλλον για τη συμπλήρωση της ιεραρχίας με τα στοιχεία αυτού του έργου. Δεν αποθηκεύονται δεδομένα στο αρχείο .sln, αν και οι πληροφορίες του έργου μπορούν να εγγραφούν στο αρχείο .sln, εάν απαιτείται.

## **Ιστορικό εκδόσεων SLN** ##

Η έκδοση μορφής λύσης έχει εξελιχθεί με κάθε λύση του Microsoft Visual Studio με το πέρασμα του χρόνου. Οι λεπτομέρειες σχετικά με αυτά έχουν ως εξής.


|Έκδοση Visual Studio|Έκδοση μορφής λύσης
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Περιεχόμενα ενός αρχείου λύσης** ###

Ένα αρχείο λύσης αποτελείται από πολλές ενότητες που διαβάζονται από το περιβάλλον για τη φόρτωση του έργου. Ένα δείγμα περιεχομένων αρχείου .sln είναι όπως φαίνεται παρακάτω.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Δήλωση έργου** ###

Ένα αρχείο λύσης μπορεί να περιέχει περισσότερες από μία δηλώσεις έργων και αυτή επίσης διαφορετικών τύπων έργου. Για παράδειγμα, ένα μεμονωμένο αρχείο λύσης μπορεί να περιέχει ένα έργο CSharp καθώς και ένα έργο VB.NET. Αυτοί οι τύποι διακρίνονται σε μια λύση χρησιμοποιώντας το [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Η παραπάνω δήλωση έργου μπορεί να γενικευτεί ως εξής για σαφή κατανόηση.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Το Project-Type-GUID είναι μοναδικό για διαφορετικούς τύπους έργων και χρησιμοποιείται από το πρόγραμμα ανάγνωσης λύσεων για τον προσδιορισμό του τύπου του έργου. Σε αυτήν την περίπτωση, το F184B08F-C81C-45F6-A57F-5ABD9991F28F δείχνει ότι πρόκειται για έργο VB.NET.

`Project GUID:` Το μοναδικό GUID του έργου που το διαφοροποιεί από άλλα έργα στη λύση. Το μοναδικό αναγνωριστικό ενός έργου στη λύση επιτρέπει σε άλλα έργα στη λύση να έχουν πρόσβαση σε αυτό.

Με βάση τις πληροφορίες που περιέχονται στην ενότητα έργου του αρχείου .sln, το περιβάλλον φορτώνει κάθε αρχείο έργου. Στη συνέχεια, το ίδιο το έργο είναι υπεύθυνο για τη συμπλήρωση της ιεραρχίας του έργου και τη φόρτωση τυχόν ένθετων έργων. Οποιεσδήποτε αλλαγές γίνονται στη λύση αποθηκεύονται ξανά στο αρχείο λύσης κατά την αποθήκευση ή το κλείσιμο του έργου.

## Λύση Visual Studio VS έργο

**Έργο:** Λογικά, όταν ξεκινάτε να δημιουργείτε μια εφαρμογή ή λογισμικό χρησιμοποιώντας το Visual Studio, ξεκινάτε ένα νέο έργο. Ένα έργο περιέχει όλα τα απαραίτητα αρχεία, όπως πηγαίο κώδικα, εικονίδια, εικόνες, αρχεία δεδομένων και άλλα, που θα μεταγλωττιστούν σε μια εκτελέσιμη εφαρμογή, ιστότοπο ή βιβλιοθήκη.

**Λύση:** Μια λύση περιέχει ένα ή περισσότερα έργα. Έτσι, η λύση είναι ακριβώς σαν ένα κοντέινερ για έργα Visual Studio. Λογικά, μπορούμε να πούμε ότι κάποιος θέλει να βρει μια ολοκληρωμένη λύση για την επιχείρησή του, συμπεριλαμβανομένων ενός ιστότοπου, μιας εφαρμογής για υπολογιστές, μιας ξεκούραστης υπηρεσίας και μιας εφαρμογής για κινητά.

### **Βιβλιογραφικές αναφορές** ###

* [Αρχείο λύσης - Από MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

