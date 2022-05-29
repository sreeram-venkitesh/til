## Installing extensions in your postgres server

Recently in work I was given a set of DDLs to create tables from. Some of the tables in these DDLs involved using the `uuid_generate_v4()` function. At first I got an error saying that the function was not installed and after some googling, I found out this command, with which I was able to install it

```sql
CREATE EXTENSION IF NOT EXISTS "uuid-ossp";
``` 
I was able to run all the CREATE TABLE commands with this. Everything's good. I thought that I knew everything that I needed to know about postgres extensions and how to install them.

The next day I had to walk my friend through the same process so that she can get the same data loaded in her local postgres as well. I told her that we need to install the extension first and then we can run the CREATE TABLE commands. We tried doing all this but we were still getting the same error, saying that `uuid_generate_v4()` was not found. Thanks to the sharp eye of my friend, she figured out that the function was not installed in the database that we were working with. It was installed in the default user database since we ran the CREATE EXTENSION command right after getting into psql and we hadn't `\c`'d into the database that we were working with. She was able to see the list of all the functions that are installed in each database from pgAdmin as well.

