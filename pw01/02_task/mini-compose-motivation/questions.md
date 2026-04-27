# Fragen – Mini Compose Motivation

Name: <Nachname> <Vorname>  
Klasse: <Klasse>

---

## 1. Services verstehen

Welche Services sind in `compose.yaml` definiert?

Antwort:  
  web, api, admin

---

Welcher Service verwendet ein fertiges Image (`image`)?

Antwort:  
  web, admin

---

Welcher Service wird aus einem Dockerfile gebaut (`build`)?

Antwort:  
  api

---

## 2. Ports und Zugriff

Über welchen Host-Port ist der Web-Service **zu Beginn** erreichbar?

Antwort:  
  8080

---

Welchen Port verwendet der API-Service?

Antwort:  
  5000

---

Auf welchen Port haben Sie den Web-Service geändert?

Antwort:  
  8000

---

## 3. Verständnis Docker Compose

Warum ist Docker Compose in diesem Beispiel sinnvoll?

Antwort:  
  Es startet 3 Containers

---

Was ist der Unterschied zwischen `image` und `build`?

Antwort:  
  Image ist vom Registry geladen und build erstellt ein image lokal

---

Was macht der Befehl `docker compose up --build`?

Antwort:  
  Buildet die Images neu wo `build` configuriet ist und dann startet alle definierten Services

---

## 4. Fehleranalyse

Startete das System beim ersten Versuch vollständig?

Antwort:  
  Nein

---

Welcher Service hatte ein Problem?

Antwort:  
  api

---

Was war die Ursache für das Problem?

Antwort:  
  build: . statt build: ./api

---

Wie haben Sie das Problem gelöst?

Antwort:  
  Ordner angepasst (build: ./api)

---

## 5. Docker Compose CLI

Was ist der Unterschied zwischen:

- `docker compose stop`  
- `docker compose pause`  

Antwort:  
  stop stoppt der Container komplett, pause friert den Container ein

---

Was zeigt der Befehl `docker compose logs` an?

Antwort:  
  Der Befehl zeigt die Log-Ausgaben aller Container an

---

Was zeigt der Befehl `docker compose ps` an?

Antwort:  
  Der Befehl zeigt den aktuellen Status der Container

---

## 6. Reflexion

Was war für Sie heute neu oder besonders wichtig?

Antwort:  
  

---

Was ist noch unklar oder möchten Sie noch besser verstehen?

Antwort:  
  