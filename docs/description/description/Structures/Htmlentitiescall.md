htmlentities() and htmlspecialchars() are used to prevent injecting special characters in HTML code. As a bare minimum, they take a string and encode it for HTML.

The second argument of the functions is the type of protection. The protection may apply to quotes or not, to HTML4 or 5, etc. It is highly recommended to set it explicitely.

The third argument of the functions is the encoding of the string. In PHP 5.3, it as 'ISO-8859-1', in 5.4, was 'UTF-8', and in 5.6, it is now default_charset, a php.ini configuration that has the default value of 'UTF-8'. It is highly recommended to set this argument too, to avoid distortions from the configuration.

Also, note that arguments 2 and 3 are constants and string (respectively), and should be issued from the list of values available in the manual. Other values than those will make PHP use the default values. 
