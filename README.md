# Digitalni-dvojcek
## Posodovitev Ubuntu sistema in nadgradnja
     sudo apt update && sudo apt upgrade
## Namestitev SSH serverja
     sudo apt-get install openssh-server
## Omogoči SSH
     sudo systemctl enable ssh
     ## OR enable and start the ssh service immediately ##
     sudo systemctl enable ssh --now
## Start ssh
     sudo systemctl start ssh
## Namestitev docker
      **# Add Docker's official GPG key:
      sudo apt-get update
      sudo apt-get install ca-certificates curl
      sudo install -m 0755 -d /etc/apt/keyrings
      sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
      sudo chmod a+r /etc/apt/keyrings/docker.asc
      
      # Add the repository to Apt sources:
      echo \
        "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
        $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
        sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
      sudo apt-get update
## Namestitev docker
     sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

## Testiraj docker instanco
     sudo docker run hello-world

### Uporabi docker brez su
     sudo groupadd docker
     sudo usermod -aG docker $USER
     newgrp docker
### Test docker brez sudo
     docker run hello-world

## Namestitev Docker paketov
run command in the same folder as docker-compose.yml file

     docker compose up -d
     
