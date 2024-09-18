# Kafka Installation and Setup on EC2

```bash
# Step 1: Download and Extract Kafka
wget https://downloads.apache.org/kafka/3.8.0/kafka_2.13-3.8.0.tgz
tar -xvf kafka_2.13-3.8.0.tgz

# Step 2: Install Java
# Check if Java is installed
java -version

# If Java is not installed, install it
sudo yum install java-1.8.0-openjdk ( or the latest version available )

# Verify the Java installation
java -version

# Step 3: Start ZooKeeper
cd kafka_2.13-3.8.0
bin/zookeeper-server-start.sh config/zookeeper.properties

# Step 4: Start Kafka Server
# Open another terminal window and SSH into your EC2 instance
export KAFKA_HEAP_OPTS="-Xmx256M -Xms128M"
cd kafka_2.13-3.8.0
bin/kafka-server-start.sh config/server.properties

# Step 5:  Stop zookeeper and server and Update server.properties for public IP
# Run this command to edit the file:
sudo nano config/server.properties

# Update ADVERTISED_LISTENERS to the public IP of your EC2 instance and then again start the zookeeper and server

# Step 6: Create a Kafka Topic
# In a new terminal session, SSH into your EC2 instance and run the following:
cd kafka_2.13-3.8.0
bin/kafka-topics.sh --create --topic demo_testing2 --bootstrap-server {Public_IP_of_EC2_Instance:9092} --replication-factor 1 --partitions 1

# Step 7: Start Kafka Producer
bin/kafka-console-producer.sh --topic demo_testing2 --bootstrap-server {Public_IP_of_EC2_Instance:9092}

# Step 8: Start Kafka Consumer
# Open a new terminal session, SSH into your EC2 instance, and run:
cd kafka_2.13-3.8.0
bin/kafka-console-consumer.sh --topic demo_testing2 --bootstrap-server {Public_IP_of_EC2_Instance:9092}

# Step 9: Stop Kafka Server
./bin/kafka-server-stop.sh
# Or use Ctrl + Z to stop the server
