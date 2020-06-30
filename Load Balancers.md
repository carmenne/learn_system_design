### Load Balancers
Typically, the load balancer sits between the client and the server and distributes the traffic (load)
between multiple backend servers using various algorithm.

#### Layers where a load balancer can be added
- Between the user and the web server
- Between the web server and the application servers or cache servers (internal platforms layer)
- Between the internal platforms layer and database

#### Algorithms
Health Checks - Load balancers should only forward traffic to “healthy” backend servers. 
- Least Connection Method (LB redirects to the server with the fewest active connections)
- Least Response TIme Method (LB redirects to the server with the fewest active connections and the
least response time)
- Least Bandwith Method (LB redirects to the server with the least amount of traffic measured as
megabit per seconds - Mbps)
- Round Robin Method
- Weighted Round Robin Method
- IP Hash

Redundant Load Balancers (**A**ctive - **P**assive)
The load balancer can be a single point of failure; to overcome this, a second load balancer
can be connected to the first to form a cluster. Each LB monitors the health of the other and, 
since both of them are equally capable of serving traffic and failure detection, 
in the event the main load balancer fails, the second load balancer takes over.