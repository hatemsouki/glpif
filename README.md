# GLPI_
GLPI_ITSM
# GLPI com Docker compose e dados persistentes

Este repositório com o docker compose necessário para executar o GLPI através de **Docker** em sua ultima versão.

## Procedimento

### Instlando o docker:

### GLPI v9.5

### Instancias: EC2 na AWS com RDS

###container Docker : imagem ubuntu com Apache e PHP


###Pipeline Jenkins para build e deploy. 

Passo a passo do ambiente sendo montado no arquivo "Dockerfile", basta ter também a pasta "glpi" no memso diretório que o arquivo "Dockerfile". 
E com o arquivo "Jenkinsfile" através de uma configuração de webhook neste repositório github,
 toda vez que a um commit, ativa uma trigger no Jenkins que esta instalado(imagem docker) numa instancia na Amazon Web Services,
 e quando ativada essa trigger ele faz checout neste repositório faz o build de da imagem docker baseado no "Dockerfile"
 e sobre um container onde o deploy é feito. 

### Executando os containers

```bash
docker-compose up -d

