## *Communication* ##
------------

### How do devices share information? ###
Devices communicate via MQTT.  

All communication happens over MQTT.  The backend of automate includes an MQTT broker.
Automate includes tooling that enhances MQTT topics, but does not violate anything you could otherwise do with MQTT.

The system also supports actions and states that are not powered via MQTT, and while the paradigm is perfectly supported,
I recommend using MQTT to architect your system.  That being said, you can make you own judgements, and you probably know
better for yourself than a general readme, because I don't have to lie to you to sell you anything.

Using mqtt's pathing system topics publishes with these paths:

actions: /action/<rest of topic path>
states: /state/<rest of topic path>

Simply by publishes to the state endpoint, you will be able to use it in the mqtt system and create conditions, sequences, see graphs in the UI, and so on.

Currently, besides the actions and states, there is another special path which is used as an event log:
/event/<rest of path>

Events can be configured by the user to send of emails, or text messages, etc.  See events for more information (coming soon).

