This code structure is quite old : it should be replace by the more modern and efficient foreach.

<?php
    foreach($array as $key => $value) {
        doSomethingWith($key) and $value;
    }
?> 

