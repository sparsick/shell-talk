---
author: Sandra Parsick
date: DD.MM.YYYY
---


# Per Shell durch die Techie-Galaxy

IT Tage 2022, Remote

15.12.2022

@SandraParsick

---

## Über mich

* freiberuflicher Developer und Consultant im Java-Umfeld
* Schwerpunkte:
	* Backend-Entwicklung
	* Software Craftmanship
	* Automatisierung von Entwicklungsprozessen
* Training / Workshop
* Java Champion
* Cyberland
* Podcast: Ready-for-Review.dev
* Homepage: https://www.sandra-parsick.de
* Mastodon:@sparsick@mastodon.social
* Twitter: @SandraParsick


---
## Motivation

Danke an

- die Weihnachtssessions der Softwerkskammer Ruhrgebiet "Show me your favourite tool"
- die zahlreiche Pair-Programming-Sessions mit Kollegen
- Martin Leyrer für seine Vorträge zu Kommandozeilenwerkzeugen https://martin.leyrer.priv.at/

---
## Mein Hintergrund

* Programmmiersprache: Java, manchmal Groovy und Kotlin, sehr selten Go, JavaScript
* OS: Hauptsächlich Linux, manchmal (kastriertes) Windows, kenne Mac nur von Pair Programming
* Plattformen: Kubernetes, Docker

---
## Plan für heute

### Terminals
### Shells und ihre Erweiterungen und Themes (zumindest, die ich benutze)
### Shellwerkzeuge, die meinen Alltag vereinfachen

---
## Bevor wir loslegen ...

Dieser Vortrag wird im Terminal vorgestellt mit Hilfe von:
* https://github.com/maaslalani/slides

---
## Terminals


