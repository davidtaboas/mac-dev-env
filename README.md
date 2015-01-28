# MAC DEV ENV



## Homebrew + Cask + Paquetes + Software

  `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

  

Creamos un archivo llamado "[Brewfile](https://github.com/davidtaboas/mac-dev-env/blob/master/Brewfile)":
```
tap josegonzalez/php
tap homebrew/dupes
install openssl
install php54-mcrypt
install josegonzalez/php/composer
install wget
install optipng
install redis
install mysql
install phpunit
install postgresql

install fish
install git
install nodeno
install rbenv ruby-build
install heroku-toolbelt

# Install Cask
install caskroom/cask/brew-cask

# Install Casks
cask install alfred
cask install caffeine
cask install flux

cask install virtualbox
cask install vagrant
cask install boot2docker

cask install sublime-text-3
cask install google-chrome
cask install iterm2
cask install phpstorm
cask install sequel-pro
cask install macvim

cask install adium
cask install nvalt
cask install rdio
cask install slack
cask install textexpander
cask install vlc
cask install the-unarchiver

cask install sourcetree
cask install github
cask install transmit
```
Ahora ejecutamos:

`brew bundle Brewfile`
  
## XCode

[Download](https://developer.apple.com/xcode/downloads/)




## Shell setup - Fish

Uso [Fish](http://fishshell.com/) con su extensión [Oh My Fish](https://github.com/bpinto/oh-my-fish)
  `curl -L https://github.com/bpinto/oh-my-fish/raw/master/tools/install.fish | fish`
  
Para cambiar a fish en la shell:

```
grep -q '^/usr/local/bin/fish$' /etc/shells; or echo '/usr/local/bin/fish' | sudo tee -a /etc/shells
chsh -s /usr/local/bin/fish
```

Este es mi archivo de configuración de fish, al que accedo con:
  
  `subl ~/.config/fish/config.fish`
  
Tengo esta configuración, con algunos plugins activos:

  ```
  # Path to your oh-my-fish.
  set fish_path $HOME/.oh-my-fish

  # Theme
  set fish_theme agnoster
  
  # Which plugins would you like to load? (plugins can be found in ~/.oh-my-fish/plugins/*)
  # Custom plugins may be added to ~/.oh-my-fish/custom/plugins/
  # Example format: set fish_plugins autojump bundler
  set fish_plugins autojump brew bundler localhost node rails sublime vi-mode rbenv
  
  
  # Path to your custom folder (default path is $FISH/custom)
  #set fish_custom $HOME/dotfiles/oh-my-fish
  
  # Load oh-my-fish configuration.
  . $fish_path/oh-my-fish.fish
  ```


## Sublime Text 3

El editor de código que utilizo es [SublimeText 3](http://www.sublimetext.com/3).

Instalo el plugin [Package Controller](https://sublime.wbond.net) y uso el paquete [Syncing](https://packagecontrol.io/docs/syncing) para sincronizar todas las instalaciones y la configuración.


## Docker

Para ciertos usos, uso [Docker](https://docs.docker.com/installation/mac/).

## Paquetes


### postgresql

```
ln -sfv /usr/local/opt/postgresql/*plist ~/Library/LaunchAgents
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
  ```

### ruby + rails

Instalamos la versión de ruby e indicamos que se use de manera global. Instalamos rails.
```
rbenv install 2.1.3
rbenv global 2.1.3
gem install rails
rbenv rehash
```


### bower

```
npm install bower
```

### pow + powder

Instalamos pow y powder para que el manejo sea más sencillo.
```
curl get.pow.cx | sh
gem install powder
```
Podemos levantar o apagar pow con el siguiente comando:

`powder up/down`
  
## Software


### Google Chrome /Canary/

  
Utilizo las siguientes extensiones:
  
  * [Stylish](https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe): aplicar estilos a páginas web. Yo uso un [tema simplificado y limpio para Trello](https://userstyles.org/styles/80236/trello-theme-gray).
  * [YSlow](https://chrome.google.com/webstore/detail/yslow/ninejjcohidippngpapiilnmkgllmakh): análisis de webs
  * [Toggl](https://chrome.google.com/webstore/detail/toggl-button/oejgccbfbmkkpaidnkphaiaecficdnfn)
  * [DevTools Theme: Zero Dark Matrix](https://chrome.google.com/webstore/detail/devtools-theme-zero-dark/bomhdjeadceaggdgfoefmpeafkjhegbo): activar experiments en chrome://flags y permitir temas personalizados
  * [StayFocusd](https://chrome.google.com/webstore/detail/stayfocusd/laankejkbhbdhmipfmgcngdelahlfoji): para mantener un control sobre las páginas web a las que entrar, horarios, etc.
