# Hola Mundo con Apache Kafka

## Descripción
Este proyecto muestra un ejemplo básico de Apache Kafka utilizando Docker Compose.

## Tecnologías usadas
- Apache Kafka
- Docker
- Docker Compose

## Imagen usada
https://hub.docker.com/r/apache/kafka

## Ejecutar el proyecto

```bash
docker compose up -d
```

## Crear tópico

```bash
docker exec -it kafka /opt/kafka/bin/kafka-topics.sh --create --topic hola-mundo --bootstrap-server localhost:9092
```

## Producer

```bash
docker exec -it kafka /opt/kafka/bin/kafka-console-producer.sh --topic hola-mundo --bootstrap-server localhost:9092
```

Mensaje enviado:

```text
Hola Mundo Kafka
```

## Consumer

```bash
docker exec -it kafka /opt/kafka/bin/kafka-console-consumer.sh --topic hola-mundo --from-beginning --bootstrap-server localhost:9092
```

Resultado:

```text
Hola Mundo Kafka
```
