# Schema Manager

### Import schema manager module
from neuro_python.neuro_data import schema_manager as sm
### List tables in a data store
sm.list_tables("DataStoreName")
### Create a new table definition
cols=[sm.column_definition(‘Col1’,’DateTime’,column_type=‘TimeStampKey’),
sm.column_definition(‘Col2’,’Decimal(10,3)’),
sm.column_definition(‘Col3’,’Double’)]
table_def=sm.table_definition(cols,’TimeSeries’)
sm.create_table(‘DataStoreName’,’TableName’,table_def)
### Clone an existing table and change it's schema type to Processed
table_def=sm.get_table_definition(‘DataStoreName’,’TableName’)
table_def[‘SchemaType’]=2
sm.create_table(‘DataStoreName’,’ProcessedTableName’,table_def)
