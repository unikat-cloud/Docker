## 2. Grundlagen

### 2.1 Container vs. Image vs. Dockerfile

- **Docker Image:** Ein Docker Image ist eine unveränderliche, schlanke Vorlage, die alle notwendigen Dateien, Bibliotheken, Abhängigkeiten und Konfigurationsinformationen enthält, um eine Anwendung auszuführen. Es ist vergleichbar mit einem Schnappschuss oder einer Blaupause, die beschreibt, wie ein Container gestartet wird. Images werden häufig in Schichten (Layers) aufgebaut, sodass Änderungen modular und effizient verwaltet werden können.

- **Docker Container:** Ein Container ist eine laufende Instanz eines Docker Images. Er ist die ausführbare Umgebung, die auf dem Host-System gestartet wird und die Anwendung isoliert von anderen Containern oder dem Host ausführt. Container sind temporär und zustandslos, können aber bei Bedarf auch dauerhafte Daten speichern (z.B. über Volumes).

- **Dockerfile:** Ein Dockerfile ist eine Textdatei, die eine Schritt-für-Schritt-Anleitung enthält, wie ein Docker Image zu bauen ist. Es beschreibt unter anderem die Ausgangsbasis (Base Image), die Installation von Software, das Kopieren von Dateien und die Konfiguration der Laufzeitumgebung. Mit dem Befehl `docker build` wird anhand des Dockerfiles das eigentliche Image erzeugt.

---

### 2.2 Container-Orchestrierung (kurz, z.B. mit Docker Compose, Kubernetes)

Container-Orchestrierung bezeichnet die automatisierte Verwaltung, Skalierung und Vernetzung von Containern in komplexen Umgebungen, insbesondere wenn mehrere Container zusammenarbeiten oder mehrere Instanzen einer Anwendung betrieben werden.

- **Docker Compose:** Ein einfaches Orchestrierungstool, das es ermöglicht, mehrere Container-Anwendungen mit einer YAML-Konfigurationsdatei zu definieren, zu starten und zu vernetzen. Docker Compose ist besonders geeignet für Entwicklungs- und Testumgebungen.

- **Kubernetes:** Ein mächtiges Open-Source-Orchestrierungssystem zur Automatisierung von Deployment, Skalierung und Betrieb von Container-Anwendungen in großen produktiven Umgebungen. Kubernetes verwaltet Container über Cluster hinweg, sorgt für Selbstheilung, Lastverteilung und Rollout-Strategien.

Orchestrierung erleichtert somit den Betrieb von verteilten Anwendungen und macht komplexe Systeme stabil, skalierbar und verwaltbar.

---

### 2.3 Docker-Architektur und Komponenten

#### Docker Daemon

Der Docker Daemon (`dockerd`) ist der zentrale Hintergrundprozess, der auf dem Host läuft und die Container verwaltet. Er übernimmt Aufgaben wie Erstellen, Starten, Stoppen und Überwachen von Containern sowie das Handling von Images und Netzwerken. Clients kommunizieren mit dem Daemon über eine REST-API.

#### Docker CLI

Die Docker CLI (`docker`) ist das Kommandozeilen-Werkzeug, mit dem Benutzer direkt mit dem Docker Daemon interagieren. Über Befehle wie `docker run`, `docker build` oder `docker pull` können Container gesteuert, Images erstellt oder heruntergeladen und weitere Operationen ausgeführt werden.

#### Docker Registry

In einer Docker Registry werden Docker Images gespeichert und verwaltet. Bekannte öffentliche Registries sind z.B. Docker Hub oder GitHub Container Registry. Private Registries ermöglichen es Unternehmen, eigene Images sicher zu speichern und bereitzustellen. Über die Registry können Images hochgeladen (`push`) und heruntergeladen (`pull`) werden.

---

### 2.4 Wichtige Begriffe

#### Images

Ein Image ist das Template, aus dem ein Container gestartet wird. Es ist schreibgeschützt und besteht aus mehreren Layern, die Änderungen separat speichern. Images werden versioniert und können aus Registries bezogen oder selbst gebaut werden.

#### Containers

Containers sind laufende Instanzen von Images. Sie stellen eine isolierte Laufzeitumgebung bereit, die Anwendungen abkapselt. Container leben nur solange sie laufen und können bei Bedarf gestoppt, gelöscht oder gespeichert werden.

#### Volumes

Volumes sind persistente Speicherbereiche, die über die Lebenszeit von Containern hinweg bestehen bleiben und Daten speichern können. Sie ermöglichen es, Daten unabhängig vom Container-File-System dauerhaft zu sichern und zwischen Containern zu teilen.

#### Netzwerke

Docker Netzwerke verbinden Container miteinander sowie mit der Außenwelt. Standardmäßig wird jedes Containernetzwerk isoliert betrieben, aber verschiedene Netzwerktypen (Bridge, Host, Overlay) erlauben unterschiedliche Kommunikationswege und Einsatzszenarien. So können Container sicher und flexibel miteinander interagieren.