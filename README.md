# Debian-Data-Science
Debian customizations for Data Science

Primeiro, baixe a imagem ISO do endereço: <https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/weekly-builds/amd64/iso-cd/>
Não utilize a versão EDU.

Autorizar o usuário a usar o sudo

    sudo usermod -aG sudo username

Disable Root Login in Linux with passwd Command

To disable the root login, you can use the passwd command as below:

    sudo passwd -l root

This will lock the password for the root user and you won’t be able to access the root account with its password until a new one is set.

Install git

    sudo apt install git


Clonar o repositório a ser usado

    git clone https://github.com/armando-nahmias/Debian-Data-Science/

Se precisar fazer alterações no repositório, será necessário configurar o git

git config –global user.email "email"
git config –global user.name "nome"


Mudar a lista de fontes para o debian sid

    cp /etc/apt/sources.list /etc/apt/sources.list.bak
    cp sources.list /etc/apt/sources.list 

Instalar dependências para o pyenv

    sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

How to verify that I have set up pyenv correctly?

Check that pyenv is in your PATH:

    which pyenv

Check that pyenv's shims directory is in your PATH:

    echo $PATH | grep --color=auto "$(pyenv root)/shims"

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

Depois que o pyenv estiver funcionando 

Conferir as versões disponíveis do Python

    pyenv install -l

Escolher uma versão e instalar

    pyenv install 3.10.0

marcar versão para uso global

    pyenv global 3.10.0




Instalando o pipx

    pip install pipx

Garantir que o pipx esteja no path
    pipx ensurepath
      
    
Se nao funcionar, adicione a seguinte linha ao final do arquivo de configuração do seu bash

    .bashrc if you use bash
    .zshrc if you use zsh

```
export PYTHONPATH="$HOME/.local/bin"
```

Depois, reinicie o terminal

Instalar o poetry
    pipx install poetry
