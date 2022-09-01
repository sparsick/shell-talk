---
author: Sandra Parsick
date: DD.MM.YYYY
---


# Per Shell durch die Techie-Galaxy

Herbstcampus 2022, Nürnberg

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
Tilix 
Konsole


Mac: iterm2

Weitere Terminals, die angepriesen werden
* Terminology
* Terminator
* fig
* warp

Windows

---

## Shells: ein Überblick

* Standard: Bash
* Nah an der Bash: zsh
* Alternative zu zsh: Fish

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
* jump - allows to mark dirs and jump to marks
* z - autojump
* history-substring-search -  zsh implementation of the Fish shell's history search feature
* git - git alias and functions
* mvn - maven completion and alias
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

* zsh implementation of the Fish shell's history search feature
* type in any part of any command from history and then press chosen keys, such as the UP and DOWN arrows, to cycle through matches

###### zsh-autosuggestions

https://github.com/zsh-users/zsh-autosuggestions

It suggests commands as you type based on history and completions.

---

###### git

---
###### mvn


###### kubectl

---

## Shellwerkzeuge, die meinen Alltag vereinfachen

### Vereinfachung von Toolverwaltung
### Entwicklungstätigkeiten
### Netzwerk
### Containertools
### Suchen und finden
### Weitere nützliche Quellen zur Shell

---
### Vereinfachung von Toolverwaltung

* sdkman
* nvm

---

### Entwicklungstätigkeiten

* neofetch
* gitfetch
* cloc
* scc
* bat
* watch
* atop/htop


---

### Netzwerk

* httpie
* mosh
* xxh
* tmux
* siege
* dig
* termshark / tshark

---

### Containertools
* Dive
* trivy
* k9s

---

### Suchen und finden
* ag
- sort
- unique
* jg
* yg
* XMLStarlet

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

### Help Flag

```shell
<command> -h | --help
```

---

## Fragen?

@SandraParsick
mail@sandra-parsick.de
https://github.com/sparsick/shell-talk