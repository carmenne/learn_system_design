### Key Characteristics of Distributed Systems
#### Reliability
For the whole distributed system: the capability of the whole system to be able to service the user even if
one component is failing.
#### Availability
The time a system remains operational to perform its function (often measured as percentage).
A reliable system is also available, but an available system is not necessarily available.

##### Example
Let’s take the example of an online retail store that has 99.99% availability for the first 
two years after its launch. However, the system was launched without any information security testing.
The customers are happy with the system, but they don’t realize that it isn’t very reliable as 
it is vulnerable to likely risks. In the third year, the system experiences a series of
 information security incidents that suddenly result in extremely low availability 
 for extended periods of time. This results in reputational and financial damage to the customers.

#### Scalability
The system should be designed so that it can handle increased load in such a way that performance 
is not lost
(ven load distribution amongst the nodes should be achieved)
- Vertical scaling (add more CPU, RAM, storage)
- Horizontal scaling (add more machines)
#### Serviceability or Manageability (maintainability)
The ease of diagnosing and understanding problems when they occur.
The ease of making updates or modifications.
The ease of operating the system (does it routinely operates without errors and/or failures).
#### Efficiency
Two standard measures of its efficiency are the response time (or latency) that denotes
the delay to obtain the first item and the throughput (or bandwidth) which denotes 
the number of items delivered in a given time unit.