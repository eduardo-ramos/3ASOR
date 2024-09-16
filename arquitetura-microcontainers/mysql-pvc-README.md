# MySQL PersistentVolumeClaim (PVC)

Este README fornece uma visão geral do arquivo `mysql-pvc.yaml`, que define um PersistentVolumeClaim (PVC) no Kubernetes para um banco de dados MySQL. 

## O que é um PersistentVolumeClaim (PVC)?

No Kubernetes, um PersistentVolumeClaim (PVC) é uma solicitação de armazenamento feita por um usuário. Ele pode ser atendido por um PersistentVolume (PV), que é uma peça de armazenamento no cluster. PVCs são independentes do ciclo de vida dos Pods e preservam os dados mesmo após reinicializações, reprogramações e exclusões de Pods.

### Componentes Principais

- **apiVersion**: A versão da API Kubernetes utilizada.
- **kind**: O tipo de recurso, neste caso, `PersistentVolumeClaim`.
- **metadata**: Informações sobre o PVC, incluindo o nome (`mysql-pvc`) e rótulos (`app: mysql`).
- **spec**: Especificações do PVC, incluindo:
  - **accessModes**: Define o modo de acesso ao volume. `ReadWriteOnce` permite que o volume seja montado como leitura/gravação por um único nó.
  - **storageClassName**: Define a classe de armazenamento utilizada. `local-path` é uma classe de armazenamento comum para ambientes de desenvolvimento.
  - **resources**: Especifica os recursos solicitados, neste caso, `1Gi` de armazenamento.

## Implementação

### Pré-requisitos

- Um cluster Kubernetes em funcionamento.
- A ferramenta de linha de comando `kubectl` configurada para se comunicar com o cluster.

### Passos para Implementar
Para aplicar o PVC no Cluster, use o comando `kubectl apply`, conforme abaixo:

   ```sh
   kubectl apply -f mysql-pvc.yaml
   ```

Verifique se o PVC foi criado:

   ```sh
   kubectl get pvc mysql-pvc
   ```

## Conclusão

Este README fornece uma visão geral de como criar e usar um PersistentVolumeClaim (PVC) no Kubernetes para um deployment do MySQL. O PVC garante que os dados do MySQL sejam armazenados de forma persistente, mesmo que os pods sejam reiniciados ou reprogramados.

## Referências
[Documentação do Kubernetes sobre PersistentVolumes e PersistentVolumeClaims](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)
