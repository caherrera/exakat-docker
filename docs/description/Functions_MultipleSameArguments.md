A method's signature is holding twice (or more) the same argument. For example, function x ($a, $a) { ... }. 

This is accepted as is by PHP, and the last parameter's value will be assigned to the variable : 

function x ($a, $a) { print $a; };
x(1,2); => will display 2

However, this is not common programming practise : all arguments should be named differently.
