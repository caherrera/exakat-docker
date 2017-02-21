Some operators have a compact 'do-and-assign' version.

They looks like a compacted version for = and the operator. This syntax is good for readability, and saves some memory in the process. 

<?php

$a = $a + 0;
$a += 0;

$b = $b - 1;
$b -= 1;

$c = $c * 2;
$c *= 2;

$d = $d / 3;
$d /= 3;

$e = $e % 4;
$e %= 4;

$f = $f | 5;
$f |= 5;

$g = $g & 6;
$g &= 6;

$h = $h ^ 7;
$h ^= 7;

$i = $i >> 8;
$i >>= 8;

$j = $j << 9;
$j <<= 9;

?>

