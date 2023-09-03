# Setup son premier serveur linux

## Création d'un utilisateur

```bash
sudo useradd -m <username>
```

## Ajout de l'utilisateur au groupe sudo

```bash
sudo usermod -aG sudo <username>
```
```bash
sudo usermod -aG root <username>
```
```bash
sudo passwd <username>
```

## Editer les droits sudo

```bash
sudo visudo
```
Add these line at the end of the document
```bash
%sudo ALL=(ALL:ALL) NOPASSWD: ALL
```

## Setup SSH
### SSH_Keygen
```bash
ssh-keygen
```
### Copy SSH_Keygen to server
```bash
ssh-copy-id -i ~/.ssh/id_rsa.pub remote_user@ip
```
### Remove login info
```bash
touch .hushlogin
```

## Setup console
### Install zsh
```bash
sudo apt install zsh
```
```bash
chsh -s $(which zsh)
```
### Install oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Install neovim
```bash
sudo apt install neovim
```

