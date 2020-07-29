# Kafka hello world

This is simple example to use Kafka producer and consumer.


![Sample image](https://github.com/diegoandrepoli/kafka/blob/master/sample-kafka.png)


## Donwload and extract
Download kafka at https://kafka.apache.org/downloads, for direct link to 2.12 version click [here](http://ftp.unicamp.br/pub/apache/kafka/2.5.0/kafka_2.12-2.5.0.tgz).

Extract binaries on your prefered directory, example to extract.

```
$ tar -zxvf kafka_2.12-2.5.0.tgz
```

## Start Zookeeper

Start Zookeeper with default settings.

```
$ ./zookeeper-server-start.sh ../config/zookeeper.properties
```

## Start Kafka server

Start Kafka with default settings.

```
$ ./bin/kafka-server-start.sh config/server.properties
```

##  Start Kafka producer 

Start a kafka producer at foo topic.

```
$ ./kafka-console-producer.sh --broker-list localhost:9092 --topic foo
```

## Start Kafka consumer

Start a consumer at foo topic.

```
$ ./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic foo --from-beginning
```
