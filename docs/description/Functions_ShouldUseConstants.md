The following functions have related constants that should be used as arguments, instead of scalar literals, such as integers or strings.

For example, $lines = file('file.txt', 2); is less readable than $lines = file('file.txt', FILE_IGNORE_NEW_LINES)