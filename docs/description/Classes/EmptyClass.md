List of empty classes. Classes that are directly derived from an exception are omited.

<?php

//Empty class
class foo extends bar {}

//Not an empty class
class foo2 extends bar {
    const FOO = 2;
}

//Not an empty class, as derived from Exception
class barException extends \Exception {}

?>
