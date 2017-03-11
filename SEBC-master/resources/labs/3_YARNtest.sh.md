#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hadoop-mapreduce
HADOOP=/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 8    
do
   # Reducer containers
   for j in 1 
   do                 
      # Container memory
      for k in 512 1024 
      do                         
         # Set mapper JVM heap 
         MAP_MB=`echo "($k*0.8)/1" | bc` 

         # Set reducer JVM heap 
         RED_MB=`echo "($k*0.8)/1" | bc` 

      time ${HADOOP}/hadoop jar ${MR}/hadoop-mapreduce-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     51200000 /tmp/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
 
       time ${HADOOP}/hadoop jar ${MR}/hadoop-mapreduce-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
	             /tmp/tg-10GB-${i}-${j}-${k}  \
                     /tmp/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err                        

        $HADOOP/hadoop dfs -rm -r -skipTrash /tmp/tg-10GB-${i}-${j}-${k}                         
        $HADOOP/hadoop dfs -rm -r -skipTrash /tmp/ts-10GB-${i}-${j}-${k}                 
      done
   done
done

echo Testing loop ended on `date`
 
