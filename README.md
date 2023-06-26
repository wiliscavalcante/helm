
# Meu Chart

Este é o chart do Helm para o Meu Aplicativo.

## Descrição

O Meu Aplicativo é uma aplicação web incrível que faz coisas incríveis. Este chart permite implantar facilmente o Meu Aplicativo em um cluster Kubernetes usando o Helm.

## Pré-requisitos

- Kubernetes 1.10+
- Helm 3.0+

## Instalação

Para instalar o Meu Aplicativo no seu cluster Kubernetes, siga as instruções abaixo.

Adicione o repositório do chart:
```
helm repo add meu-repo https://exemplo.com/meu-repo
helm repo update
```

Instale o chart:
```
helm install meu-app meu-repo/meu-chart
```

## Configuração

A tabela a seguir descreve os parâmetros de configuração disponíveis para o chart.

| Parâmetro                  | Descrição                              | Valor Padrão |
|----------------------------|----------------------------------------|--------------|
| `image.repository`         | Repositório da imagem do container      | `meu-app`    |
| `image.tag`                | Tag da imagem do container              | `latest`     |
| `replicaCount`             | Número de réplicas                      | `1`          |
| `service.type`             | Tipo de serviço                         | `ClusterIP`  |
| `service.port`             | Porta do serviço                        | `80`         |
| `resources.limits.cpu`     | Limite de CPU para o container          | `500m`       |
| `resources.limits.memory`  | Limite de memória para o container      | `1Gi`        |
| `resources.requests.cpu`   | Requisição de CPU para o container      | `200m`       |
| `resources.requests.memory`| Requisição de memória para o container  | `500Mi`      |

Para personalizar a instalação do chart, você pode especificar os valores desejados usando a opção `--set` no comando `helm install`, ou fornecer um arquivo de valores personalizados usando a opção `-f`:
```
helm install meu-app meu-repo/meu-chart --set service.type=NodePort
```

## Desinstalação

Para desinstalar o Meu Aplicativo do seu cluster Kubernetes, execute o seguinte comando:
```
helm uninstall meu-app
```

## Contribuição

Se você encontrar algum problema ou tiver alguma sugestão de melhoria, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
