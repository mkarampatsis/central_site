---
layout: wiki
title: Matlab batch jobs
permalink: /batch-matlab/
---

### Matlab batch jobs
{: .top-buffer }

Η υποβολή εργασιών επίλυσης που χρησιμοποιούν το λογισμικό Matlab προϋποθέτει ότι έχετε ήδη στον τοπικό σας υπολογιστή ένα πρόγραμμα `job.m` σε Matlab και θέλετε να το εκτελέσετε στην υποδομή του υπολογιστικού πλέγματος. Πρέπει να διαμορφώσετε ένα αρχείο μέ κάποιο όνομα, π.χ. job.sh και να το προσαρμόσετε στα δεδομένα που αφορούν στο πρόβλημά σας.

* Αλλάξτε τη γραμμή `#$ -M chfrag ΑΤ central.ntua.gr` βάζοντας το δικό σας email για να λαμβάνετε ειδοποιήσεις σχετικά με την πορεία της επίλυσης.
* Αλλάξτε τη γραμμή `SCRIPT=job` βάζοντας το όνομα του αρχείου που περιέχει το πρόγραμμα του Matlab που θέλετε να εκτελέσετε.

```bash
#!/bin/bash
#
#$ -cwd
#$ -M chfrag AT central.ntua.gr
#$ -m baes
#$ -S /bin/bash
#$ -e ./errors.txt
#$ -o ./output.txt
#$ -N matlab_test_job
#

MATLAB=/usr/local/MATLAB/R2016a/bin/matlab
SCRIPT=job

$MATLAB nodesktop -nosplash -r $SCRIPT
```
