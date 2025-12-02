# Git Branches & Pull Requests (PRs)

**Date:** 03.12.2025  
**Coach:** Felix Kirchhoff

---

## Warum Branches?

Wenn mehrere Leute an einem Projekt arbeiten, darf niemand direkt im main herumeditieren. Branches sorgen dafür, dass jede Änderung sauber getrennt bleibt.
Ein Branch ist eine Abzweigung vom Hauptentwicklungsstrang (main):
Er startet an einem Commit und entwickelt danach eine eigene Historie.

### Typischer Workflow

1. Feature-Branch erstellen (z. B. für ein Feature)
2. Auf dem Branch arbeiten und commits machen
3. Feature fertigstellen → testen → reviewen lassen
4. Branch in 'main' mergen
5. 'main' bleibt stabil & sauber

> Regel im Bootcamp: Wir arbeiten NIE auf main. Nie.

### Branch-Namen

→ kurz, eindeutig, lesbar: 'contact-form', 'fix-navbar', 'add-darkmode'
→ immer klein & mit Bindestrichen (weil es am lesbarsten ist).

### Git Branch Befehle

| Befehl                   | Bedeutung                                      |
| ------------------------ | ---------------------------------------------- |
| `git checkout <branch>`  | neuen Branch erstellen                         |
| `git switch -c <branch>` | neuen Branch erstellen **und** in ihn wechseln |
| `git switch <branch>`    | zu bestehendem Branch wechseln                 |
| `git branch`             | listet alle lokalen Branches                   |
| `git branch -a`          | listet lokale und remote Branches              |
| `git branch -d <branch>` | Branch lokal löschen                           |

### Pull Requests (PRs)

Ein Pull Request ist eine Anfrage, einen Branch in einen anderen (meist main) zu mergen.
Im PR passiert der komplette Review-Prozess:

-   Code ansehen
-   Feedback geben
-   Änderungen einfordern
-   Kommentare, Diskussionen

Gemerget wird immer auf GitHub, idealerweise im Vier-Augen-Prinzip.

### Standard-Workflow eines Pull Requests

1. Branch erstellen und in ihn wechseln:

```bash
git switch -c <branchname>
```

2. Code schreiben / Änderungen machen

3. Branch das erste Mal pushen:

```bash
git push -u origin <branchname>
```

(später reicht einfach git push)

4. Pull Request auf GitHub erstellen → von deinem Branch in main
5. PR teilen (Team einladen zum Review)
6. Feedback umsetzen → Änderungen committen + wieder pushen
7. PR mergen, wenn alles sauber ist
8. Lokal auf main wechseln und updaten:

```bash
git switch main
git pull
```

9. Branch löschen – auf GitHub und lokal

## Wichtige Hinweise

-   Der main-Branch wird nie direkt bearbeitet.
-   Auf main finden ausschließlich merge commits statt.
-   Jeder arbeitet ausschließlich auf seinem Feature-Branch.
-   Merge-Vorgänge passieren ausschließlich auf GitHub.
-   Best Practice: immer jemanden anderes mergen lassen (Review-Sicherheit).

### Typische Befehle

```bash
git@github.com:uxbyweng/git-demo.git
git remote add origin git@github.com:uxbyweng/git-demo.git

git push -u origin maingit pull origin main

```

### Basic Workflow for a pull request

-   Create a new branch with git switch -c <branchname>.
-   Make changes to the code / write your code fpr the feature.
-   Push the changes and the new branch with git push -u origin <branchname> (after you have done this once you can use git push for this branch)
-   Create a pull request on GitHub from the new branch into main
-   Share the pull request with your team
-   Review the pull request, implement changes if needed, push again to update the pull request until it gets approved
-   Merge the pull request into main
-   Don’t forget to git pull inside the main branch on your local machine
-   Delete the new branch on GitHub and locally
