## *Sequences* ##
------------

### What is a sequence? ###
A sequence is a specification to perform one or more actions in a particular sequence, or order, 
with extra timing information.

A sequence can be thought of a special type of action, which is a grouping of actions.
For example, given you have an action available to turn off the light, and another action to turn on the tv, and then on to turn on your video game system,
you may specify a sequence as turning on the lights, then two seconds later turning on the tv and video game system.


### How do I create a sequence ###

A sequence is a json configuration file that has the following format.  
The sequence has the following structure:

~~~~
{
    "actions": [ array of directives]
     ]
}
~~~~
where the two types of directives are:
Meaning to call and action and pass in he paramteres to it as specified in value

~~~~
{
    "name": "action"
    "value": <value>
}
~~~~
or 
~~~~
{
    "name": "wait"
    "value": <time to wait in ms>
}
~~~~


### Using automate UI to create sequences ###
Coming soon