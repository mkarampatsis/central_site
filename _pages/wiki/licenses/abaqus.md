---
layout: wiki
title: Abaqus
permalink: /abaqus/
---
### ABAQUS
{: .top-buffer }

Το ABAQUS είναι μια ομάδα προγραμμάτων που μοντελοποιούν και αναλύουν πάσης φύσεως διατάξεις στον τομέα της μηχανικής, βασισμένο στην μέθοδο πεπερασμένων στοιχείων. Είναι διαθέσιμο στην αγορά από την εταιρία Dassault Systèmes, μέρος των λογισμικών SIMULIA Product Life-cycle Management (PLM). Το πρόγραμμα αυτό, μεταξύ άλλων, έχει τα ακόλουθα πλεονεκτήματα:

*   Περιέχει εκτεταμένη βιβλιοθήκη με στοιχεία τα οποία μπορούν να μοντελοποιήσουν πρακτικά οποιαδήποτε γεωμετρία.
*   Υπάρχει η δυνατότητα εισαγωγής γεωμετρίας από πολλά διαφορετικά πακέτα λογισμικού CAD.
*   Δυνατότητα χρήσης αρκετών διαφορετικών μοντέλων υλικών για μοντελοποίηση της συμπεριφοράς των πιο τυπικών από αυτά, όπως μέταλλα, ελαστικά, πολυμερή, σύνθετα υλικά, οπλισμένο σκυρόδεμα και γεωτεχνικά υλικά όπως είδη εδαφών και βράχος.
*   Είναι σχεδιασμένο ως εργαλείο μοντελοποίησης γενικής χρήσης, ενώ μπορεί να χρησιμοποιηθεί πέραν προβλημάτων τάσης/παραμόρφωσης. Μπορεί να μοντελοποιήσει προβλήματα σε τομείς όπως μεταφορά θερμότητας, διάχυση μάζας, θερμική διαχείριση σε ηλεκτρικονικά εξαρτήματα, ακουστική, πιεζοηλεκτρική ανάλυση και προβλήματα γεωλογίας.
*   Παρέχει μεγάλο εύρος δυνατοτήτων για μοντελοποίηση γραμμικών και μή γραμμικών εφαρμογών. Προβλήματα με πολλά μέλη μοντελοποιούνται με το να συσχετιστεί η γεωμετρία ορίζοντας κάθε μέλος με το αντίστοιχο υλικό και διευκρινίζοντας τις αλληλεπιδράσεις μεταξύ των μελών. Στη μη γραμμική ανάλυση, το Abaqus επιλέγει αυτόματα τα κατάλληλα επαυξητικά βήματα ανάλυσης και ανοχής για κάθε φορτίο και τα προσαρμόζει συνεχώς κατά την πορεία της ανάλυσης για να επιβεβαιώνει ότι επιτυγχάνεται μια ακριβής επίλυση.
*   Δυνατότητα στατικής και δυναμικής ανάλυσης.

Το Abaqus σε σχέση με το ANSYS έχει πολύ καλή απόκριση σε μη-γραμμικά και περίπλοκα γεωμετρικά προβλήματα. Κατ’ ακρίβειαν, δημιουργήθηκε με σκοπό την επίλυση μη-γραμμικών προβλημάτων. Χρησιμοποιείται περισσότερο στον ακαδημαϊκό τομέα διότι υπάρχει η ευκολία στο να δημιουργήσει ο χρήστης υλικά με συγκεκριμένες ιδιότητες, όπως στην συγκεκριμένη εφαρμογή με το ψεκασμό πλάσματος μπορούμε να δημιουργήσουμε υλικά με κράμα κεραμικών. Τα άλλα προγράμματα χρησιμοποιούνται περισσότερο στη βιομηχανία, διότι έχουν συγκεκριμένα υλικά με συγκεκριμένες ιδιότητες, όπως μέταλλα. Επίσης στο Abaqus υπάρχει η ρουτίνα UEL. To Abaqus λειτουργεί με στιγμές (instances), δηλαδή το που βρίσκεται το κάθε κομμάτι της διάταξης σε δεδομένη στιγμή, οπότε με αυτό τον τρόπο μπορούν να γίνουν διαφορετικά βήματα ανάλυσης σε κάθε πρόβλημα.

