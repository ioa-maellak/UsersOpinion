Εξαγωγή Θετικών και Αρνητικών απόψεων χρηστων.
----------------------------------------------

 

Δημιουργία συστήματος εξαγωγής της άποψης (από τα σχόλια στην Αγγλική γλώσσα)
των χρηστών με τη χρήση του **Rapidminer** v5.3.

![](<https://github.com/ioa-maellak/UsersOpinion/blob/master/images/rapidminer-logo.jpg>)

Το συστημα μας μπορει αν συνδιαστεί με οποιοδήποτε πληροφοριακό σύστημα που
μπορούν να εξαχθούν τα σχόλια των χρηστών π.χ φορουμ, blog ή διάφορα API
συστημάτων (π.χ youtube, twitter κλπ.) σε μορφή κειμένου.

Το σύστημα μας αποτελείται από δυο μερη. Το πρώτο κανει φιλτράρισμα του καθε
σχολίου και αποθήκευση μόνο των ουσιαστικών που έχει γράψει ο χρήστης
(αφαιρούνται άρθρα, ρήματα κι επίθετα). Το δεύτερο δημιουργει το μοντελο με
εκπαιδευση του με εφαρμογή βάσεων λέξεων θετικών και αρνητικών λέξεων και επειτα
το εφαρμοζει στα σχολια που εχουν εξαχθει απο το πρώτο μερος. Τέλος
δημιουργείται πίνακας που κατηγοριοποιεί αυτόματα τα σχόλια σε θετικά ή αρνητικά
και σε ποιό ποσοστό. Στην παρακάτω εικόνα παρουσιάζεται η παραπάνω μεθοδολογία
με γραφικό τρόπο.

 

![](<https://github.com/ioa-maellak/UsersOpinion/blob/master/images/method.jpg>)

Εικόνα 1. Μεθοδολογία

Text Filtering
--------------

Φιλτράρισμα κειμένου και εμφάνιση μόνο των ουσιαστικών (nouns) 2-25 χαρακτήρων.
Η πιο κάτω εικόνα παρουσιάζει την υλοποίηση στο Rapidminer.

 

![](<https://github.com/ioa-maellak/UsersOpinion/blob/master/images/keep-nouns.jpg>)

Εικόνα 2. Text Filtering

Opinion Mining
--------------

Δημιουργία Τraining Model και Διανύσματος Λέξεων Σχολίων. Εφαρμογή του μοντελου
στο διάνυσμα των λεξεων (ανα σχόλιο) κι αυτόματη κατηγοριοποιήση των σχολίων σε
θετικά και αρνητικά. Οι πιο κάτω εικόνες παρουσιάζουν την υλοποίηση στο
Rapidminer.

 

![](<https://github.com/ioa-maellak/UsersOpinion/blob/master/images/training_model.jpg>)

Εικόνα 3. Training Model (βασισμένο στο SVM Linear)

 

![](<https://github.com/ioa-maellak/UsersOpinion/blob/master/images/word-vector.jpg>)

Εικόνα 4. Word Vector List
