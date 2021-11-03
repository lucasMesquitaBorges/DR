<h1 align="center">👋 EMPRESA-DR 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-v0-blue.svg?cacheSeconds=2592000" />
</p>

> Documento criado para orientação em reconstruir o ambiente produtivo em caso de desastre

### 🏠 [Guia](/)

* **Item #01** - [TERRAFORM](https://github.com/spaschoalick/DR)

* **Item #02** - [RANCHER](https://github.com/spaschoalick/DR) 

* **Aula #03** - [VELERO](https://github.com/spaschoalick/DR)

* **Aula #04** - [MSQL](https://github.com/spaschoalick/DR)

## Instalação

Este documento visa apresentar um forma rápida para garantir a reconstrucao do ambiente produtivo da EMPRESA com as principais aplicações para garantir o mínimo das funcionalidades da EMPRESA

* Pre-requisitos
Pensando em um cenário de desastre, se faz necessário como premissa os backups de banco de dados MYSQL arquivos de backup do VELERO.

* Skills
Partindo do principio que todo o ambiente da FRETEBRAS foi perdido, as skill necessárias para a reconstrução são conhecimento em AWS, Terraform, Docker, K8S, Rancher e VELERO
Todo o ambiente da Fretebras é construído de forma inicial dentro do k8s, no caso utiliza-se o EKS (serviço gerenciado da AWS) para garantir níveis mais altos de disponibilidade.

Este documento visa dar uma visão geral, imaginando que a operação básica da Fretebras é baseada nos sistemas abaixo 
Aplicações envolvidas.
ADM, Central, Site e APP

* RANCHER
Com docker instalado, execute o comando no terminal de sua disto para provisionar um rancher single instance em seu equipamento
## Autor

👤 **Santiago Paschoalick**

* LinkedIn: [@spaschoalick](linkedin.com/in/spaschoalick)

## 🤝 Contribuições

Agradeço ao time do CORE pela oportunidade e confiança.

## 📝 License

Copyright © 2021 [Santiago Paschoalick](https://github.com/spaschoalick).<br />
