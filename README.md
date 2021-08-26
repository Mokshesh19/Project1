# PROJECT1

## Project Description

To implement a data warehouse system using Apache Hive built on top of Apache Hadoop for providing data query and analysis.

## Technologies Used

* Hortonworks Data Platform - version 2.6.5
* Apache Hive - version 1.2
* Sqoop - version 1.4.6
* MySql - version 14.14
* Git - version 1.8.3.1

## Features

List of features ready and TODOs for future development
* Used various joins and partitions to optimize query processing
* Includes multiple import methods for the data onto the Hive 
* Queries are written in a common SELECT,FROM,WHERE format similar to many database management systems which make them easier to read understand

To-do list:
* To include Bucketing
* Importing data from MySql creates some descripencies in data, which requires a fix

## Getting Started
  
## Prerequisites
A hadoop ecosytem with its components 
- HDFS
- YARN
- AMBARI
- Sqoop
- Hive
- MySql
# Hardware requirements:
- Cpu with 4 or more logical cores
- Atleast 12gb of ram
- Storage like Hard disk or SSD with atleast 50-60GB of space

## Usage

#Steps to be followed:
-Login onto the VM using ssh command give your domain name and password
```
ssh username@sandbox-hdp.hortonworks.com -p 2222
```
- Clone the repository on the Local VM using the following command 
```
$ git clone https://github.com/Mokshesh19/Project1.git
```
Once cloned it can be any changes to the repositry can be replicated by doing a pull  
```
$ git pull
```
- Push the data onto the hdfs file system by giving the right path and file name
```
hdfs dfs -put <filename>
```
- Then the data can be loaded onto the HIVE data warehouse system using either the GUI present in AMBARI in the HIVE section or through CLI using the command
```
LOAD DATA INPATH <PATH>
```
> ensure the data being loaded from the csv file does not have a header, if it does delete the header and create tables on hive and then import the data

- Once the data is loaded the quries present in the tasks.txt can be run in the format
```
SELECT <column_name> FROM <Table_name> WHERE <conditions>
```

