# Real-time Job Postings System

This is a simple system created to demonstrate how messaging, data processing and data streaming work in reactive sytems. It has four main parts
1. **Data publisher service** - is a scheduled program that runs in a specific time interval and generates random job postings data to a kafka topic
2. **Data processor service** - is a Kafka streaming service that does filtering on the data generated by data publisher and sends it back to a separate Kafka topic
3. **Data consumer service** - is a subscriber that listens to incoming messages in Kafka topics, saves the messages to reactive mongo database. It also uses server sent events to send them as streams for external clients 
4. **Single page angular application** - makes http calls to the consumer service to get real-time data

## Technologies used

* SpringBoot
* Spring Webflux
* Reactive mongo db
* Spring kafka
* Spring kafka streams
* Angular

![Architecture](https://github.com/Gebreegziabher/job-postings/assets/6954726/ef290f54-f040-47f3-a428-e1b99c78f856)
