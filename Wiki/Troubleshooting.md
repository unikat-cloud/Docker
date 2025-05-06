## 10. Troubleshooting

### 10.1 Häufige Probleme

Beim Arbeiten mit Docker treten immer wieder typische Probleme auf, wie zum Beispiel:

- **Container starten nicht:** Ursachen können fehlende Images, fehlerhafte Konfigurationen oder Port-Konflikte sein.
- **Netzwerkprobleme:** Container können sich nicht verbinden, oft wegen falscher Netzwerk-Einstellungen oder Firewall-Regeln.
- **Speicherprobleme:** Volumes sind nicht korrekt eingebunden oder Datenverluste durch falsch konfigurierte Persistenz.
- **Performanceprobleme:** Container laufen langsam aufgrund von Ressourcenbeschränkungen oder falscher Limits.
- **Berechtigungsfehler:** Probleme durch fehlende Rechte auf Dateien, Verzeichnisse oder beim Zugriff auf Docker daemons.
- **Image-Build Fehler:** Syntaxfehler im Dockerfile oder fehlende Abhängigkeiten.
- **Docker-Daemon startet nicht:** Fehlerhafte Installation oder Systemprobleme.

---

### 10.2 Diagnostic-Tools

Zur Fehlersuche und Diagnose stehen verschiedene Tools und Befehle zur Verfügung:

- `docker logs <container>`  
  Zeigt die Log-Ausgabe eines Containers an.

- `docker ps -a`  
  Listet alle Container (laufend und gestoppt) mit Statusinformationen.

- `docker inspect <container|image>`  
  Liefert detaillierte Metadaten eines Containers oder Images.

- `docker stats`  
  Zeigt Echtzeit-Statistiken über Ressourcenverbrauch laufender Container.

- `docker events`  
  Überwacht Docker Ereignisse in Echtzeit zur Analyse von Aktionen.

- `docker-compose logs`  
  Gibt Logs aller oder einzelner Services einer Compose-Anwendung aus.

- **Externe Tools:**  
  - **Dive:** Analyse von Docker-Images zur Optimierung und Fehlererkennung.  
  - **ctop:** Echtzeit-Überwachung von Containern.  
  - **Trivy / Clair:** Sicherheits-Scanner für Images.

---

### 10.3 Unterstützung und Community-Resourcen

Bei Problemen und Fragen sind folgende Ressourcen hilfreich:

- **Offizielle Docker-Dokumentation:**  
  [https://docs.docker.com/](https://docs.docker.com/)

- **Docker Community Forum:**  
  [https://forums.docker.com/](https://forums.docker.com/)

- **Stack Overflow:**  
  Umfangreiche Fragen und Lösungen rund um Docker mit aktiver Community.

- **GitHub Issues:**  
  Für Fehlerberichte und Feedback zu Docker-Projekten.

- **Blogs und Tutorials:**  
  Viele Anbieter und Entwickler teilen Best Practices, Lösungen und Tipps.

- **Lokale Meetup-Gruppen und Konferenzen:**  
  Teilnahme an Docker- und Container-Events zum Austausch mit Experten.

Durch die Nutzung dieser Ressourcen lassen sich Fehler meist schnell beheben und das Wissen rund um Docker vertiefen.