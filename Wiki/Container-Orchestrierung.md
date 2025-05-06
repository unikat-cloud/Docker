## 6. Container-Orchestrierung

### 6.1 Einführung in Orchestrierungskonzepte

Container-Orchestrierung bezeichnet die automatisierte Verwaltung, Koordination und Skalierung von Containern in komplexen, verteilten Umgebungen. Während einzelne Container einfach mit Docker oder Docker Compose betrieben werden können, wachsen bei größeren Anwendungen mit vielen Containern die Anforderungen an Ausfallsicherheit, Lastverteilung, Service-Discovery, Netzwerkkonfiguration und Ressourcenmanagement. Orchestrierungslösungen übernehmen deshalb zentrale Aufgaben wie:

- Starten, Stoppen und Neustarten von Containern basierend auf definierten Regeln
- Automatische Skalierung der Container-Anzahl je nach Bedarf
- Verteilung von Containern auf verschiedene Hosts und Cluster-Ressourcen
- Verwaltung der Netzwerkkonnektivität zwischen Containern
- Monitoring und Selbstheilung (z.B. Neustart bei Fehlfunktionen)
- Rollouts und Updates ohne Unterbrechung (Zero Downtime Deployments)

Diese Automatisierung ist essenziell für den Betrieb von Microservice-Architekturen und cloudnativen Anwendungen.

---

### 6.2 Kubernetes (kurz, Vergleich zu Docker Compose)

**Kubernetes** ist ein weitverbreitetes, Open-Source-Orchestrierungssystem zur Verwaltung containerisierter Anwendungen in Clustern. Es bietet umfangreiche Funktionen, die weit über Docker Compose hinausgehen:

| Feature                | Docker Compose                     | Kubernetes                                |
|------------------------|----------------------------------|-------------------------------------------|
| Skalierung             | Manuell, über `docker-compose up`| Automatisch, basierend auf Ressourcen     |
| Multi-Host Betrieb     | Eingeschränkt, meist Single-Host  | Vollständig Multi-Host / Clusterfähig      |
| Selbstheilung          | Keine eingebauten Mechanismen     | Automatisches Neustarten / Replizieren     |
| Service Discovery      | Grundlegendes Netzwerkmanagement | Eingebaute Service Discovery und Load Balancing |
| Rolling Updates        | Manuell                         | Unterstützt sanfte Rollouts mit Rollbacks  |
| Umfangreiche APIs      | Limitierte CLI                   | Erweiterbare APIs, umfangreiche Steuerung |

Kubernetes ist damit die bevorzugte Lösung für produktive Umgebungen mit hohen Anforderungen, während Docker Compose vor allem für lokale Entwicklung und kleinere Umgebungen genutzt wird.

---

### 6.3 Automatisierung und Skalierung

Orchestrierungssysteme wie Kubernetes ermöglichen:

- **Automatische Skalierung:** Durch Ressourcenüberwachung (CPU, Speicher, Netzwerk) können Container-Instanzen abhängig von der Last automatisch hoch- oder runtergefahren werden (Horizontal Pod Autoscaling).
  
- **Selbstheilung:** Defekte oder ausgefallene Container werden erkannt und automatisch neu gestartet, um Ausfallzeiten zu minimieren.
  
- **Deklarative Konfiguration:** Anwender beschreiben den gewünschten Zustand der Anwendung (Anzahl Container, Netzwerke, Speicher) in Konfigurationsdateien, Kubernetes sorgt dafür, dass dieser Zustand eingehalten wird.
  
- **Automatische Rollouts und Rollbacks:** Neue Versionen von Anwendungen können schrittweise ausgerollt werden. Bei Problemen ermöglicht Kubernetes ein Zurückrollen auf eine funktionierende Version.
  
- **Integration in CI/CD Pipelines:** Automatisierte Workflows können auf Basis von Container-Orchestrierung neue Versionen testen, deployen und überwachen.

Diese Features sorgen für hohe Verfügbarkeit, Flexibilität und Effizienz im Cloud- und Cluster-Betrieb moderner Anwendungen.