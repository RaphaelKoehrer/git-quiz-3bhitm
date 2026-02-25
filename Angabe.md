# GIT Quiz - Angabe

## Aufgabenstellung
**Name:** Raphael Köhrer  

### Ziel
Zeige in diesem Quiz, dass du die Grundlagen von Git verstanden hast.
Du arbeitest strukturiert mit Branches, führst saubere Commits durch und kannst eine bestehende Git-History analysieren.

### Aufgaben

1. **Repository duplizieren = FORK (2 Punkte)**
   - Erstelle ein Duplikat = FORK des Repositories in deinem eigenen Account. 
   - Klone das Repository auf deinen lokalen Rechner.

2. **Erste Commits durchführen (3 Punkte)** 
   - Öffne die Datei index.html. 
   - Ergänze in der Datei eigenen Code an der markierten Stelle. 
   - Stage die Änderung. Erstelle einen sinnvollen Commit mit einer aussagekräftigen Message. Die Commit-Message wird bewertet!

3. **Branches erstellen (4 Punkte)**
   - Erstellen Sie einen Branch `commit-branch`. 
   - Wechsle auf diesen Branch. 
   - In diesem Branch sollst du das File `index.html` überarbeiten. 
   - Du findest dort einen Bereich mit schlechten Commit-Messages. KOPIERE den Bereich, und verbessere die Nachrichten.
   - Stagen und Commiten. Achtung: AM BRANCH!

4. **Merge-Conflict provozieren (5 Punkte)**
   - Wechsle nun zurück zum Hauptbranch `main` und bearbeite auch hier die Datei `index.html`. Ergänze an der gleichen Stelle wie im Branch `commit-branch` eigenen Code.
   - Stagen und Commiten. Achtung: AM HAUPTBRANCH!
   - Nun versuche den Branch `commit-branch` in den Hauptbranch `main` zu mergen.
   - Es sollte ein Merge-Conflict entstehen. Löse diesen korrekt.
   - Committe die Lösung.
  

5. **GIT-History analysieren (4 Punkte)**
Schaue dir nun die komplette Commit-History an. Denn im aktuellen Projekt funktioniert die Navigation nicht korrekt. Finde heraus, in welchem Commit der Fehler eingeführt werde. Beschreibe kurz / gibt die Commit-ID an. Mit welchem Befehl hast du dies herausgefunden? Wie viele Commits wurden insgesamt in diesem Projekt erstellt?

----------------------- 

Du hast das Quiz nun erfolgreich abgeschlossen. Gib HIER den Link zu deinem geforkten Repository an: (https://github.com/RaphaelKoehrer/git-quiz-3bhitm.git)

Gib anschließend dieses ANGABE-File bei MOODLE ab!

# git-quiz-3bhitm
# Punkt 5: Git-History analysieren

## Fehler-Commit
Der Fehler in der Navigation wurde im Commit **d87473d** (`feature`) eingeführt.

## Vorgehensweise / Befehl
Um den fehlerhaften Commit zu finden, habe ich `git bisect` verwendet:

```bash
git bisect start
git bisect bad
git bisect good 6215e02
# nach jedem Test:
git bisect good   # oder git bisect bad
git bisect reset