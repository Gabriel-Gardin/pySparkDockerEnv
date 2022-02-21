# Template de uma aplicação distribuida pySPark


## Requerimentos

1. Docker
2. Docker Compose

Template para simular um ambiente real de processamento de dados com um cluster spark distribuído. Utilizando imagens docker e docker-compose para criar uma aplicação distribuída contendo uma IDE JupyterLab, Spark master node e dois Spark Worker nodes.

## Reproduzindo

Após clonar o repositório entre no seu diretório e execute os comandos abaixo:

Primeiro é necessário construir as imagens Docker, para isso precisamos alterar a permissão de exucação do arquivo build.sh

```bash
chmod +x build.sh
```

Em sequência construa as imagens(Etapa um pouco demorada ~10 minutos):

```bash
./build.sh
```

Finalmente podemos subir o cluster com o comando:

```bash
docker-compose up
```

Os nodes da aplicação podem ser acessados pelos links:

- JupyterLab: [localhost:8888]();
- Spark master: [localhost:8080]();
- Spark worker I: [localhost:8081]();
- Spark worker II: [localhost:8082]();

## Referências

[Spark cluster com docker](https://towardsdatascience.com/apache-spark-cluster-on-docker-ft-a-juyterlab-interface-418383c95445)
[Spark cluster](https://github.com/cluster-apps-on-docker/spark-standalone-cluster-on-docker)
