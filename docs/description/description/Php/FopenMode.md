fopen has a few modes, as described in the documentation : 'r', 'r+', for reading;  'w', 'w+' for writing; 'a', 'a+' for appending; 'x', 'x+' for modifying; 'c', 'c+' for writing and locking, 't' for text files and windows only.
An optional 'b' may be used to make the fopen() call more portable and binary safe. 

Any other values are not understood by PHP. 