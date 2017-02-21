When a method expects objects as argument, those arguments should be typehinted, so as to provide early warning that a wrong object is being sent to the method.

The analyzer will detect situations where a class, or the keywords 'array' or 'callable'. 

<?php

// What are the possible classes that have a 'foo' method? 
function foo($bar) {
    return $bar->foo();
}

?>

Closure arguments are omitted.
