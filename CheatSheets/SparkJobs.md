# Spark Jobs
### Import spark manager
from neuro_python.neuro_compute import spark_manager as spm
### list jobs on default cluster
spm.list_jobs()
### list jobs on non default cluster
spm.list_jobs(cluster_id=‘xxxx-xxx…’)
### list runs of a job
spm.list_runs(job_id)
### list last 4 runs of a schedule
spm.list_runs(job_id,schedule_id=‘xxxx-…’,max_returned=4)
### define a import table
itable = spm.import_table(‘df1’,’DataStore’,’table_name’)
### define a export table
etable = spm.export_table(‘df2’,’DataStore’,’table_name’)
### define script parameter
param = spm.script_parameter(‘limit’,’10’)
### submit a job
script = spm.load_pyspark_notebook_to_str('notebookfilename.ipynb')</br>
job = spm.submit_job(‘Test’,</br>
	script,</br>
	import_tables=[itable],</br>
	export_tables=[etable],</br>
	script_parameters=[param])
### run a job with 5 rows
param = spm.script_parameter(‘limit’,’5’)</br>
spm.run_job(job[‘JobId’],’Test’,override_script_parameters=[param])
### run a schedule 6 minutes after the hour with 6 rows
param = spm.script_parameter(‘limit’,’6’)</br>
spm.run_schedule(job[‘JobId’],’Test’,’6 * * * *’,</br>
	override_script_parameters=[param])
### Crontab
https://crontab.guru/
