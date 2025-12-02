# Git & Markdown

**Date:** 28.11.2025  
**Coach:** Roland Hufnagel

## Überblick

Session zu **Git**, **Versionierung**, **Markdown** und grundlegenden Arbeitsprozessen mit GitHub.

## Was ist Versionierung?

-   Git speichert **nur Änderungen**, nicht komplette Dateien → effizient & schnell.
-   Entwickelt von **Linus Torvalds** (Linux-Erfinder).
-   Git hat sich global als Standard etabliert.
-   Jeder Commit basiert automatisch auf seinem direkten Vorgänger.

## Git Grundkonzepte

-   **Repository:**
    -   Projektordner, der von Git überwacht wird
-   **Commit:**
    -   Speichert eine Änderungsversion
    -   Sammlung von Änderungen
    -   In einem einzelnen Commit werden nur die Änderungen zum vorherigen Stand gespeichert
    -   Speicherpunkt aka eine Version
-   **Branch:** Eigener Arbeitszweig
-   **Remote:** Verbindung zu GitHub oder anderen Servern

## Commit Messages – Best Practices

Gute Commit Messages sind essenziell — sie sind ein nachvollziehbares Protokoll.

**Regeln:**

1. **Kurz & präzise halten**
2. **Immer Englisch**
3. **Start mit Verb (Imperativ):**
    - add
    - fix
    - remove
    - update
4. **Keine Vergangenheit:**
    - ❌ _added shop page_
    - ✔️ _add shop page_
5. **Kein Punkt am Ende**
6. **„Warum“ statt „wie“ beschreiben:**
    - ✔️ _fix typo_
    - ❌ _replaced the letter a with e in the second word_
