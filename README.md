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