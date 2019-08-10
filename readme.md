# linuxmuster-ddns

Update Funktionen für den linuxmuster.net ynDNS-Dienst fuer Vereinsmitglieder.

## Benutzung

Zunächst muss (am besten über das Forum) ein DDNS Hostname "beantragt" werden - das geht nur für Vereinsmitglieder. Die Hostnamen haben alle die Domain "linuxmuster.org", also z.B. ``superschule.linuxmuster.org``-

### Paketinstallation auf dem Server

```
apt-get update
apt-get install linuxmuster-ddns
```

### Konfiguration und Betrieb

Jetzt muss der Hostname, der Benutzername und das Passwort in der Datei ``/etc/linuxmuster/ddns.conf`` eingetragen werden, dann kann man die Aktualisierung erstmalig "von Hand" anstossen, indem man auf der Konsole den Befehl ``/usr/sbin/linuxmuster-ddns`` ausführt.

Im weiteren wird die Aktualisierung von einem Cronjob übernmommen (definiert in der Datei ``/etc/cron.d/linuxmuster-ddns``) die Ergebnisse der Bemühungen werden in der Datei ``/var/log/linuxmuster-ddns.log`` festgehalten.






