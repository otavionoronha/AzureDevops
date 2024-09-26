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
Caso opte por criar manualmente, tanto o **dockerfile** quanto o **start.sh**

    touch linux-agent.dockerfile start.sh