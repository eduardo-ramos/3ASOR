# WordPress Ingress

## O que é um Ingress?
No Kubernetes, um Ingress é um recurso que gerencia o acesso externo aos serviços em um cluster, geralmente HTTP. Ele fornece regras de roteamento que permitem que você exponha seus serviços para fora do cluster de maneira controlada.

### Componentes Principais
- **Ingress Controller**: Um controlador que implementa as regras definidas no recurso Ingress.
- **Ingress Resource**: O objeto Kubernetes que define as regras de roteamento.
- **Service**: O serviço Kubernetes que o Ingress expõe.

## Implementação

### Pré-requisitos
- Um cluster Kubernetes em funcionamento.
- `kubectl` configurado para se comunicar com o cluster.
- Um Ingress Controller instalado no cluster (por exemplo, NGINX Ingress Controller).


### Passos para Implementar

Para aplicar o PVC no Cluster, use o comando `kubectl apply`, conforme abaixo:

    ```sh
    kubectl apply -f wordpress-ingress.yaml
    ```

Verifique se o Ingress foi criado:

    ```sh
    kubectl get services
    ```

## Conclusão
Com esses passos, você configurou um serviço no Kubernetes para expor seu deployment do WordPress. Isso permite que o WordPress seja acessível através da rede, utilizando as políticas de acesso e balanceamento de carga definidas.

## Referências
- [Documentação Oficial do Kubernetes](https://kubernetes.io/docs/concepts/services-networking/service/)
