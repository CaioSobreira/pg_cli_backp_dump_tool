pgbackup
========

CLI for backup remote PostgreSQL database either locally or to S3

Project created following A Cloud Guru Python 3 for system administrators course lessons.

Course instructor and original code author: Keith Thompson


Preparing the development
-------------------------

1. Ensure ``pip`` and ``pipenv`` are installed.
2. Clone repository: ``git clone git@github.com:example/pgbackup``
3. ``cd`` into the repository.
4. Fetch developent dependencies ``make install``
5. Activate virtualenv: ``pipenv shell``

Usage
-----

Pass in a full dataase URL, the storage driver, and the destination.

S3 Example w/ bucket name:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups

S3 Example w/ bucket name:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active:

::

    $ make

If virtualenv isn't active then use

::

    $ pipenv run make
