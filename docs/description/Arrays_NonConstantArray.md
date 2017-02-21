In '$array[index]', PHP cannot find index as a constant, but, as a default behavior, turns it into the string 'index'. 

This default behavior raise concerns when a corresponding constant is defined, either using define() or the const keyword (outside a class). The definition of the index constant will modify the behavior of the index, as it will now use the constant definition, and not the 'index' string. 

$array[index] = 1; // assign 1 to the element index in $array
define('index', 2);
$array[index] = 1; // now 1 to the element 2 in $array

It is recommended to make index a real string (with ' or "), or to define the corresponding constant to avoid any future surprise.
