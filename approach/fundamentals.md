## Scalable Web Architecture and Distributed Systems
### Principles of Web Distributed Systems Design
- What exactly does it mean to build and operate a scalable web site or application? 
- At a primitive level it's just connecting users with remote resources via the Internet—the part that 
    - makes it scalable is that the resources, or 
    - access to those resources, 
    - are distributed across multiple servers.
- Like most things in life, taking the time to plan ahead when building a web service can help in the long run; 
- understanding some of the considerations and 
- tradeoffs behind big websites can result in smarter decisions at the creation of smaller web sites. 

### Some of the key principles that influence the design of large-scale web systems:
#### Availability: 
- The uptime of a website is absolutely critical to the reputation and functionality of many companies. 
- For some of the larger online retail sites, 
    - being unavailable for even minutes can result in thousands or millions of dollars in lost revenue, 
    - so designing their systems to be constantly available and resilient to failure is both a fundamental business and a technology requirement. 
    - High availability in distributed systems requires the careful consideration of redundancy for key components, 
    - rapid recovery in the event of partial system failures, and 
    - graceful degradation when problems occur.
#### Performance: 
- Website performance has become an important consideration for most sites. 
- The speed of a website affects usage and 
    - user satisfaction, 
    - as well as search engine rankings, 
    - a factor that directly correlates to revenue and retention. 
- As a result, creating a system that is optimized for fast responses and low latency is key.

#### Reliability: 
- A system needs to be reliable, 
    - such that a request for data will consistently return the same data. 
- In the event the data changes or is updated, then that same request should return the new data. 
- Users need to know that if something is written to the system, or stored, it will persist and can be relied on to be in place for future retrieval.

#### Scalability: 
- When it comes to any large distributed system, size is just one aspect of scale that needs to be considered. 
- Just as important is the effort required to increase capacity to handle greater amounts of load, 
    - commonly referred to as the scalability of the system. 
- Scalability can refer to many different parameters of the system: 
    - how much additional traffic can it handle, 
    - how easy is it to add more storage capacity, 
    - or even how many more transactions can be processed.

#### Manageability: 
- Designing a system that is easy to operate is another important consideration. 
- The manageability of the system equates to the scalability of operations: maintenance and updates. 
- Things to consider for manageability are 
    - the ease of diagnosing and 
    - understanding problems when they occur, 
    - ease of making updates or modifications,
    - and how simple the system is to operate. 
    - (I.e., does it routinely operate without failure or exceptions?)

#### Cost: 
- Cost is an important factor. 
- This obviously can include hardware and software costs, 
    - but it is also important to consider other facets needed to deploy and maintain the system. 
- The amount of developer time the system takes to build, 
    - the amount of operational effort required to run the system, and 
    - even the amount of training required should all be considered. 
- Cost is the total cost of ownership.

Each of these principles provides the basis for decisions in designing a distributed web architecture. However, they also
can be at odds with one another, such that achieving one objective comes at the cost of another. A basic example:
choosing to address capacity by simply adding more servers (scalability) can come at the price of manageability (you
have to operate an additional server) and cost (the price of the servers).
When designing any sort of web application it is important to consider these key principles, even if it is to acknowledge
that a design may sacrifice one or more of them.