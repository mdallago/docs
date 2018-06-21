We've replaced the original database system of Libbitcoin with an alternative SQLite implementation, instead of original hashtable.
It’s primitive because it’s not optimized yet to perform as well as the hashtable.  This [branch]( https://github.com/bitprim/bitprim-database/tree/sqlite) acts as a guide to developers if they want to change the Bitprim’s storage method. 
The change from the hashtable to SQL allows users with less computer specs to be able to run our software and still perform correctly.
