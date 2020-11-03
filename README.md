# Docker working with Database

## For import database from sql file

1. Copy file (example.sql) to db_data folder
2. From root of plugin folder in terminal tape

`docker exec -ti kiadev_db bash`

`cd /var/lib/mysql`

`mysql -u noir -p ace_db < example.sql`

`exit`

use password from docker_compose.yml file ('secret' by default)

Database is imported.

## For export database to sql file

1. From root of plugin folder in terminal tape

`docker exec -ti kiadev_db bash`

`cd /var/lib/mysql`

`mysqldump --add-drop-table -u noir -p ace_db > new_file_name.sql`

`exit`

use password from docker_compose.yml file ('secret' by default)

Database will be export to db_data/new_file_name.sql file.