Η Simulia παρέχει πολύ καλή υποστήριξη στους χρήστες σε σχέση με τα άλλα προγράμματα, ενώ υπάρχουν ολοκληρωμένα εγχειρίδια τα οποία επιτρέπουν στο χρήστη πρόσβαση σε οποιαδήποτε πληροφορία ψάχνει. Υπάρχει επίσης η δυνατότητα ενσωμάτωσης κι άλλων προγραμμάτων όπως την πλατφόρμα CATIA για εφαρμογές PLM, αλλάζοντας ουσιαστικά τον τρόπο σχεδίασης, ανάπτυξης και κατασκευής χρησιμοποιώντας τα πακέτα αυτά.

Το Abaqus επιτρέπει στο χρήστη να δημιουργεί το πρόγραμμα (script) μέσω της γλώσσας Python για δημιουργία μοντέλων. Το Python είναι γλώσσα προγραμματισμού ευρείας χρήσης και ανεξάρτητη. Οτιδήποτε μπορεί να δημιουργηθεί στο Abaqus/CAE χρησιμοποιώντας GUI (graphic user interface), μπορεί επίσης να δημιουργηθεί γράφοντας κώδικα. Επιπλέον το Abaqus επιτρέπει στο χρήστη να δημιουργεί κώδικα γραμμένο στο C++ για γρήγορη επεξεργασία σε δεύτερο στάδιο.

Μειονεκτήματα: υστερεί στο ότι δεν είναι τόσο φιλικό στο χρήστη. Χρειάζεται αρκετά βαθιά κατανόηση μη-γραμμικής ανάλυσης. Τα υλικά πρέπει να ορίζονται πλήρως όσον αφορά τις ιδιότητες τους, κάτι που καθιστά το ΑΒΑQUS λιγότερο εύχρηστο για τη βιομηχανία.

