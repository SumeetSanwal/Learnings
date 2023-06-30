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

Eg : We have the following Transactional data : 
* 1, Sumeet, PI 
* 2, Praneeth, Online
* 3, Gokila,PI

In **row format** the data will be written in sequencial order in the disk blocks as:
1, Sumeet, PI, 2, Praneeth, Online, 3, Gokila,PI

In **columnar format** the data will be written in sequencial order in the disk blocks as:
1,2,3, Sumeet,Praneeth,Gokila, PI,Online,PI


<h3> Links </h3>

* Best Article - [Big Data File Formats and Comparison](https://www.upsolver.com/blog/the-file-format-fundamentals-of-big-data)
* Youtube - [Row vs Column DB](https://www.youtube.com/watch?v=uMkVi4SDLbM)
