Connect to postgres - setup postgres server
## Create New Database --> create database <db_name>;
## Create New User --> create user <db_user_name> with password '<user_password>';
## Grant permissions to the user --> grant all privileges on database <db_name> to <db_user_name>;
## Alter permission for user --> ALTER user <db_user_name> CREATEDB;

List all databases - \l
List all roles - \du

## Create dump for posgres export 

Create dump using pg_dump -h <localhost> -p <port> -U <username> --format=c <database_name> > ibdb.dump   
drop ib_db (Because I already had a database created)  
pg_restore -C -d postgres ibdb.dump  
Link https://www.postgresql.org/docs/9.2/app-pgrestore.html   
  
  