Linux:
* Konsole
* [Tilix](https://gnunn1.github.io/tilix-web/)

Mac: [iterm2](https://iterm2.com)

Weitere Terminals, die angepriesen werden
* [Terminology](https://www.enlightenment.org/about-terminology)
* [fig](https://fig.io/) (nur Mac)
* [warp](https://www.warp.dev/) (nur Mac)
* [Hyper](https://hyper.is/)


---

## Shells: ein Überblick

* Standard: Bash
* Nah an der Bash: zsh
* Alternative zu zsh: Fish

https://www.zsh.org/

https://fishshell.com/

---

### Mein Shell-Favorite: zsh

Gründe:
* Umstieg von Bash auf zsh gestaltete sich einfach
* Wegen Framework oh-my-zsh (Framework um zsh Konfiguration zu verwalten)

---

### oh-my-zsh

https://ohmyz.sh/

Sammlung von Themes, Shortcuts und Plugins 

---

#### oh-my-zsh Themes

```shell
$ cat ~/.zshrc

# Set name of the theme to load.
# Look in ~/.oh-my-zsh/themes/
# Optionally, if you set this to "random", it'll load a random theme each
# time that oh-my-zsh is loaded.
#ZSH_THEME="agnoster"
#ZSH_THEME="simple"
ZSH_THEME="spaceship"
```

##### Bundled Themes

https://github.com/ohmyzsh/ohmyzsh/wiki/Themes


##### External Themes

https://github.com/unixorn/awesome-zsh-plugins#themes

---

##### External Themes - Spaceship

https://spaceship-prompt.sh/

---

#### oh-my-zsh Shortcuts

```shell
# Switching directory
<directory name>='cd <directory name>'
..='cd ..'
...='cd ../..'

# Create directory
md='mkdir -p'

# List directory content
l='ls -lah'
ll='ls -lh'


```

---

#### oh-my-zsh Plugins

```shell
$ cat ~/.zshrc

# Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(sdk git jump z extract history web-search history-substring-search 
	mvn gitignore zsh-autosuggestions kubectl sublime asciidoctor ansible vagrant )
```

##### Bundled Plugins

https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins-Overview

##### Externe Plugins

https://github.com/unixorn/awesome-zsh-plugins#plugins


---

#### Meine favorisierten oh-my-zsh Plugins

###### Bundled Plugins

* jump - kann Ordner markiereen und zu diesen Markierungen springen
* z - autojump
* history-substring-search -  zsh Implementierung des Fish shell's history search feature
* git - git alias und  Funktionen
* mvn - maven completion und alias
* kubectl - kubectl completion and alias

###### External Plugins

* zsh-autosuggestions - Fish-like fast/unobtrusive autosuggestions for zsh.

https://github.com/zsh-users/zsh-autosuggestions


---

###### jump

```shell
jump <mark-name> 	
mark [mark-name] 	
unmark <mark-name> 	
marks
```

---

###### z

```shell
z [-chlrtx] [regex1 regex2 ... regexn]
OPTIONS
       -c     restrict matches to subdirectories of the current directory
       -e     echo the best match, don't cd
       -h     show a brief help message
       -l     list only
       -r     match by rank only
       -t     match by recent access only
       -x     remove the current directory from the datafile
```
---
###### history-substring-search

* zsh Implementierung der the Fish shell's history search feature


###### zsh-autosuggestions

https://github.com/zsh-users/zsh-autosuggestions

Empfiehlt Befehle, während man in der CLI tippt, basierend auf history

---

###### git

```shell
g
gcl
gl
gco
gaa
gcmsg
gp
```

---
###### mvn

```shell
mvncv
mvnci
mvncvst
```


###### kubectl

```shell
k
kgp
kgpw
kdp
kdel
kdelp
```

---

## Shellwerkzeuge, die meinen Alltag vereinfachen

### Vereinfachung von Toolverwaltung
### Entwicklungstätigkeiten
### Suchen und finden
### Containertools
### Netzwerk
### Weitere nützliche Quellen zur Shell

---
### Vereinfachung der Toolverwaltung

* sdkman
* nvm
* asdf

---
#### sdkman 

SDKMAN! hilft bei der Verwaltung mehrerer SDKs aus dem Java Ökosystem

https://sdkman.io/


```shell
sdk list
sdk list maven
sdk install maven 3.8.6
sdk use java 8.0.282.hs-adpt
sdk env init
```

---
#### nvm

nvm hilft bei der Verwaltung verschiedener NodeJS Versionen

https://github.com/nvm-sh/nvm

```shell
nvm install 16                   
nvm use 16                        
nvm alias default 8.1.0               
```

---
#### asdf

asdf verwaltet die Versionen von allen möglichen Runtime Tools

https://asdf-vm.com

---

### Entwicklungstätigkeiten

* neofetch
* onefetch
* cloc
* scc
* bat
* watch
* atop/htop
* httpie

---

#### neofetch

System Informations Tool

https://github.com/dylanaraps/neofetch

---


#### onefetch

Neofetch für Git Repositories

https://github.com/o2sh/onefetch

---

#### cloc

cloc zählt Leerzeilen, Kommentarzeilen und physikalische Zeilen in verschiedenen Programmiersprachen

https://github.com/AlDanial/cloc

---

#### scc (Sloc Cloc and Code)

scc zählt wie cloc Zeilen, berechnet aber noch zusätzlich die Code Komplexität

https://github.com/boyter/scc

---


#### bat

cat mit Syntaxhighlighting

https://github.com/sharkdp/bat

---

#### watch

* Ein built-in Linux Kommando
* Es lässt benutzer-definierte Befehle im Intervall durchlaufen

---


#### atop / htop

* Prozessmanager
* `top` weitergedacht

https://www.atoptool.nl/

https://htop.dev/

---

#### httpie

Intuitiver HTTP Client

https://httpie.io/cli

Beispiel API: https://swapi.dev/

---

### Suchen und finden
* ag
* jq
* yq
* XMLStarlet
* sort
* uniq


---

#### ag

Werkzeug, um Code durchzusuchen

https://geoff.greer.fm/ag/


---

#### jq

* JSON Processor
* `sed` für JSON Daten

https://stedolan.github.io/jq/

---

#### yq

* YAML Processor
* angelehnt an jq
* kann auch JSON und XML


https://mikefarah.gitbook.io/yq/

---


#### XMLStarlet

* Es transformiert, durchsucht, validiert und editiert XML-Dokumente 

http://xmlstar.sourceforge.net/

---
#### sort

* Sortierer
* Teil der GNU CoreUtils

https://www.gnu.org/software/coreutils/

---

#### uniq

* Sucht und zählt duplizierte Zeile
* Teil der GNU CoreUtils

https://www.gnu.org/software/coreutils/

---

### Containertools
* dive
* trivy
* k9s

---

#### dive

Werkzeug, um die einzelnen Layer eines Docker Images zu inspektieren

https://github.com/wagoodman/dive

---

#### trivy

Vulnerability/Misconfiguration/secret Scanner für Container und andere Artifakte

https://aquasecurity.github.io/trivy

---

#### k9s
K8s Manager für das Terminal

https://k9scli.io/

---

### Netzwerk

* siege
* mosh
* xxh
* tmux
* dig
* termshark / tshark

---

#### siege

Load Tester und Benchmark

https://github.com/JoeDog/siege

---


#### mosh

Mobile Shell 
* Ersatz für SSH Terminals, wenn die Verbindungen mal schlecht sind

https://mosh.org/

---

#### xxh

Remote Shell Konfigurator

https://github.com/xxh/xxh

---

#### tmux

Terminal- Multiplexer

https://github.com/tmux/tmux

---

#### dig

DNS lookup

Teil der dnstool Sammlung

---

#### termshark

Wireshark für das Terminal

https://termshark.io/

---
### Weitere nützliche Quellen zur Shell

* http://conqueringthecommandline.com/book
* https://explainshell.com/
* https://n.jo-so.de/leyrer-cli-gpn20#


---

## Tipps und Tricks

### Cheat Sheets

* https://tmuxcheatsheet.com/
* https://vim.rtorr.com/

### Man Pages

```shell
man <command>
```

### tldr pages

https://tldr.sh/

### Help Flag

```shell
<command> -h | --help
```

---

## Fragen?

@SandraParsick

@sparsick@mastodon.social

mail@sandra-parsick.de


https://github.com/sparsick/shell-talk