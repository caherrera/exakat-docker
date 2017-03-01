time() and microtime() shouldn't be used to calculate duration or with durations. 

time() and microtime() are subject to variations, depending on system clock variations, such as daylight saving time difference (every spring and fall, one hour variation), or leap seconds, happening on June, 30th or december 31th, as announcec by IERS.

<?php

// Calculating tomorow, same hour, the wrong way
// tomorrow is not always in 86400s, especially in countries with daylight saving 
$tomorrow = time()  + 86400; 

// Good way to calculate tomorrow
$datetime = new DateTime('tomorrow');

?>

When the difference may be rounded to a larger time unit (rounding the difference to days, or several hours), the variation may be ignored safely.

When the difference is very small, it requires a better way to mesure time difference, such as ticks, ext/hrtime, or including a check on the actual time zone (ini_get() with 'date.timezone'). 
