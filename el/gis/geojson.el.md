{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο geojson", "τι είναι ένα αρχείο geojson", "αρχείο", "παράδειγμα geojson", "επέκταση αρχείου geojson", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Μορφή γεωγραφικού αρχείου βάσει JSON",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου GeoJSON και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο GeoJSON;

Το GeoJSON είναι μια μορφή που βασίζεται σε JSON και έχει σχεδιαστεί για να αντιπροσωπεύει τα γεωγραφικά χαρακτηριστικά με τα μη χωρικά χαρακτηριστικά τους. Αυτή η μορφή ορίζει διαφορετικά αντικείμενα JSON (JavaScript Object Notation) και τον τρόπο σύνδεσής τους. Η μορφή JSON αντιπροσωπεύει μια συλλογική πληροφορία σχετικά με τα γεωγραφικά χαρακτηριστικά, τη χωρική τους έκταση και τις ιδιότητες. Ένα αντικείμενο αυτού του αρχείου μπορεί να υποδεικνύει μια γεωμετρία (Point, LineString, Πολύγωνο), ένα χαρακτηριστικό ή μια συλλογή χαρακτηριστικών. Τα χαρακτηριστικά αντικατοπτρίζουν διευθύνσεις και μέρη ως δρόμους σημείου, κύριους δρόμους και σύνορα ως συμβολοσειρές γραμμών και χώρες, επαρχίες και περιοχές γης ως πολύγωνα. Χρησιμοποιώντας το GeoJSON, διαφορετικές εφαρμογές δρομολόγησης και πλοήγησης για κινητά μπορούν να υποδείξουν την κάλυψη των υπηρεσιών τους. Μια επέκταση του GeoJSON είναι το TopoJSON που είναι μικρότερο σε μέγεθος και κωδικοποιεί τη γεωχωρική τοπολογία.

## Σύντομη Ιστορία ##

Η Ομάδα Εργασίας Μηχανικής Διαδικτύου (IETF), σε συνεργασία με τους συντάκτες της μορφής, διαμόρφωσαν ένα [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) για να κυκλοφορήσει το GeoJSON τον Απρίλιο του 2015. Αντικαθιστώντας το 2008 Προδιαγραφή GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), η νέα τυπική προδιαγραφή της μορφής GeoJSON που δημοσιεύτηκε τον Αύγουστο του 2016.

## Μορφή αρχείου GeoJSON ##

### Συντεταγμένος ###

Η συντεταγμένη είναι το βασικό στοιχείο οποιωνδήποτε γεωγραφικών δεδομένων. Αυτή είναι μια ενιαία διάσταση (Γεωγραφικό μήκος, γεωγραφικό πλάτος) που αντιπροσωπεύει έναν μόνο αριθμό (δεκαδική μορφή) και μερικές φορές καταγράφει μια συντεταγμένη για το υψόμετρο. Ο χρόνος είναι επίσης μια διάσταση, αλλά η πολυπλοκότητά του καθιστά δύσκολη την καταγραφή του ως συντεταγμένη. Οι συντεταγμένες και στα δύο JSON GeoJSON έχουν τη μορφή αριθμών.

### Θέση ###

Ένας διατεταγμένος πίνακας συντεταγμένων αντιπροσωπεύει τη [θέση](https://geojson.org/geojson-spec.html#positions). Αυτή είναι η μικρότερη μονάδα που μπορεί να υποδείξει ένα σημείο στη γη.

«[Γεωγραφικό μήκος, πλάτος, υψόμετρο]».

Πριν από την κυκλοφορία της τρέχουσας προδιαγραφής, η GeoJSON επέτρεπε την εγγραφή τριών συντεταγμένων ανά θέση, αλλά δεν επιτρέπεται από τη νέα προδιαγραφή.

### Γεωμετρία ###

Οι γεωμετρίες είναι απλά σχήματα (σημεία, καμπύλες και επιφάνειες) στο GeoJSON που αποτελούνται από έναν τύπο και μια συλλογή συντεταγμένων. Το σημείο είναι η απλούστερη γεωμετρία που αντιπροσωπεύει μια ενιαία θέση

`{ "type": "Point", "coordinates": [0, 0] }`

### Γραμμικές συμβολοσειρές ###

Τουλάχιστον δύο συνδεδεμένες θέσεις χρησιμοποιούνται για την αναπαράσταση μιας γραμμής.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Οι συμβολοσειρές σημείου και γραμμής είναι οι δύο απλούστερες κατηγορίες γεωμετρίας. Και οι δύο τύποι γεωμετρίας δεν ενοχλούν πολλούς γεωμετρικούς κανόνες. Ένα σημείο μπορεί να αναπαρασταθεί σε ένα μέρος οπουδήποτε, και μια γραμμή μπορεί να έχει περισσότερα από ένα σημεία, ακόμα κι αν τα σημεία διασταυρώνονται.

### Πολύγωνα ###

Οι γεωμετρίες GeoJSON φαίνονται πολύ πιο περίπλοκες στα Πολύγωνα. Τα πολύγωνα έχουν εσωτερικές και εξωτερικές περιοχές και μπορούν να έχουν τρύπες σε αυτό το εσωτερικό.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

Σε σύγκριση με το LineStrings, στα πολύγωνα, η λίστα των συντεταγμένων είναι ένα ακόμη επίπεδο ένθετο και μπορεί να έχει κοψίματα όπως ντόνατς.

### Επίπεδο συντεταγμένων ###

Σε μορφή GeoJSON, για την ιδιότητα συντεταγμένων, υπάρχουν τέσσερα επίπεδα βάθους.

### Χαρακτηριστικά ###

Οι γεωμετρίες είναι το κεντρικό μέρος του GeoJSON, επομένως, τα δεδομένα του πραγματικού κόσμου είναι περισσότερα από αυτά τα απλά σχήματα που έχουν ταυτότητα και χαρακτηριστικά. Τα χαρακτηριστικά καταγράφουν τη γεωμετρία καθώς και τις ιδιότητές τους.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Οι ιδιότητες ενός χαρακτηριστικού μπορεί να είναι ένας τύπος αντικειμένου [JSON](http://json.org/) που περιέχει αντιστοιχίσεις τιμών κλειδιού ενός βάθους.

### Συλλογή χαρακτηριστικών ###

Στο ανώτατο επίπεδο των αρχείων GeoJSON, το FeatureCollection είναι το πιο συνηθισμένο πράγμα που μοιάζει με:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Πολλά πακέτα λογισμικού χαρτογράφησης και GIS υποστηρίζουν το GeoJSON, συμπεριλαμβανομένων των λογισμικών GeoDjango, OpenLayers και Geoforge. Είναι επίσης συμβατό με PostGIS και Mapnik. Οι υπηρεσίες API των χαρτών Google, yahoo και Bing υποστηρίζουν επίσης GeoJSON.

## Βιβλιογραφικές αναφορές ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Από τη Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

