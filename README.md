# DevOps Challenge
Implementation of a complete system with monitoring and CICD with Kubernetes on AWS

![](https://github.com/AlphaEzops/kubernetes-challenge/blob/main/docs/system-workflow.gif)

## Table of Contents
1. [Requirements](#1-requirements)
2. [Components](#2-components)
3. [challenge](#3-challenge)

## 1. Requirements
you need install all the tools below:
- [terraform](./docs/requirements/terraform.md) - tools for provisioning and managing cloud infrastructure 
- [kubectl](./docs/requirements/kubectl.md) - command-line tool for Kubernetes 
- [aws cli](./docs/requirements/aws-cli.md) - command-line tool for AWS 
- [helm](./docs/requirements/helm.md) - package manager for Kubernetes  
- [golang](./docs/requirements/golang.md) - programming language 
- [docker](./docs/requirements/docker.md) - container platform

## 2. Components
 Infrastructure components and key fundamentals. It covers the integration of Continuous Integration/Continuous Delivery (CI/CD) practices, Domain Name System (DNS) management, scalability solutions, and computing in a cloud environment. Additionally, it explores the monitoring tools employed for effective observation.
- [components](./docs/components.md) - components of the system

## 3. Challenge
O desafio consiste em criar e gerenciar um ambiente Kubernetes altamente eficiente na AWS, utilizando as melhores práticas de DevOps. Abaixo, detalhamos cada passo e fornecemos mais informações para orientar a execução:

#### 1. Provisionamento de Infraestrutura com Terraform:
- Utilize o Terraform para criar a infraestrutura na AWS, incluindo VPC, AWS DEV TOOLS, Helms chart ,EKS, ArgoCD, e outros recursos essenciais.
- Organize e modularize seus recursos com módulos Terraform para facilitar a manutenção.
- Armazene o estado do Terraform remotamente, preferencialmente no Amazon S3, para garantir consistência e colaboração.

#### 2. AutoScaling com Cluster Autoscaler e HPA:
- Configure o Cluster Autoscaler para escalabilidade automática do número de nós no cluster, garantindo resposta dinâmica à demanda e economia de recursos.
- Implemente o Horizontal Pod Autoscaler (HPA) para a API Golang, ajustando automaticamente o número de réplicas conforme a carga de trabalho.

#### 3. DNS com Ingress e Cert-Manager:
- Configure o Ingress para direcionar tráfego HTTP para a API Golang, garantindo uma comunicação eficiente.
- Utilize o Cert-Manager para provisionar automaticamente certificados SSL, garantindo a segurança das comunicações.

#### 4. API Service com Golang utilizando Helm:
- Desenvolva uma API em Golang, com endpoints para listar buckets do S3 e deletar um bucket.
- Crie um Helm chart para a aplicação, facilitando o gerenciamento de configurações e atualizações.
- Dockerize API

#### 6. Integração com CodePipeline e CodeBuild:
- Configure pipelines no CodePipeline para automatizar o processo de CI, integrando testes e validações.
- Construa uma imagem da API em Golang utilizando um Dockerfile e envie para o Elastic Container Registry (ECR) para garantir rastreabilidade e versionamento.
- Integre tags da imagem ao deployment, mantendo um histórico claro das mudanças no repositório.
- Faça intergraçao do code build com o ArgoCD (code build deve fazer o CI e o ArgoCD de fazer o CD).

#### 7. Deployment com ArgoCD:
- Instale e configure o ArgoCD no cluster Kubernetes para facilitar o deployment contínuo
- configure o ArgoCD para fazer a sincronização com o repositório Git onde se encontra o GO APP.

#### 8. Monitoramento com Prometheus e Grafana:
- Implemente o Prometheus para coletar métricas do cluster e da API, configurando alertas para ações proativas.
- Configure o Grafana para criar dashboards informativos, permitindo uma visualização fácil da saúde do cluster e da aplicação.

Este desafio visa avaliar sua capacidade de projetar e implementar uma infraestrutura escalável, integrada e monitorada, utilizando ferramentas populares de DevOps. Boa sorte!
