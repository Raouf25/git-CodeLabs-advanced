# git-CodeLabs-advanced

## Présentation

Le codeLabs gitAdvanced est une formation sur les cas avancés d'utilisations de git

Une question ? Une difficulté ? : **gabin.darras@ineat-conseil.fr**

## Builder le codelab

### Installation de Go

Le codelabs utilise le language Go qui va permettre de créer un site web static à partir du fichier MarkDown.
Sur MacOS:

```
brew install go
```

### Modification $PATH

export GOPATH=$HOME/Go
export GOROOT=/usr/local/opt/go/libexec
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:$GOROOT/bin

### Installation de CLaaT (Codelabs as a Thing)

CLaaT est un outil pour manager et creer les codelabs a partir de fichier MarkDown ou Google Slides

```
go get -u -v -x github.com/googlecodelabs/tools/claat
```

### Générer le codelab (site static)

**Générer le template HTML**

```
claat export gitAdvanced.md
```

puis
**Générer le site complet**

```
claat serve gitAdvanced.md
```

Cette commande lance directement un serveur web.
Fermer le serveur Web

### Fixer l'architecture foireuse du codelabs

Déplacer le répertoire **bower_components** et **elements** dans le répertoire codelabs-gitEasy.
**Modifier** les chemins d'import de _bower_components_ et _elements_ dans le fichier **index.html**.

Vous avez votre site static prêt a être déployé sur le serveur de votre choix.
