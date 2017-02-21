The following classes used to have a very specific behavior during instantiation : they were able to return NULL on new.

After issuing a 'new' with those classes, it was important to check if the returned object were null (sic) or not. No exception were thrown.

<?php

// Example extracted from the wiki below
$mf = new MessageFormatter('en_US', '{this was made intentionally incorrect}');
if ($mf === null) {
    echo 'Surprise!';
}

?>

This inconsistency has been cleaned in PHP 7 : see See [Internal Constructor Behavior](https://wiki.php.net/rfc/internal_constructor_behaviour)

