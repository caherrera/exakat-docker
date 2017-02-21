PHP is good at manipulating data. However, it is also good to preprocess those values, and put them in the code directly as expected, rather than have PHP go the extra step and do it for you.

For example : 

<?php
  $x = explode(',', 'a,b,c,d'); 
?>

could be written 

<?php
  $x = array('a', 'b', 'c', 'd');
?>

and avoid preprocessing the string into an array first. 