Those brackets have no use here. 

They may be a left over of an old instruction, or a misunderstanding of the alternative syntax.

<?php

// The following brackets are useless : they are a leftover from an older instruction
// if (DEBUG) 
{
    $a = 1;
}

// Here, the extra brackets are useless
for($a = 2; $a < 5; $a++) : {
    $b++;
} endfor;

?>
