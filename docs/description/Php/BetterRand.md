rand() and mt_rand() should be replaced with random_int().

At worse, rand() should be replaced with mt_rand(), which is a drop-in replacement and srand() by mt_srand(). 

random_int() replaces rand(), and has no seeding function like srand().

<?php

// Avoid using this
$random = rand(0, 10);

// Drop-in replacement
$random = mt_rand(0, 10);

// Even better but different : 
// valid with PHP 7.0+
try {
    $random = random_int(0, 10);
} catch (\Exception $e) {
    // process case of not enoug random values
}


?>

Since PHP 7, random_int() along with random_bytes(), provides cryptographically secure pseudo-random bytes, which are good to be used
when security is involved. openssl_random_pseudo_bytes() may be used when the OpenSSL extension is available.