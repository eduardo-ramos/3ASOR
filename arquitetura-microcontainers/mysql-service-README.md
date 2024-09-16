# MySQL Service

## O que é um Service?
No Kubernetes, um **Service** é um recurso que define uma forma lógica de agrupar um conjunto de pods e expor uma forma de acessá-los. Ele permite que você defina políticas de acesso e balanceamento de carga para os pods selecionados.

### Componentes Principais
- **Tipo de Serviço**: Define como o serviço será exposto. No nosso caso, é do tipo `Service`.
- **Metadados**: Inclui informações como o nome do serviço (`mysql-service`) e rótulos (`app: mysql`).
- **Seleção**: Especifica quais pods serão selecionados pelo serviço, usando rótulos (`app: mysql`).
- **Portas**: Define as portas que serão expostas pelo serviço, tanto internamente quanto externamente (porta `3306`).

## Implementação

### Pré-requisitos
- Um cluster Kubernetes funcionando.
- `kubectl` configurado para se comunicar com o cluster.
- Um deployment do MySQL já configurado e rodando no cluster.

### Passos para Implementar

Para aplicar o Service no Cluster, use o comando `kubectl apply`, conforme abaixo:

    ```sh
    kubectl apply -f mysql-service.yaml
    ```

Verifique se o Service foi criado:

    ```sh
    kubectl get services
    ```

## Conclusão
Com esses passos, você configurou um serviço no Kubernetes para expor seu deployment do MySQL. Isso permite que o MySQL seja acessível através da rede, utilizando as políticas de acesso e balanceamento de carga definidas.

## Referências
- [Documentação Oficial do Kubernetes](https://kubernetes.io/docs/concepts/services-networking/service/)
