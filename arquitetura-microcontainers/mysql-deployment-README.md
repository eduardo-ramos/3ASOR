# MySQL Deployment

## O que é um Deployment?

Um Deployment no Kubernetes é um recurso que gerencia a criação e atualização de um conjunto de Pods. Ele garante que um número especificado de Pods esteja rodando em qualquer momento..

### Componentes Principais
- **Nome do Deployment**: `mysql-deployment`
- **Pod**: Contém o contêiner do MySQL.
- **Contêiner**: Utiliza a imagem `mysql:8.0`
- **Variáveis de Ambiente**: 
  - `MYSQL_USER`
  - `MYSQL_PASSWORD`
  - `MYSQL_DATABASE`
  - `MYSQL_ROOT_PASSWORD`
- **Volumes**: Montagem de volume persistente com `mysql-pvc`

## Implementação

### Pré-requisitos
- Cluster Kubernetes configurado
- `kubectl` instalado e configurado para se comunicar com o cluster
- PersistentVolumeClaim (PVC) configurado para armazenamento persistente

### Passos para Implementar

Para aplicar o Deployment no Cluster, use o comando `kubectl apply`, conforme abaixo:

   ```sh
   kubectl apply -f mysql-deployment.yaml
   ```

Verifique se o Deployment foi criado:

   ```sh
   kubectl get deployments
   kubectl get pods
   ```

## Conclusão
Este README fornece uma visão geral de como configurar e implementar um Deployment do MySQL no Kubernetes. Seguindo os passos acima, você poderá gerenciar a implantação de um banco de dados MySQL em seu cluster Kubernetes.

## Referências
- [Documentação do Kubernetes](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- [Imagem Docker do MySQL](https://hub.docker.com/_/mysql)
