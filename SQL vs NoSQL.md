#### Relational databases
RDBMSs represent data in tabular form: entities are mapped to tables 
that have relationships between them expressed via foreign keys. 
In order to put all the needed data together, JOIN statements are performed. 
The more normalized the data, the higher the number of JOINs is required.
#### NoSQL
NoSQL are not structured into tables linked via foreign keys. 
They can be represented in tables (Cassandra), documents (mongoDB), or key-value (others) 
and they store the linked entities together allowing for redundancy, 
however optimizing for fast-reads.

#### Comparison
##### ACID
RDBMSs are ACID, NoSQL are BASE.
when it comes to data reliability and safe guarantee 
of performing transactions, SQL databases are still the better bet.
##### Schema
Relational databases have a fixed schema and structured data, while noSql have dynamic
schema and unstructured data.
##### Scalability
Scalability: In most common situations, SQL databases are vertically scalable, 
i.e., by increasing the horsepower (higher Memory, CPU, etc.) of the hardware, 
which can get very expensive. 
It is possible to scale a relational database across multiple servers, 
but this is a challenging and time-consuming process.
On the other hand, NoSQL databases are horizontally scalable, 
meaning we can add more servers easily in our NoSQL database infrastructure 
to handle a lot of traffic. Any cheap commodity hardware or cloud instances 
can host NoSQL databases, thus making it a lot more cost-effective than vertical scaling. 
A lot of NoSQL technologies also distribute data across servers automatically.
##### Querying
SQL has a standardized language for querying the database irrespective of implementation, 
while NoSQL database have their own proprietary query languages (UnQL).

#### SQL VS. NoSQL - Which one to use?

##### Relational Databases
- We need to ensure ACID compliance. ACID compliance reduces anomalies and 
protects the integrity of your database by prescribing exactly how 
transactions interact with the database. 
Generally, NoSQL databases sacrifice ACID compliance for scalability and processing speed, 
but for many e-commerce and financial applications, 
an ACID-compliant database remains the preferred option.
- Your data is structured and unchanging. If your business is not experiencing 
massive growth that would require more servers and if you’re only working with data 
that is consistent, then there may be no reason to use a system designed to support 
a variety of data types and high traffic volume.

##### NoSQL
- Data has little or no structure (With document-based databases, 
you can store data in one place without having to define what “types” of data 
those are in advance.)
- Cloud-based storage is an excellent cost-saving solution but requires data to be
easily spread across multiple servers to scale up. 
Using commodity (affordable, smaller) hardware on-site or in the cloud saves you the hassle
of additional software and NoSQL databases like Cassandra are designed to be scaled
across multiple data centers out of the box, without a lot of headaches.
- Rapid development. NoSQL is extremely useful for rapid development 
as it doesn’t need to be prepped ahead of time. If you’re working on quick iterations of 
your system which require making frequent updates to the data structure without 
a lot of downtime between versions, a relational database will slow you down.