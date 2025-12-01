# Session Notes – HTML and the Web

**Date:** 01.12.2025  
**Coach:** Felix

---

## 1. Was passiert, wenn ich eine Website aufrufe?

(Gruppenarbeit – 15 Minuten)

### Browser → DNS → Server → Browser

1. **URL eingeben**

    - Jede Domain zeigt auf eine **IP-Adresse**.
    - Die IP wird über einen **DNS-Server** (Domain Name System) aufgelöst.

2. **DNS Lookup**

    - Client fragt DNS: _„Welche IP hat developer.mozilla.org?“_
    - DNS antwortet mit der passenden IP.

3. **Client sendet HTTP-Anfrage** (meist GET)  
   Beispiele:

    - `GET /` → index.html
    - `GET /about/` → about/index.html

4. **Server empfängt Anfrage**

    - Server ist ein Programm (z.B. nginx, Apache, Node server.js).
    - Dieses Programm liefert die passenden Dateien aus.

5. **Browser lädt Ressourcen**

    - Zuerst index.html
    - Danach weitere Dateien (CSS, Bilder, JS)

6. **Rendering im Browser**

    - HTML strukturieren
    - CSS anwenden
    - JavaScript ausführen

7. **Wichtig:**
    - Du bist **nicht auf dem Server**, sondern der Server sendet dir eine **Kopie** aller Dateien → dein Browser rendert alles lokal.

---

## 2. Wie funktioniert HTML?

### Grundprinzipien

-   HTML = **Hyper Text Markup Language**
-   HTML beschreibt **Struktur**, nicht Aussehen
-   Elemente bestehen aus:

---

## Inhalt

-   Manche sind **self-closing**:

```html
<br />
<img />
```

### HTML Attribute

```html
<img src="logo.png" alt="Firmenlogo" />
<a href="https://example.com">Link</a>
<input type="date" />
```

### Aufbau einer HTML Datei

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Meta-Daten, CSS, JS -->
    </head>
    <body>
        <!-- Sichtbarer Inhalt -->
    </body>
</html>
```

### Semantic HTML (wichtige Elemente)

| Element     | Bedeutung                       |
| ----------- | ------------------------------- |
| `<main>`    | Hauptinhalt                     |
| `<header>`  | Kopfbereich / Intro             |
| `<footer>`  | Fußzeile                        |
| `<nav>`     | Navigation                      |
| `<section>` | Inhaltlicher Block              |
| `<article>` | Unabhängiger Beitrag            |
| `<aside>`   | Ergänzender Inhalt (Randspalte) |
| `<ul>/<ol>` | Listen                          |

### Nesting (Verschachtelung)

```html
<ul>
    <li>Item</li>
</ul>

<article>
    <h2>Headline</h2>
    <p>Text</p>
    <a href="#">Link</a>
</article>
```
