# MitoZ
Instalar e rodar MitoZ

#Rodar no terminal
sudo apt update && sudo apt upgrade && sudo apt install -y build-essential libssl-dev uuid-dev libgpgme11-dev squashfs-tools libseccomp-dev pkg-config && wget https://github.com/sylabs/singularity/releases/download/v3.11.2/singularity-ce_3.11.2-focal_amd64.deb && sudo dpkg -i singularity-ce_3.11.2-focal_amd64.deb

#Se der erro de alguns pacotes não instalarem rodar esse
apt --fix-broken install

#Se der erro de root seguir esses passos V
sudo rm -rf /var/lib/apt/lists/lock
sudo apt-get update
sudo dpkg –configure -a
sudo apt-get -f install

