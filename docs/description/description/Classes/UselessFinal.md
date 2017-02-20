When a class is declared final, all of its methods are also final by default. 

There is no need to declare them individually final.

<?php

    final class foo {
        // Useless final, as the whole class is final
        final function method() { }
    }

    class bar {
        // Usefule final, as the whole class is not final
        final function method() { }
    }

?>
