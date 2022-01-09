# Debian-Data-Science
Debian customizations for Data Science

## Requirements
_This install changes Debian to the SID (Dev) Branch_

### Download Debian non-free netinstall

Use the following Debian ISO as the base <https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/weekly-builds/amd64/iso-cd/>

*do NOT grab the EDU download and this includes non-free and firmware*
### Base Stuff - Root

Autorizar o usuário a usar o sudo

    sudo usermod -aG sudo username

Install git

    sudo apt install git


Clonar o repositório a ser usado

    git clone https://github.com/armando-nahmias/Debian-Data-Science/

_Run as ROOT_

    cp /etc/apt/sources.list /etc/apt/sources.list.bak
    cp sources.list /etc/apt/sources.list 

Instalar dependências para o pyenv

    sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev
    curl -L https://raw.githubusercontent.com/pyenv/pyenv-installer/master/bin/pyenv-installer | bash

Validando a instalação do pyenv

Conferindo a versão instalada do pyenv

    pyenv -v
    
Se der erro, adicione as seguintes linhas ao final do arquivo de configuração do seu bash

    .bashrc if you use bash
    .zshrc if you use zsh

```
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
if command -v pyenv 1>/dev/null 2>&1; then
 eval "$(pyenv init -)"
fi
```

Depois, reinicie o terminal



