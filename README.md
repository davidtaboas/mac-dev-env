# MAC DEV ENV



## Homebrew + Cask + Paquetes + Software

  `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

  

Creamos un archivo llamado "Brewfile":
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
  brew bundle Brewfile
  
## XCode

[Download](https://developer.apple.com/xcode/downloads/)




## Shell setup - Fish

Uso [Fish](http://fishshell.com/) con su extensión [Oh My Fish](https://github.com/bpinto/oh-my-fish)
  curl -L https://github.com/bpinto/oh-my-fish/raw/master/tools/install.fish | fish
  
Para cambiar a fish en la shell:
  grep -q '^/usr/local/bin/fish$' /etc/shells; or echo '/usr/local/bin/fish' | sudo tee -a /etc/shells
  chsh -s /usr/local/bin/fish
  
Este es mi archivo de configuración de fish, al que accedo con:
  subl ~/.config/fish/config.fish
  
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

  ln -sfv /usr/local/opt/postgresql/*plist ~/Library/LaunchAgents
  
  launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
  

### ruby + rails
  echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
  source ~/.bash_profile
  rbenv install 2.1.3
  rbenv global 2.1.3
  gem install rails
  rbenv rehash

### bower
  npm install bower

### pow + powder

  curl get.pow.cx | sh
  gem install powder
  
  powder up/down
  
## Software


### Google Chrome /Canary/

  
Utilizo las siguientes extensiones:
  
  * [Stylish](http://sobolev.us/stylish/) which allows me to install two styles that brings back the 
    * [card numbers](https://userstyles.org/styles/79880/trello-card-ids-small)
  * [YSlow]()
  * [Toggl]()

