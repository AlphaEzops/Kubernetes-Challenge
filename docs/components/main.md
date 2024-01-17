## SUMMARY
- [Components](#components)
  - [CI/CD (Continuous Integration / Continuous Delivery)](#cicd-continuous-integration--continuous-delivery)
  - [DNS (Domain Name System)](#dns-domain-name-system)
  - [Scalability](#scalability)
  - [Computing](#computing)
  - [Monitoring](#monitoring)

### CI/CD (Continuous Integration / Continuous Delivery)

- **[CodePipeline:](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html)** Used to automate and orchestrate CI/CD pipelines, enabling continuous integration and continuous delivery.

- **[CodeBuild:](https://docs.aws.amazon.com/codebuild/latest/userguide/welcome.html)** Fully managed build service, essential for the build stage in CI/CD pipelines.

- **[ArgoCD:](https://argoproj.github.io/argo-cd/)** Continuous Delivery (CD) tool operating on the GitOps model, enabling continuous deployment and updates of applications on Kubernetes.

### DNS (Domain Name System)

- **[Route 53:](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html)** Provides DNS services for domain registration, DNS zone management, and traffic routing in the cloud.

### Scalability

- **[ELB (Elastic Load Balancer):](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html)** Ensures horizontal scalability, distributing traffic among multiple instances to improve performance and availability.

- **[Horizontal Pod Autoscaler (HPA):](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/)** Kubernetes feature that automatically adjusts the number of pods in a deployment or replica set based on observed CPU or memory utilization.

### Computing

- **[EKS Cluster (Amazon Elastic Kubernetes Service):](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)** Provides a managed environment for running Kubernetes clusters, facilitating distributed computing and container orchestration.

### Monitoring

- **[Grafana:](https://grafana.com/docs/)** Used for monitoring, metrics collection, and visualization, allowing effective performance observation.

- **[Prometheus:](https://prometheus.io/docs/)** Monitoring and alerting system designed for dynamic cloud environments.

These components form an integrated ecosystem supporting the essential fundamentals for successful development, operation, and scalability of modern systems in the cloud. Be sure to check the [official ArgoCD documentation](https://argoproj.github.io/argo-cd/) to understand its integration in the CI/CD cycle.