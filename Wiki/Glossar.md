## 12. Glossar

Hier eine Erklärung wichtiger Begriffe rund um Docker und Container-Technologien:

- **Docker Container:**  
  Eine leichtgewichtige, isolierte Laufzeitumgebung, die eine Anwendung und ihre Abhängigkeiten kapselt. Container basieren auf OS-Level-Virtualisierung und teilen sich den Host-Kernel.

- **Docker Image:**  
  Ein unveränderliches Template, das alle Bestandteile und Konfigurationen enthält, um einen Container zu starten. Images sind in Layers aufgebaut und werden häufig in Registries gespeichert.

- **Dockerfile:**  
  Eine Textdatei mit einer Schritt-für-Schritt-Anleitung zum Erstellen eines Docker Images. Enthält Anweisungen wie Basis-Image, Kopieren von Dateien, Installieren von Software und Startbefehle.

- **Docker Daemon (`dockerd`):**  
  Der Prozess auf dem Host, der Docker-Container verwaltet, überwacht und ausführt. Kommuniziert über REST-API mit der Docker CLI.

- **Docker CLI (`docker`):**  
  Das Kommandozeilen-Interface zur Interaktion mit dem Docker Daemon. Ermöglicht das Erstellen, Verwalten und Steuern von Containern und Images.

- **Docker Registry:**  
  Eine zentrale Ablage für Docker Images. Beispiele sind Docker Hub (öffentlich) oder private Registries. Images können dort hochgeladen (`push`) und heruntergeladen (`pull`) werden.

- **Volumes:**  
  Persistente Speicherbereiche, die von Containern genutzt werden, um Daten auch nach dem Stoppen oder Neustarten eines Containers zu erhalten. Ermöglichen Datenaustausch zwischen Containern und persistente Speicherung.

- **Netzwerke (Bridge, Host, Overlay):**  
  Mechanismen zur Vernetzung von Containern:  
  - *Bridge:* Standardnetzwerk, isoliert Container, erlaubt Kommunikation auf demselben Host.  
  - *Host:* Container teilen das Netzwerk des Hosts direkt.  
  - *Overlay:* Vernetzt Container über mehrere Hosts hinweg in Clustern.

- **Docker Compose:**  
  Ein Tool zur Definition und Verwaltung von Multi-Container-Anwendungen mittels einer YAML-Konfigurationsdatei (`docker-compose.yml`). Erleichtert das Starten, Stoppen und Skalieren mehrerer Container als Einheit.

- **Container-Orchestrierung:**  
  Automatisierte Verwaltung und Skalierung von Containern in produktiven Umgebungen. Beispiele sind Kubernetes und Docker Swarm, die Funktionen wie Lastverteilung, Selbstheilung, Rollouts und Multi-Host-Betrieb bieten.

- **Multi-Stage Builds:**  
  Eine Methode zur Optimierung von Docker Images, bei der unterschiedliche Build-Phasen in einem Dockerfile definiert werden, um schlankere, produktive Images ohne überflüssige Build-Artefakte zu erzeugen.

- **CI/CD (Continuous Integration / Continuous Deployment):**  
  Automatisierte Prozesse, die das häufige Bauen, Testen und Deployen von Software mit Docker-Containern ermöglichen, um Entwicklungszyklen zu beschleunigen und Qualität zu erhöhen.

- **Security Best Practices:**  
  Empfehlungen zur Sicherung von Docker-Containern, wie die Nutzung minimaler Basisimages, Vermeidung von Root-Nutzern, regelmäßige Updates, Einsatz von Runtime-Sicherheitsmechanismen (z.B. SELinux, AppArmor) und Absicherung von Zugriffsrechten.

- **Bind Mount:**  
  Ein Verzeichnis oder eine Datei vom Host-System, die direkt in einen Container eingebunden wird. Anders als Volumes sind Bind Mounts vom Host-Dateisystem abhängig und weniger portabel.

- **Docker Hub:**  
  Die offizielle öffentliche Registry von Docker, in der viele vorgefertigte Images bereitgestellt werden und eigene Images gehostet werden können.

- **Role-Based Access Control (RBAC):**  
  Ein Berechtigungsmodell, das den Zugriff auf Ressourcen (z.B. Container, Images) über Rollen und Rechte in Orchestrierungssystemen wie Kubernetes steuert.

Dieses Glossar bietet eine kompakte Übersicht zentraler Begriffe, die für das Verständnis und den Umgang mit Docker essenziell sind.