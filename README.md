# Natural Language Processing: HW03

# Natural Language Processing - HomeWork 02
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

Then, install `docker-compose`:

    $ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    $ sudo chmod +x /usr/local/bin/docker-compose

Then execute the bash command:

    $ docker-compose up

The console will output the address with the token that is used to connect a browser to Jupyter. To persist data, a volume is set to bind the main directory of this repository to `/tf` inside the container.
