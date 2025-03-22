# Baikal und Docker: Kalender und Kontakte selbst hosten

Baikal ist eine Open-Source-Anwendung, die es Benutzern ermöglicht, ihre Kalender und Kontakte auf einem eigenen Server zu hosten. Sie unterstützt die Standards CalDAV und CardDAV, was bedeutet, dass sie mit einer Vielzahl von Clients und Geräten kompatibel ist.

Hier sind einige wichtige Informationen zu Baikal und Docker:

* **Docker-Image**:
    * Obwohl es kein offizielles Docker-Image für Baikal gibt, wird ein von der Community gepflegtes Image namens `ckulka/baikal` auf Docker Hub angeboten.
    * Dieses Image erleichtert die Installation und Konfiguration von Baikal erheblich.
* **Vorteile der Verwendung von Docker**:
    * **Einfache Installation**: Docker vereinfacht die Installation von Baikal, indem es alle erforderlichen Abhängigkeiten in einem Container kapselt.
    * **Isolation**: Docker-Container isolieren Baikal von anderen Anwendungen auf Ihrem Server, wodurch potenzielle Konflikte vermieden werden.
    * **Portabilität**: Docker-Container können problemlos zwischen verschiedenen Systemen verschoben werden.
* **Installation**:
    * Die Installation von Baikal mit Docker ist relativ einfach. Sie müssen lediglich das Docker-Image herunterladen und einen Container erstellen.
    * Auf Github unter ckulka/baikal-docker, werden beispiele für eine docker-compose.yaml bereitgestellt.
    * Es gibt viele Anleitungen im Netz, die eine Installtion via Docker und Baikal beschreiben.
