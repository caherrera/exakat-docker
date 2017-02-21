List of properties and methods that are accessed using 'parent' keyword but are not defined in the parent class. 

This will be compilable but will yield a fatal error during execution.

Note that if the parent is defined (extends someClass) but someClass is not available in the tested code (it may be in composer,
another dependency, or just not there) it will not be reported.
