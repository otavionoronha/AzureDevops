# Pré-Requisitos

 - Docker
 - Cluster Kubernets
 - Conta Azure Devops

**Preparando o ambiente**

 - Azure Devops
	 -  Criar uma access token para ser usado ao subir os agent pool
 - Docker
	 - Criar uma imagem com as informações
 - Kubernets
	 - Subir a imagem no cluster

## Docker

    mkdir /root/azure-linux-agent
    cd /root/azure-linux-agent
Caso opte por criar manualmente, tanto o **dockerfile** quanto o **start.sh**, basta acessar a KB de criação, [LINK](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops)

    touch linux-agent.dockerfile start.sh

Se desejar, pode baixar usando os comandos abaixo
	
     wget https://github.com/otavionoronha/AzureDevops/blob/main/linux-agent.dockerfile
     wget https://github.com/otavionoronha/AzureDevops/blob/main/start.sh
   
   Após isso seguir com a criação da imagem docker
   
    docker build --tag "azp-agent:linux" --file "./linux-agent.dockerfile" .