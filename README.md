Archive, Compress, Encrypt, Backup
==================================

This script compresses specific folders to tar.gz, encrypts with openssl & des3 and uses rsync to transfer to a remote filesystem.

Warning
-------

This script copies the entire contents of the backup each time it is run so heavy traffic can accur.


USAGE
-----

Open the main.cfg file and configure. Execute `backups`.

**You will need:**
* List of folders to backup
* A folder for the script to save temporary files to
* Location to store backups

This script works with cron. The easiest way is to symlink (ln -s) it to the /etc/cron.daily folder.


RESTORING BACKUPS
-----------------

Use the `acerestore` script:

	acerestore example.tar.gz.des3

	tar -xzf example.tar.gz
