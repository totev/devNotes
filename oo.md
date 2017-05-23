	"Functions that change state should not return values and functions that return values should not change state."
	Bertrand Meyer
	
	Commands return void and queries return values.
	Use exceptions rather than returning and checking for error states.
	
Law of Demeter:
	"Each unit should have only limited knowledge about other units: only units “closely” related to the current unit. Each unit should only talk to its friends; don’t talk to strangers."


Credits, sources and some links of interest for further reading:
--
* https://hackernoon.com/oo-tricks-the-art-of-command-query-separation-9343e50a3de0