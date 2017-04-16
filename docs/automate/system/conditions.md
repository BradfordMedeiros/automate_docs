## *Conditions* ##
------------

### What is a condition? ###
A condition is a rule to perform actions, given system state. 
For example, a condition may be to turn on the fan when the room gets hot, turn a light on when it is dark, and so on. 

Conditions allow the user to perform logic that will happen automatically when the system is in a certain state


### How do I create a condition ###

A condition is a json configuration file that has the following format.  
The actions are called when the eval statement returns true.  

The condition has the following structure:

~~~~
{
	"state":[array of states to used in the condition evaluation], // required
	"eval": <evaluation function ==> states are passed in as arguments in the order of the states> // required
	"action":[array of actions to perform when the eval returns true],          // required
	"values": < map from action name to parameter to pass into that action >    // optional   
}
~~~~

More functionality will be added to specify rate limiting, frequency, transitions, and so on very soon.

### Using automate UI to create conditions ###
You can create conditions via the automate ui as well.  Currently the UI is simply a layer that allows you to input the 
json condition format above.  This is considered temporary and will eventually support a more noob friendly method.