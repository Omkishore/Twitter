t# Twitter
Processing Twitter  Data with KStreams



# to Start ZooKeeper
.\bin\windows\zokeeper-server-start.bat .\config\zookeeper.properties

# to Start Kafka Server
.\bin\windows\kafka-server-start.bat .\config\server.properties

#to create topic
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic twitter

.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic twitter_output

# Kafka connect to push the topic data to File System.
.\bin\windows\connect-standalone.bat .\config\my-standalone.properties .\config\my-sink-properties



