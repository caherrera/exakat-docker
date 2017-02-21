Adding 0 is useless, as 0 is the neutral element for addition. It may trigger a cast (to integer), though behavior changes from PHP 7.0 to PHP 7.1. 

<?php

$a = 123 + 0;
$a = 0 + 123;

// Also works with minus
$b = 0 - $c; // drop the 0, but keep the minus
$b = $c - 0; // drop the 0 and the minus

?>

If it is used to type cast a value to integer, then casting (integer) is clearer. 
