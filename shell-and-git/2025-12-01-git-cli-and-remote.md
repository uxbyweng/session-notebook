# Session Notes – Git CLI & Remote

**Date:** 01.12.2025  
**Coach:** Felix

---

## 1. Was ist ein Repository?

Ein **Repository (Repo)** ist ein Projektordner, in dem Git alle Änderungen versioniert.

---

## 2. Was sind Commits?

-   Ein Commit ist **eine gespeicherte Version** der Dateien.
-   Der **erste Commit** speichert den vollständigen Stand.
-   Alle nächsten Commits speichern nur **die Änderungen**.
-   Jeder Commit stellt einen **Zeitpunkt** dar, den man jederzeit wiederherstellen kann.

### Praktisch:

```bash
git add .
git commit -m "add feature: something"
```

---

## 3. Git Versionierung – Grundidee

-   Ein Versionierungstool (wie Git) kann:
    -- viele Versionen verwalten
    -- Änderungen nachvollziehbar machen
    -- Teamarbeit ermöglichen
    -- Fehler rückgängig machen (git restore, git checkout, git revert)

## 4. Wichtige Git CLI Befehle

### Lokales Repo initialisieren

```bash
git init
```

### Remote hinzufügen

```bash
git remote add origin git@github.com:<username>/<repo>.git
```

### Dein Beispiel:

```bash
git remote add origin git@github.com:uxbyweng/web-challenges.git
```

### Pushen

```bash
git push origin main
```

### Pullen

```bash
git pull origin main
```

### Klonen

```bash
git clone git@github.com:neuefische/pirates-fssd-ber-25.git
```

## Upload Web Challenges (Aufgabe)

**Ziel**: Der Ordner web-challenges wird ein Git-Repo und auf GitHub hochgeladen.

### Schritte:

1.  Ordner betreten

```bash
cd web-challenges
```

2.  Repo initialisieren

```bash
git init
```

3.  Neues GitHub-Repo anlegen (leer)

```
Auf GitHub ein neues (leeres) Repository anlegen
https://github.com/
```

4.  Remote verbinden

```bash
git remote add origin git@github.com:uxbyweng/web-challenges.git
```

5. Änderungen hinzufügen -> alle geänderten Dateien (!Vorsicht - am besten vorher mit git status checken was alles dabei ist)

```bash
git add .
```

Änderungen hinzufügen -> bestimmte Datei(en)

```bash
git add <dateiname>
```

6. Änderungen committen

```bash
git push -m "Aussagekräftige Commit-Message"
```

7. Änderungen pushen (initial - mit 'set upstream' - nur beim ersten push im Repository)

```bash
git push -u origin main
```

Änderungen pushen

```bash
git push
```

### Weitere git Befehle

Git Logfile anzeigen lassen

```bash
git log   -> kompaktere ansicht
```

Git Logfile kompakt anzeigen lassen

```bash
git log --oneline
```
