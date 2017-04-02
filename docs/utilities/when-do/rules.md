# *when_do --> rules* #
------------

### Description ###
**rules** is a utility class to evaulate when certain conditions become true.
Upon calling do the actions will start to be evaluated.  Functions used as evaluators should be pure and lightweight.
The library works internally by calling these functions and evaluating them on a loop. This means it fits certain use
cases well, but is not meant as a replacement for a basic if statement since it is a continuous check.

rules // -> main object used to create rules

General pattern is below:
When the evaluator returns true, the function will call function_to_perform.
Options may be specified that specify the frequency to call the evaluator, rate, action limit, rate limit.  See below for details

~~~~
rules.(evaluator).do(function_to_perform: function, options: object)
~~~

Methods

~~~~
    when(object_to_evaluate: any, evaluator_function: function<bool>) // will perform the action when the evaluator is true
    transition(evaluator_function1: function<bool>, evaluator_function2: function<bool>, action: function<any>) // will perform the action when the first evaluator is true, and then the second becomes true
    expectWithin(evaluator_function1: function<bool>, evaluator_function2: function<bool>, action: function<any>, resolve, reject) // when the first condition becomes true, call the resolve callback if the func2 returns true, else call the back callback
~~~~

Examples:
----
Ex1.
~~~~

----
Ex2.
~~~~
~~~~


Ex3.
~~~~

~~~~
