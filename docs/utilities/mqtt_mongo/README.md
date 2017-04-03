# *when-do* --> mqtt_mongo #
------------

### Description ###
**mqtt_mongo** is an npm library used in automate that allows you to log all mqtt topics to a mongo database.

API
~~~~
    function: 
        log_mqtt_topics_to_mongo(MQTT_BROKER_URL: string, MONGO_URL: string, MQTT_CONNECTION_TIMEOUT_IN_MS: Number, MONGO_CONNECTION_TIMEOUT_IN_MS: Number
~~~~

### Basic Usage through CLI ###
~~~
    mqtt_mongo -mongoURL <mongoUrl> -mqttURL <mqttUrl>
~~~

### Basic Usage as Code ###
~~~~
const mqtt_mongo = require('mqtt_mongo');
mqtt_mongo.iog_mqtt_topics_to_mongo(MQTT_BROKER_URL, MONGO_URL);
~~~~

### Accessing the MongoDb and MQTT clients ###
Note: This promise will resolve upon succesful connection to the MQTT and Mongo brokers
~~~
const mqtt_mongo = require('mqtt_mongo');
mqtt_mongo
    .iog_mqtt_topics_to_mongo(MQTT_BROKER_URL, MONGO_URL)
    .then((mongoConnection, mqttConnection) => {
        ...
    });
~~~

#### Installation ####
~~~~
npm install mqtt_mongo
~~~~