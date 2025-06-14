#  Docker Compose Stacks 

Dieses Verzeichnis beherbergt eine Sammlung von Docker Compose YAML-Dateien, die darauf ausgelegt sind, verschiedene Anwendungen und Dienste mit Docker Compose mühelos zu starten.

##  Was sind Docker Compose Stacks?

Docker Compose vereinfacht die Verwaltung von Multi-Container-Docker-Anwendungen. Ein "Stack" ist im Wesentlichen eine Zusammenstellung von Diensten, die harmonisch zusammenarbeiten, um eine vollständige Anwendung zu bilden. Die YAML-Dateien in diesem Verzeichnis dienen als Baupläne, die beschreiben, wie diese Dienste konfiguriert und miteinander verknüpft werden sollen.

##  Verfügbare Stacks

Hier ist eine Übersicht der verfügbaren Docker Compose Stacks in diesem Verzeichnis:

| Datei                     | Beschreibung                                                                                              | Tags                     | Link zum offiziellen GitHub-Repository                                                                                                  |
|---------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|--------------------------------------------------------------------------------------------------------------------|
| Adguard.yml               | Netzwerkweiter Werbe- und Trackingschutz mit AdGuard Home                                                 | Netzwerk, Sicherheit      | [AdGuardTeam/AdGuardHome](https://github.com/AdGuardTeam/AdGuardHome)                                               |
| Baikal.yml                | Einfacher CalDAV- und CardDAV-Server für Kalender und Kontakte (Baïkal)                                     | Kalender, Kontakte       | [sabre-io/Baikal](https://github.com/sabre-io/Baikal)                                                              |
| Beszel + Agent.yml        | Beszel und sein zugehöriger Agent für spezifische Anwendungen                                               | Automatisierung, Agent    | [beszel-dev/beszel](https://github.com/henrygd/beszel)                                                             |
| Dockge.yml                | Docker Compose Stack Manager                                                                              | Docker, Verwaltung        | [louislam/dockge](https://github.com/louislam/dockge)                                                               |
| Dockwatch.yml             | Überwachung von Docker-Containern mit Dockwatch                                                             | Überwachung, Docker       | [notifiarr/dockwatch](https://github.com/Notifiarr/dockwatch)                                                       |
| FreshRSS.yml              | Selbstgehosteter RSS-Aggregator zum Abonnieren von Nachrichtenfeeds (FreshRSS)                             | RSS, Nachrichten           | [FreshRSS/FreshRSS](https://github.com/FreshRSS/FreshRSS)                                                           |
| Gitea.yml                 | Selbstgehosteter Git-Service zur Versionsverwaltung von Code (Gitea)                                        | Git, Versionsverwaltung  | [go-gitea/gitea](https://github.com/go-gitea/gitea)                                                                 |
| Heimdall.yml              | Application Dashboard / Startseite                                                                        | Dashboard, Tools           | [linuxserver/Heimdall](https://github.com/linuxserver/Heimdall)                                                       |
| Homarr.yml                | Dashboard-Anwendung zur Organisation von Diensten                                                           | Dashboard, Tools           | [ajnart/homarr](https://github.com/ajnart/homarr)                                                                    |
| Homepage.yml              | Dashboard-Anwendung zur Organisation von Diensten                                                           | Dashboard, Tools           | [gethomepage/homepage](https://github.com/gethomepage/homepage)                                                       |
| Immich.yml                | Foto- und Video-Backup-Lösung für die eigene Cloud (Immich)                                                 | Backup, Multimedia       | [immich-app/immich](https://github.com/immich-app/immich)                                                             |
| Joplin.yml                | Notiz-App für die Organisation von Notizen und Aufgaben (Joplin)                                            | Notizen, Organisation      | [laurent22/joplin](https://github.com/laurent22/joplin)                                                              |
| Linkstack.yml             | Lesezeichen-Tool zur Verwaltung von Web-Links (Linkstack)                                                    | Lesezeichen, Tools        | [linkstackorg/linkstack](https://github.com/linkstackorg/linkstack)                                                 |
| N8N.yml                   | Automatisierungsplattform zur Verbindung verschiedener Dienste (N8N)                                       | Automatisierung, Integration| [n8n-io/n8n](https://github.com/n8n-io/n8n)                                                                         |
| Nextcloud (Cron-Edition).yml| Nextcloud mit Cronjob-Container für geplante Aufgaben                                                        | Cloud, Produktivität      | [nextcloud/docker](https://github.com/nextcloud/docker) (basiert auf dem offiziellen Nextcloud Docker-Image)      |
| Nginx.yml                 | Nginx Proxy Manager zur Verwaltung von Reverse-Proxies                                                      | Netzwerk, Proxy            | [NginxProxyManager/nginx-proxy-manager](https://github.com/NginxProxyManager/nginx-proxy-manager)                  |
| OpenVpn-AS.yml            | OpenVPN Access Server für sichere VPN-Verbindungen                                                         | VPN, Sicherheit           | [OpenVPN/as-docker](https://github.com/OpenVPN/as-docker)  (offizielle OpenVPN-Distribution)                |
| Paperless + AI.yml        | Paperless-ngx mit KI-Funktionen zur Dokumentenverwaltung                                                    | Dokumente, KI              | [paperless-ngx/paperless-ngx](https://github.com/paperless-ngx/paperless-ngx)                                       |
| Pi-Hole.yml               | Netzwerkweiter Werbe- und Trackingschutz mit Pi-hole                                                       | Netzwerk, Sicherheit      | [pi-hole/pi-hole](https://github.com/pi-hole/pi-hole)                                                               |                               |
| Rustdesk.yml              | Remote-Desktop-Anwendung für Fernzugriff (Rustdesk)                                                         | Fernzugriff, Tools        | [rustdesk/rustdesk](https://github.com/rustdesk/rustdesk)                                                           |
| Seafile.yml               | Datei-Synchronisations- und Freigabe-Server (Seafile)                                                        | Cloud, Dateiverwaltung   | [haiwen/seafile-docker](https://github.com/haiwen/seafile-docker) (offizielles Seafile Docker-Image)                |
| Snipe-IT.yml              | Asset-Management-System zur Verwaltung von Hardware und Software (Snipe-IT)                               | Asset-Management, IT       | [snipe/snipe-it](https://github.com/snipe/snipe-it)                                                                 |
| Stirling-PDF.yml          | PDF-Bearbeitungstool für verschiedene PDF-Manipulationen (Stirling-PDF)                                      | PDF, Tools                | [Stirling-Tools/Stirling-PDF](https://github.com/Stirling-Tools/Stirling-PDF)                                     |
| Uptime-Kuma.yml           | Überwachungstool zur Prüfung der Verfügbarkeit von Diensten (Uptime Kuma)                                    | Überwachung, Tools        | [louislam/uptime-kuma](https://github.com/louislam/uptime-kuma)                                                    |
| Vaultwarden.yml           | Passwortmanager zur sicheren Speicherung von Passwörtern (Vaultwarden)                                       | Passwortmanager, Sicherheit| [dani-garcia/vaultwarden](https://github.com/dani-garcia/vaultwarden)                                               |
| Wallos.yml                | Webanwendung für spezifische Zwecke (Wallos)                                                               | Webanwendung, Sonstiges    | [ellite/wallos](https://github.com/ellite/Wallos)                                                               |
| KitchenOwl.yml      | Rezept- und Einkaufslisten-Manager (KitchenOwl)        | Kochen, Organisation   | [TomBursch/kitchenowl](https://github.com/TomBursch/kitchenowl)              |
| Docuseal.yml      | Dokumentenmanagement und digitale Signaturen (Docuseal)                                                                     | Dokumentenmanagement, Signatur | [docuseal/docuseal](https://github.com/docusealco/docuseal)                     |
| OnlyOffice_Documentserver.yml | OnlyOffice Documentserver für die Online-Zusammenarbeit an Dokumenten | Cloud, Produktivität | [onlyoffice/documentserver](https://github.com/onlyoffice/documentserver) |
| Kasm-Workspace.yml      | Remote Browser Isolation Platform (Kasm Workspace)                                                                | Remote, Browser            | [kasmtech/Kasm-Workspaces](https://github.com/kasmtech) 
| netboot.xyz.yml           | PXE-Boot-Server für Netzwerkinstallationen (netboot.xyz)                                          | Netzwerk, Tools        | [netbootxyz/netboot.xyz](https://github.com/netbootxyz/netboot.xyz)                                                        |                                                |
| Duplicati.yml             | Backup-Software für sichere Datensicherungen (Duplicati)                                                     | Backup, Tools            | [duplicati/duplicati](https://github.com/duplicati/duplicati)                                                              |
| Suitecrm.yml              | Open-Source Customer Relationship Management (CRM) Software                                               | CRM, Sales, Open Source  | [salesagility/SuiteCRM](https://github.com/salesagility/SuiteCRM)                                                  |
| OpenWebUI.yml              | Benutzerfreundliche Web-Oberfläche für KI-Modelle (Open WebUI)                                | KI, Oberfläche          | [open-webui/open-webui](https://github.com/open-webui/open-webui)                                  |
| Postiz.yml                  | Kostenloses, quelloffenes Tool zur Planung von Social-Media-Beiträgen mit KI-Funktionen | Social Media, Planung, KI | [gitroomhq/postiz-app](https://github.com/gitroomhq/postiz-app) |
| CoreControl.yml           | Dashboard zur Verwaltung Ihrer gesamten Serverinfrastruktur. Ermöglicht das Organisieren von Serverdaten, das Hinzufügen von selbstgehosteten Anwendungen mit Schnellzugriffslinks und die Überwachung deren Verfügbarkeit. | Dashboard, Verwaltung, Überwachung | [crocofied/CoreControl](https://github.com/crocofied/CoreControl)                                               |
| Ghostboard.yml            | Leichtgewichtige, selbstgehostete Lösung für die gemeinsame Nutzung von Text in Echtzeit über Web oder CLI. | Textfreigabe, Echtzeit, Tools | [jon6fingrs/ghostboard](https://github.com/jon6fingrs/ghostboard)                                      |
| Spoolman.yml | Filament-Managementsystem für 3D-Druck (Spoolman) | 3D-Druck, Verwaltung | [donkie/spoolman](https://github.com/OctoPrint/OctoPrint) |
| Octoprint.yml | Webinterface zur Steuerung und Überwachung von 3D-Druckern (OctoPrint) | 3D-Druck, Überwachung | [OctoPrint/OctoPrint](https://github.com/OctoPrint/OctoPrint) |
| Komodo.yml | Tool zum Erstellen und Bereitstellen von Software auf mehreren Servern, inklusive Docker Container und Docker Compose Management | Docker, CI/CD, Verwaltung | [moghtech/komodo](https://github.com/moghtech/komodo) |
| Easy-Wireguard.yml | Eine einfache Oberfläche zur Verwaltung von WireGuard-VPN-Konfigurationen | VPN, Tools | [wg-easy/wg-easy](https://github.com/wg-easy/wg-easy) |
| Glance.yml | Ein selbstgehostetes Dashboard, das alle Ihre Feeds an einem Ort vereint (Glance) | Dashboard, RSS, Tools | [glanceapp/glance](https://github.com/glanceapp/glance) |

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

* **Passwörter:** Ändern Sie unbedingt alle Standardpasswörter in den YAML-Dateien vor der Bereitstellung.
* **Umgebungsvariablen:** Passen Sie die Umgebungsvariablen in den YAML-Dateien an Ihre spezifischen Anforderungen an.
* **Volumes:** Stellen Sie sicher, dass die Volumes korrekt konfiguriert sind, um Datenpersistenz zu gewährleisten.
* **Netzwerke:** Einige Stacks erfordern möglicherweise benutzerdefinierte Netzwerke. Konfigurieren Sie diese entsprechend.
* **Domains/URLs:** Ersetzen Sie die Platzhalter-Domains und URLs in den YAML-Dateien durch Ihre eigenen.

**Bitte beachten Sie, dass die hier aufgeführten Anwendungen nicht von mir stammen. Sie wurden lediglich aufbereitet, um sie einer breiteren Community zugänglich zu machen und die Bereitstellung zu vereinfachen. Sollten Sie als Urheber Einwände gegen die Bereitstellung haben, kontaktieren Sie mich bitte, damit wir eine Lösung finden können.**