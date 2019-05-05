# Project-Kafka
Kafka projects


1. Start zookeeper
```
zookeeper-server-start.bat ..\..\config\zookeeper.properties
```

2. Start broker
```
kafka-server-start.bat ..\..\config\server.properties
```

3. Ceate Topic 
```
kafka-topics.bat --create --topic topic-1 -zookeeper localhost:2181 --replication-factor 1 --partitions 1
```

4. List all topics created
```
kafka-topics.bat --describe -zookeeper localhost:2181
```

5. Run producer and publish messages
```
kafka-console-producer.bat  --broker-list localhost:9092  --topic topic-1
```

6. Run consuler and read messages from begining
```
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic topic-1  --from-beginning
```


