# RabbitMQ com Python

Para utilizar o RabbitMQ com Python vamos utilizar a imagem oficial do [Docker do RabbitMQ]:

```bash
    docker pull rabbitmq
```
Para rodar com o Docker utilize o seguinte comando:

```bash
    docker run --rm -p 5672:5672 -p 8080:15672 rabbitmq:3-management
```

O Docker pode ser acessado através da porta 8080 com as credenciais default (**username:guest e password:guest**).Na tela principal do RabbitMQ podemos visualizar e gerenciar o consumo das filas, além de importar e exportar as configurações.

![Captura de tela de 2021-10-25 20-20-34](https://user-images.githubusercontent.com/52939036/138783852-645cba33-816d-40df-a650-da32e821384a.png)


## Conceitos

Para entender o [RabbitMQ com Python] precisamos entender alguns conceitos:

**Exchange**: As mensagens são publicadas em um exchange por um producer, que por sua vez direciona as mesmas para uma ou mais filas.

**Queue**: Fila que recebe e guarda as mensagens que devem ser entregues a um ou mais consumidores.

**Binding**: Regra para mandar a mensagem para uma ou mais filas. É o relacionamento entre o exchange e a fila.

## Trocando mensagens

Para enviar uma mensagem usando python, vamos usar a biblioteca [pika].

```bash 
    pip install -r requirements.txt
```

[Docker do RabbitMQ]: https://hub.docker.com/_/rabbitmq/
[RabbitMQ com Python]: https://www.rabbitmq.com/tutorials/tutorial-three-python.html
[pika]: https://pika.readthedocs.io/en/1.2.0/