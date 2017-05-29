https://store.docker.com/editions/community/docker-ce-server-ubuntu

/* PREPARE THE ENVIRONMENT AND INSTALL DOCKER */

sudo apt-get -y install apt-transport-https ca-certificates curl

sudo apt-get autoremove

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get -y install docker-ce

/* TEST DOCKER CE */

sudo docker run hello-world

/* Manage Docker as a non-root user */

sudo groupadd docker

sudo usermod -aG docker $USER

/* ------------------------ now restrt the vm

/* Neo4j password is 'arianne'

/* run neo4j

docker run --publish=7474:7474 --publish=7687:7687 --volume=$HOME/arianne/2017/neo4j/data:/data --volume=$HOME/arianne/2017/neo4j/logs:/logs neo4j:3.0


