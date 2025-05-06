## 5. Docker Compose

### 5.1 Einführung und Nutzen

Docker Compose ist ein Werkzeug, mit dem mehrere Docker-Container als eine zusammenhängende Anwendung definiert und verwaltet werden können. Anstatt jeden Container einzeln zu starten und zu konfigurieren, ermöglicht Docker Compose die Beschreibung der gesamten Multi-Container-Anwendung in einer einzigen YAML-Datei (`docker-compose.yml`). Dies erleichtert die Automatisierung, Wiederholbarkeit und Verwaltung von komplexen Systemen, z.B. wenn eine Anwendung aus mehreren Services wie Datenbanken, Webservern und Caches besteht. Docker Compose ist besonders hilfreich in Entwicklungs-, Test- und Staging-Umgebungen, um schnell komplette Umgebungen zu starten und zu stoppen, aber auch im produktiven Einsatz möglich.

---

### 5.2 Aufbau einer docker-compose.yml

Eine `docker-compose.yml` sichert die Definition der Container, der zu verwendenden Images, der Netzwerke, Volumes und weiterer Einstellungen. Wichtige Bestandteile sind:

```yaml
version: '3.8'                # Version der Compose Spezifikation
services:                    # Definition der Container-Services
  web:
    image: nginx:latest       # Image für den Service
    ports:
      - "8080:80"             # Port-Mapping Host zu Container
    volumes:
      - ./html:/usr/share/nginx/html   # Volume-Mount
    depends_on:
      - db                    # Abhängigkeit von db-Service

  db:
    image: postgres:13
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
    volumes:
      - pgdata:/var/lib/postgresql/data

volumes:
  pgdata:                     # definiertes benanntes Volume
```

Diese Datei beschreibt z.B. eine Anwendung mit einem `web`-Service (Nginx-Webserver) und einer `db`-Datenbank (PostgreSQL), inklusive Portweiterleitung, Volumes und Umgebungsvariablen.

---

### 5.3 Beispiel für Multi-Container-Anwendungen

Ein einfaches Beispiel mit einem Webserver und einer Datenbank:

```yaml
version: '3.8'
services:
  app:
    build: ./app             # Dockerfile im Ordner app verwenden
    ports:
      - "5000:5000"
    environment:
      - DATABASE_URL=postgres://user:pass@db:5432/mydb
    depends_on:
      - db

  db:
    image: postgres:13
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
    volumes:
      - pgdata:/var/lib/postgresql/data

volumes:
  pgdata:
```

Hier wird der `app`-Container aus einem lokalen Dockerfile gebaut und kommuniziert mit der PostgreSQL-Datenbank `db`. Das Volume `pgdata` sorgt für persistente Daten.

---

### 5.4 Befehle (up, down, ps, logs etc.)

Die wichtigsten Docker Compose Befehle sind:

- `docker-compose up`  
  Startet alle in der `docker-compose.yml` definierten Container. Mit der Option `-d` läuft alles im Hintergrund (detached).

- `docker-compose down`  
  Stoppt und entfernt alle Container, Netzwerke und Volumes, die durch `up` erzeugt wurden.

- `docker-compose ps`  
  Zeigt den Status aller laufenden Container der Compose-Anwendung an.

- `docker-compose logs [Service]`  
  Zeigt die Protokolle (Logs) aller oder eines spezifischen Services an.

- `docker-compose build`  
  Baut alle oder bestimmte Container-Images neu.

- `docker-compose stop` / `start`  
  Stoppt oder startet bereits erstellte Container.

Diese Befehle erleichtern den Umgang mit Multi-Container-Setups und helfen bei Entwicklung, Debugging und Betrieb.

---