# Developer Week 2016 PostgreSQL / NoSQL Dev Session

## Anforderungen

Folgende Software Komponenten werden benötigt:
- [Vagrant](https://www.vagrantup.com/downloads.html) V1.8.0 oder neuer
- [Virtualbox](https://www.virtualbox.org/wiki/Downloads) V5.0.16 oder neuer
- graphischer PostgreSQL Client bsp. [pgAdmin](http://www.pgadmin.org/download/) oder [DataGrip](https://www.jetbrains.com/datagrip/)

## Vagrant Box starten

Im geklonten Verzeichnis folgendes Kommando ausführen:

```
vagrant up
```

## Datenbank und Datenbankbenutzer anlegen:

In die virtuelle Maschine einloggen und zum PostgreSQL User wechseln
```
vagrant ssh
sudo su postgres
```

Datenbankbenutzer anlegen:
```
createuser dwx16 -l -P -s
```

Datenbank anlegen:
```
createdb dwx16 -O dwx16
```

## Verbindungsaufbau

Im PostgreSQL Client auf dem Hostsystem folgende Zugangsdaten verwenden:
- Hostname: localhost
- Port: 8432 (siehe Definition im [Vagrantfile](https://github.com/bitExpert/psql-nosql-workshop-dwx16/blob/master/Vagrantfile#L54))
- Benutzername: dwx16
- Passwort: Das gewählte Passwort
- Datenbank: dwx16
