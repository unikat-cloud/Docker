#  Docker Compose Stacks 

Dieses Verzeichnis beherbergt eine Sammlung von Docker Compose YAML-Dateien, die darauf ausgelegt sind, verschiedene Anwendungen und Dienste mit Docker Compose mühelos zu starten.

##  Was sind Docker Compose Stacks?

Docker Compose vereinfacht die Verwaltung von Multi-Container-Docker-Anwendungen. Ein "Stack" ist im Wesentlichen eine Zusammenstellung von Diensten, die harmonisch zusammenarbeiten, um eine vollständige Anwendung zu bilden. Die YAML-Dateien in diesem Verzeichnis dienen als Baupläne, die beschreiben, wie diese Dienste konfiguriert und miteinander verknüpft werden sollen.

##  Verfügbare Stacks

Hier ist eine Übersicht der verfügbaren Docker Compose Stacks in diesem Verzeichnis:

| Datei                           | Beschreibung                                                                  | Tags                     |
| :-------------------------------- | :------------------------------------------------------------------------------ | :------------------------- |
| `Adguard.yml`                     | Netzwerkweiter Werbe- und Trackingschutz mit AdGuard Home                      | Netzwerk, Sicherheit       |
| `Baikal.yml`                      | Einfacher CalDAV- und CardDAV-Server für Kalender und Kontakte (Baïkal)         | Kalender, Kontakte         |
| `Beszel+Agent.yml`                | Beszel und sein zugehöriger Agent für spezifische Anwendungen                   | Automatisierung, Agent     |
| `Dockge.yml`                      | Docker Compose Stack Manager                                                    | Docker, Verwaltung         |
| `Dockwatch.yml`                   | Überwachung von Docker-Containern mit Dockwatch                                | Überwachung, Docker        |
| `FreshRSS.yml`                    | Selbstgehosteter RSS-Aggregator zum Abonnieren von Nachrichtenfeeds (FreshRSS)  | RSS, Nachrichten           |
| `Gitea.yml`                       | Selbstgehosteter Git-Service zur Versionsverwaltung von Code (Gitea)           | Git, Versionsverwaltung    |
| `Heimdall.yml`                    | Application Dashboard / Startseite                                              | Dashboard, Tools           |
| `Homarr.yml`                      | Dashboard-Anwendung zur Organisation von Diensten                               | Dashboard, Tools           |
| `Homepage.yml`                    | Dashboard-Anwendung zur Organisation von Diensten                               | Dashboard, Tools           |
| `Immich.yml`                      | Foto- und Video-Backup-Lösung für die eigene Cloud (Immich)                   | Backup, Multimedia         |
| `Joplin.yml`                      | Notiz-App für die Organisation von Notizen und Aufgaben (Joplin)               | Notizen, Organisation      |
| `Linkstack.yml`                   | Lesezeichen-Tool zur Verwaltung von Web-Links (Linkstack)                       | Lesezeichen, Tools         |
| `N8N.yml`                         | Automatisierungsplattform zur Verbindung verschiedener Dienste (N8N)           | Automatisierung, Integration |
| `Nextcloud (Cron-Edition).yml`     | Nextcloud mit Cronjob-Container für geplante Aufgaben                          | Cloud, Produktivität       |
| `Nginx.yml`                       | Nginx Proxy Manager zur Verwaltung von Reverse-Proxies                         | Netzwerk, Proxy            |
| `OpenVpn-AS.yml`                  | OpenVPN Access Server für sichere VPN-Verbindungen                             | VPN, Sicherheit            |
| `Paperless+AI.yml`                | Paperless-ngx mit KI-Funktionen zur Dokumentenverwaltung                       | Dokumente, KI              |
| `Pi-Hole.yml`                     | Netzwerkweiter Werbe- und Trackingschutz mit Pi-hole                            | Netzwerk, Sicherheit       |
| `README.md`                      | Dokumentation der Docker Compose Stacks                                        | Dokumentation, Metadaten   |
| `Rustdesk.yml`                    | Remote-Desktop-Anwendung für Fernzugriff (Rustdesk)                            | Fernzugriff, Tools         |
| `seafile.yml`                     | Datei-Synchronisations- und Freigabe-Server (Seafile)                           | Cloud, Dateiverwaltung     |
| `Snipe-IT.yml`                    | Asset-Management-System zur Verwaltung von Hardware und Software (Snipe-IT)    | Asset-Management, IT       |
| `Stirling-PDF.yml`                | PDF-Bearbeitungstool für verschiedene PDF-Manipulationen (Stirling-PDF)         | PDF, Tools                 |
| `Uptime-Kuma.yml`                 | Überwachungstool zur Prüfung der Verfügbarkeit von Diensten (Uptime Kuma)     | Überwachung, Tools         |
| `Vaultwarden.yml`                 | Passwortmanager zur sicheren Speicherung von Passwörtern (Vaultwarden)         | Passwortmanager, Sicherheit |
| `Wallos.yml`                      | Webanwendung für spezifische Zwecke (Wallos)                                   | Webanwendung, Sonstiges    |

##  Verwendung mit Portainer

Portainer ist eine intuitive, webbasierte Oberfläche zur Verwaltung von Docker-Umgebungen. Mit den Docker Compose Stacks in diesem Verzeichnis können Sie Anwendungen in Portainer mühelos bereitstellen.

###  Schritte

1.  **Portainer öffnen:** Melden Sie sich bei Ihrer Portainer-Instanz an.
2.  **Stacks auswählen:** Klicken Sie im linken Menü auf "Stacks".
3.  **Stack hinzufügen:** Klicken Sie auf "Add stack".
4.  **Name eingeben:** Geben Sie einen aussagekräftigen Namen für Ihren Stack ein.
5.  **YAML-Datei hochladen/einfügen:**
    * Kopieren Sie den Inhalt einer YAML-Datei aus diesem Verzeichnis in das Textfeld "Web editor".
    * Alternativ können Sie eine YAML-Datei über die Option "Upload from file" hochladen.
6.  **Bereitstellen:** Klicken Sie auf "Deploy the stack", um den Stack in Betrieb zu nehmen.

Nach der Bereitstellung können Sie die Container und Dienste bequem in Portainer verwalten.

## ⚠️ Wichtige Hinweise

* Passwörter: Ändern Sie unbedingt alle Standardpasswörter in den YAML-Dateien vor der Bereitstellung.
* Umgebungsvariablen: Passen Sie die Umgebungsvariablen in den YAML-Dateien an Ihre spezifischen Anforderungen an.
* Volumes: Stellen Sie sicher, dass die Volumes korrekt konfiguriert sind, um Datenpersistenz zu gewährleisten.
* Netzwerke: Einige Stacks erfordern möglicherweise benutzerdefinierte Netzwerke. Konfigurieren Sie diese entsprechend.
* Domains/URLs: Ersetzen Sie die Platzhalter-Domains und URLs in den YAML-Dateien durch Ihre eigenen.
