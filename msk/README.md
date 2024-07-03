# MSK Example for Java

Example code for connecting to a AWS MSK cluster and authenticate with SSL_SASL and SCRAM. 

## Running locally

If you just want to test it out.

### Configure

All of the authentication settings can be found in the Details page for your CloudKarafka instance.

```
export CLOUD_KAFKA_BROKERS=broker1:9094,broker2:9094,broker3:9094
export CLOUD_KAFKA_USERNAME=<username>
export CLOUD_KAFKA_PASSWORD=<password>
```

### Run

```
git clone 
cd msk
mvn clean compile assembly:single
java -jar target/msk-0.0.1-SNAPSHOT-jar-with-dependencies.jar
```

This will start a Java application that pushes messages to AWS MSK cluster in one Thread and read messages in the main Thread. 
The output you will see in the terminal is the messages received in the consumer.
