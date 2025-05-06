# Wiki: Docker Container

## 1. Einleitung

### 1.1 Was sind Docker Container?

Docker Container sind eine Technologie, mit der Anwendungen und deren Abhängigkeiten in isolierten, portablen und leichtgewichtigen Umgebungen ausgeführt werden können. Ein Container kapselt dabei die Anwendung zusammen mit all ihren Bibliotheken, Konfigurationsdateien und Laufzeitkomponenten ein, sodass sie unabhängig von der zugrundeliegenden Infrastruktur überall gleich läuft. Technisch basieren Docker Container auf OS-Level-Virtualisierung (meist Linux-Namespaces und cgroups), wodurch mehrere Container auf demselben Betriebssystem-Kernel isoliert ausgeführt werden können, ohne den Overhead vollständiger Betriebssystemvirtualisierung wie bei traditionellen virtuellen Maschinen. Docker stellt hierzu eine einheitliche Plattform und Werkzeuge bereit, um Container einfach zu erstellen, zu starten, zu stoppen und zu verwalten. In der Praxis ermöglichen Docker Container eine schnelle, konsistente und reproduzierbare Bereitstellung von Anwendungen über verschiedene Umgebungen hinweg – von lokalen Developer-Maschinen über Test- und Staging-Systeme bis hin zu Produktionsservern in der Cloud.

---

### 1.2 Geschichte und Entwicklung von Docker

Docker wurde 2013 von Solomon Hykes als Open-Source-Projekt gestartet und hat die Art und Weise revolutioniert, wie Software entwickelt, verteilt und betrieben wird. Ursprünglich entstand Docker innerhalb des Cloud-Hosting-Anbieters dotCloud (später umbenannt in Docker Inc.) und basierte auf bestehenden Linux-Technologien wie LXC (Linux Containers). Der Durchbruch gelang mit der Entwicklung eines einfach zu bedienenden, standardisierten Tools, das Container-Images handhabbar macht, die Laufzeitumgebung abstrahiert und die Portabilität von Containern sicherstellt. Seit der Veröffentlichung der ersten Version hat Docker viele Ergänzungen und Ökosystemkomponenten erhalten, darunter das Docker Hub (ein Registry-Dienst für Container-Images) und Werkzeuge für Netzwerk, Speicher und Orchestrierung. Docker hat in der Folge auch andere Container-Technologien inspiriert und gemeinsam mit Kubernetes das Container-Ökosystem stark geprägt. Heute ist Docker ein zentraler Baustein moderner DevOps-Prozesse und Cloud-Infrastrukturen.

---

### 1.3 Vorteile von Containern gegenüber herkömmlichen Virtual Machines

Docker Container bieten gegenüber klassischen virtuellen Maschinen (VMs) mehrere wichtige Vorteile:

- **Ressourceneffizienz:** Container teilen sich den Kernel des Host-Betriebssystems und benötigen somit weniger Speicher und CPU-Ressourcen als vollständige VMs, die jeweils ein komplettes Betriebssystem laden.
- **Schnellere Startzeiten:** Container starten üblicherweise in Sekundenbruchteilen, während VMs oft Minuten zum Booten benötigen.
- **Portabilität:** Container sind plattformunabhängig und können auf allen Systemen mit kompatibler Container-Laufzeit identisch laufen, unabhängig von der darunterliegenden Infrastruktur.
- **Einfachheit in der Verteilung:** Durch containerisierte Images können ganze Anwendungspakete inklusive aller Abhängigkeiten versioniert und zwischen Entwicklern, Testern und Betriebsteams ausgetauscht werden.
- **Geringerer Verwaltungsaufwand:** Das Bereitstellen und Aktualisieren von Containeranwendungen erfordert weniger Aufwand, da Änderungen in Images eingepackt und verteilt werden, ohne Hostsysteme anfassen zu müssen.
- **Isolierung und Sicherheit:** Container isolieren Anwendungen voneinander, wodurch Fehlfunktionen in einem Container andere nicht direkt beeinflussen. Zugleich läuft alles auf dem gleichen OS-Kernel, was jedoch auch Herausforderungen bei der Sicherheit bedeutet, die mit zusätzlichen Mechanismen adressiert werden.

Im Vergleich dazu sind VMs durch ihren isolierten Hypervisor-Ansatz zwar bei Mehrmandanten-Umgebungen und unterschiedlichen Betriebssystemen oft sicherer und flexibler, aber deutlich schwergewichtiger und weniger dynamisch.

---

### 1.4 Einsatzbereiche und Anwendungsfälle

Docker Container und Container-Technologie haben eine Vielzahl von Einsatzgebieten und Anwendungsfällen:

- **Entwicklung und Testing:** Entwickler können komplette Software-Stacks als Container definieren, was das Reproduzieren von Fehlern und Testumgebungen erheblich erleichtert.
- **Continuous Integration / Continuous Deployment (CI/CD):** Automatisierte Pipelines nutzen Container, um Anwendungen in konsistenten Umgebungen zu bauen, zu testen und nahtlos zu deployen.
- **Microservices:** Container eignen sich hervorragend für die Umsetzung von Microservice-Architekturen, da jeder Service als eigenständiger Container betrieben, skaliert und aktualisiert werden kann.
- **Cloud Native Anwendungen:** Container lassen sich leicht in Cloud-Umgebungen integrieren, wodurch flexible Skalierbarkeit und Orchestrierung via Kubernetes oder anderen Tools möglich wird.
- **Legacy-Anwendungsmigration:** Container können auch Legacy-Applikationen einschließen und so deren Betrieb auf moderner Infrastruktur ermöglichen, ohne die Anwendungen selbst umfassend zu ändern.
- **Edge Computing und IoT:** Auf Geräten mit begrenzten Ressourcen bieten Container effiziente Methoden für den Betrieb isolierter Anwendungen.
- **Sicherheitsisolierung:** Durch Container können Applikationen mit geringerer gegenseitiger Abhängigkeit betrieben werden, wodurch Angriffsflächen reduziert werden.

Insgesamt haben Docker Container die Softwareentwicklung, den Betrieb und die Cloud-Architektur nachhaltig geprägt und sind heute ein Standardwerkzeug in zahlreichen IT-Projekten.