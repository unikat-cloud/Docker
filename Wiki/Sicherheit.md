## 7. Sicherheit

### 7.1 Best Practices beim Erstellen von Containern

Die Sicherheit von Docker-Containern beginnt bereits beim Erstellen der Images. Einige bewährte Vorgehensweisen sind:

- **Minimalistische Basisimages verwenden:** Nutze schlanke und offizielle Basisimages (z.B. Alpine), um den Angriffsflächenbereich zu reduzieren.
- **Nur benötigte Pakete installieren:** Vermeide unnötige Software und Abhängigkeiten im Image, um potenzielle Sicherheitslücken zu minimieren.
- **Mehrstufiges Bauen (Multi-Stage Builds):** Nutze Multi-Stage Builds, um unnötige Build-Tools und temporäre Dateien nicht ins finale Image zu übernehmen.
- **Benutzerrechte einschränken:** Führe Anwendungen im Container als nicht-root Benutzer aus, wenn möglich, um Schadcode-Effekte zu begrenzen.
- **Secrets nicht im Image speichern:** Vermeide es, sensible Daten wie Passwörter oder API-Schlüssel direkt im Image oder im Dockerfile abzulegen.
- **Regelmäßige Updates:** Halte Basisimages und verwendete Abhängigkeiten aktuell, um bekannte Sicherheitslücken zu schließen.
- **Container-Scans verwenden:** Nutze Tools zur Analyse von Images auf bekannte Schwachstellen (z.B. Clair, Trivy).

---

### 7.2 Sicherheitslücken und -maßnahmen

Container-Technologie bringt eigene Sicherheitsherausforderungen mit sich:

- **Kernel-Sharing:** Container teilen sich den Host-Kernel, weshalb Kernel-Sicherheitslücken potenziell alle Container betreffen können.
- **Escape-Angriffe:** Angreifer könnten versuchen, aus dem Container auszubrechen und Zugriff auf den Host zu erlangen.
- **Unsichere Netzwerke:** Standardmäßig können Container untereinander kommunizieren; unkontrollierte Netzwerke können Angriffsflächen darstellen.
- **Image-Integrität:** Gefälschte oder manipulierte Images aus unsicheren Quellen können Schadcode enthalten.

Typische Maßnahmen sind:

- **Kernel-Sicherheitsupdates:** Halte das Host-System immer aktuell.
- **Container-Runtime-Limits:** Nutze Linux-Sicherheitsmechanismen wie seccomp, AppArmor oder SELinux, um Container einzuschränken.
- **Netzwerksegmentation:** Verwende Container-Netzwerke mit Regelwerken, um Zugriffe einzuschränken.
- **Image-Authentifizierung:** Nutze signierte Images und vertrauenswürdige Registries.
- **Least Privilege Prinzip:** Vermeide zu weitreichende Rechte und root-Zugriffe in Containern.
- **Monitoring und Logging:** Überwache Containeraktivitäten und prüfe ungewöhnliche Verhaltensweisen.

---

### 7.3 Benutzer- und Zugriffsverwaltung

Eine sorgfältige Kontrolle von Benutzerrechten und Zugriffsrechten ist essenziell für die Sicherheit:

- **Docker-Gruppenrechte:** Auf Linux-Systemen erhalten Nutzer der Docker-Gruppe indirekt Root-Rechte. Gruppenmitglieder sollten daher nur vertrauenswürdige Benutzer sein.
- **Role-Based Access Control (RBAC):** In Kubernetes und anderen Orchestrierungssystemen können feingranulare Zugriffsrechte für Benutzer und Dienste definiert werden.
- **Credentials und Secrets:** Nutze spezielle Mechanismen zur sicheren Verwaltung von Zugangsdaten und geheimen Schlüsseln, etwa Docker Secrets oder Kubernetes Secrets.
- **API-Schutz:** Schütze die Docker-Daemon-API gegen unbefugten Zugriff, indem sie nur über sichere Verbindungen oder mit Authentifizierung erreichbar ist.
- **Audit-Logging:** Führe Protokolle über Zugriffe und Aktionen, um im Sicherheitsfall Ursachen und Verantwortlichkeiten nachvollziehen zu können.

Durch eine Kombination von technischer Absicherung, organisatorischen Regeln und regelmäßigen Überprüfungen lässt sich das Risiko von Container-Komponenten deutlich reduzieren.