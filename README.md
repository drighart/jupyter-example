# jupyter-example

In dit voorbeeld project wordt vanuit een Jupyter notebook de gemaakte bestanden ge-pushed naar Github. Zorg dat je een Jupyter notebook kunt openen. Open een **terminal tab** (dit staat in dezelfde popup waar je voor een Python2 of Python3 notebook kunt kiezen). In de terminal (bash) is een Linux prompt $ zichtbaar waarin allerlei linux commando's ingegeven kunnen worden. Middels **conda** kun je op deze manier bijvoorbeeld nieuwe packages installeren. Je kunt ook het commando **git** gebruiken om bestanden in te checken in GitHub.

Op de terminal tab (zwart scherm) staat een prompt, zoiets als:
```console
jovyan@xxxxx-jupyter-test-2196714232-0sblt:~/work$
```
Hieronder is deze pompt aangegeven als $.

Om te beginnen is het handig om een aantal handige Git globale variabele te zetten:
```console
$ git config --global user.email "emailaddress"
$ git config --global user.name "username"
```

Begin met de Git repository te initialiseren:
```console
$ git init
```
Er wordt een .git folder aangemaakt. Open een Python 3 notebook en geef enkele regels in in het notebook (zie voorbeeld IPYNB-bestand). Sla de notebook op met een ludieke naam. Er ontstaat een IPYNB bestand. Je kunt eventueel nog een README.md file aanmaken en daar tekst ingeven waar de repository over gaat. Hieronder staat een commando om even snel een README.md aan te maken.
```console
$ echo "# jupyter-example" >> README.md
```
Daarna kun je de README.md en andere bestanden (zoals IPYNB-bestanden toevoegen een de Git-repository:
```console
$ git add .
```
Middels commit worden de wijzigingen doorgevoerd op de lokale repository. Met -m kun je een korte omschrijving opgeven aan de commit.
```console
$ git commit -m "first commit"
```
Het volgende commando zorgt er voor dat deze repository wordt gekoppeld aan de repository op Github. Dit hoef je maar eenmalig te doen.
```console
$ git remote add origin https://github.com/drighart/jupyter-example.git
```
En uiteindelijk worden de wijzigingen naar Github (de remote repository) ge-pushed (in dit geval naar de master branch):
```console
$ git push -u origin master
```

## Wijzigingen aan de bestanden
Wanneer het notebook nu opnieuw wordt aangepast (of meerdere) dan kun je opnieuw de wijzigingen doorzetten naar Github, middels:
```console
$ git add .
$ git commit -m "second commit"
$ git push -u origin master
```
Middels
```console
$ git status
```
kun je altijd tussentijds controleren welke bestanden wel zijn toegevoegd aan de lokale repository en welke niet (en je dus alsnog moet toevoegen).

## IPYNB bestanden in Github
Na de eerste commit kun je in Github kijken of de bestanden geplaatst zijn op Github en kun je (via de website) het IPYNB bestand openen. Github geeft het bestand weer als in Jupyter notebook!

## Een nieuw Jupyter Notebook
Wanneer er reeds een repository op Github is waar je gebruik van wilt maken, dan kun je eenvoudig deze repository lokaal in het notebook plaatsen middels:
```console
$ git clone https://github.com/drighart/jupyter-example.git
```
De url kun je kopieren van de website van Github bij de repository. Klik op de knop "Clone or download"

Zie verder: https://git-scm.com/docs/gittutorial 
