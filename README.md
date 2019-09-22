# jacks-tools-docker

Docker image aimed at making the access to Jacks MH database a bit easier.
The image contains a mysql 5.7 server preloaded with the data from the keybase nightly backups: https://keybase.pub/devjacksmith/mh_backups/

The database is set up with the following credentials/names:

```
ENV MYSQL_ROOT_PASSWORD=secret
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=admin
ENV MYSQL_DATABASE=mhhunthelper
```

## Getting it and running it

```bash
$ docker pull bavovanachte/mousehunt-jacksdb
$ docker run -p 3306:3306 -d bavovanachte/mousehunt-jacksdb
```

This should set up a mysql server that you can query on localhost. 
