<h1 align="center">FRETEBRAS-DR 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-v0-blue.svg?cacheSeconds=2592000" />
</p>

> Doc para orientação sobre recosntrução do ambiente produtivo em caso de desastre

### 🏠 [Guia](/)

* **Aula #00 - Conceitos básicos e VPC** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula00_vpc) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #01 - Terraformando o EKS Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula01_eks) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #02 - Node groups** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula02_nodes) - [Video](https://www.youtube.com/watch?v=kXqiqZ5Nap8)

* **Aula #03 - Traefik no EKS** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula03_traefik) - [Video](https://www.youtube.com/watch?v=ThONqZT2Mfs&t=9s)

* **Aula #04 - Auto Scale do Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula04_scale) - [Video](https://www.youtube.com/watch?v=tYikrqYRAaQ)

### ✨ [Demo](/)

## Instalação

```sh
terraform init
```

## Aplicando

```sh
terraform apply --auto-approve
```

## Validação

```sh
terraform validate
```

## Adicionando o contexto do nosso cluster ao kubectl

```bash
aws eks --region us-east-1 update-kubeconfig --name nome-do-cluster
aws eks --region us-east-1 update-kubeconfig --name k8s-demo
```

```bash
kubectl get nodes
```

## Deploy o Ingress

```bash
kubectl apply -f kubernetes/traefik/ingress.yml
```

## Deploy demo services

* [Whois App](https://github.com/msfidelis/microservice-nadave-whois)
* [Faker App](https://github.com/msfidelis/microservice-nadave-fake-person)
* [Pudim](https://github.com/msfidelis/pudim)

```bash
kubectl apply -f kubernetes/apps/whois.yml
kubectl apply -f kubernetes/apps/faker.yml
kubectl apply -f kubernetes/apps/pudim.yml
```

## Deploy do Metric Server

```bash
kubectl apply -f kubernetes/metric-server/metric-server.yml
```

## Author

👤 **Matheus Fidelis**

* Website: https://raj.ninja
* Twitter: [@fidelissauro](https://twitter.com/fidelissauro)
* Github: [@msfidelis](https://github.com/msfidelis)
* LinkedIn: [@msfidelis](https://linkedin.com/in/msfidelis)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2020 [Matheus Fidelis](https://github.com/msfidelis).<br />
This project is [MIT](LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR

santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % LS
README.md	kubernetes	modules		modules.tf	output.tf	provider.tf	variables.tf
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % NANO README.md 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR






























santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % 
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % A
zsh: command not found: A
santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % CLEAR







santiagopaschoalick@FBSP-TECH-0365 terraformando-eks % nano README.md 




































  GNU nano 2.0.6                                       File: README.md                                                                                      

kubectl apply -f kubernetes/metric-server/metric-server.yml
```

## Author

👤 **Matheus Fidelis**

* Website: https://raj.ninja
* Twitter: [@fidelissauro](https://twitter.com/fidelissauro)
* Github: [@msfidelis](https://github.com/msfidelis)
* LinkedIn: [@msfidelis](https://linkedin.com/in/msfidelis)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](/issues).

## Show your support

Give a  ️ if this project helped you!

## 📝 License

Copyright © 2020 [Matheus Fidelis](https://github.com/msfidelis).<br />
This project is [MIT](LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
