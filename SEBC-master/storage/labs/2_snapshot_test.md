1- Create "precious" directory
    #hdfs dfs -mkdir -p /precious
2-Allowing creation of snapshots:
    # hdfs dfsadmin -allowSnapshot  /precious
3-Copying the required file to precious:
     #hdfs dfs -put /tmp/SEBC.zip /precious
4-Creating a Snapshot
Take snaphot usingn the GUI interface
