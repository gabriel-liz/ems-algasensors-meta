# ems-algasensors-meta

Projeto de processamento e monitoração de dispositivos de temperatura

* FluxoDeTeste.txt para facilitar e lembrar o fluxo basico da operação


Adicionado RabbitMQ no projeto
localhost:15672

Para iniciar o rabbitMQ: 
docker-compose up -d



################################

**No rabbitMQ:**

Obs: Já estamos criando a exchagen direto com o java, mas em produção isso não é uma boa pratica.

Criar as exchanges no rabbitMQ:
* temperature-processing.temperature-received.v1.e
*  type: fanout

Adicionar a QUEUES:
temperature-monitoring.process-temperature.v1.q

**Conectar a Queue a Exchange**

Em Exchanges, acessar a exchange:

Bindings -> "To queue": temperature-monitoring.process-temperature.v1.q -> Bind

##################################









  