## *States* ##
------------

### What is an state? ###
An state represent system state. 
For example, an state may represent the door state (open/closed), the room temperature, 
or if an email has been sent in the last 5 minutes.

Systems represent a unit of system state, and can be used in conditions, and have various UI elements to support showing
system status.

States can be configured in automate in two ways.
- MQTT topics
- Executabe or js in automate_core folder which publish state content in json format via stdout


### How do I create a state ###

If the action is an MQTT topic, states are implied and the system will automatically register them in the system 
and therefore the UI when a topic with the prefix /state/ is sent out.

You can also create a state via placing an execute or js file in the /states directory of automate_core root folder.
These needs to live in /state folder and be name <anything>.state.<js else assumed executable>.

State content will be read from stdout of the program.
Format of all state is expected to json.


### Using automate UI to create states ###
You can create states via the automate ui as well.  Currently the UI supports making javascript actions only. 
You can use it how you see fit, but javascript states I find are good for creating simple logical utilities.  
For example, while I may have devices publishing humidity as a state, I have a javascript script set up that 
acts a simple program to determine if it is night time or not. 
