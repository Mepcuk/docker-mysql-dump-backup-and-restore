# docker-mysql-dump-backup-and-restore

Command reminder how to backup ( create dump ) and restore MySQL MariaDB database from running docker container

# Backup from running container mysql mariadb
```docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql```

# Restore to running container mysql mariadb
```cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE```


#  P.s. CONTAINER = CONTAINER ID or NAMES (check via command "docker ps")
