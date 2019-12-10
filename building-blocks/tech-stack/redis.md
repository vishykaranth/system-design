## Redis 

### How does Redis work?
- All Redis data resides in-memory, in contrast to databases that store data on disk or SSDs. By eliminating the need to access disks, in-memory data stores such as Redis avoid seek time delays and can access data in microseconds. Redis features versatile data structures, high availability, geospatial, Lua scripting, transactions, on-disk persistence, and cluster support making it simpler to build real-time internet scale apps.
### Redis Vs Memcached
- Both Redis and MemCached are in-memory, open-source data stores. Memcached, a high-performance distributed memory cache service, is designed for simplicity while Redis offers a rich set of features that make it effective for a wide range of use cases. For more detailed feature comparision to help you make a decision, view Redis vs Memcached.  They work with relational or key-value databases to improve performance, such as MySQL, Postgres, Aurora, Oracle, SQL Server, DynamoDB, and more. 

### What is new with Redis 5.0
- Redis 5, and now Redis 5.0.3, is the latest GA version of open-source Redis. Since its initial release in 2009, open-source Redis has evolved beyond a caching technology to an easy to use, fast, in-memory data store, which provides versatile data structures and sub-millisecond responses. Redis reached a major milestone with the release of 5.0, which includes a variety of advancements and improvements. The big story here is the introduction of Streams, the first entirely new data structure in Redis since HyperLogLog. This release also added more commands for Sorted Sets, and new capabilities for Module APIs.
### Amazon ElastiCache for Redis
- Fully-managed Redis with encryption, online cluster resizing, high availability, and compliance.
### Benefits of Redis
- In-memory data store
- All Redis data resides in the server’s main memory, in contrast to databases such as PostgreSQL, Cassandra, MongoDB and others that store most data on disk or on SSDs. In comparison to traditional disk based databases where most operations require a roundtrip to disk, in-memory data stores such as Redis don’t suffer the same penalty. They can therefore support an order of magnitude more operations and faster response times. The result is – blazing fast performance with average read or write operations taking less than a millisecond and support for millions of operations per second.
### Flexible data structures
- Unlike simplistic key-value data stores that offer limited data structures, Redis has a vast variety of data structures to meet your application needs. Redis data types include:
    - Strings – text or binary data up to 512MB in size
    - Lists – a collection of Strings in the order they were added
    - Sets – an unordered collection of strings with the ability to intersect, union, and diff other Set types
    - Sorted Sets – Sets ordered by a value
    - Hashes – a data structure for storing a list of fields and values
    - Bitmaps – a data type that offers bit level operations
    - HyperLogLogs – a probabilistic data structure to estimate the unique items in a data set
### Simplicity and ease-of-use
- Redis simplifies your code by enabling you to write fewer lines of code to store, access, and use data in your applications. For example, if your application has data stored in a hashmap, and you want to store that data in a data store – you can simply use the Redis hash data structure to store the data. A similar task on a data store with no hash data structures would require many lines of code to convert from one format to another. Redis comes with native data structures and many options to manipulate and interact with your data. Over a hundred open source clients are available for Redis developers. Supported languages include Java, Python, PHP, C, C++, C#, JavaScript, Node.js, Ruby, R, Go and many others.
### Replication and persistence
- Redis employs a primary-replica architecture and supports asynchronous replication where data can be replicated to multiple replica servers. This provides improved read performance (as requests can be split among the servers) and faster recovery when the primary server experiences an outage. For persistence, Redis supports point-in-time backups (copying the Redis data set to disk).
### High availability and scalability
- Redis offers a primary-replica architecture in a single node primary or a clustered topology. This allows you to build highly available solutions providing consistent performance and reliability. When you need to adjust your cluster size, various options to scale up and scale in or out are also available. This allows your cluster to grow with your demands.
### Extensibility
- Redis is an open source project supported by a vibrant community. There’s no vendor or technology lock in as Redis is open standards based, supports open data formats, and features a rich set of clients.
### Popular Redis Use Cases
#### Caching
- Redis is a great choice for implementing a highly available in-memory cache to decrease data access latency, increase throughput, and ease the load off your relational or NoSQL database and application. Redis can serve frequently requested items at sub-millisecond response times, and enables you to easily scale for higher loads without growing the costlier backend. Database query results caching, persistent session caching, web page caching, and caching of frequently used objects such as images, files, and metadata are all popular examples of caching with Redis.
#### Chat, messaging, and queues
- Redis supports Pub/Sub with pattern matching and a variety of data structures such as lists, sorted sets, and hashes. This allows Redis to support high performance chat rooms, real-time comment streams, social media feeds and server intercommunication. The Redis List data structure makes it easy to implement a lightweight queue. Lists offer atomic operations as well as blocking capabilities, making them suitable for a variety of applications that require a reliable message broker or a circular list.
#### Gaming leaderboards
- Redis is a popular choice among game developers looking to build real-time leaderboards. Simply use the Redis Sorted Set data structure, which provides uniqueness of elements while maintaining the list sorted by users' scores. Creating a real-time ranked list is as easy as updating a user's score each time it changes. You can also use Sorted Sets to handle time series data by using timestamps as the score.
#### Session store
- Redis as an in-memory data store with high availability and persistence is a popular choice among application developers to store and manage session data for internet-scale applications. Redis provides the sub-millisecond latency, scale, and resiliency required to manage session data such as user profiles, credentials, session state, and user-specific personalization.
#### Rich media streaming
- Redis offers a fast, in-memory data store to power live streaming use cases. Redis can be used to store metadata about users' profiles and viewing histories, authentication information/tokens for millions of users, and manifest files to enable CDNs to stream videos to millions of mobile and desktop users at a time.
#### Geospatial
- Redis offers purpose-built in-memory data structures and operators to manage real-time geospatial data at scale and speed. Commands such as GEOADD, GEODIST, GEORADIUS, and GEORADIUSBYMEMBER to store, process, and analyze geospatial data in real-time make geospatial easy and fast with Redis. You can use Redis to add location-based features such as drive time, drive distance, and points of interest to your applications.
#### Machine Learning
- Modern data-driven applications require machine learning to quickly process a massive volume, variety, and velocity of data and automate decision making. For use cases like fraud detection in gaming and financial services, real-time bidding in ad-tech, and matchmaking in dating and ride sharing, the ability to process live data and make decisions within tens of milliseconds is of utmost importance. Redis gives you a fast in-memory data store to build, train, and deploy machine learning models quickly.
#### Real-time analytics
- Redis can be used with streaming solutions such as Apache Kafka and Amazon Kinesis as an in-memory data store to ingest, process, and analyze real-time data with sub-millisecond latency. Redis is an ideal choice for real-time analytics use cases such as social media analytics, ad targeting, personalization, and IoT.

