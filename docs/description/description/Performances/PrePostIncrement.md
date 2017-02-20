When possible, use the pre-increment operator (++$i or --$i) instead of the post-increment operator ($i++ or $i--).

The latter needs an extra memory allocation that costs about 10% of performances. 

<?php

// ++$i should be preferred over $i++, as current value is not important
for($i = 0; $i <10; ++$i) {
    // do Something
}

// ++$b and $b++ have different impact here, since $a will collect $b + 1 or $b, respectively.
$a = $b++;

?>

