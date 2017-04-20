How to use: 
Mammoth is a memory-centric MapReduce based on hadoop-1.0.1 aiming to solve the problem of I/O bottleneck in 
data-intensive applications. About how to use hadoop, you can refer to its homepage: http://hadoop.apache.org/. 
In the following part of this document, we assume you are familiar with hadoop.
You can just replace the "hadoop-core-1.0.1.jar" under $HADOOP_HOME with the compiled "hadoop-core-1.0.1-mammoth-0.9.0.jar".
After that you can use mammoth just in the same way with original hadoop.
Mammoth is developed with 64-bit jdk7, and you are suggested to use the same.
You must specify the child jvm options before running your job, eg:
<property>
   <name>mapred.job.child.java.opts</name>
   <value>-d64 -Xmx8000M -Xms8000M</value>
</property>
This parameter is the only one required to be manually specified because Mammoth can maximize the usage of memory 
in runtime using a rule-based heuristic. You can learn more about the Mammoth on the following page: 
http://grid.hust.edu.cn/xhshi/projects/mammoth.htm.

The technical paper about Mammoth has been published in IEEE Transactions on Parallel and Distributed systems, which has been recommended as Spotlight of Transactions in IEEE Computer. More information are as follows:

Xuanhua Shi, Ming Chen, Ligang He, Xu Xie, Lu Lu, Hai Jin, Yong Chen, and Song Wu, "Mammoth: Gearing Hadoop Towards Memory-Intensive MapReduce Applications", IEEE Transactions on Parallel and Distributed Systems, 26(8):2300-2315, 2015.

Hai Jin, "When Data Grows Big", Computer, 2014
