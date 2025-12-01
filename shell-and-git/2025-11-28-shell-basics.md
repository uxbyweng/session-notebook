# Session Notes – Shell Basics & Computer Setup

**Date:** 28.11.2025  
**Coach:** Roland Hufnagel

---

## Einführung in die Shell

Eine Shell ist eine **Schnittstelle zwischen Nutzer und Betriebssystem**.  
Wir unterscheiden drei Ebenen:

1. **OS (Operating System)** – Layer 1
2. **Shell (zsh, bash, PowerShell)** – Layer 2
3. **Terminal (Git Bash, Windows Terminal, iTerm2)** – Layer 3

**Terminal → Shell → Betriebssystem**

---

## Navigation in der Shell

### `cd` – Verzeichnisse wechseln

-   `cd ..` → eine Ebene nach oben
-   `cd .` → bleibt im aktuellen Ordner
-   `cd folder` → in Ordner wechseln

### `ls` – Dateien anzeigen

-   `ls` → zeigt Inhalte
-   `ls -a` → zeigt _alle_ Inhalte inkl. versteckter Dateien

### Weitere Basisbefehle

-   `pwd` → zeigt aktuellen Pfad
-   `clear` → Terminal leeren
-   Tab ↹ → Autovervollständigung
-   Pfeiltasten ↑↓ → alte Befehle durchscrollen

---

## Dateien & Ordner erstellen

### Ordner erzeugen

```shell
mkdir ordnername
```

### Datei erzeugen

```shell
touch datei.md
```

### Dateiinhalt anzeigen

```shell
cat datei.md
```

### Datei im Editor öffnen

```shell
code index.html
```

---

## Dateien & Ordner löschen

⚠️ Vorsicht: Dieser Befehl löscht **alles ohne Nachfrage**

```shell
rm -rf test
```

---

## Shell Game: Treasure Hunt (Challenge)

Ziel: Durch Verzeichnisstruktur navigieren und versteckte Hinweise finden.

Beispiel aus dem gelösten Run:

```bash
uxbyweng@PAPAYA ~/web-bootcamp/.../.secret-door/tunnel $ cd ..
uxbyweng@PAPAYA ~/web-bootcamp/...$ cat chest.md
Behold the secret treasure!
  .     '     ,
    _________
 _ /_|_____|_\ _
   '. \   / .'
     '.\ /.'
       '.'
```

## Dateien & Ordner verschieben / umbenennen (mv)

### 1. Datei verschieben

```bash
mv index.html assets/
```

### 2. Datei umbenennen

```bash
mv style.css main.css
```

### 3. Datei verschieben + umbenennen

```bash
mv script.js assets/js/app.js
```

### 4. Mehrere Dateien verschieben

```bash
mv *.png assets/img/
```

### 5. Ganzen Ordner verschieben

```bash
mv old_folder/ new_location/
```

### 6. Ordner umbenennen

```bash
mv images old_images
```

### 7. Datei eine Ebene nach oben verschieben

```bash
mv about.html ../
```
