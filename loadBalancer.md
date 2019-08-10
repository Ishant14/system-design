## Load Balancer 

A load balancer is a device that distributes network or application traffic across a cluster of servers. Load balancing improves responsiveness and increases availability of applications.

A load balancer sits between the client and the server farm accepting incoming network and application traffic and distributing the traffic across multiple backend servers using various methods. By balancing application requests across multiple servers, a load balancer reduces individual server load and prevents any one application server from becoming a single point of failure, thus improving overall application availability and responsiveness.

> Load balancing is the most straightforward method of scaling out an application server infrastructure. As application demand increases, new servers can be easily added to the resource pool, and the load balancer will immediately begin sending traffic to the new server.

## Types of Load Balancer : 

1. **Hardware LoadBalancer** : 
   - They are hardware which work as a load balancer, but they are very expensive. 
 
2. **Software LoadBalancer** : 
- Its a hybrid approach. HAProxy is a popular software load balacer.
- Every client request on the port(where HAProxy is running) will be recieved by the proxy and then passed to the backened server efficiently.
- HAproxy manages health checks, will add or remove machines to those pools.
                
## Load Balancer Algorithm         
        
1. **The Least Connection Method**
- The default method, when a virtual server is configured to use the least connection, it selects the service with the fewest active connections.

2. **The Round Robin Method**
- This method continuously rotates a list of services that are attached to it. When the virtual server receives a request, it assigns the connection to the first service in the list, and then moves that service to the bottom of the list.

3. **The Least Response Time Method**
- This method selects the service with the fewest active connections and the lowest average response time.

4. **The Least Bandwidth Method** 
- This method selects the service that is currently serving the least amount of traffic, measured in megabits per second (Mbps).

5. **The Least Packets Method** 
- This method selects the service that has received the fewest packets over a specified period of time.

6. **The Custom Load Method**
- When using this method, the load balancing appliance chooses a service that is not handling any active transactions. If all of the services in the load balancing setup are handling active transactions, the appliance selects the service with the smallest load.
