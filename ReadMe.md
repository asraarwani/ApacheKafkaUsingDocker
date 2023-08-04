Assuming you have docker installed on your machine.

Commands:
  From the root directory (/ApacheKafkaUsingDocker), run the following, make sure docker daemon is running on your machine:

docker compose -f .\docker-compose.yml up -d     -> Downloads the images which we have specified in docker-compose.yml file

docker images   -> shows the images have been downloaded

docker ps -> shows the container are running

docker exec -it kafka /bin/sh   -> to start the terminal for running various commands 

go to /opt/kafka_2.13-2.8.1/bin and then run following commands in different terminals:

    Create a topic by running following command : kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quick-start
    Start producer by running following command : kafka-console-producer.sh --topic quick-start --bootstrap-server localhost:9092
    Start consumer by running following command : kafka-console-consumer.sh --topic quick-start --from-beginning --bootstrap-server localhost:9092
    
You can also view the contents of topic using Kafka explorer tool as well.

