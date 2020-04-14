# How to do Install Ubuntu

## Install form usb

## Basic Setting on ubuntu

### Keyboard

[Link](http://snowdeer.github.io/linux/2018/01/21/ubuntu-16p04-install-korean-keyboard/)

[Ubuntu 18.04.2](http://snowdeer.github.io/linux/2018/07/11/ubuntu-18p04-install-korean-keyboard/)

## Applycation Install

### Git

 Version check

~~~
git --version
~~~

install

~~~
sudo apt-get install git
~~~

### Tig

Version Check

~~~
tig -v
~~~

install

~~~
sudo apt-get install tig
~~~

[link](https://zetawiki.com/wiki/%EC%9A%B0%EB%B6%84%ED%88%AC_tig_%EC%84%A4%EC%B9%98)

[[번역] Tig Manual](https://ujuc.github.io/2016/02/10/tig-manual/)

### typora

```linux
# or use
# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -

# add Typora's repository
sudo add-apt-repository 'deb https://typora.io/linux ./'
sudo apt-get update

# install typora
sudo apt-get install typora
```

[Link](https://support.typora.io/Typora-on-Linux/)

### Snap

~~~
sudo apt update
sudo apt install snapd
~~~

[Link](https://codeburst.io/how-to-install-and-use-snap-on-ubuntu-18-04-9fcb6e3b34f9)

### Telegram

~~~
sudo snap install telegram-desktop
sudo snap install telegram-cli
~~~



[Link](https://linuxconfig.org/how-to-install-telegram-on-ubuntu-18-04-bionic-beaver-linux)

### GitKraken

~~~
sudo snap install gitkraken
~~~

### VSCode

[Link](https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/)

~~~
sudo apt update

sudo apt install software-properties-common apt-transport-https wget

wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"

sudo apt install code
~~~

Install extention

- c++ intel
- pytion3



### ZSH

Link

[터미널 초보의 필수품](https://nolboo.kim/blog/2015/08/21/oh-my-zsh/)

[우분투에 ZSH와 OH MY ZSH 설치하기](https://the-illusionist.me/47)



### zsh-syntax-highlighting 설치하기

이제 시스템의 `PATH`에 등록된 명령어들을 자동으로 Syntax HighLighting을 해주는 `zsh-syntax-highlighting`를 설치해 봅시다.

아래 명령어 두줄을 터미널에 입력해 주세요.

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git

echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
```