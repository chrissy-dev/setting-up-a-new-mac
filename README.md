When setting up a new Mac this should be the bare minimal that is installed and working.
* git
* [homebrew](https://brew.sh/)
* [rbenv](https://github.com/rbenv/rbenv)
* [nvm](https://github.com/creationix/nvm) 

## Assumptions
* Should be a managed admin or full admin.

## Install Apple Command Line Tools (Installs Git)

```bash
xcode-select --install
```

## Install oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Install nvm 

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```

>The script clones the nvm repository to ```~/.nvm``` and adds the source line to your profile (~/.bash_profile, ```~/.zshrc```, ```~/.profile```, or ```~/.bashrc```).
>```bash
>export NVM_DIR="$HOME/.nvm"
>[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
>```

## Install a node version
```bash
nvm install 6.9.1
```

## Install Homebrew
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install rbenv 
```bash
brew install rbenv 
``` 
>You will need to add the following source line to your profile (~/.bash_profile, ```~/.zshrc```,```~/.profile```, or ```~/.bashrc```).
>```bash
># Load rbenv
>export PATH="$HOME/.rbenv/bin:$PATH"
>eval "$(rbenv init -)"
>```


## Install a Ruby version
```bash
rbenv install 2.3.0 
```
>If you run into errors with ```zlib``` install a ruby version using the following.
>```bash
>brew install zlib
>RUBY_CONFIGURE_OPTS="--with-zlib-dir=$(brew --prefix zlib)" rbenv install 2.3.0 
>```

## Install software with homebrew cask
```bash
brew cask install iterm2 atom tower slack google-chrome firefox sketch spectacle 
```
