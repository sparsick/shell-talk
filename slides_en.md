---
author: Sandra Parsick
date: DD.MM.YYYY
---


# A Guide to the Shell Galaxy

JCON Europe, Cologne

15.05.2025

Sandra Parsick

---

[Slido Q&A](https://wall.sli.do/event/oEv4GaswkD61fCAD3uoV4K/?section=24e01485-4b2c-43a7-9832-ee70976c86ca)

---

## About me

* Freelance Java Developer
* Main topics:
	* Backend Development
	* Software Craftmanship
	* Automation in Development
* Training / Workshop
* Java Champion
* Cyberland
* Podcast: https://ready-for-review.dev
* Homepage: https://www.sandra-parsick.de
* Mastodon:@sparsick@mastodon.social


---
## Motivation

Thanks to

- Christmas Sessions of Softwerkskammer Ruhrgebiet "Show me your favourite tool"
- Pair Programming Sessions with colleagues
- Martin Leyrer for his talks about CLI tools https://martin.leyrer.priv.at/

---
## My Background

* Programming languages: Java, sometimes Groovy und Kotlin, rarely GoLang, JavaScript
* OS: mostly Linux, sometimes (retricted) Windows, know Mac only in Pair Programming sessions
* Platforms: Kubernetes, Docker

---
## Plan for Today

### Terminals
### Shells, Extensions and Themes
### CLI Tools for the Daily Work

---
## Before we start...

This slides are created with
* https://github.com/maaslalani/slides

---
## Terminals vs. Shell

- _Terminal_ - user interface for interacting with the computer via text input and output
- _Shell_ - command-line interpreter, a program that reads and execute commands

---
## Terminals

My current favourite:
* [Ghostty](https://ghostty.org/)

Other:
* [Konsole](https://konsole.kde.org/) (for Linux)
* [Tilix](https://gnunn1.github.io/tilix-web/) (for Linux)
* [iterm2](https://iterm2.com) (for Mac)
* [warp](https://www.warp.dev/)
* [Hyper](https://hyper.is/)


---

## Shells: An Overview

* Standard on many systems: Bash
* Similiar to bash: zsh
* Alternative to zsh: Fish

https://www.zsh.org/

https://fishshell.com/

---

### My Shell favourite: zsh

Reasons:
* Switch from Bash to zsh was easier
* Because of the framework *oh-my-zsh* ( a framework to manage zsh configurations)

---

### oh-my-zsh

https://ohmyz.sh/

Collection of themes, short cuts and plugins

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

##### External Plugins

https://github.com/unixorn/awesome-zsh-plugins#plugins


---

#### My favourite oh-my-zsh Plugins

###### Bundled Plugins

* jump - can mark directories and jump to the marks
* z - autojump
* history-substring-search -  zsh implementation of Fish shell's history search feature
* git - git alias and functions
* mvn - Maven completion and alias
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


###### zsh-autosuggestions

https://github.com/zsh-users/zsh-autosuggestions

It suggests commands during you are typing

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

## Shell Tools for the daily business

### Tool Version Management
### Tools for Developments
### Search and Found
### Container tools
### Further good sources for shell tooling

---
### Tool Version Management

* sdkman
* nvm

---
#### sdkman

*SDKMAN!* helps to manage SDKs from the Java ecosystem

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

*nvm* helps to manage several NodeJS version at the same time

https://github.com/nvm-sh/nvm

```shell
nvm install 16
nvm use 16
nvm alias default 8.1.0
```

---

### Tools for Development

* fastfetch
* onefetch
* cloc
* scc
* bat
* micro
* watch
* atop/htop
* httpie

---

#### fastfetch

System Informations Tool

https://github.com/fastfetch-cli/fastfetch

---


#### onefetch

Fastfetch for Git Repositories

https://github.com/o2sh/onefetch

---

#### cloc

*cloc* counts blank lines, comment lines and physical lines in various programming languages

https://github.com/AlDanial/cloc

---

#### scc (Sloc Cloc and Code)

*scc* counts lines like *cloc*, but also calculates the code complexity

https://github.com/boyter/scc

---


#### bat

cat with syntax highlighting

https://github.com/sharkdp/bat

---

#### micro

a modern and intuitive terminal-based text editor

https://micro-editor.github.io/

---

#### watch

* A built-in Linux command
* It runs user-defined commands in intervals

---


#### atop / htop

* process manager
* `top` further thinking

https://www.atoptool.nl/

https://htop.dev/

---

#### httpie

More intuitive HTTP client

https://httpie.io/cli

Sample API: https://www.swapi.tech/api

---

### Search and Found
* ag
* jq
* yq
* sort
* uniq


---

#### ag - Silversearcher

*grep* for source code

https://geoff.greer.fm/ag/


---

#### jq

* JSON Processor
* `sed` for JSON data

https://stedolan.github.io/jq/

---

#### yq

* YAML Processor
* similar to *jq*
* understands also JSON and XML


https://mikefarah.gitbook.io/yq/

---

#### sort

* Sorter
* part of GNU CoreUtils

https://www.gnu.org/software/coreutils/

---

#### uniq

* Search and count duplicated lines
* part of GNU CoreUtils

https://www.gnu.org/software/coreutils/

---

### Containertools
* dive
* trivy
* k9s

---

#### dive

Tool, to inspect every single layer of a Docker image

https://github.com/wagoodman/dive

---

#### trivy

Vulnerability/Misconfiguration/secret Scanner for container and other artefacts

https://aquasecurity.github.io/trivy

---

#### k9s
K8s Terminal Manager

https://k9scli.io/


---
### Other good sources for Shell Tools

* http://conqueringthecommandline.com/book
* https://explainshell.com/
* https://n.jo-so.de/leyrer-cli-gpn20#


---

## Tips and Tricks

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

## Questions?

@sparsick@mastodon.social

mail@sandra-parsick.de

[Slido Q&A](https://wall.sli.do/event/oEv4GaswkD61fCAD3uoV4K/?section=24e01485-4b2c-43a7-9832-ee70976c86ca)

https://github.com/sparsick/shell-talk
