pgbackup
========

CLI for backup remote postgresql database either locally or to S3

Preparing the Development
-------------------------

1. Ensure ``pip`` and ``pipenv`` are installed
2. Clone repository: ``git clone https://github.com/praveenreddy544/pythonproject``
3. ``cd`` into the repository
4. Fetch development dependencies ``make install``
5. Activate virtualenv: ``pipenv shell``

Usuage
------

Pass in full database URL, storage driver, and destination.

S3 Example w/bucker name:

::

     $pgbackup postgres://chintu@servername:5432/db_one --driver s3 backups

Local Example w/ localpath:

::

    $pgbackup postgres://chintu@servername:5432/<Databsecreatedname> --driver local /var/dumps/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active

::

    $ make

If virtualenv isn't active then use:

::

    $ pipenv run make or use pipenv shell


