[root@ip-172-31-31-148 cloudera-scm-server]# more cloudera-scm-server.log
2018-05-17 15:39:44,492 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding
=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/
cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryErro
r, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.13.3 (#6 built by jenkins on 201803
28-1830 git: f90c58536c252d70a23bde6d94514d92a1f111d4)



[root@ip-172-31-31-148 cloudera-scm-server]# cat cloudera-scm-server.log |grep 'Started Jetty server'
2018-05-17 15:40:51,565 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
