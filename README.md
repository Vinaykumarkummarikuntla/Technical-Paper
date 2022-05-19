# Load Balancers

####  Load balancing

Load balancing is about troubleshooting the distribution of inbound network and application traffic across multiple servers. With hundreds of user (or client) requests coming in every minute, it’s hard for any one server to keep up and continually display high-quality photos, videos, text, and application data at the speed at which many users have become accustomed.

### 1. About  Load Balancers

**1.1 Understanding the functions of load balancers**

In general, a Load Balancer acts as a ‘traffic controller’ for your server and directs the requests to an available one, capable of fulfilling the request efficiently. This ensures that requests are responded to fast and no server is over-stressed to degrade the performance.

In an organization’s attempt to meet the application demands, Load Balancer assists in deciding which server can efficiently handle the requests. This creates a better user experience.

By helping servers move data efficiently, information flow between the server and endpoint device is also managed by the load balancer. It also assesses the request-handling health of the server, and if necessary, Load Balancer removes the unhealthy server until it is restored.

As the servers can also be physical or virtual, a load balancer can also be a hardware appliance or a software-based virtual one. When a server goes down, the requests are directed to the remaining servers and when a new server gets added, the requests automatically start getting transferred to it.

**2.2 Types of Load Balancers – Based on Functions**

Several load balancing techniques are there for addressing the specific network issues:

* Network Load Balancer / Layer 4 (L4) Load Balancer:
* Application Load Balancer / Layer 7 (L7) Load Balancer:
* Global Server Load Balancer/Multi-site Load Balancer:
  
##### 2.3 Types of Load Balancers – Based on Configurations

* Hardware Load Balancers
* Software Load Balancers
* Virtual Load Balancers
  
#### 3.Benefits of Load Balancers

**1.**Enhanced Performance:****

Load Balancers reduce the additional load on a particular server and ensures seamless operations and response, giving the clients a better experience.

**2.**Resilience:****

The failed and under-performing components can be substituted immediately and giving information about which equipment needs service, with nil or negligible downtime.

**3. Security:**

Without any change in any form, Load Balancer gives an additional layer of security to your website and applications.

# Scalibility

The scalability of an application can be measured by the number of requests it can effectively support simultaneously. The point at which an application can no longer handle additional requests effectively is the limit of its scalability. This limit is reached when a critical hardware resource runs out, requiring different or more machines. Scaling these resources can include any combination of adjustments to CPU and physical memory (different or more machines), hard disk (bigger hard drives, less “live” data, solid state drives), and/or the network bandwidth (multiple network interface controllers, bigger NICs, fiber, etc.).

![this is the Image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210209202449/Scaling-Concept.png)

**1. Vertical Scaling**

In simple terms upgrading the capacity of a single machine or moving to a new machine with more power is called vertical scaling. You can add more powers to your machine by adding better processors, increasing RAM, or other power increasing adjustments. Vertical scaling can be easily achieved by switching from small to bigger machines but remember that this involves downtime. You can enhance the capability of your server without manipulating your code.

* This approach is also referred to as the ‘scale-up‘ approach.
* It doesn’t require any partitioning of data and all the traffic resides on a single node with more capacity.
* Easy implementation.
* Less administrative efforts as you need to manage just one system.
* Application compatibility is maintained.
* Mostly used in small and mid-sized companies.
* MySQL and Amazon RDS is a good example of vertical scaling.

 **Drawbacks**

* Limited Scaling.
* Limited potential for improving network I/O or disk I/O.
* Replacing the server will require downtime in this approach.
* Greater risk of outages and hardware failures.
* Finite scope of upgradeability in the future.
* Implementation cost is expensive.
  
**2. Horizontal Scaling**

This approach is the best solution for projects which have requirements for high availability or failover. In horizontal scaling, we enhance the performance of the server by adding more machines to the network, sharing the processing and memory workload across multiple devices. We simply add more instances of the server to the existing pool of servers and distribute the load among these servers. In this approach, there is no need to change the capacity of the server or replace the server. Also, like vertical scaling, there is no downtime while adding more servers to the network. Most organizations choose this approach because it includes increasing I/O concurrency, reducing the load on existing nodes, and increasing disk capacity.

* This approach is also referred to as the ‘scale-out’ approach.
* Horizontal scalability can be achieved with the help of a distributed file system, clustering, and load–balancing.
* Traffic can be managed effectively.
* Easier to run fault-tolerance.
* Easy to upgrade
* Instant and continuous availability.
* Easy to size and resize properly to your needs.
* Implementation cost is less expensive compared to scaling-up Google with its Gmail and YouTube, Yahoo, Facebook, eBay, Amazon, etc. are heavily utilizing horizontal scaling.

**Drawbacks**

* Complicated architectural design
* High licensing fees
* High utility costs such (cooling and electricity)
* The requirement of extra networking equipment such as routers and switches.

### Comparison between Horizontal and Vertical

|  Horizontal Scaling| Vertical Scaling|
| --- | ---|
|  Load balancing required | Load balancing not required
|Utilizes Network Calls | Interprocess communication |
|Data inconsistency |Data consistent|
|Scales well | Hardware limit|

#### Conclusion

It doesn’t always make sense to choose between horizontal and vertical scaling. Moving between the two models is often a better choice. For instance, in storage, we often want to switch between a single local disk to a distributed storage system.

Building flexibility into the system, where some layers of the application run on vertically scaled machines and other layers on horizontally scaled infrastructure remains a matter of designing for parallelization. To achieve this, (i) design it from the outset as a decoupled set of services, making the code easier to move, meaning you can add more resources when needed without breaking the ties between your code sets; (ii) partition your application and data model so the parallel units don’t share anything.

It’s likely that the industry will increasingly migrate towards a horizontally distributed approach to scaling architecture. This trend is driven by the demand for more reliability through a redundancy strategy, and the requirement for improved utilization through resource sharing as a result of migration to cloud/SaaS environments. However, combining this with a vertical scaling approach can allow us to benefit from both paradigms.
