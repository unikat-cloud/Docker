## 8. Netzwerk und Volumes

### 8.1 Container-Netzwerke

Docker bietet verschiedene Netzwerk-Treiber, die unterschiedliche Anwendungsfälle abdecken. Die wichtigsten sind:

- **Bridge-Netzwerk:**  
  Das Standard-Netzwerk für einzelne Docker-Hosts. Container in einem Bridge-Netzwerk können miteinander kommunizieren, sind aber vom Host-Netzwerk isoliert. Ein Bridge-Netzwerk macht es einfach, Container miteinander zu verbinden und IP-Adressen dynamisch zu vergeben.

- **Host-Netzwerk:**  
  Hier teilen sich Container direkt das Netzwerk des Host-Systems. Der Container nutzt dabei die Netzwerk-Schnittstellen und Ports des Hosts ohne Isolation. Dies führt zu einer höheren Performance, birgt aber auch Sicherheitsrisiken, da die Isolation entfällt.

- **Overlay-Netzwerk:**  
  Ermöglicht die Vernetzung von Containern über mehrere Docker-Hosts hinweg, die zusammen ein Cluster bilden (z.B. bei Docker Swarm oder Kubernetes). Overlay-Netzwerke abstrahieren das zugrundeliegende physische Netzwerk, wodurch Container auf verschiedenen Hosts so verbunden sind, als wären sie im selben lokalen Netzwerk.

---

### 8.2 Data Persistent Storage mit Volumes

Container sind von Natur aus zustandslos und flüchtig – beim Stoppen oder Löschen eines Containers gehen alle gespeicherten Daten verloren, sofern diese nicht extern gespeichert werden. Volumes bieten eine Möglichkeit, Daten persistent und unabhängig von der Lebensdauer eines Containers zu speichern.

- **Volumes:**  
  Managed Storage-Bereiche, die von Docker verwaltet werden. Sie sind einfach zu verwenden, robust und ideal für Persistenz. Volumes können zwischen mehreren Containern geteilt werden und sind unabhängig vom verwendeten Host-Dateisystem.

- **Vorteile von Volumes:**  
  - Unabhängigkeit vom Containerlebenszyklus  
  - Einfaches Backup und Migration  
  - Verbesserte Performance gegenüber Bind Mounts

---

### 8.3 Daten auf Host-Systeme mounten

Neben Volumes gibt es auch die Möglichkeit, Verzeichnisse oder Dateien vom Host-System direkt in einen Container einzubinden (sogenannte Bind Mounts). Dies ist besonders nützlich für:

- Entwicklung, um Quellcode direkt im Container verfügbar zu machen  
- Zugriff auf Konfigurationsdateien oder Logs auf dem Host  
- Nutzung spezieller Hardware oder Ressourcen des Hosts

**Beispiel für einen Bind Mount:**

- Dabei wird das Verzeichnis /pfad/auf/dem/host vom Host in den Container unter /pfad/im/container eingebunden.