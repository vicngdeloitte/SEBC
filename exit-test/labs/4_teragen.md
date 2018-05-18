# Challenge 4 - HDFS Testing


1. Teragen command output and time output:

[root@ip-172-31-23-103 ~]# time sudo -u groot hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Ddfs.blocksize=64m -Dmapreduce.map.memory.mb=1024 -Dmapred.map.tasks=40 50000000 /user/groot/tgen
18/05/18 05:18:42 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-20-123.ap-southeast-1.compute.internal/172.31.20.123:8032
18/05/18 05:18:42 INFO terasort.TeraGen: Generating 50000000 using 40
18/05/18 05:18:42 INFO mapreduce.JobSubmitter: number of splits:40
18/05/18 05:18:42 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/18 05:18:42 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526617757809_0003
18/05/18 05:18:43 INFO impl.YarnClientImpl: Submitted application application_1526617757809_0003
18/05/18 05:18:43 INFO mapreduce.Job: The url to track the job: http://ip-172-31-20-123.ap-southeast-1.compute.internal:8088/proxy/application_1526617757809_0003/
18/05/18 05:18:43 INFO mapreduce.Job: Running job: job_1526617757809_0003
18/05/18 05:18:49 INFO mapreduce.Job: Job job_1526617757809_0003 running in uber mode : false
18/05/18 05:18:49 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:18:56 INFO mapreduce.Job:  map 3% reduce 0%
18/05/18 05:18:57 INFO mapreduce.Job:  map 8% reduce 0%
18/05/18 05:18:59 INFO mapreduce.Job:  map 13% reduce 0%
18/05/18 05:19:02 INFO mapreduce.Job:  map 15% reduce 0%
18/05/18 05:19:03 INFO mapreduce.Job:  map 17% reduce 0%
18/05/18 05:19:04 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 05:19:07 INFO mapreduce.Job:  map 22% reduce 0%
18/05/18 05:19:08 INFO mapreduce.Job:  map 28% reduce 0%
18/05/18 05:19:09 INFO mapreduce.Job:  map 30% reduce 0%
18/05/18 05:19:11 INFO mapreduce.Job:  map 32% reduce 0%
18/05/18 05:19:16 INFO mapreduce.Job:  map 38% reduce 0%
18/05/18 05:19:21 INFO mapreduce.Job:  map 40% reduce 0%
18/05/18 05:19:22 INFO mapreduce.Job:  map 47% reduce 0%
18/05/18 05:19:28 INFO mapreduce.Job:  map 50% reduce 0%
18/05/18 05:19:32 INFO mapreduce.Job:  map 52% reduce 0%
18/05/18 05:19:33 INFO mapreduce.Job:  map 57% reduce 0%
18/05/18 05:19:34 INFO mapreduce.Job:  map 63% reduce 0%
18/05/18 05:19:39 INFO mapreduce.Job:  map 65% reduce 0%
18/05/18 05:19:43 INFO mapreduce.Job:  map 68% reduce 0%
18/05/18 05:19:45 INFO mapreduce.Job:  map 73% reduce 0%
18/05/18 05:19:48 INFO mapreduce.Job:  map 75% reduce 0%
18/05/18 05:19:53 INFO mapreduce.Job:  map 82% reduce 0%
18/05/18 05:19:54 INFO mapreduce.Job:  map 85% reduce 0%
18/05/18 05:19:55 INFO mapreduce.Job:  map 88% reduce 0%
18/05/18 05:20:00 INFO mapreduce.Job:  map 93% reduce 0%
18/05/18 05:20:01 INFO mapreduce.Job:  map 95% reduce 0%
18/05/18 05:20:02 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 05:20:02 INFO mapreduce.Job: Job job_1526617757809_0003 completed successfully
18/05/18 05:20:03 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=5121190
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=3423
                HDFS: Number of bytes written=5000000000
                HDFS: Number of read operations=160
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=80
        Job Counters
                Launched map tasks=40
                Other local map tasks=40
                Total time spent by all maps in occupied slots (ms)=318589
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=318589
                Total vcore-milliseconds taken by all map tasks=318589
                Total megabyte-milliseconds taken by all map tasks=326235136
        Map-Reduce Framework
                Map input records=50000000
                Map output records=50000000
                Input split bytes=3423
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=3421
                CPU time spent (ms)=180520
                Physical memory (bytes) snapshot=14019469312
                Virtual memory (bytes) snapshot=63270383616
                Total committed heap usage (bytes)=17865113600
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=107387891658806101
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5000000000

real    1m23.334s
user    0m5.784s
sys     0m0.339s
[root@ip-172-31-23-103 ~]#



2. hdfs dfs -ls /user/groot/tgen


[root@ip-172-31-23-103 ~]# hdfs dfs -ls /user/groot/tgen
Found 41 items
-rw-r--r--   3 groot avengers          0 2018-05-18 05:20 /user/groot/tgen/_SUCCESS
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:18 /user/groot/tgen/part-m-00000
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:18 /user/groot/tgen/part-m-00001
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:18 /user/groot/tgen/part-m-00002
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:18 /user/groot/tgen/part-m-00003
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:18 /user/groot/tgen/part-m-00004
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00005
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00006
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00007
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00008
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00009
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00010
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00011
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00012
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00013
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00014
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00015
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00016
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00017
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00018
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00019
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00020
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00021
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00022
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00023
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00024
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00025
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00026
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00027
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00028
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00029
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00030
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00031
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00032
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00033
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00034
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:20 /user/groot/tgen/part-m-00035
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:20 /user/groot/tgen/part-m-00036
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00037
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:19 /user/groot/tgen/part-m-00038
-rw-r--r--   3 groot avengers  125000000 2018-05-18 05:20 /user/groot/tgen/part-m-00039
[root@ip-172-31-23-103 ~]#




3.hadoop fsck -blocks /user/groot


[root@ip-172-31-23-103 ~]# sudo -u hdfs hadoop fsck -blocks /user/groot
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-20-123.ap-southeast-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.23.103 for path /user/groot at Fri May 18 05:22:45 UTC 2018
.....................................................................................Status: HEALTHY
 Total size:    10000100000 B
 Total dirs:    9
 Total files:   85
 Total symlinks:                0
 Total blocks (validated):      162 (avg. block size 61729012 B)
 Minimally replicated blocks:   162 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri May 18 05:22:45 UTC 2018 in 17 milliseconds


The filesystem under path '/user/groot' is HEALTHY
[root@ip-172-31-23-103 ~]#
