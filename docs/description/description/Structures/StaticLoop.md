It looks like the following loops are static : the same code is executed each time, without taking into account loop variables.

<?php

// Static loop
$total = 0;
for($i = 0; $i < 10; $i++) {
    $total += $i;
}

// Non-Static loop (the loop depends on the size of the array)
$n = count($array);
for($i = 0; $i < $n; $i++) {
    $total += $i;
}

?>

It is possible to create loops that don't use any blind variables, though this is fairly rare.  