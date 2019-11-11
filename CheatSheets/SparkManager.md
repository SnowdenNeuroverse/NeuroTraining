# Manage clusters for spark
### import spark manager module
from neuro_python.neuro_compute import spark_manager as spm
### List clusters
spm.list_clusters()
### Start default cluster
spm.start_cluster()
### Start non default cluster
spm.start_cluster(cluster_id='xxxx-xx...')
### List python libraries on default cluster
spm.list_libraries()
### Install python library on default cluster
spm.install_library('LibraryName','LibraryVersion')
### Upgrade python library on default cluster
spm.upgrade_library('LibraryName','LibraryVersion')
### Uninstall python library on default cluster
spm.uninstall_library('LibraryName','LibraryVersion')
