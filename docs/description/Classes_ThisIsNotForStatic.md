Static methods shouldn't use $this variable.

$this variable represents an object (the current object) and it is not compatible with a static method, which may operate without any object. 

<?php

class foo {
    static public function bar() {
        return $this->a;   // No $this usage in a static method
    }
}

?>
