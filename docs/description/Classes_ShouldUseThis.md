Methods in a class should use the class, or be functions.

Methods should use $this with another method or a property, or call parent::. Static methods should call another static method, or a static property. 

<?php

class foo {
    public function __construct() {
        // This method should do something locally, or be removed.
    }
}

class bar extends foo {
    private $a = 1;
    
    public function __construct() {
        // Calling parent:: is sufficient
        parent::__construct();
    }

    public function barbar() {
        // This is acting on the local object
        $this->a++;
    }

    public function barfoo($b) {
        // This has no action on the local object. It could be a function
        return 3 + $b;
    }
}

?>


