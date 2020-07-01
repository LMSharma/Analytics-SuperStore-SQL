## SQL for Data Analysis

[superstoreDump.sql](https://github.com/LMSharma/Analytics-SQL/blob/master/superstoreDump.sql) containes data in the normalized form.

Original Data Set : [Superstore Dataset on Tableau](https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls?language=en_US)

I have to remove some of the rows in order to mantain ACID properties. Dump was taken using [PostgreSQL](https://www.postgresql.org) .
Mentioned questions are based on analytical purpose from Basics to Advanced level.

## PostgreSQL Installation
For Postgres Setup follow the links:
* [Ubuntu](https://www.howtoforge.com/how-to-install-postgresql-and-pgadmin4-on-ubuntu-1804-lts/)
* [Windows](https://www.postgresql.org/download/windows/)

## Usage
How to restore .sql dump [Restore dump file](https://o7planning.org/en/11913/backup-and-restore-postgres-database-with-pgadmin)
You can use .sql instead of .backup file as shown in the link.

### DB_Schema
![SuperStore Data Database schema](https://github.com/LMSharma/SQL/raw/master/Superstore_data_db_schema.png)


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.
