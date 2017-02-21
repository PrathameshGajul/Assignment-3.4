Q1.Explain the importance of Namenode in Hadoop cluster.
Ans:
-The NameNode is the focus point of an HDFS file system.
-It keeps the directory tree of all files in the file system and tracks the file data where across the cluster is kept.
-It does not store the data of these files by itself.
-Client applications talk to the NameNode whenever they wish to locate a file, or when they want to add/copy/move/delete a file.
-The NameNode responds the successful requests by returning a list of relevant DataNode servers where the data lives.
-The NameNode is a Single Point of Failure for the HDFS Cluster.
-HDFS is not currently a High Availability system.
-When the NameNode goes down, the file system goes offline.
-There is an optional SecondaryNameNode that can be hosted on a separate machine.
-It only creates checkpoints of the namespace by merging the edits file into the fsimage file and does not provide any real redundancy.
-It is essential to look after the NameNode. Here are some recommendations:
   -Use a good server with lots of RAM. The more RAM you have, the bigger the file system, or the smaller the block size.
   -Use ECC RAM.
   -List more than one name node directory in the configuration, so that multiple copies of the file system meta-data will be stored.As long as the directories are on separate disks, a single disk failure will not corrupt the meta-data.
   -Configure the NameNode to store one set of transaction logs on a separate disk from the image.
   -Configure the NameNode to store another set of transaction logs to a network mounted disk.
   -Monitor the disk space available to the NameNode. If free space is getting low, add more storage.
   -Do not host DataNode, JobTracker or TaskTracker services on the same system.
  
  
  Q2.Practice the beginners commands for HDFS from the below link
     https://acadgild.com/blog/hdfs-commands-for-beginners/
     Share the screenshot of the commands used.
     
  Ans:Screenshots Attached.
