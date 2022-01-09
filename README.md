# Debian-Data-Science
Debian customizations for Data Science

## Requirements
_This install changes Debian to the SID (Dev) Branch_

### Download Debian non-free netinstall

Use the following Debian ISO as the base <https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/weekly-builds/amd64/iso-cd/>

*do NOT grab the EDU download and this includes non-free and firmware*
### Base Stuff - Root

Autorizar o usuário a usar o sudo
```
sudo usermod -aG sudo username
```

Install git
```
sudo apt install git
```

Clonar o repositório a ser usado
```
git clone https://github.com/armando-nahmias/Debian-Data-Science/
```

_Run as ROOT_
```
sudo su
./root.sh
```
