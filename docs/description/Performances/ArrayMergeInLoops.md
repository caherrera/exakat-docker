array_merge() is memory intensive : every call will duplicate the arguments in memory, before merging them. 

Since arrays may be quite big, it is recommended to avoid using array_merge() in a loop. Instead, one should use array_merge() with as many arguments as possible, making the merge a on time call.

<?php

// Creating a large multidimensional array
$source = ['a' => ['a', 'b', /*...*/],
           'b' => ['b', 'c', 'd', /*...*/],
           /*...*/
           ];

// Slow way
$b = array();
foreach($source as $key => $values) {
    $b = array_merge($b, $values);
}

// Faster way
$b = array();
foreach($source as $key => $values) {
    //Collect in an array
    $b[] = $values;
}
// One call to array_merge
$b = call_user_func_array('array_merge', $b);
// or with variadic
$b = call_user_func('array_merge', ..$b);

// Fastest way (with above example, without checking nor data pulling)
$b = call_user_func_array('array_merge', array_values($source))
// or
$b = call_user_func('array_merge', ...array_values($source))

?>

Note that array_merge_recursive() and file_put_contents() are also affected and reported.
