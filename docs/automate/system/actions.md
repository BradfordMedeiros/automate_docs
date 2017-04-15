## *Actions* ##
------------

### What is an action? ###
An action is something that the system can do. 
For example, an action may be to open a door, set the room temperature, send an email, and so on. 

Actions represent a unit of what the system can do, and can be used in sequences, conditions, and will show up as actions
available to the user within the UI.

Actions can be configured in automate in two ways.
- MQTT topics
- Executabe or js in automate_core folder


### How do I create an action ###

If the action is an MQTT topic, actions are implied and the system will automatically register them in the system 
and therefore the UI when a topic with the prefix /action/ is sent out.

You can also create an action via placing an execute or js file in the /actions directory of automate_core root folder.
These needs to live in /actions folder and be name <anything>.action.<js else assumed executable>


### Using automate UI to create actions ###
You can create actions via the automate ui as well.  Currently the UI supports making javascript actions only. 
You can use it how you see fit, but javascript actions are created with the intent of sending simple scripts, 
especially involving basic http triggering.  This will actually live on the backend as opposed to being an action trigger from 
a stand alone device. 

