PHP's regex support the following list of options : eimsuxADJSUX. They are detailled in the manual : [http://php.net/manual/en/reference.pcre.pattern.modifiers.php](http://php.net/manual/en/reference.pcre.pattern.modifiers.php). 

All other options are not supported, may be ignored or raise an error.

<?php

// all options are available
if (preg_match('/\d+/isA', $string, $results)) { }

// p and h are not regex options, p is double
if (preg_match('/\d+/php', $string, $results)) { }

?>
