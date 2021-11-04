<h1 align="center">👋 FRETEBRAS-DR 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-v0-blue.svg?cacheSeconds=2592000" />
</p>

> Documento criado para orientação em reconstruir o ambiente produtivo em caso de desastre

### 🏠 [Guia](/)

* **Item #01** - [TERRAFORM](https://github.com/spaschoalick/DR)

* **Item #02** - [RANCHER](https://github.com/spaschoalick/DR) 

* **Aula #03** - [VELERO](https://github.com/spaschoalick/DR)

* **Aula #04** - [MSQL](https://github.com/spaschoalick/DR)

## Apresentacao

Este documento visa apresentar uma forma de garantir a reconstrucao do ambiente produtivo da EMPRESA com as aplicações para garantir o mínimo das funcionalidades da empresa.

* Pre-requisitos
Pensando em um cenário de desastre, se faz necessário como premissa os backups de banco de dados MYSQL e arquivos de backup do VELERO.

* Skills
Partindo do principio que todo o ambiente da FRETEBRAS foi perdido, as skill necessárias para a reconstrução são conhecimento em AWS, Terraform, Docker, K8S, Rancher, VELERO e claro knowhow na FRETEBRAS em si. 
Todo o ambiente é construído de forma inicial dentro do k8s, no caso utiliza-se o EKS (serviço gerenciado da AWS) para garantir níveis mais altos de disponibilidade.

Este documento visa dar uma visão geral, imaginando que a operação básica da empresa é baseada nos sistemas abaixo
Aplicações envolvidas.
ADM, Central, Site e APP

## Processo
1. Com um conta da AWS o primeiro passo a ser gerado é criaçao de uma conta de usuário com a permissáo de de <AdministratorAccess> para que possamos utilizá-lo tanto na criação dos recursos de Terraform como o próprio EKS utilizando o Rancher

2. Para utilizar o Terraform precisamos configurar em nosso dispositivo o console de gernciamento <CLI> da AWS com a Id / Key gerados no passo anterior
  a. Em um equipamento x86 execute o comando abaixo para instalar a CLI:
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    unzip awscliv2.zip
    sudo ./aws/install
  b. No diretório raiz foi criada a pasta oculta aws, acesso < cd && cd .aws >
  c. Caso o arquivo <credentials> não tenha sido criado, crie <mkdir credentials> e adicione o id e key como no exemplo abaixo;
    [default]
    aws_access_key_id=IDIDIDIDIDIDIDID
    aws_secret_access_key=KEYKEYKEYKEYKEYKEYKEYKEY

3. Agora vamos instalar o Terraform
  a. Acesse https://www.terraform.io/downloads.html e baixe a versao disponivel para seu sistema operacional e descompacte em /usr/local/bin
  b. faça a copia da pasta TERRAFORM deste repositório e entre na pasta fretebras-dr
  c. execute o comando <terraform init> para efetuar a instalação dos módulos configurados
  d. execute o comando <terraform plan> para analisar o que vai ser instalado

  
4. Estamos utilizando o Rancher para facilitar a criação do cluster de dr no serviço gerenciado do EKS
  a. Instale o docker, não vou entrar em detalhes de como fazer isso porque varia muito entre as distros. 
  b. com o serviço do docker ativo. copie e scritp shell localizado na pasta RANCHER deste repo, de a permissão de execução +x
  c. ./rancher.sh
  d. este passo demora alguns minutos, neste momento uma instancia do Rancher single instance esta sendo provisionado em seu equipamento
  e. acesse a url https://localhost 
  f. será exibido uma linha de comando para que a senha de admin seja apresentanda (substitua o container id usando docker ps)
  g. copie a senha gerada no terminal e cole na interface do Rancher 
  h. crie uma senha para acesso ao rancher.

## Autor

👤 **Santiago Paschoalick**

* LinkedIn: [@spaschoalick](linkedin.com/in/spaschoalick)

## 🤝 Contribuições

Agradeço ao time do CORE pela oportunidade e confiança.

## 📝 License

Copyright © 2021 [Santiago Paschoalick](https://github.com/spaschoalick).<br />
