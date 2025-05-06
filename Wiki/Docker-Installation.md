## 3. Docker Installation

### 3.1 Voraussetzungen

Bevor Docker auf einem System installiert werden kann, sollten folgende Voraussetzungen erfüllt sein:

- **64-Bit-Architektur:** Docker benötigt ein 64-Bit-Betriebssystem.
- **Betriebssystem:** Für Docker Desktop werden Windows 10 (64-bit) Version 1903 oder höher, macOS 10.14 oder höher sowie verschiedene Linux-Distributionen unterstützt.
- **Virtualisierung:** Die Virtualisierungstechnologie muss im BIOS/UEFI aktiviert sein (z.B. Intel VT-x oder AMD-V).
- **Systemressourcen:** Mindestens 4 GB RAM werden empfohlen, um Docker-Container flüssig laufen zu lassen.
- **Benutzerrechte:** Administrator- oder Root-Rechte sind für die Installation erforderlich.
- **Linux-Kernel:** Auf Linux-Systemen sollte der Kernel mindestens Version 3.10 unterstützen, da Docker auf Linux-Namespaces und cgroups angewiesen ist.

---

### 3.2 Installationsanleitung für Windows, macOS, Linux

#### Windows

1. **Docker Desktop herunterladen:**  
   Besuche die offizielle Webseite [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop) und lade die Windows-Version herunter.

2. **Installation ausführen:**  
   Starte den Installer und folge den Anweisungen. Optional wird empfohlen, WSL2 (Windows Subsystem for Linux 2) für bessere Performance zu installieren und zu aktivieren.

3. **System neu starten:**  
   Nach der Installation ist meist ein Neustart erforderlich.

4. **Docker starten:**  
   Öffne Docker Desktop über das Startmenü und überprüfe im Terminal mit  
   ```bash
   docker version
   ```  
   ob die Installation erfolgreich war.

#### macOS

1. **Docker Desktop herunterladen:**  
   Lade die macOS-Version von der offiziellen Docker-Webseite herunter.

2. **Installation:**  
   Öffne die heruntergeladene `.dmg`-Datei und ziehe das Docker-Symbol in den Programme-Ordner.

3. **Docker starten:**  
   Starte Docker über den Programme-Ordner oder Spotlight.

4. **Überprüfung:**  
   Öffne das Terminal und führe  
   ```bash
   docker version
   ```  
   oder  
   ```bash
   docker info
   ```  
   aus, um sicherzustellen, dass Docker läuft.

#### Linux (z.B. Ubuntu)

1. **Repository vorbereiten:**  
   Aktualisiere die Paketliste und installiere benötigte Pakete:
   ```bash
   sudo apt update
   sudo apt install apt-transport-https ca-certificates curl gnupg lsb-release
   ```

2. **Docker GPG-Schlüssel hinzufügen:**  
   ```bash
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```

3. **Docker-Repository hinzufügen:**  
   ```bash
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```

4. **Docker Engine installieren:**  
   ```bash
   sudo apt update
   sudo apt install docker-ce docker-ce-cli containerd.io
   ```

5. **Docker-Dienst starten und aktivieren:**  
   ```bash
   sudo systemctl start docker
   sudo systemctl enable docker
   ```

6. **Installation überprüfen:**  
   Teste mit folgendem Befehl die Installation:  
   ```bash
   docker run hello-world
   ```

---

## 3.3 Erste Schritte nach der Installation

Nach der erfolgreichen Installation von Docker empfiehlt es sich, einige grundlegende Schritte durchzuführen, um Docker effektiv nutzen zu können:

- **Benutzerrechte konfigurieren (Linux):**  
  Um Docker-Befehle ohne `sudo` auszuführen, kann der eigene Benutzer zur Docker-Gruppe hinzugefügt werden:
  ```bash
  sudo usermod -aG docker $USER
  ```
  Danach ist ein Ab- und erneutes Anmelden erforderlich.

- **Docker Version prüfen:**  
  Mit dem Befehl  
  ```bash
  docker version
  ```  
  wird die installierte Docker-Version und die verfügbaren Komponenten angezeigt.

- **Hallo-Welt-Container starten:**  
  Um sicherzustellen, dass alles korrekt funktioniert, kann folgender Befehl ausgeführt werden:  
  ```bash
  docker run hello-world
  ```  
  Dieser lädt ein Test-Image aus der Docker Registry und startet einen Container, der eine Erfolgsmeldung ausgibt.

- **Docker Hub Konto anlegen (optional):**  
  Für das Herunterladen und Hochladen eigener Images ist ein Account auf **Docker Hub** sinnvoll.

- **Erkundung der Docker CLI:**  
  Erste Befehle wie `docker ps` (laufende Container anzeigen), `docker images` (vorhandene Images auflisten) oder `docker stop <container_id>` (Container stoppen) helfen beim Einstieg.

- **Dokumentation lesen:**  
  Die offizielle Docker-Dokumentation bietet viele weiterführende Informationen und Beispiele.