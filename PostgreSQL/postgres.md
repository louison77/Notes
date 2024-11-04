# PostgreSQL

## Principles

* It is an Open Source relational Database
* PostgreSql is implemented on one server. To store more data, it is required to have more storage because the replication methods are complex.
* Postgres is considered as a object relationnal database managment system (ORDBMS)
* It is compatible on different OS like Windows, MacOS and Linux.
* For non-relationnal request, postgres can be used with JSON format requests.

## Main commands

* `psql -d <db-name> -U <username>` : Connect to a database with a specific User.
* `psql -d <db-name> -U <username> -w` : -w flag force the password authentication.
* `psql -h <database-host-address> -d <db-name> -U <username>` : Connect to a database on a different host.
* `\l` : list databases.
* `\c <db-name>`: change to antoher database.
* `\dt` : list tables.
* `\d or \d+` : describe a table with or without more information.
* `\du` : list users.
* `\df` : list functions.
* `\o` : save the query result to a file.
* `\q` : quit the psql terminal.

## Good practices and tips

* On debian distribution, postgresql and its client can be downloaded with apt with the command `apt install postgresql postgresql-client`.
* Postgresql worked as a service, the command to start the service are `service postgresql start` or `systemctl enable --now postgresql`
* By default, the username is postgres and the default database is also called postgres.
* The main postgresql's configuration file is located at `/etc/postresql/<version number>/main.postgresql.conf`. In this file, to connect outside of localhost, it is important to change `listen_addresses = '*'`
* The client connections file managment is `/etc/postgresql/11/main/pg_hba.conf`.
