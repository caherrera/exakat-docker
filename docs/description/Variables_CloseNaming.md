The following variables's name are very close and may lead to confusion.

Variables are 3 letters long (at least). Variables names build with an extra 's' are omitted.
Variables may be scattered across the code, or close to each other. 

<?php

    // Variable names with one letter difference
    $fWScale = 1;
    $fHScale = 1;
    $fScale = 2;
    
    $oFrame = 3;
    $iFrame = new Foo();
    
    $v2_norm = array();
    $v1_norm = 'string';
    
    $exept11 = 1;
    $exept10 = 2;
    $exept8 = 3;
    
    // This even looks like a typo
    $privileges  = 1;
    $privilieges = true;
    
    // This is not reported : Adding extra s is tolerated.
    $rows[] = $row;
    
?>

