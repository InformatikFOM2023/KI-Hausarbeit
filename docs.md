git# Dokumentation

## Git
__Get started:__
1. Auf dem Client muss `Git` und `Git LFS` Service installiert sein

   [Git](https://git-scm.com/downloads)

   [Git LFS](https://git-lfs.com/)
          
2. Starte `Git Bash`
3. Nach der Installation, navigiere in einen Pfad wo du das Projekt platzieren möchtest
4. Kopiere den Pfad
5. Setze den kopierten Pfad als Argument für den Befehl `cd`
```bash
cd "c:\MeineProjekte\Projekt"
```
6. Initializiere Git Verwaltung in dem Pfad

```bash
git init
```
7. Clone die Projekt Repository
```bash
git clone https://github.com/InformatikFOM2023/RezeptTool.git
```
Alternativ kann man Schritte 5 bis 7 auch in einem Befehl durchführen:
```bash
git git clone https://github.com/InformatikFOM2023/RezeptTool.git "<Pfad>"
```
8. Pulle die Datenbank mit `Git LFS`
```bash
git lfs pull --include="Testset.json"
```        
9. Navigiere in dem Explorer zu dem Projekt Pfad. Dort findest du das gesamte Projet. In den Ordner `Data` findest du die JSON Datenbank


__Arbeiten mit Git:__

1. Git User Namen einstellen
```bash
git config --global user.name "Max Mustermann"
```

1. Bevor man beginnt mit dem Code zu arbeiten sollte man eine Arbeits Branch erstellen
```bash
git checkout -b devBranch
```

1. Änderungen bestimmter dateien stagen
```bash
git add Doc.md
```

1. Alle Änderungen stagen
```bash
git add -A
```

1. Commiten der gestagten Änderungen
```bash
git commit -m "Mein Kommentar bezüglich des Commits"
```

1. Branch in die Repository pushen
```bash
git push https://github.com/InformatikFOM2023/RezeptTool.git
```

1. Entweicklungsbranch in die Main Branch mergen
```bash
git checkout main
git merge devBranch
git push https://github.com/InformatikFOM2023/RezeptTool.git
```

1. Hinzufügen eines Remotes damit man nicht immer die URL eingeben muss
```bash
git remote add MyRemote https://github.com/InformatikFOM2023/RezeptTool.git
git push --set-upstream MyRemote
```
Dann kann man statt der URl folgendes schreiben
```bash
git push MyRemote
```
1. Redundante `Branches` sollten gelöscht werden
```bash
git branch -d devBranch
git push MyRemote -d devBranch
```


> [!Tip]
> Das mergen sollte man nicht über `Bash` machn. Es wird empfohlen einen `Push` in die Repository zu machen und das Mergen über `GitHub` `PullRequest`

> [!WARNING]
> Dies soll bitte nicht als sichere Quelle wargenommen werden! Hier habe ich beschrieben wie ich das mach und wie es für mich funktionier! Sehr gerne lerne ich dazu und nehme Verbesserungsvorschläge an!
> Die Vorschläge gerne über `Pull Request` pushen

___
