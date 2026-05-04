# Fragen – Integration der Services (DL10)

Name: Kakhnych Nataliia
Klasse: S-INA24bl

---

## 1. Services verstehen

Welche Services haben Sie in Ihrer `compose.yaml` definiert?

Antwort: frontend, api, adminer, db

---

Welche Aufgabe hat jeder Service in Ihrem System?

Antwort: 

* api: stellt die Anwendungsschnittstelle (Backend) bereit
* db: speichert die Daten in einer PostgreSQL-Datenbank
* adminer: ermöglicht den Zugriff auf die Datenbank über ein Webinterface
* frontend: stellt die Benutzeroberfläche dar

---

## 2. Service-Kommunikation

Welchen Servicenamen verwendet die API, um die Datenbank zu erreichen?

Antwort: ticketboard_db

---

Warum funktioniert `localhost` innerhalb eines Containers nicht für die Kommunikation mit anderen Services?

Antwort: Weil `localhost` immer auf den eigenen Container zeigt und nicht auf andere Container im Netzwerk

---

Wie stellt Docker Compose sicher, dass sich Services gegenseitig finden können?

Antwort: Durch ein gemeinsames Netzwerk mit automatischer DNS-Auflösung über Servicenamen

---

## 3. Ports und Zugriff

Über welche Ports sind folgende Services erreichbar?

* API
* Adminer
* Frontend

Antwort:

* API       5000
* Adminer   8080
* Frontend  8000

---

Welcher Unterschied besteht zwischen:

* Container-Port
* Host-Port

Antwort:

* Container-Port: Port innerhalb des Containers
* Host-Port:      Port auf dem PC

---

## 4. Persistenz

Was passiert mit den Daten, wenn ein Container ohne Volume gelöscht wird?

Antwort: Die Daten gehen verloren

---

Wie haben Sie die Persistenz für die Datenbank umgesetzt?

Antwort: Named Volume

---

Warum ist ein Volume für die Datenbank notwendig?

Antwort: Um die Daten persistent zu speichern

---

## 5. Compose-Konfiguration

Welche Elemente haben Sie in Ihrer `compose.yaml` definiert?

Antwort: 
services, ports, environment, volumes, depends_on, image, build, container_name, env_file

---

Welche Umgebungsvariablen sind für die Datenbank-Verbindung notwendig?

Antwort:
    POSTGRES_DB
    POSTGRES_USER
    POSTGRES_PASSWORD

---

Wofür wird `depends_on` verwendet?

Antwort:
Um die Startreihenfolge von Services zu definieren

---

## 6. Systemtest

Hat das System beim ersten Start vollständig funktioniert?

Antwort:
Nein

---

Welche Probleme sind aufgetreten?

Antwort:
Umgebungsvariablen nicht gesetzt

---

Wie haben Sie diese Probleme gelöst?

Antwort:
Umgebungsvariablen gesetzt

---

## 7. Verständnis

Beschreiben Sie kurz den Datenfluss in Ihrem System.

(Beispiel: Frontend → API → Datenbank)

Antwort:
Frontend → API → Datenbank
Adminer → Datenbank

---

Was passiert beim Befehl:

```bash
docker compose down
```

Antwort:
Die Container und Netzwerke werden gestoppt und gelöscht, Volumes bleiben bestehen

---

## 8. Reflexion

Was war für Sie heute die wichtigste Erkenntnis?

Antwort:
Alles war wichtig

---

Was war schwierig oder noch unklar?

Antwort:
Wo finde ich die Werte für POSTGRES-Umgebungsvariable