Starting at PHP 5.6, $HTTP_RAW_POST_DATA is deprecated, and should be replaced by php://input. You may get ready by setting always_populate_raw_post_data to -1.

<?php

// PHP 5.5 and older
$postdata = $HTTP_RAW_POST_DATA;

// PHP 5.6 and more recent
$postdata = file_get_contents(php://input);

?>

