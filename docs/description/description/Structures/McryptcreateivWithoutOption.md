mcrypt_create_iv used to have MCRYPT_DEV_RANDOM as default values, and in PHP 5.6, it now uses MCRYPT_DEV_URANDOM.

If the code doesn't have a second argument, it relies on the default value. It is recommended to set explicitely the value, so has to avoid problems while migrating.