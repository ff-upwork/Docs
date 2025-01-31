---
date: 2019-10-11
keywords: flv, .flv, μορφή αρχείου flv, μορφή αρχείου .flv, επέκταση .flv, επέκταση flv, μορφή βίντεο flv
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Μάθετε για τη μορφή αρχείου FLV και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FLV."
title: Μορφή αρχείου FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Τι είναι ένα αρχείο FLV; ##

Το FLV (Flash Video) είναι μια μορφή αρχείου κοντέινερ με επέκταση .flv. Το FLV χρησιμοποιείται για την παράδοση περιεχομένου ήχου/βίντεο μέσω του Διαδικτύου χρησιμοποιώντας το Adobe Flash Player ή το Adobe Air. Τα δεδομένα στα αρχεία FLV κωδικοποιούνται με τον ίδιο τρόπο όπως τα αρχεία SWF. Η άμεση υποστήριξη προστέθηκε στο Flash Player 7 το 2003. Τα συστήματα της Adobe δημιούργησαν το F4V το 2007 λόγω των περιορισμών του FLV.

### Κωδικοποίηση ###

Τα αρχεία FLV περιέχουν bitstreams βίντεο του Sorenson Spark που είναι μια αποκλειστική παραλλαγή του προτύπου βίντεο H.263. Είναι η απαιτούμενη μορφή συμπίεσης για το Flash Player 6 και 7. Η έκδοση 8 του Flash Player υποστηρίζει ροές bit βίντεο On2 TrueMotion VP6. Είναι η προτεινόμενη μορφή συμπίεσης για Flash Player 8 και νεότερη έκδοση. Το FLV υποστηρίζει ήχο σε MP3, Nellymoser Asao Codec και τον κωδικοποιητή ανοιχτού κώδικα Speex. Υποστηρίζει επίσης ασυμπίεστο ήχο ή ήχο μορφής ADPCM. Το AAC (HE-AAC/AAC SBR, AAC Main Profile και AAC-LC) υποστηρίζονται από τις πρόσφατες εκδόσεις του Flash Player 9.

## Δομή ##

Τα αρχεία FLV αποτελούνται από κεφαλίδα και πακέτα. Ένα αρχείο FLV ξεκινά με την κεφαλίδα. Η κεφαλίδα έχει τα ακόλουθα πεδία.

- **Υπογραφή**: Η τιμή του είναι FLV
- **Έκδοση**: Η προεπιλεγμένη τιμή του είναι 1. Μόνο 0x01 ισχύει.
- **Σημαίες**: Το 0x04 χρησιμοποιείται για ήχο και το 0x01 για βίντεο, επομένως το 0x05 χρησιμοποιείται τόσο για ήχο όσο και για βίντεο.
- **Μέγεθος κεφαλίδας**: Η προεπιλεγμένη τιμή είναι 9. Χρησιμοποιείται για την παράλειψη μιας νεότερης διευρυμένης κεφαλίδας.

Μετά την κεφαλίδα έρχονται τα Πακέτα. Το αρχείο FLV χωρίζεται σε πολλαπλά πακέτα που ονομάζονται ετικέτες FLV που έχουν κεφαλίδες 15 byte. Τα πακέτα περιέχουν τα μεταδεδομένα για ήχο, βίντεο, σενάρια, πληροφορίες κρυπτογράφησης και ωφέλιμο φορτίο. Τα πακέτα FLV έχουν τα ακόλουθα πεδία.

- **Δέσμευση**: Προορίζεται για FMS και πρέπει να είναι 0.
- **Φίλτρο**: Υποδεικνύει εάν τα πακέτα είναι φιλτραρισμένα ή όχι.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Τύπος πακέτου**: Αυτό καθορίζει τον τύπο περιεχομένου στο πακέτο.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Μέγεθος δεδομένων**: Αυτό υποδηλώνει τη διάρκεια του μηνύματος.
- **Χαμηλότερη σήμανση χρόνου**: Αυτό αποθηκεύει τη χρονική σήμανση σε χιλιοστά του δευτερολέπτου στα οποία ισχύουν τα δεδομένα της ετικέτας. Έχει οριστεί σε NULL για το πρώτο πακέτο.
- **Χρονική σήμανση Άνω**: Επέκταση για τη δημιουργία τιμής uint32_be.
- **Αναγνωριστικό ροής**: Έχει οριστεί σε NULL για την πρώτη ροή.
- **Δεδομένα ωφέλιμου φορτίου**: Αυτά είναι τα δεδομένα που βασίζονται στον τύπο του πακέτου.

## Βιβλιογραφικές αναφορές ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

