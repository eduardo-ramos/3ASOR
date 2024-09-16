# WordPress PersistentVolumeClaim (PVC)

Este README fornece uma visão geral do arquivo PersistentVolumeClaim (PVC) utilizado para um deployment do WordPress no Kubernetes. O PVC é um recurso que permite que os pods solicitem armazenamento persistente no cluster.

## O que é um PersistentVolumeClaim (PVC)?

No Kubernetes, um PersistentVolumeClaim (PVC) é uma solicitação de armazenamento feita por um usuário. Ele pode ser atendido por um PersistentVolume (PV), que é uma peça de armazenamento no cluster. PVCs são independentes do ciclo de vida dos Pods e preservam os dados mesmo após reinicializações, reprogramações e exclusões de Pods.

### Componentes Principais

- **Nome**: `wordpress-pvc`
- **Rótulo**: `app: wordpress`
- **Modo de Acesso**: `ReadWriteOnce`
- **StorageClass**: `local-path`
- **Capacidade Solicitada**: `1Gi`

## O que é um PersistentVolumeClaim?

Um PersistentVolumeClaim (PVC) é uma solicitação de armazenamento feita por um usuário. Ele pode ser atendido por um PersistentVolume (PV), que é uma peça de armazenamento no cluster. Os PVCs são independentes do ciclo de vida dos pods e preservam os dados mesmo após reinicializações, reprogramações e exclusões de pods.

## Implementação

### Pré-requisitos

- Um cluster Kubernetes em funcionamento.
- A ferramenta de linha de comando `kubectl` configurada para se comunicar com o cluster.

### Passos para Implementar

Para aplicar o PVC no Cluster, use o comando `kubectl apply`, conforme abaixo:

   ```sh
   kubectl apply -f wordpress-pvc.yaml
   ```

Verifique se o PVC foi criado:

   ```sh
   kubectl get pvc
   ```

## Conclusão

Este README fornece uma visão geral de como criar e usar um PersistentVolumeClaim (PVC) no Kubernetes para um deployment do WordPress. O PVC garante que os dados do WordPress sejam armazenados de forma persistente, mesmo que os pods sejam reiniciados ou reprogramados.

## Referências
Para mais informações, consulte a [documentação oficial do Kubernetes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/).