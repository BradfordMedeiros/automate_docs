## *automate_core* ##
------------

### What is automate_core? ###
Automate core is the backend for automate

Automate core is the logic for everything the UI can do.  
It provides mechaisms for the logic such as scheduling, conditions, patterns for broadcasting actions, and states.

Features of automate core include:
- MQTT Actions and States as conventions to endpoints
- Rule engine
- Scheduling 
- Action sequencing
- MQTT data logging
- Event logging
- Email alerts

### How do deploy automate core? ###
Simply run the command 
automate_core -data_folder (root_folder)

The root folder is important.
This can be generally ignored (just point it to an empty folder), and everything will work normally, but to do certain advanced features some knowledge of 
this will be needed.

At a high level the structure internally will look as such
<pre>
/
    /actions
    /states
    /conditions
    /sequences
</pre>
    
Where the actions and states are the axiomatic types which defined simple states and actions in the system.  Conditions
and sequences can be thought of as configuration files that create sequences (chains of actions executed with certain timings)
or conditions (rules that trigger actions when a certain configuration of states is met)

       
### Does automate_core require the UI ###
No, but you lose, well, all the user-interface, as well as user-interface specific things like graphs, voice controls (which may see front-end agnostic support eventually), and other features.