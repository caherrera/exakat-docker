PHP supports variables with certain characters. 

<?literal 
[a-zA-Z_\x7f-\xff][a-zA-Z0-9_\x7f-\xff]*

?>

In practice, letters outside the scope of a-zA-Z0-9 are rare, and require more care when editing the code or passing it from OS to OS. 

<?php

class 人 {
    // An actual working class in PHP.
    public function __construct() {
        echo __CLASS__;
    }
}

$people = new 人();

?>