[πηγή](https://dspace.lib.ntua.gr/dspace2/bitstream/handle/123456789/39744/ierodiaconou.pdf?sequence=1)

#### Διαθέσιμες Άδειες

Οι διαθέσιμες άδειες για τη σουΐτα των προγραμμάτων του Abaqus είναι οι παρακάτω

| Πρόγραμμα | Τύπος χρήσης | Αριθμός αδειών |
|-----------|--------------|----------------|
| &nbsp;    | Research     | Base License   |
| CAE       | Research     | 3+1            |
| Analysis  | Reseach      | 64+5 Tokens    |
{: .table }
{: .table-striped }

#### Download των λογισμικών

Τα λογισμικά της Dassault Systemes που συνθέτουν τη σουΐτα του Abaqus είναι διαθέσιμα μετά από έλεγχο πρόσβασης στον ftp server του Κέντρου Ηλεκτρονικών Υπολογιστών [ftp.central.ntua.gr](ftp://ftp.central.ntua.gr). Μετά τον επιτυχή έλεγχο πρόσβασης επιλέγετε την έκδοση που σας ενδιαφέρει και μεταφορτώνετε στον υπολογιστή σας τα αρχεία `.tar`. Για τον έλεγχο της ορθότητας των αρχείων που κατεβάσατε χρησιμοποιήστε το αρχείο με τα `md5 sums`.

Τα ίδια αρχεία μπορούν να χρησιμοποιηθούν για εγκατάσταση τόσο σε πλατφόρμα Windows όσο και σε πλατφόρμα Linux.

![](/assets/img/wiki/licenses/abaqus/download/abaqus0.png)

![](/assets/img/wiki/licenses/abaqus/download/abaqus1.png)

Σας συνιστούμε να αποθηκεύσετε τα αρχεία σε κάποιο κατάλογο και να τα αποσυμπιέσετε σε αυτόν όποτε να δημιουργηθούν δύο κατάλογοι. Στον ένα κατάλογο `AM_DOC_SIM_EstPrd.AllOS` βρίσκεται το Documentation ενώ στο άλλο κατάλογο `AM_SIM_Abaqus.AllOS` βρίσκονται τα προγράμματα.

![](/assets/img/wiki/licenses/abaqus/download/abaqus2.png)

Hint: Ξεκινήστε με την εγκατάσταση του Documentation γιατί αυτό είναι απαραίτητο για την αποτελεσματική πρόσβαση στη βοήθεια μέσα από το πρόγραμμα.

#### Documentation

Ξεκινήστε την εγκατάσταση επιλέγοντας το κατάλληλο αρχείο για την πλατφόρμα σας από τον παρακάτω κατάλογο:

![](/assets/img/wiki/licenses/abaqus/doc/folder0.png)

Η εγκατάσταση είναι μια απλή σειρά αποδοχής των εξορισμού επιλογών εκτός από την 5η εικόνα όπου θα πρέπει να συμπληρώσετε το όνομα του υπολογιστή σας.

![](/assets/img/wiki/licenses/abaqus/doc/abaqus0.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus1.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus2.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus3.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus4.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus5.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus6.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus7.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus8.png)

![](/assets/img/wiki/licenses/abaqus/doc/abaqus9.png)

To Documentation θα είναι προσβάσιμο μέσω κάποιου webbrowser στην τοπική πόρτα `2180`:

![](/assets/img/wiki/licenses/abaqus/doc/abaqus10.png)

#### Ειδικά για την εγκατάσταση σε Linux

Το Αbaqus 2016 έχει υϊοθετήσει μια νέα μέθοδο εγκατάστασης που αρνείται να προχωρήσει αν δεν βρεθεί διανομή RHEL ή SUSE με ένα μήνυμα σαν το παρακάτω:

```bash
christodoulos@ntuadesk:~$ /home/christodoulos/Downloads/abaqus6.16/AM_SIM_Abaqus.AllOS/1/CAA_3DEXPERIENCE_AbaqusSolver/Linux64/1/StartGUI.sh
CurrentMediaDir initial="/home/christodoulos/Downloads/abaqus6.16/AM_SIM_Abaqus.AllOS/1/CAA_3DEXPERIENCE_AbaqusSolver/Linux64/1"
CurrentMediaDir="/home/christodoulos/Downloads/abaqus6.16/AM_SIM_Abaqus.AllOS/1/CAA_3DEXPERIENCE_AbaqusSolver/Linux64/1"
Current operating system: "Linux"
DSY_OS_Release="Ubuntu"
Unknown linux release "Ubuntu"
exit 8
```

Για να προχωρήσει η εγκατάσταση θα πρέπει να γίνει μια μικρή αλλαγή στα αρχεία που φαίνονται στις παρακάτω διαδρομές (πρόκειται για το ίδιο αρχείο σε τρεις διαφορετικές διαδρομές):

![](/assets/img/wiki/licenses/abaqus/linuxmods/folder0.png)

![](/assets/img/wiki/licenses/abaqus/linuxmods/folder1.png)

![](/assets/img/wiki/licenses/abaqus/linuxmods/folder2.png)

Η επέμβαση που πρέπει να γίνει είναι να σχολιαστεί η τρίτη γραμμή και να εισαχθεί η τέταρτη όπως φαίνεται στην εικόνα:

![](/assets/img/wiki/licenses/abaqus/linuxmods/file.png)

#### Solvers

Μετακινηθείτε στον κατάλληλο φάκελο για την πλατφόρμα που χρησιμοποιείτε και επιλέξτε το πρόγραμμα της εγκατάστασης.

![](/assets/img/wiki/licenses/abaqus/solvers/folder0.png)

![](/assets/img/wiki/licenses/abaqus/solvers/folder1.png)

Προχωρήστε στην εγκατάσταση.

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus0.png)

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus1.png)

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus2.png)

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus3.png)

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus4.png)

![](/assets/img/wiki/licenses/abaqus/solvers/abaqus6.png)

#### CAE

Μετακινηθείτε στον κατάλληλο φάκελο για την πλατφόρμα που χρησιμοποιείτε και επιλέξτε το πρόγραμμα της εγκατάστασης.

![](/assets/img/wiki/licenses/abaqus/cae/folder0.png)

![](/assets/img/wiki/licenses/abaqus/cae/folder1.png)

Προχωρήστε στην εγκατάσταση.

![](/assets/img/wiki/licenses/abaqus/cae/abaqus0.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus1.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus2.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus3.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus4.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus5.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus6.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus7.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus8.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus9.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus10.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus11.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus12.png)

![](/assets/img/wiki/licenses/abaqus/cae/abaqus13.png)

Το περιβάλλον του Abaqus CAE είναι έτοιμο για χρήση:

![](/assets/img/wiki/licenses/abaqus/cae/abaqus14.png)
