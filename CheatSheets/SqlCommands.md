# Sql Commands
### Import sql commands
from neuro_python.neuro_data import sql_commands as sc
### select from table into dataframe named df
df = sc.run_sql(‘DataStoreName’,’select * from table_name’,return_df=True)
### select from table into dataframe named df
%%sql -sn DataStoreName -o df
select *
from table_name
### select from table and view result
%%sql -sn DataStoreName
select *
from table_name
### append dataframe into sql table
sc.df_to_sql(‘DataStoreName’,’table_name’,df)
