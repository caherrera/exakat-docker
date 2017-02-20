Declaring a namespace in the code and not using it for structure declarations (classes, interfaces, etc...) or global instructions is useless.

Using simple style : 

<?php

namespace X;
// This is useless

namespace Y;

class foo {}

?>

Using bracket-style syntax : 

<?php

namespace X {
    // This is useless
}

namespace Y {

    class foo {}

}

?>


