# UbuntuSetup
A quick guide to setup a new Ubuntu machine 

## Setting up terminal right
After creating your new Ubuntu machine, open a new terminal and run the following commands:

```
sudo apt update
sudo atp upgrade -y
sudo apt-get install git -y
sudo apt install curl -y
sudo apt install zsh -y
chsh -s ../../bin/zsh
sudo reboot
```

At this point the system should have restarted and the default terminal is zsh. Upon opening a new terminal you should be asked to choose some settings. For now, press Q and continue on with these commands:

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sudo apt-get install fonts-powerline
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
nano ~/.zshrc
```

Now edit the file by chaning it to 
```
ZSH_THEME="powerlevel10k/powerlevel10k"
```
After doing so, save file, and then close and re-open terminal and continue on:

```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions 
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
nano ~/.zshrc
```

Now edit plugins to 

```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting). 
```
Then close and re-open terminal. Now Terminal is setup

## VS code for ARM64
```
cd Downloads
curl -L https://aka.ms/linux-arm64-deb > code_arm64.deb
sudo apt install ./code_arm64.deb
```
