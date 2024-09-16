# Projeto 3ASOR - Arquitetura de Microcontainers

Este repositório contém os arquivos de configuração para a implementação de uma arquitetura de microcontainers utilizando MySQL e WordPress.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos instalados:

- [Docker](https://www.docker.com/)
- [Kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Kubelet](https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet/)

## Estrutura do Repositório

- **ubuntu-k3s-lab**: Pasta contendo os arquivos de configuração do cluster Kubernetes.
- **ubuntu-k3s-lab/mysql-deployment.yaml**: Configuração de deployment para o MySQL.
- **ubuntu-k3s-lab/mysql-pvc.yaml**: Configuração de Persistent Volume Claim (PVC) para o MySQL.
- **ubuntu-k3s-lab/mysql-service.yaml**: Configuração de serviço para o MySQL.
- **ubuntu-k3s-lab/wordpress-deployment.yaml**: Configuração de deployment para o WordPress.
- **ubuntu-k3s-lab/wordpress-ingress.yaml**: Configuração de ingress para o WordPress.
- **ubuntu-k3s-lab/wordpress-pvc.yaml**: Configuração de Persistent Volume Claim (PVC) para o WordPress.
- **ubuntu-k3s-lab/wordpress-service.yaml**: Configuração de serviço para o WordPress.

## Como Utilizar

1. Clone este repositório:
    ```bash
    git clone https://github.com/eduardo-ramos/3ASOR.git
    ```
2. Acesse o diretório do projeto:
    ```bash
    cd 3ASOR/arquitetura-microcontainers
    ```
3. Aplique os arquivos de configuração no seu cluster Kubernetes:
    ```bash
    kubectl apply -f mysql-deployment.yaml
    kubectl apply -f mysql-pvc.yaml
    kubectl apply -f mysql-service.yaml
    kubectl apply -f wordpress-deployment.yaml
    kubectl apply -f wordpress-ingress.yaml
    kubectl apply -f wordpress-pvc.yaml
    kubectl apply -f wordpress-service.yaml
    ```

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
