## *Communication* ##
------------

### How do devices share information ###
Devices communicate via MQTT.  
All communication happens over MQTT.  The backend of automate includes an MQTT broker.
Automate includes tooling that enhances MQTT topics, but does not violate anything you could otherwise do with MQTT.

Automate does enhance topics, and to use the features, I recommend following following convention and I recommend
reading about actions, states, and conditions before proceeding.

Using mqtt's pathing system topics publishes with these paths:

actions: /action/<rest of topic path>
states: /state/<rest of topic path>

Simply by publishes to the state endpoint, you will be able to use it in the mqtt system and create conditions, sequences, see graphs in the UI, and so on.

Currently, besides the actions and states, there is another special path which is used as an event log:
/event/<rest of path>

Events can be configured by the user to send of emails, or text messages, etc.  See events for more information (coming soon).

