The try...catch structure uses some variables that also in use in this scope. In case of a caught exception, the exception will be put in the catch variable, and overwrite the current value, loosing some data.

It is recommended to use another name for these catch variables.