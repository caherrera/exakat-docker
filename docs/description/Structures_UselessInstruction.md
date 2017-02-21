The instructions below are useless, or contains useless parts. For example, running '&lt;?php 1 + 1; ?&gt;' does nothing : the addition is actually performed, but not used : not displayed, not stored, not set. Just plain lost. 

Here the useless instructions that are spotted : 

<?php

// Empty string in a concatenation
$a = 'abc' . '';

// Returning expression, whose result is not used (additions, comparisons, properties, closures, new without =, ...)
1 + 2;

// Returning post-incrementation
function foo($a) {
    return $a++;
}

// array_merge() with only one argument
$merge = array_merge($array);

// @ operator on source array, in foreach, or when assigning literals
$array = @array(1,2,3);

// Comparisons in a for loop : only the last is actually used.
for($i = 0; $j = 0; $j < 10, $i < 20; ++$j, ++$i) {
    print $i.' '.$j.PHP_EOL;
}

?>

