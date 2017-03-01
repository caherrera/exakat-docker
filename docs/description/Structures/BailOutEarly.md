When using conditions, it is recommended to return in the then, and avoid else clause. 

The main benefit is to make clear the method applies a condition, and stop quickly went it is not satisfied. 
The main sequence is then focused on the useful code. 

This works with break, continue too, inside loops. 

<?php

// Bailing out early, low level of indentation
function foo1($a) {
    if ($a > 0) {
        return false;
    } 
    
    $a++;
    return $a;
}

// Works with continue too
foreach($array as $a => $b) {
    if ($a > 0) {
        continue false;
    } 
    
    $a++;
    return $a;
}

// No need for else
function foo2($a) {
    if ($a > 0) {
        return false;
    } else {
        $a++;
    }
    
    return $a;
}

// No need for else : return goes into then. 
function foo3($a) {
    if ($a < 0) {
        $a++;
    } else {
        return false;
    }
    
    return $a;
}

?>

