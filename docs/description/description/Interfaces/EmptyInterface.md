Empty interfaces. Interfaces should contains some function, and not be totally empty.

<?php

// an empty interface
interface empty {}

// an normal interface
interface normal {
    public function i() ;
}

// an constant interface
interface constantsOnly {
    const FOO = 1;
}

?>

