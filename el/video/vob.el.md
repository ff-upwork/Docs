---
date: 2019-10-11
keywords: vob, .vob, μορφή αρχείου vob, μορφή αρχείου .vob, επέκταση .vob, επέκταση vob, μορφή βίντεο vob, αρχεία dvd vob
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Μάθετε για τη μορφή αρχείου VOB και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VOB."
title: Μορφή αρχείου VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Τι είναι ένα αρχείο VOB; ##

Τα αρχεία VOB αποθηκεύονται συνήθως στον κατάλογο VIDEO_TS σε ένα DVD με επέκταση .vob. Τα αρχεία VOB περιέχουν δεδομένα βίντεο και ήχου καθώς και άλλα δεδομένα όπως μενού και υπότιτλους. Το VOB βασίζεται στη μορφή ροής προγράμματος MPEG-2, αλλά έχει πρόσθετους περιορισμούς και προδιαγραφές σε ιδιωτικές ροές. Τα αρχεία VOB είναι ένα αυστηρό υποσύνολο των ροών προγραμμάτων MPEG, επομένως όλα τα αρχεία VOB είναι ροές προγραμμάτων MPEG, αλλά όλες οι ροές προγραμμάτων MPEG δεν είναι συμβατές με VOB.

## Δομή βίντεο DVD ##

Όταν ανοίγει ένα DVD σε έναν υπολογιστή, το VIDEO_TS είναι ο κατάλογος ανώτατου επιπέδου με AUDIO_TS. Το AUDIO_TS είναι κενό και δεν χρησιμοποιείται. Μέσα στον κατάλογο VIDEO_TS, υπάρχουν αρχεία VOB, BUP και IFO. Τα αρχεία VOB περιέχουν το περιεχόμενο MPEG. Αυτά χωρίζονται σε κομμάτια μεγέθους 1 GB ή μικρότερου ώστε να είναι συμβατά με όλα τα λειτουργικά συστήματα. Τα αρχεία IFO περιέχουν πληροφορίες σχετικά με τα μενού και τη δομή του τίτλου. Τα αρχεία BUK είναι αρχεία αντιγράφων ασφαλείας των αρχείων IFO με το ίδιο όνομα. Αυτά τα αρχεία προορίζονται να διατηρούνται σε χωριστή περιοχή φυσικά, έτσι ώστε σε περίπτωση που το αρχείο IFO καταστραφεί λόγω φυσικής βλάβης στο DVD, το αρχείο BUK μπορεί να παρέχει τις ίδιες πληροφορίες.

### Φυσική διάταξη ###

- Όλα τα αρχεία στο δίσκο πρέπει να είναι συνεχόμενα.
- Τα σχετικά αρχεία πρέπει να είναι το ένα δίπλα στο άλλο (VOB, IFO, BUP).
- Τα αριθμημένα αρχεία πρέπει να είναι σε αύξουσα σειρά.

## Προστασία αντιγραφής ##

Πολλά βίντεο DVD είναι κρυπτογραφημένα και εμποδίζουν την αντιγραφή δεδομένων από το DVD. Απαιτούνται κλειδιά ελέγχου ταυτότητας και αποκρυπτογράφησης για την αναπαραγωγή των αρχείων που βρίσκονται στη μη προσβάσιμη περιοχή εισόδου του DVD. Αυτά τα κλειδιά χρησιμοποιούνται από το λογισμικό αποκρυπτογράφησης CSS που υπάρχει στη συσκευή αναπαραγωγής DVD ή στη συσκευή αναπαραγωγής λογισμικού. Χωρίς τα πλήκτρα, τα αρχεία βίντεο δεν μπορούν να αναπαραχθούν καθώς τα πλήκτρα θα ζητηθούν όταν ανοίξουν τα αρχεία.

## Βιβλιογραφικές αναφορές ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

