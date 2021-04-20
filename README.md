# Natural Language Processing - HomeWork 03
This repository gathers the notebooks developed to answer the third task of
ISIS4221-Natural Language Processing 2021-10.

The instructions are available in _HW03-ISIS4221.pdf_.

## Dataset

## Developers
* Juan David García Hernández (jd.garciah@uniandes.edu.co)
* Nicolás Rocha Pacheco (n.rocha11@uniandes.edu.co)
* César Daniel Garrido Urbano (cd.garrido@uniandes.edu.co)

## Contents

## Docker
Docker will be used in order to have an efficent and safe interaction with the GPU. In order to run the docker development server make sure to install `docker` and `docker-compose`. To install `docker` on Ubuntu:

    $ sudo apt-get update
    $ sudo apt-get 	install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    $ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    $ sudo apt-get update
    $ sudo apt-get install docker-ce docker-ce-cli containerd.io

The previous commands come from the Ubuntu [Docker documentation](https://docs.docker.com/install/linux/docker-ce/ubuntu/). If you are using another OS, please check the documentation for your OS. If you want to run Docker without any root permissions (without sudo), execute:

    $ sudo groupadd docker
    $ sudo usermod -aG docker $USER
    $ newgrp docker

As the installation commands, those commands come from Ubuntu [Docker documentation](https://docs.docker.com/install/linux/linux-postinstall/). We invite you to check your OS documentation if you are not using Ubuntu. We also encourage you to check the documentation if any error shows up during the installation process. To test if Docker was installed successfully do:

    $ docker run hello-world

If the previous command shows a Hello World! on the console output, Docker was installed succesfully. Add `sudo` if you are still using root permisions with Docker. Then, install `docker-compose`:

    $ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    $ sudo chmod +x /usr/local/bin/docker-compose

In order to use the GPU with Docker, make sure to install both the Nvidia drivers (`nvidia-driver-XXX`) and the Nvidia container runtime (`nvidia-container-runtime`). Once you are sure that both the Nvidia driver and the Nvidia container runtime are installed execute the bash command:

    $ docker-compose up

The console will output the address with the token that is used to connect a browser to Jupyter. To persist data, a volume is set to bind the main directory of this repository to `/tf` inside the container.
