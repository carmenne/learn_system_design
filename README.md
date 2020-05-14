### Partitioning in general
Partitioning = the technique of breaking up a big DB in smaller parts across multiple machines in order to improve manageability, performance (scalability), availability and load balancing. 

Justification: After a certain scale point, it is more efficient (and cheaper) to scale horizontally (by adding more machines) than vertically.

### Partitioning methods
The following partitioning methods exist:

#### Horizontal partitioning (Data Sharding, range based partitioning)
Refers to put different rows in different tables  (e.g. zipcodes).

Issue: if the key used for partitioning is not chosen carefully, it can lead to unbalanced servers. 

#### Vertical Partitioning
Partition based on feature (tables representing different features are on different machines, e.g. Instagram like application may chose to place user profiles on one server and photos on a different server)

#### Directory Based Partitioning
This is a loosely coupled approach that creates lookup services that abstracts the partitioning key from the DB access code. This means that tasks like adding servers to the DB pool or changing the partitioning scheme does not impact the application)

### Partitioning criterias:
Key-based partitioning
ID % 100 will distribute the entry based on the ID on the ID % 100th server. 

The issue with this approach is that the number of servers used for partitioning is fixed.

#### List partitioning
The partitioning criteria is kept in a list. For instance all the entries for countries like Denmark, Norway, Sweden can go to Nordic Countries list. The list is consulted before for finding out to which server the entry should be forwarded.

#### Round-robin partitioning
This sends the entries in a round robin fashion (n mod i)

The advantage is that it leads to balanced loads.

#### Composite partitioning
A combination of the above criterias: list + hashing.

#### Consistent hashing

### Commons problems of partitioning
#### Joins and denormalizations

#### Referential integrity

#### Rebalancing

