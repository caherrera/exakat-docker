Use array notation $string[$position] to reach a single byte in a string.

There are two ways to access a byte in a string : substr() and $v[$pos];

The second one is more readable. It may be up to four times faster, though it is a micro-optimization. 
It is recommended to use it. 

PHP 7.1 also introduces the support of negative offsets as string index : negative offset are also reported here.

<?php

$string = ab人cde;

echo substr($string, $pos, 1);
echo $string[$pos];
echo mb_substr($string, $pos, 1);

// $pos = 1
// bbb
// $pos = 2
// ??人

?>

Beware that substr() and $v[$pos] are similar, while mb_substr() is not. The first functions works on bytes, while the latter works on characters.