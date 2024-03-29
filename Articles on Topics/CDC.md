<h3> Change Data Capture </h3>

* It is a style of data movement. Usually good for capturing live changes to a database(real-time).

<h3> Types of CDC </h3>

* <h4> Query Based CDC </h4>

    * Here you query the data in the source to pick up changes . Usually need an update timestamp in data to pick up changes.

* <h4> Log Based CDC </h4>
    
    * When a new transaction comes into a database it gets logged into a log file with no impact on the source system.
      Which can then be picked up and moved from the log file.

![Alt Text](../Images/CDC_log_based.png)


* <h4> Trigger Based CDC </h4>

    * In this approach, you change the source application to trigger the write to a change table and then move it. This approach reduces database performance because it requires multiple writes each time a row is updated, inserted, or deleted.







<h3> Links </h3>

* Article - [CDC](https://www.qlik.com/us/change-data-capture/cdc-change-data-capture#:~:text=Change%20data%20capture%20(CDC)%20refers,a%20downstream%20process%20or%20system.)
* Article - [CDC](https://www.striim.com/blog/change-data-capture-cdc-what-it-is-and-how-it-works/)
* Article - [CDC using Debezium](https://www.startdataengineering.com/post/change-data-capture-using-debezium-kafka-and-pg/)
* Article - [CDC using Singer](https://www.startdataengineering.com/post/cdc-using-singer/)
