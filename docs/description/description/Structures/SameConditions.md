Several If then else structures are chained, and some conditions are identical. The latter will be ignored.

<?php

if ($a == 1) { doSomething(); }
elseif ($b == 1) { doSomething(); }
elseif ($c == 1) { doSomething(); }
elseif ($a == 1) { doSomething(); }
else {}

// Also works on if then else if chains
if ($a == 1) { doSomething(); }
else if ($b == 1) { doSomething(); }
else if ($c == 1) { doSomething(); }
else if ($a == 1) { doSomething(); }
else {}

?>
