Those constants are defined in the code but never used. Defining unused constants will slow down the application, has they are executed and stored in PHP hashtables. 

It is recommended to comment them out, and only define them when it is necessary.