# KafkaProducer
KafkaProducer SpringBoot



1)go to the  D:\Softwares\kafka_2.11-2.4.0\bin\windows and select the top of the window folder box and type cmd.

2)start zookeeper.start bat file like below
Type this command in the cmd prompt
zookeeper-server-start.bat D:\Softwares\kafka_2.11-2.4.0\config\zookeeper.properties
3)start kafka server
kafka-server-start.bat   D:\Softwares\kafka_2.11-2.4.0\config\server.properties
4)Create Topic:
Kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic KafkaTopic
------------------------------------------------------------------------------------------------------
Here if you had created the producer program then use the second one(if you want consumer) and viseversa
----->)Produce a message
kafka-console-producer.bat --broker-list localhost:9092 --topic KafkaTopic
----->)Consume a message
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic KafkaTopic
