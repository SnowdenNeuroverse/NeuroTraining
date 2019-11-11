# Spark Magics
### Import spark manager
import neuro_python.neuro_compute.spark_manager as spm
### Create context on the default cluster (Remember to ensure the cluster is running)
spm.create_context(‘Lee’)
### Import delta table and view first 10 lines
#cell1</br>
%%spark_import_table</br>
import_table(‘df1’,’DownerRailDL’,’D3S_Training_9021_MaxTemp’)</br>

#cell2</br>
%%spark_sql</br>
Select *</br>
From df1</br>
Limit(10)
### Import delta table and view first 10 lines
#cell1</br>
%%spark_import_table</br>
import_table(‘df1’,’DownerRailDL’,’D3S_Training_9021_MaxTemp’)</br>

#cell2</br>
%%spark</br>
df2=df1.limit(10)</br>

#cell3</br>
%spark_pandas –df df2

