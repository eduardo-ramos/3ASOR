# WordPress Deployment

## O que é um Deployment?

Um Deployment no Kubernetes é um recurso que gerencia a criação e atualização de um conjunto de Pods. Ele garante que um número especificado de Pods esteja rodando em qualquer momento.

### Componentes Principais

- **Deployment**: Define o número de réplicas e a estratégia de atualização.
- **Pod**: Contém o contêiner do WordPress.
- **Contêiner**: Utiliza a imagem `wordpress:php8.3-apache`.
- **Variáveis de Ambiente**: Configurações necessárias para conectar ao banco de dados MySQL.
- **Volumes**: Monta um volume persistente para armazenar os dados do WordPress.

## Implementação

### Pré-requisitos

- Cluster Kubernetes configurado.
- `kubectl` instalado e configurado para se conectar ao cluster.
- PersistentVolumeClaim (PVC) configurado para armazenamento persistente

### Passos para Implementar

1Para aplicar o Deployment no Cluster, use o comando `kubectl apply`, conforme abaixo:

    ```sh
    kubectl apply -f wordpress-deployment.yaml
    ```

Verifique se o Deployment foi criado:

    ```sh
    kubectl get deployments
    kubectl get pods
    ```

## Conclusão

Este README fornece uma visão geral de como implementar um Deployment do WordPress no Kubernetes. Seguindo os passos acima, você pode configurar e executar seu próprio site WordPress em um cluster Kubernetes.

## Referências

- [Documentação do Kubernetes](https://kubernetes.io/docs/home/)
- [Imagem Docker do WordPress](https://hub.docker.com/_/wordpress)
