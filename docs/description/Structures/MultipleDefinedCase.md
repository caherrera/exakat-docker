Some cases are defined multiple times, but only one will be processed. Check the list of cases, and remove the extra one.

Exakat tries to find the value of the case as much as possible, and ignore any dynamic cases (using variables).

<?php

case ($x) {
    case 1 : 
        break;
    case true:    // This is a duplicate of the previous
        break; 
    case 1 + 0:   // This is a duplicate of the previous
        break; 
    case 1.0 :    // This is a duplicate of the previous
        break; 
    case $y  :    // This is not reported.
        break; 
    default:
        
}
?>
