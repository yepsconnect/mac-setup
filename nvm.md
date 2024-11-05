# NVM
## Install

Open terminal
```sh
cd ~
```
Create files
```sh
touch .zshrc
touch .bash_profile
```
Before proceeding to the next step I needed to manually install Rosetta 2 in order run apps not built for Apple silicon.
```sh
softwareupdate --install-rosetta
```

Install NVM using curl
```sh
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```
Setup zshrc
```sh
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "$NVM_DIR/nvm.sh" ] && \\. "$NVM_DIR/nvm.sh"' >> ~/.zshrc
echo '[ -s "$NVM_DIR/bash_completion" ] && \\. "$NVM_DIR/bash_completion"' >> ~/.zshrc
```
Setup bash_profile
```sh
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.bash_profile
echo '[ -s "$NVM_DIR/nvm.sh" ] && \\. "$NVM_DIR/nvm.sh"' >> ~/.bash_profile
echo '[ -s "$NVM_DIR/bash_completion" ] && \\. "$NVM_DIR/bash_completion"' >> ~/.bash_profile
```
install NodeJS
```sh
nvm install node
```


## Uninstall
```sh
rm -rf ~/.nvm
sudo rm -rf ~/.npm ~/.nvm ~/node_modules ~/.node-gyp ~/.npmrc ~/.node_repl_history 
sudo rm -rf /usr/local/bin/npm /usr/local/bin/node-debug /usr/local/bin/node /usr/local/bin/node-gyp
sudo rm -rf /usr/local/share/man/man1/node* /usr/local/share/man/man1/npm*
sudo rm -rf /usr/local/include/node /usr/local/include/node_modules
sudo rm -rf /usr/local/lib/node /usr/local/lib/node_modules /usr/local/lib/dtrace/node.d
sudo rm -rf /opt/local/include/node /opt/local/bin/node /opt/local/lib/node
sudo rm -rf /usr/local/share/doc/node sudo rm -rf /usr/local/share/systemtap/tapset/node.stp 

brew uninstall node
brew doctor 
brew cleanup --prune-prefix
```




