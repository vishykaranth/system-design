## CAP Trade-Off

### Objective 
- The key objective of this article is to provide an understanding of how the design choices made for the key building blocks such as,  
    - metadata service, 
    - replication, 
    - locking, etc. 
- impacts the overall properties of the shared nothing storage architecture, 
- and also mapping it to the application data model and storage workload requirements.
- Eric Brewer coined the CAP theorem to convey that the design of a scale-out system involves trade-offs. 
- CAP is commonly oversimplified to mean that between Consistency, Availability, and Partition tolerance, 
- Only two of the three attributes can be realized in a system. In general, the architecture of any shared nothing scale-out storage involves a collection of design choices and trade-offs that ultimately dictate the observable behavior of the system. Following are some choices involved in the design of a shared nothing storage solution:

### Trade-Off Questions 
- Data locality versus cluster scalability?
- Master versus Master-less metadata architectures?
- Locking versus multi-version concurrency control?
- Strong versus eventual versus weak consistency?
- Replication versus RAID?
- Node-to-node communication: UDP versus TCP versus RDMA?
- Two-phase commit versus Paxos versus Multi-Paxos?
- In-memory data grids versus disk-based DAS architectures?
- Data models: ACID versus BASE (Basically Available, Soft state, Eventually consistent)?
- We will start the tutorial with a bare-bones skeleton of the architecture, 
    - then incrementally populate the building blocks. 
    - For each building block, we discuss popular design choices, 
    - followed by an interactive discussion on the implications of mix-and-match of these building blocks 
    - (for example, matching coarse-grained data sharding for better data locality performance, 
    - with appropriate patterns for scaling and distributed data recovery). 
    - The tutorial assumes a basic knowledge of distributed systems. 
    - Additionally, to better appreciate the under-the-hood exploration, we expect an awareness of the cloud storage landscape, 
    - and a high-level understanding of the popular solutions.