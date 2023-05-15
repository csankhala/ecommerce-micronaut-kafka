## How to start Kafka Docker container Locally

1. Install Docker on your local machine
2. Open a terminal and run the following command to download the Kafka image from Docker Hub:
docker pull wurstmeister/kafka

3. Run the following command to create a Docker network that Kafka will use
docker network create kafka-net

4. Start a ZooKeeper container by running the following command:
docker run --name zookeeper --network kafka-net -p 2181:2181 -d zookeeper

This will start a ZooKeeper container on the Kafka network, using port 2181.

5. Start a Kafka container by running the following command:
docker run --name kafka --network kafka-net -p 9092:9092 -e KAFKA_ADVERTISED_HOST_NAME=localhost -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 -e KAFKA_CREATE_TOPICS="topic1:1:1" -d wurstmeister/kafka

This will start a Kafka container on the Kafka network, using port 9092.

6. Verify that both ZooKeeper and Kafka are running by running the following command:
docker ps
This will display a list of all the running Docker containers on your machine. You should see both the ZooKeeper and Kafka containers listed.

That's it! You now have a Kafka instance running locally on your machine using Docker.

## Next time simply run below commands (Its same command but without name field)
docker run --network kafka-net -p 2181:2181 -d zookeeper
docker run --network kafka-net -p 9092:9092 -e KAFKA_ADVERTISED_HOST_NAME=localhost -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 -e KAFKA_CREATE_TOPICS="topic1:1:1" -d wurstmeister/kafka

## Kafka UI

docker run -it -p 8080:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui

Then access the web UI at http://localhost:8080
