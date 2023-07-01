<h3> Row vs Columnar Format </h3>

<h4> Row Format </h4>

* Write Intensive - i.e faster write operations
* Slow Read
* Compression inefficient
* OLTP


<h4> Column Format </h4>

* Read Intensive - i.e faster read operations
* Slow Write 
* Good compression : In columnar format we can achieve great compression as similar datatype objects are stored together.  
* OLAP



<h3> Internal Working in of ROW & COLUMNAR DB </h3>

* Let's consider that data is written into a hdd by these databases on a usual basis.
With each hdd containing several blocks on which the actual data is written and read from. 

* In case of a row based db, the complete transactional data is written in sequential manner on each block and once the blocks gets filled
the writing head moves to the next block. 
* In case on columnar db, the complete column is written into the block and once the column is completed the next column is written in sequential manner.

Eg : We have the following Transactional data : 
* 1, Sumeet, PI 
* 2, Praneeth, Online
* 3, Gokila,PI

In **row format** the data will be written in sequencial order in the disk blocks as:
1, Sumeet, PI, 2, Praneeth, Online, 3, Gokila,PI

In **columnar format** the data will be written in sequencial order in the disk blocks as:
1,2,3, Sumeet,Praneeth,Gokila, PI,Online,PI


Case scenarios :
1. SELECT * FROM X where id='a';
   1. In case on row based db, the best case scenarios would be **one I/O** operations where the record is found on first block and all columns are fetched as row based have complete transaction together. Worst case scenarios would be n I/O operations considering the record was on last block and sequentially all blocks were read before it was found.
   2. In case on columnar db, the best case scenarios would be **n I/O** operations, considering each column to be on a different block to get all column for the record n I/O operation would be needed, that why doing a select * on columnar db is not recommended. In this worst case would be same as best case i.e n I/O operations.
2. SELECT SUM(sal) from X;
   1. In case on row based db, the best case scenarios would be **n I/O** operations as all records are to be scanned and the sal value has to be extracted from each record to do the aggregation. Worst case is same as best case here.
   2. In case on columnar db, the best case scenarios would be **1 I/O** operations, considering each column to be on a different block and occuping just 1 block, to get all records for column 'sal' only 1 I/O operation would be needed. In this worst case would be still less than n I/O operations as max blocks that would needed to be read is equal to blocks occupied by records for col 'sal'.


<h3> Links </h3>

* Best Article - [Big Data File Formats and Comparison](https://www.upsolver.com/blog/the-file-format-fundamentals-of-big-data)
* Youtube - [Row vs Column DB](https://www.youtube.com/watch?v=uMkVi4SDLbM)
