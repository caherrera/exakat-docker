It is recommended to use echo with multiple arguments, or a concatenation with print, instead of multiple calls to print echo, when outputting several blob of text.

Write : 

<?php
  echo 'a', $b, 'c';
  print 'a' . $b . 'c';
?>

Don't write :  

<?php
  print 'a';
  print $b;
  print 'c';
?>  

