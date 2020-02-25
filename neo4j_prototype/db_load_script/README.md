WARNING:  You must set up directories, and make changes to the script before running.

This directory contains the script that was used to spin up the LINCS1000 postgres database in docker
you'll need to examine the scripts and make all required adjustments for your local configuration, directories and disks

Examples (not all inclusive):
```
DATASET_DIR="/home/plastic/d/downloads/drugcentral_lincs.postgres2"
DATABASE_DIR="/data2/db/${DATABASE}/"
```

Notes:
- The database may required up to 30% extra space on disk, during the load phase, once loaded total size is a bit over 1TB.  (the database, this does not include the size of the dump file being loaded)
- The database took 39 hours to load onto a pair of RAID0 spinning disks, (and not CPU limited)