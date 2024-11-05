# SSH
## Move from another device
### On current device
Copy your keys 
```sh
cp ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub ~/Downloads/
```
Move keys for your new device to Downloads folder
### On new device
open terminal and run
```sh
cd ~
```
Create .ssh folder 
```sh
mkdir -p ~/.ssh
```
Move your keys from Downoads to .ssh
```sh
mv ~/Downloads/ssh-keys/id_ed25519 ~/Downloads/ssh-keys/id_ed25519.pub ~/.ssh/
```

Set access for keys private key
```sh
chmod 600 ~/.ssh/id_ed25519
```
Set access for public key
```sh
chmod 644 ~/.ssh/id_ed25519.pub
```

Run SSH-agent
```sh
eval "$(ssh-agent -s)"
```
Add private key to ssh-agent
```sh
ssh-add ~/.ssh/id_ed25519
```

## Generate
```sh
ssh-keygen -t ed25519
```







