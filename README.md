# RabbitMQ

[RabbitMQ] é um servidor de mensageria de código aberto (open source) implementado para suportar mensagens em um protocolo AMQP (*Advanced Message Queuing Protocol*). Ele possibilita lidar com o tráfego de mensagens de forma rápida e confiável, além de ser compatível com diversas linguagens de programação, possuir interface de administração nativa e ser multiplataforma.

Dentre as aplicabilidades do RabbitMQ estão possibilitar a garantia de assincronicidade entre aplicações, diminuir o acoplamento entre aplicações, distribuir alertas, controlar fila de trabalhos em background.

### Principais conceitos

**Mensagem**

Uma mensagem é dividida em duas partes:

* Payload: Corpo da mensagem; suporta diversos formatos como array e json.
* Label: Contém a descrição do payload e identificador de quem receberá a mensagem.

**Fila**

Onde as mensagens ficam retidas:
![Captura de tela de 2021-10-25 20-07-37](https://user-images.githubusercontent.com/52939036/138782872-d2096451-fced-40fc-a9a1-1127bfc5daa5.png)

**Publisher**

É o responsável por incluir cada nova mensagem na fila, ou seja enviar a mensagem.

![Captura de tela de 2021-10-25 20-09-41](https://user-images.githubusercontent.com/52939036/138783053-6797c1e2-0a6f-4cf0-9f69-fc0f7c8e518c.png)

**Consumer**

Responsável por consumir a informação, ou seja, retirar a mensagem da fila.

![Captura de tela de 2021-10-25 20-10-42](https://user-images.githubusercontent.com/52939036/138783073-4f12a465-8c5e-4052-90f5-74fd6892d3ca.png)


## RabbitMQ com Python

Utilizando o RabbitMQ com Python.


[RabbitMQ]: https://www.rabbitmq.com/documentation.html

[Docker do RabbitMQ]: https://hub.docker.com/_/rabbitmq/