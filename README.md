# MitoZ
Instalar e rodar MitoZ

#Rodar no terminal
```
sudo apt update && sudo apt upgrade && sudo apt install -y build-essential libssl-dev uuid-dev libgpgme11-dev squashfs-tools libseccomp-dev pkg-config && wget https://github.com/sylabs/singularity/releases/download/v3.11.2/singularity-ce_3.11.2-focal_amd64.deb && sudo dpkg -i singularity-ce_3.11.2-focal_amd64.deb
```

#Se der erro de alguns pacotes não instalarem rodar esse
```
apt --fix-broken install
```
#Se der erro de root seguir esses passos

```sudo rm -rf /var/lib/apt/lists/lock```

```sudo apt-get update```

```sudo dpkg –configure -a```

```sudo apt-get -f install```

#Rodando MitoZ com dados fasta | alterar para o local onde está o MitoZ | Fazer o mesmo para onde está o fasta, mas caso dê error, pode colocar o fasta no /root e rodar com comando sudo [...]
#Alterações: outprefix com nome do gênero; nome do fasta; nome da espécie conforme o fasta
```
singularity exec /home/iann/Downloads/MItoz/MitoZ_v3.4.sif mitoz annotate --outprefix Dekeyseria --thread_number 12 --fastafiles dekeyseria.fasta --species_name D_amazonica --genetic_code 2 --clade Chordata
```
#O arquivo fasta precisa vir iniciando assim. Não exceder 13 caracteres
```">D_amazonica topology=circular"```
