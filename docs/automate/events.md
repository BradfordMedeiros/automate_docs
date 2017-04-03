## *Events* ##
------------

### What is an event? ###
An event is something which would be of interest to the user. 
For example, an event may be something like a door opening, the cat being fed, a light turning on, and so on.

Events are currently consumed by automate for two purposes.
- Email alerts
- History log


### How do I log an event? ###

Using MQTT publish a topic with the prefix, /event to the automate system.

Examples: 
- /event/DoorOpened 
- /event/LightTurnedOn

Overload via the message body in json format:
~~~~
{   
  eventName, // the name that will show up to the user via guis
  value: // the value, for example you could say lightState as the event name, and on/off here
}
~~~~

### What is a good event ###
Events can be used as seen fit, but it is recommended to use events to communicate significant system happenings.

For example
##### Good Events #####
- Door opened
- Cat fed
- Light turned on in the office
- Temperature limit exceeded

##### Bad Events #####
- Humidity: 63 degrees (overly specific, probably too frequent)
- Time: 6pm  (overly specific, probably to frequent)
- DoorState: on (non-user friendly text, and what is DoorState actually mean?)
- dataSource:null (what is dataSource and what does it mean for it to be null here?)

