The name of your postgresql schema can include letters, digits and underscores (_). 

I came across this error while copying data to postgres via [Airbyte](https://airbyte.io) and when my sync failed because I had given a schema name with hyphens in it from Airbyte.
