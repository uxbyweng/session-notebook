# Git Branches & Pull Requests (PRs)

**Date:** 02.12.2025  
**Coach:** Felix

---

## Git Branches – warum überhaupt?

Wenn mehrere Leute an einem Projekt arbeiten, will niemand direkt im main-Branch herumfummeln. Branches lösen genau dieses Problem:
Ich kann an meinem Feature arbeiten, ohne das Risiko, anderen den Code zu zerschießen.

Ein Branch ist im Grunde eine Abzweigung vom Hauptentwicklungsstrang. Er startet an einem bestimmten Commit, teilt sich danach ab und entwickelt eine eigene Historie.

### Typischer Workflow:

1. Neuen Branch erstellen – z. B. für ein Feature.
2. Auf diesem Branch arbeiten und commits machen.
3. Feature fertigstellen, testen, reviewen lassen.
4. Branch in main mergen, wenn alles passt.
5. Der main-Branch bleibt damit immer stabil und sauber.

### Branch-Namen

Kurze, beschreibende Namen sind Gold wert:
Beispiele: contact-form, fix-navbar, add-darkmode
Ich nutze immer Kleinbuchstaben und Bindestriche, weil es am lesbarsten ist.

### Git Branch Befehle

| Befehl                   | Bedeutung                                      |
| ------------------------ | ---------------------------------------------- |
| `git switch -c <branch>` | neuen Branch erstellen **und** in ihn wechseln |
| `git switch <branch>`    | zu bestehendem Branch wechseln                 |
| `git branch`             | listet alle lokalen Branches                   |
| `git branch -a`          | listet lokale und remote Branches              |
| `git branch -d <branch>` | Branch lokal löschen                           |

### Pull Requests (PRs)

Ein Pull Request ist eine Anfrage, einen Branch in einen anderen zu mergen – meistens in main.
Dort findet der gesamte Review-Prozess statt: Kommentare, Vorschläge, Änderungen.

Erst wenn der PR genehmigt ist, wird gemergt. So bleibt der Code hochwertig und nachvollziehbar.

### Standard-Workflow für einen Pull Request

1. Branch erstellen:

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

## 2. Was sind Git pull requests und wie benutzt man sie?

-
-

### Praktisch:

```bash

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