### QUICK OVERVIEW
- Redis (REmote DIctionary Server) is an in-memory, key-value database, commonly referred to as a data structure server. 
- One of the key differences between Redis and other key-value databases is Redis’s ability to store and manipulate high-level data types. 
- These data types are fundamental data structures (lists, maps, sets, and sorted sets) that most developers are familiar with. 
- Redis’s exceptional performance, simplicity, and atomic manipulation of data structures lends itself to solving problems that are difficult or perform poorly when implemented with traditional relational databases.

### COMMON USE CASES
- Caching 
    – Due to its high performance, developers have turned to Redis when the volume of read and write operations exceed the capabilities of traditional databases. 
    - With Redis’s capability to easily persist the data to disk, it is a superior alternative to the traditional memcached solution for caching.
- Publish and Subscribe 
    – Since version 2.0, Redis provides the capability to distribute data utilizing the Publish/Subscribe messaging paradigm. 
    - Some organizations have moved to Redis and away from other message queuing systems (i.e., RabbitMQ, zeromq) due to Redis’s simplicity and performance.
- Queues 
    – Projects such as Resque use Redis as the backend for queueing background jobs.
- Counters 
    – Atomic commands such as HINCRBY, allow for a simple and thread-save implementation of counters. 
    - Creating a counter is as simple as determining a name for a key and issuing the HINCRBY command. 
    - There is no need to read the data before incrementing, and there are no database schemas to update. 
    - Since these are atomic operations, the counters will maintain consistency when accessed from multiple application servers.

### KEY FEATURES
- High-Level Data Structures 
    – Provides five possible data types for values: strings, lists, sets, hashes, and sorted sets. 
    - Operations that are unique to those data types are provided and come with well documented time-complexity (Big O notation).
- High Performance 
    – Due to its in-memory nature, the project maintainer’s commitment to keeping complexity at a minimum, 
    - and an event-based programming model, Redis boasts exceptional performance for read and write operations.
- Lightweight With No Dependencies 
    – Written in ANSI C, and has no external dependencies. 
    - Works well in all POSIX environments. 
    - Windows is not officially supported, but an experimental build is provided by Microsoft.
- High Availability 
    – Built-in support for asynchronous, non-blocking, master/slave replication to ensure high availability of data. 
    - There is currently a high-availability solution called Redis Sentinel that is currently usable, but is still considered a work in progress.
    
### COMPANIES USING REDIS
- Twitter – Deployed a massive Redis cluster to store the timelines for all users. Utilizing the list data structure, Twitter stores the 800 most recent incoming tweets for a given user. View the presentation given by Twitter on how they distribute timelines at scale.
- Pinterest – Stores the user follower graphs in a Redis cluster where data is sharded across hundreds of instances. Pinterest turned to Redis after finding that their original solution of MySQL and memcached was reaching its limits. More on how Pinterest is using Redis.
- Github – An early adopter of the Redis project, Github has developed and open-sourced the library, Resque, to facilitate the execution of background jobs that have been placed on a queue. Github developers took advantage of the fact that Redis had solved many of the difficult queueing issues, so the developers could stay focused on the difficult worker scheduling issues. More on how Github uses Redis for their job queueing needs.
### TAKE AWAY
- The combination of high-level data structures, high performance, and overall intuitiveness allow Redis to fill the role as the Swiss Army knife of data stores for a developer.
- Redis is well suited to solving challenges encountered when developing real-time systems, thanks to the predictability of operations applied to the data in the database.
- Redis attributes much of its performance to that fact that the data always resides in-memory. Data can be persisted to disk, but incorrect configuration could lead to data loss when Redis is shutdown improperly.    

### Commands 

#### RESTORE key ttl serialized-value
- Time complexity: O(1) to create the new key and additional O(N*M) to reconstruct the serialized value, where N is the number of Redis objects composing the value and M their average size. For small string values the time complexity is thus O(1)+O(1*M) where M is small, so simply O(1). However for sorted set values the complexity is O(N*M*log(N)) because inserting values into sorted sets is O(log(N)).

### References 
- https://redis.io/commands/del
- https://docs.redislabs.com/latest/rs/administering/troubleshooting/cluster-recovery/