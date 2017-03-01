When using a foreach(), the blind variables are a copy. It is confusing to change them. 

<?php

$foo = [1, 2, 3];
foreach($foo as $bar) {
    // $bar is updated but its final value is lost
    print $bar . ' => ' . ($bar + 1) . PHP_EOL;
    // if $bar + 1 is repeated several times, consider assigning it to a variable.
    foobar($bar + 1);

}

$foo = [1, 2, 3];
foreach($foo as $bar) {
    // $bar is updated but its final value is lost
    print $bar . ' => ' . (++$bar) . PHP_EOL;
    // Now that $bar is reused, it is easy to confuse its value
    foobar($bar);
}

?>
