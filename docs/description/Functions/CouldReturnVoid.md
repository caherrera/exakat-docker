The following functions may bear the Void return typeHint. 

<?php

// This can be Void
function foo(&$a) {
    ++$a;
    return; 
}

// This can't be Void
function bar($a) {
    ++$a;
    return $a;  
}

?>

