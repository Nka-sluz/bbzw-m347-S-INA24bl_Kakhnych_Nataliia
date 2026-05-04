# Fragen – Konfiguration und Umgebungsvariablen (DL11)

Name: Kakhnych Nataliia
Klasse: S-INA24bl

---

## 1. Konfiguration

Welche Werte sind aktuell hardcoded in `compose.yml` und `app/main.py`?

Antwort:
ticketuser(username), secret(password), ticketdb(db), db_url

---

Warum ist es ein Problem, Passwörter direkt in `compose.yml` einzutragen?

Antwort:
Dann sind die Public und sichtbar für alle

---

Was ist der Unterschied zwischen `.env` und `.env.example`?

Antwort:
.env ist eine Datei mit den echten Konfigurationen, .env.example nur zeigt, was soll in .env definiert werden.

---

Warum muss `.env` in `.gitignore` eingetragen sein?

Antwort:
Um die echte sensible Daten nicht public zu machen

---

## 2. Variablen in Compose

Wie referenziert man eine Variable aus `.env` in `compose.yml`?

Antwort:
Mit ${varname}

---

Was passiert, wenn eine Variable in `.env` fehlt, aber in `compose.yml` verwendet wird?

Antwort:
Docker Compose gibt eine Warnung aus und setzt den Wert als leeren String

---

Was zeigt der Befehl `docker compose config`? Wann ist er nützlich?

Antwort:
Der Befehl gibt die vollständig aufgelöste Compose-Konfiguration aus – alle `${VARIABLE}`-Platzhalter sind durch die echten Werte aus `.env` ersetzt. Er ist nützlich zur Überprüfung vor dem Start: Man sieht sofort, ob alle Variablen korrekt substituiert werden oder ob Werte fehlen

---

## 3. Dockerfile und Build

Warum wird `requirements.txt` in einem eigenen `COPY`-Schritt vor dem App-Code kopiert?

Antwort:
Für Caching

---

Was bewirkt `.dockerignore`? Welche Dateien sollten darin stehen?

Antwort:
.dockerignore definiert welche Dateien sollen nicht ins Image drin

---

## 4. Systemtest

Funktioniert `/db-check` nach Ihrer Konfigurationsanpassung?

Antwort:
Ja

---

Was zeigt der Endpunkt `/db-check` an, wenn die Verbindung funktioniert?

Antwort:
{"db":"connected"}

---

## 5. Reflexion

Was war der wichtigste Schritt in dieser Woche?

Antwort:
.env und .env.example

---

Was ist noch unklar oder möchten Sie besser verstehen?

Antwort:
