## How to start Kafka Docker container Locally

1. Install [Docker](https://www.docker.com/products/docker-desktop/) on your local machine
2. Open a terminal and run the following command to download the Kafka image from Docker Hub:<br>
`docker pull spotify/kafka`<br>

3. Run the following command to run Kafka <br>
`docker run -p 2181:2181 -p 9092:9092 --name kafka-docker-container --env ADVERTISED_HOST=127.0.0.1 --env ADVERTISED_PORT=9092 spotify/kafka` <br>

6. Verify that Kafka running by running the following command:<br>
`docker ps`<br>

Reference: https://towardsdev.com/3-simple-steps-to-set-up-kafka-locally-using-docker-b07f71f0e2c9

## Next time simply run below commands (Its same command but without name field)
`docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=127.0.0.1 --env ADVERTISED_PORT=9092 spotify/kafka` <br>

## Kafka UI

`docker run -it -p 8080:8080 -e DYNAMIC_CONFIG_ENABLED=true provectuslabs/kafka-ui`

Then access the web UI at `http://localhost:8080`
