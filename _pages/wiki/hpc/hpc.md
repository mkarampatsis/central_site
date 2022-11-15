---
layout: wiki
title: HPC
permalink: /hpc/
---

### Γενικά
{: .top-buffer }

Το ΚΗΥ παρέχει πρόσβαση σε κεντρικά εγκατεστημένη υποδομή υπολογιστικού πλέγματος (Grid) και δίνει τη δυνατότητα εκτέλεσης εφαρμογών (engineering simulations) με υψηλές υπολογιστικές απαιτήσεις (High Performance Computing, HPC) σε όλους τους ερευνητές της Πολυτεχνειακής κοινότητας. Η χρήση της υποδομής του υπολογιστικού πλέγματος συμβάλει στη μέγιστη δυνατή αξιοποίηση των κεντρικά εγκατεστημένων υπολογιστικών συστημάτων υψηλής απόδοσης.

#### Τρόπος πρόσβασης

Οι ερευνητές που επιθυμούν να έχουν πρόσβαση στην υποδομή του υπολογιστικού πλέγματος θα πρέπει να αιτηθούν τη χρήση του στέλνοντας email προς `adm AT central.ntua.gr` όπου απαραίτητα θα συμπεριλαμβάνονται ([δείτε](#Παράδειγμα_αίτησης_χρήσης) παράδειγμα):

 * Τα προσωπικά τους στοιχεία: το όνομα, το επώνυμο, τη σχολή, **το όνομα χρήστη στο KHY** (το `username` από το `username@central.ntua.gr` ή `username@mail.ntua.gr`), ένα τηλέφωνο επικοινωνίας, τον επιβλέποντα καθηγητή (στην περίπτωση των διδακτορικών) και την ιδιότητά τους στο ΕΜΠ (μεταπτυχιακός φοιτητής, καθηγητής, εξωτερικός συνεργάτης, κτλ).
 * Μια σύντομη περιγραφή της χρήσης που πρόκειται να κάνουν: π.χ. *"Χρήση του Abaqus στα πλαίσια της διδακτορικής μου διατριβής με τίτλο: "ΠΡΟΣΔΙΟΡΙΣΜΟΣ  ΚΡΙΤΗΡΙΩΝ  ΑΣΤΟΧΙΑΣ  ΥΛΙΚΩΝ  ΚΑΙ  ΕΦΑΡΜΟΓΗ  ΤΟΥΣ  ΣΕ  ΚΩΔΙΚΑ  ΠΕΠΕΡΑΣΜΕΝΩΝ  ΣΤΟΙΧΕΙΩΝ  ΓΙΑ  ΤΗΝ  ΠΡΟΣΟΜΟΙΩΣΗ  ΑΠΟΚΡΙΣΗΣ  ΤΗΣ  ΓΑΣΤΡΑΣ ΠΛΟΙΩΝ ΣΕ ΑΚΡΑΙΑ ΦΟΡΤΙΑ"*.
 * Το δημόσιο κλειδί τους ([δείτε](#Αντιγραφή_του_δημόσιου_κλειδιού) παρακάτω).

Note: Προς το παρόν όλοι οι ενδιαφερόμενοι χρήστες θα πρέπει να περιμένουν απαντητικό email που θα τους ενημερώνει ότι η πρόσβασή τους ενεργοποιήθηκε και στη συνέχεια να προχωρήσουν με την ενότητα [Πρόσβαση με Secure Shell](Πρόσβαση_με_Secure_Shell).

**Η υπηρεσία του υπολογιστικού πλέγματος είναι προσβάσιμη μόνο μέσα από το εσωτερικό δίκτυο του ΕΜΠ. Αν βρίσκεστε εκτός του εσωτερικού δικτύου του ΕΜΠ θα πρέπει να χρησιμοποιήσετε την υπηρεσία εικονικού ιδιωτικού δικτύου [VPN](http://www.noc.ntua.gr/index.php?module=ContentExpress&file=index&func=display&ceid=165&meid=174) που προσφέρεται από το [Κέντρο Δικτύων](http://www.noc.ntua.gr).**

Όταν ενεργοποιηθεί η πρόσβαση τότε οι χρήστες προχωρούν στην ενότητα [Πρόσβαση με Secure Shell](#Πρόσβαση_με_Secure_Shell), μπορούν να μεταφέρουν αρχεία, να υποβάλλουν εργασίες για επίλυση και να συλλέγουν τα αποτελέσματά τους.

#### Δημιουργία κλειδιών κρυπτογράφησης

Αν χρησιμοποιείτε *Windows* μια λύση είναι να χρησιμοποιήσετε το πρόγραμμα [PuTTY Key Generator](https://the.earth.li/~sgtatham/putty/latest/x86/puttygen.exe). Αφού το ξεκινήσετε και πατήσετε το κουμπί `Generate` θα πρέπει να κινήσετε το ποντίκι σας πάνω στη λευκή περιοχή έως ότου παραχθεί αρκετή τυχαιότητα για τη δημιουργία των κλειδιών σας. Μόλις δημιουργηθούν τα κλειδιά θα πρέπει να τα σώσετε στον υπολογιστή σας για την μελλοντική τους χρήση σαν κλειδιά πρόσβασης στην υποδομή του grid του ΚΗΥ.

![puttygen launch](/assets/img/wiki/hpc/ssh/puttygen-launch.png)

![puttygen randomness](/assets/img/wiki/hpc/ssh/puttygen-randomness.png)

![puttygen keys ready](/assets/img/wiki/hpc/ssh/puttygen-keysready.png)

Μπορείτε για παράδειγμα να δημιουργήσετε ένα κατάλογο `PuTTY Keys` για να αποθηκεύσετε τα κλειδιά σας. Σώστε το *δημόσιο* κλειδί (κουμπί `Save public key`) με κάποιο όνομα, π.χ. `public`. Κατά τη διάρκεια της αποθήκευσης του ιδιωτικού σας κλειδιού (κουμπί `Save private key`) σας συμβουλεύουμε να εφοδιάσετε το κλειδί σας με ένα συνθηματικό *passphrase* έτσι ώστε να είναι ασφαλέστερη η χρήση του. Αυτό σημαίνει ότι κάθε φορά πριν τη χρήση του κλειδιού σας θα σας γίνεται ερώτηση για το μυστικό *passphrase* που θα πρέπει να απαντηθεί ορθά για να συνεχίστε.

![puttygen save public](/assets/img/wiki/hpc/ssh/puttygen-savepublic.png)

![puttygen passphrase](/assets/img/wiki/hpc/ssh/puttygen-passphrase.png)

![puttygen save private](/assets/img/wiki/hpc/ssh/puttygen-saveprivate.png)

#### Αντιγραφή του δημόσιου κλειδιού

Αν χρησιμοποιείτε *Windows*, από το PuTTY Key Generator θα πρέπει να επιλέξετε (click and drag) **όλο το περιεχόμενο** του πλαισίου κάτω από τη φράση `Public key for pasting into OpenSSH authorized_keys file` και να το επικολήσετε μέσα στο email της αίτησης χρήσης της υποδομής του υπολογιστικού πλέγματος. **Προσέξτε ότι κατά τη διαδικασία της επιλογής του κειμένου η *μπάρα κύλισης (scrollbar)* στα δεξιά πρέπει να κυλίσει μέχρι το κάτω μέρος για να είστε σίγουροι πως επιλέξατε όλο το κείμενο του δημόσιου κλειδιού σας (θα πρέπει να τελειώνει σε κάτι σαν `rsa-key-20161031`)**.

#### Παράδειγμα αίτησης χρήσης

Ένα παράδειγμα μιας αίτησης χρήσης της υποδομής του υπολογιστικού πλέγματος που περιλαμβάνει ένα σωστά επιλεγμένο δημόσιο κλειδί μπορεί να είναι η παρακάτω (προσέξτε ότι κατά την επικόληση το κείμενο του δημόσιου κλειδιού θα είναι μια μεγάλη γραμμή με πολλούς χαρακτήρες που θα διπλώνει μέσα στο σώμα του μηνύματος) :

```
Όνομα:        Γιάννης
Επώνυμο:      Παπαδόπουλος
Σχολή:        Ναυπηγών
Όνομα χρήστη: johnpapado
Ιδιότητα:     Διδακτορικός φοιτητής
Επιβλέποντας: Γιώργος Χατζηδημητρακόπουλος

Περιγραφή χρήσης:

Χρήση του Abaqus στα πλαίσια της διδακτορικής μου διατριβής με τίτλο: "ΠΡΟΣΔΙΟΡΙΣΜΟΣ  ΚΡΙΤΗΡΙΩΝ  ΑΣΤΟΧΙΑΣ  ΥΛΙΚΩΝ  ΚΑΙ  ΕΦΑΡΜΟΓΗ  ΤΟΥΣ  ΣΕ  ΚΩΔΙΚΑ  ΠΕΠΕΡΑΣΜΕΝΩΝ  ΣΤΟΙΧΕΙΩΝ  ΓΙΑ  ΤΗΝ  ΠΡΟΣΟΜΟΙΩΣΗ  ΑΠΟΚΡΙΣΗΣ  ΤΗΣ  ΓΑΣΤΡΑΣ ΠΛΟΙΩΝ ΣΕ ΑΚΡΑΙΑ ΦΟΡΤΙΑ"

Δημόσιο κλειδί:

ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEAjQfeLji9stdcjfgC/2jy25VKinhtn7msTcsPNsZlYpyNydUqIh1diTkpKnjx4UCiErcBvKU680S2XHimTfh1iC/YDcsNkrWQxXw1Alr9bNEWCuRGsBmPDvbQls1WkWYS94tvwbEyCEa0UzojBO06hpgCv/yE2RHtHmqQLsL7a88DqCpEk3uh4Llk8X7mFPZY8jPNusStzDS+H3qXtZCH1Jmd8VT0JVf4DNSccjriSoXgpiySKUGkZkKNGS2SgEST0E1YZJYxuD6thf1NKZu8EeCa0//Spemji7TbUITT6txHUU1kc8ca2rrAoZA0UYNhukVaV02OHmMAR/rerobddw== rsa-key-20161031

```

#### Πρόσβαση με Secure Shell

Αν χρησιμοποιείτε Linux ή Mac υπολογιστή ανοίξτε ένα terminal και δώστε την εντολή
```
ssh -i /path/to/rsa -C username@grid.central.ntua.gr
```
Αν υπάρξει πρόβλημα σύνδεσης τις περισσότερες φορές συνδέεται με τα permissions των κλειδιών κρυπτογράφησης:
```
chmod 600 /path/to/rsa
```

Αν χρησιμοποιείτε *Windows* μια λύση είναι να χρησιμοποιήσετε το πρόγραμμα [PuTTY](https://the.earth.li/~sgtatham/putty/latest/x86/putty.exe). Για καλύτερη εμφάνιση σας προτείνουμε να ενεργοποιήσετε στην ενότητα `Window>Appearence` τη γραμματοσειρά `Consolas` και τη ρύθμιση `ClearType`. Για να επιλέγεται αυτόματα το όνομα χρήστη σας όπως και το προσωπικό σας κλειδί κρυπτογράφησης εισάγετε τις αντίστοιχες πληροφορίες στις ενότητες `Connection>Data` και `Connection>SSH>Auth`.

![consolas cleartype](/assets/img/wiki/hpc/ssh/consolas-cleartype.png)

![connection data](/assets/img/wiki/hpc/ssh/connection-data.png)

![connection ssh auth](/assets/img/wiki/hpc/ssh/connection-ssh-auth.png)

Σώστε τις επιλογές σας σε ένα session name έτσι ώστε κάθε επόμενη φορά να επιλέγετε το session και στη συνέχεια `Load`. Την πρώτη φορά που θα συνδεθείτε θα εμφανιστεί ένα παράθυρο με τίτλο `PuTTY Security Alert` όπου θα πρέπει να επιλέξετε το `Yes` για να συνδεθείτε επιτυχώς. Αν έχετε εφοδιάσει το προσωπικό σας κλειδί με Passphrase πρέπει να το πληκτρολογήσετε και αμέσως μετά θα μπορείτε να χρησιμοποιήσετε την υποδομή του grid για να υποβάλετε τις δουλειές σας.

![save grid](/assets/img/wiki/hpc/ssh/savegrid.png)

![security alert](/assets/img/wiki/hpc/ssh/security-alert.png)

![logged in](/assets/img/wiki/hpc/ssh/loggedin.png)

#### Μεταφορά αρχείων

Αν χρησιμοποιείτε *Windows* μια λύση είναι να χρησιμοποιήσετε το πρόγραμμα [WinSCP](https://winscp.net/download/WinSCP-5.9.2-Setup.exe). Αφού ξεκινήσετε το πρόγραμμα εγκατάστασης θα πρέπει να αποδεχτείτε το License Agreement, να επιλέξετε `Typical installation` και στη συνέχεια την επιλογή `Commander` σαν User interface style.

![winscp license](/assets/img/wiki/hpc/ssh/winscp-license.png)

![winscp typical](/assets/img/wiki/hpc/ssh/winscp-typical.png)

![winscp commander](/assets/img/wiki/hpc/ssh/winscp-commander.png)

Όταν θα ξεκινήσετε για πρώτη φορά το WinSCP θα πρέπει να εισάγετε το ιδιωτικό σας κλειδί, όπως κάνατε και στην περίπτωση του PuTTY. Επιλέξτε `Advanced` και στη συνέχεια στην ενότητα `SSH>Authentication` επιλέξτε το ιδιωτικό σας κλειδί. Στη συνέχεια συμπληρώστε το όνομα χρήστη στο πεδίο `User name` και τέλος πατήστε το κουμπί `Save`. Δεχτείτε ή αλλάξτε το προτεινόμενο όνομα για τη νέα σύνδεση που μόλις δημιουργήσατε και τελικά θα έχετε τη νέα σύνδεση αποθηκευμένη στο αριστερό πλαίσιο.

![winscp launch](/assets/img/wiki/hpc/ssh/winscp-launch.png)

![winscp private key](/assets/img/wiki/hpc/ssh/winscp-privatekey.png)

![winscp grid saved](/assets/img/wiki/hpc/ssh/winscp-gridsaved.png)

Για να συνδεθείτε επιλέγετε το όνομα της σύνδεσης από αριστερά και πατάτε το κουμπί `Login`. Αν έχετε εφοδιάσει το ιδιωτικό σας κλειδί με κάποιο passphrase θα πρέπει να το πληκτρολογήσετε για να συνδεθείτε με επιτυχία. Στο τέλος θα υπάρχουν δύο πλαίσια όπου στο αριστερό βρίσκεται ο τοπικός σας υπολογιστής ενώ στο δεξιό ο απομακρυσμένος. Μπορείτε να μετακινείτε αρχεία από και προς τον απομακρυσμένο υπολογιστή με τη διαδικασία του *"drag and drop"*.

![winscp grid saved](/assets/img/wiki/hpc/ssh/winscp-gridsaved.png)

![winscp passphrase](/assets/img/wiki/hpc/ssh/winscp-passphrase.png)

![winscp local remote](/assets/img/wiki/hpc/ssh/winscp-localremote.png)

#### Υποβολή εργασίας για επίλυση

Αφού έχετε μεταφέρει τα αρχεία σας με επιτυχία και τα έχετε τακτοποιήσει σε κάποιο κατάλογο, π.χ. `abaqus-multiprocessor` θα πρέπει να μετακινηθείτε στον κατάλογο με την εντολή `cd abaqus-multiprocessor` (αντικαταστήστε το όνομα του καταλόγου ανάλογα). Η εντολή `ls` μας δίνει τη λίστα των αρχείων που περιέχει ο κατάλογος. Η εργασία που θέλουμε να υποβάλουμε είναι συνήθως ένα αρχείο κειμένου (script) που περιέχει διάφορες ρυθμίσεις και εντολές. Στο συγκεκριμένο παράδειγμα η εργασία που θα υποβληθεί είναι το αρχείο `abaqus-multi.sh` και η υποβολή γίνεται με την εντολή `qsub`.

```
qsub abaqus-multi.sh
```

Το σύστημα δίνει ένα αύξοντα αριθμό στην εργασία και μας πληροφορεί με ανάλογο μήνυμα ότι η εργασία μας έχει υποβληθεί. Ταυτόχρονα θα λάβουμε κι ένα ενημερωτικό email με ανάλογο περιεχόμενο.

```
root<root@central.ntua.gr>
to chfrag

Job 10 (abaqus-multi.sh) Started
 User       = chfrag
 Queue      = all.q
 Host       = blade13
 Start Time = 11/09/2016 12:20:20
```

Για να ενημερωθούμε από το ίδιο το σύστημα για τις λεπτομέριες της εκτέλεσης χρησιμοποιούμε την εντολή `qstat`.

```
qstat -f
```

![qsub start](/assets/img/wiki/hpc/ssh/qsub-start.png)

![qsub qsub](/assets/img/wiki/hpc/ssh/qsub-sub.png)

![qsub qstat](/assets/img/wiki/hpc/ssh/qsub-qstat.png)

#### Συλλογή αποτελεσμάτων

Όταν η επίλυση τελειώσει θα λάβετε ένα ενημερωτικό email με διάφορες πληροφορίες σχετικά με την επεξεργασία που έγινε στην υποδομή του υπολογιστικού πλέγματος:

```
root<root@central.ntua.gr>
to chfrag

Job 10 (abaqus-multi.sh) Complete
 User             = chfrag
 Queue            = all.q@blade13
 Host             = blade13
 Start Time       = 11/09/2016 12:20:20
 End Time         = 11/09/2016 12:47:16
 User Time        = 00:00:01
 System Time      = 00:00:00
 Wallclock Time   = 00:26:56
 CPU              = 10:32:30
 Max vmem         = 15.173G
 Exit Status      = 0
```

Αν δώσουμε την εντολή `ls` στον κατάλογο της εργασίας θα δούμε ότι έχουν δημιουργηθεί διάφορα αρχεία σαν αποτέλεσμα της επεξεργασίας μας. Με τη χρήση του WinSCP μπορούμε να μεταφέρουμε τα αρχεία που μας ενδιαφέρουν στον τοπικό υπολογιστή.

![finished ls](/assets/img/wiki/hpc/ssh/finished-ls.png)

![finished winscp](/assets/img/wiki/hpc/ssh/finished-winscp.png)

![finished download](/assets/img/wiki/hpc/ssh/finished-download.png)
