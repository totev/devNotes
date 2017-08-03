Refactoring to Java 8
===
*	Annonymous classes
	* lambda expressions

*	Multi line lambda expressions
	* separate method calls
	* + readability
	* + better exception handling/readability

*	Abstract classes
	* interfaces annotated with @FunctionalInterface
	* !Lambda expressions can only be used with interfaces

*	Lambda with Supplier<?> supplies the recepy and not the execution
	* lazy evaluation
	* + performance

*	For Loop
	* ForEach
	* AnyMatch (does what it says finds an any match according to a given criteria)
					* ! worse performance than a simple array iteration -> avoid it by any means!
	* FindFirst
				 * orElse()
				* ! worse performance

*	Collections.removeIf => prettier, more readable, same performance!

Sum up
------
*	Follow and obey the stream flow.
*	Multiple streams arguably perform better on big collections (>100000 )
* 	Arrays.stream() is slower then going native, some benefits may present theirselves when going parallel
*	!Basic arrays still outperform anything else
*	!Debugging still remains a challange
