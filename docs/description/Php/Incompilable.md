Files that cannot be compiled, and, as such, be run by PHP. Scripts are linted against PHP versions 5.2, 5.3, 5.4, 5.5, 5.6, 7.0-dev and 7.1. 

This is usually undesirable, as all code must compile before being executed. It may simply be that such files are not compilable because they are not yet ready for an upcoming PHP version.

<?php

// Can't compile this : Print only accepts one argument
print $a, $b, $c;

?>

Code that is incompilable with older PHP versions means that the code is breaking backward compatibility : good or bad is project decision.

