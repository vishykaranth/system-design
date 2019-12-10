# System Design Interview Questions

- A curated list of System Design interview questions for SDE-1 (Experienced),SDE-2 and above.
- Targeted companies: Amazon, Google, Facebook and other biggies.
- Hope it helps you to prepare for your upcoming interviews!

# Questions
- Design commenting system
- Design subscription based sports website which can display scores, game status, history for any games.
- Design Netflix => search, video serving, authentication, encryption, dns lookup,caching strategy,serving multi quality video etc
- Design a Latency Management System
- Design a Library Management System
- Design a Notification service
- Design ESPN/Cricinfo/Cricbuzz
- Design Uber
- Design Whatsapp
- Design Quora
- Design Lookahead system
- Design Google Docs/ Collaborative Editing service
- Design URL Shortner service
- Design RedBus
- Design BookMyShow
- Design Domain Backdooring system
- Design Amazon Locker
- Design Movies Review Aggregator System >  Data should be fetched from movie rating providers like imdb, rotten tomatoes, etc
- Design offline caching system for Ecommerce platform
- Design Amazon E-commerce
- Design Online chess game/Multiplayer game
- Design gaming platform.  A number of games can be hosted on this platform. User can login and select a particular game
- Design a last-mile delivery platform in case of peak seasons
- Design Zomato/Swiggy/Foodpanda
- Design Meeting Calendar system
- Design Spotify
- Design Promo Code API by taking into account Amazon's customer traffic into picture
- Design Vending machine with following functionalities
    - Three types of Users : User, Operator, Admin
	- User can select and buy multiple items at a time. Money can be inputted multiple times (you will get the item if there is a time gap > 30 secs). He can also do window shopping (see only the prices of items and buy nothing)
	- Operator can load the items and mark the items as expired if needed, gets notified if a product goes out of stock.
	- Admin can own multiple vending machines, he should have a analytics report of the items purchased in a month. He can also change the prices directly and it should reflect in all the vending machines which he owns.
	- Exception handling in all the edge cases
- Design splitwise
- Design Google pay at scale
- Design a Job scheduler => scalability, fault tolerance, high availability, how scheduler picks up job,
    - how will you take care where one job can run for 30 min and one for 30 hour, how will you distribute jobs on servers.
    - Based on frequency & time how will you execute them ?
    - How will you notify back the user about start/stop or completion of a job ?
    - How will your system know if a job is killed / terminated due to unknown reasons ?
- Design Meeting Scheduler
- Design Debugger
- Design Automatic Parking System
- Design a ranking system. We have an infinite supply of words ending with ‘.’ We need to implement a reader program that ranks words on the basis of certain criteria
    - Example:   This is my cat.
    - This house belongs to my uncle
    - An amazing country with so many tourist places And so on..
    - Ranking System criteria : rank the words on the basis of occurrence, for example
    - Output : This:2, is:2, my:2… highest rank (sorted asc or desc based on  provided flag)
    - Design it completely and scalable Ranking System
- Design Amazon Cart system
- Design Google Search
- Design Twitter
- Design Facebook
- Design Snapchat
- Design Instagram
- Design App-store
- Design a music player application
- Design a distributed LRU Cache
- Design Gmail
- Design a recommendation system
- Design a food sharing application
- Design payment module for Uber app
- Design Truecaller type of system
- Design performance management system (appraisal workflow system) that can be used across companies.
- Design comment system like disqus
- Design flight system
- Design Tinder
- Design survey site like surveymonkey
- Design a geographically partitioned multi-player card game, that supports multiple players, multiple games at a time. Each game will have one contractor like ones we have in a bar, He can play a game or just watch it. Integrate payment systems
- Design a kind of kindle fire application where we can subscribe news channel and read the news from all publishers as a digital format
- Design a realtime Video chat like Google Duo
- Design News paper & Magazine subscription system
- Design a system like Hackerrank/Codechef/Topcoder
- Design a concurrent Hashmap
- Design an ATM Machine system which can support massive amount of transactions
- Design Airport Baggage system
- Design Flight Information Display system
- Design a conference room booking system for a company which can have offices in multiple cities, each city can have multiple buildings, each building can have multiple floors, each floor can have multiple rooms. Each room can have features like capacitiy, video conferencing available, etc.
- Design newsfeed feature of Facebook
- Design an efficient Mail delivery system
- Design like/dislike feature at Youtube scale.
- Design Paypal
- Design Air traffic control system
- Design a realtime service which tells your friends who is online
- Design Google Maps
- Design Grammarly

### Basic Knowledge about System Design

* [How to Rock a Systems Design Interview](http://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
* [System Interview](http://www.hiredintech.com/app#system-design)
* [Scalability for Dummies](http://www.lecloud.net/tagged/scalability)
* [Scalable Web Architecture and Distributed Systems](http://www.aosabook.org/en/distsys.html)
* [Numbers Everyone Should Know](http://everythingisdata.wordpress.com/2009/10/17/numbers-everyone-should-know/)
* [Fallacies of distributed systems](https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf)
* [Scalable System Design Patterns](http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
* [Introduction to Architecting Systems for Scale](http://lethain.com/introduction-to-architecting-systems-for-scale/)
* [Transactions Across Datacenters](http://snarfed.org/transactions_across_datacenters_io.html)
* [A Plain English Introduction to CAP Theorem](http://ksat.me/a-plain-english-introduction-to-cap-theorem/)
* [The CAP FAQ](https://github.com/henryr/cap-faq)
* [Paxos Made Simple](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)
* [Consistent Hashing](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
* [NOSQL Patterns](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
* [Scalability, Availability & Stability Patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns)

### Products and Systems

The following papers/articles/slides can help you to understand the general design idea of different real products and systems. 

* [Browsers: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
* [Zalando: Engineering principles with links to their application structure and blog](https://github.com/zalando/engineering-principles)
* [MapReduce: Simplied Data Processing on Large Clusters](http://static.googleusercontent.com/media/research.google.com/zh-CN/us/archive/mapreduce-osdi04.pdf)
* [Bigtable: A Distributed Storage System for Structured Data](http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/chang06bigtable.pdf)
* [The Google File System](http://static.googleusercontent.com/media/research.google.com/zh-CN/us/archive/gfs-sosp2003.pdf)
* [The Chubby lock service for loosely-coupled distributed systems](http://static.googleusercontent.com/external_content/untrusted_dlcp/research.google.com/en/us/archive/chubby-osdi06.pdf)
* [Dynamo: Amazon's Highly Available Key-value Store](http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/decandia07dynamo.pdf)
* [Introduction to Memcached](http://www.slideshare.net/oemebamo/introduction-to-memcached)
* [Cassandra Introduction Features](http://www.slideshare.net/planetcassandra/cassandra-introduction-features-30103666)
* [Introduction to HBase](http://www.slideshare.net/alexbaranau/intro-to-hbase)
* [Introduction to MongoDB](http://www.slideshare.net/mdirolf/introduction-to-mongodb)
* [Introduction to Redis](http://www.slideshare.net/dvirsky/introduction-to-redis)
* [Storm](http://www.slideshare.net/previa/storm-16094009)
* [Introduction to Zookeeper](http://www.slideshare.net/sauravhaloi/introduction-to-apache-zookeeper)
* [Kafka](http://www.slideshare.net/mumrah/kafka-talk-tri-hug)
* [YouTube Architecture](http://highscalability.com/youtube-architecture)
* [Scaling Pinterest](http://highscalability.com/blog/2013/4/15/scaling-pinterest-from-0-to-10s-of-billions-of-page-views-a.html)
* [Google Architecture](http://highscalability.com/google-architecture)
* [Scaling Twitter](http://highscalability.com/scaling-twitter-making-twitter-10000-percent-faster)
* [The WhatsApp Architecture](http://highscalability.com/blog/2014/2/26/the-whatsapp-architecture-facebook-bought-for-19-billion.html)
* [Flickr Architecture](http://highscalability.com/flickr-architecture)
* [Amazon Architecture](http://highscalability.com/amazon-architecture)
* [Stack Overflow Architecture](http://highscalability.com/blog/2009/8/5/stack-overflow-architecture.html)
* [Pinterest Architecture](http://highscalability.com/blog/2012/5/21/pinterest-architecture-update-18-million-visitors-10x-growth.html)
* [Tumblr Architecture](http://highscalability.com/blog/2012/2/13/tumblr-architecture-15-billion-page-views-a-month-and-harder.html)
* [Instagram Architecture](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)
* [TripAdvisor Architecture](http://highscalability.com/blog/2011/6/27/tripadvisor-architecture-40m-visitors-200m-dynamic-page-view.html)
* [Scaling Mailbox](http://highscalability.com/blog/2013/6/18/scaling-mailbox-from-0-to-one-million-users-in-6-weeks-and-1.html)
* [Salesforce Architecture ](http://highscalability.com/blog/2013/9/23/salesforce-architecture-how-they-handle-13-billion-transacti.html)
* [ESPN Architecture](http://highscalability.com/blog/2013/11/4/espns-architecture-at-scale-operating-at-100000-duh-nuh-nuhs.html)
* [Uber Architecture](http://highscalability.com/blog/2015/9/14/how-uber-scales-their-real-time-market-platform.html)
* [DropBox Design](https://www.youtube.com/watch?v=PE4gwstWhmc)
* [Splunk Architecture](http://www.splunk.com/view/SP-CAAABF9)

### Hot Questions and Reference

There are some good references for each question. The references here are slides and articles. 

**Design a CDN network**  
Reference:  
* [Globally Distributed Content Delivery](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2112&context=compsci)

**Design a Google document system**  
Reference:  
* [google-mobwrite](https://code.google.com/p/google-mobwrite/)
* [Differential Synchronization](https://neil.fraser.name/writing/sync/)

**Design a random ID generation system**  
Reference: 
* [Announcing Snowflake](https://blog.twitter.com/2010/announcing-snowflake) 
* [snowflake](https://github.com/twitter/snowflake/)

**Design a key-value database**  
Reference:   
* [Introduction to Redis](http://www.slideshare.net/dvirsky/introduction-to-redis)

**Design the Facebook news feed function**   
Reference:   
* [What are best practices for building something like a News Feed?](http://www.quora.com/What-are-best-practices-for-building-something-like-a-News-Feed) 
* [What are the scaling issues to keep in mind while developing a social network feed?](http://www.quora.com/Activity-Streams/What-are-the-scaling-issues-to-keep-in-mind-while-developing-a-social-network-feed) 
* [Activity Feeds Architecture](http://www.slideshare.net/danmckinley/etsy-activity-feeds-architecture)

**Design the Facebook timeline function**   
Reference: 
* [Building Timeline](https://www.facebook.com/note.php?note_id=10150468255628920) 
* [Facebook Timeline](http://highscalability.com/blog/2012/1/23/facebook-timeline-brought-to-you-by-the-power-of-denormaliza.html)

**Design a function to return the top k requests during past time interval**   
Reference:  
* [Efficient Computation of Frequent and Top-k Elements in Data Streams](http://www.cse.ust.hk/~raywong/comp5331/References/EfficientComputationOfFrequentAndTop-kElementsInDataStreams.pdf)
* [An Optimal Strategy for Monitoring Top-k Queries in Streaming Windows](http://davis.wpi.edu/xmdv/docs/EDBT11-diyang.pdf)

**Design an online multiplayer card game**   
Reference:  
* [How to Create an Asynchronous Multiplayer Game](http://www.indieflashblog.com/how-to-create-an-asynchronous-multiplayer-game.html)   
* [How to Create an Asynchronous Multiplayer Game Part 2: Saving the Game State to Online Database](http://www.indieflashblog.com/how-to-create-async-part2.html)  
* [How to Create an Asynchronous Multiplayer Game Part 3: Loading Games from the Database](http://www.indieflashblog.com/how-to-create-async-part3.html)  
* [How to Create an Asynchronous Multiplayer Game Part 4: Matchmaking](http://www.indieflashblog.com/how-to-create-async-part4-html.html#comment-4447)  
* [Real Time Multiplayer in HTML5](http://buildnewgames.com/real-time-multiplayer/)  

**Design a graph search function**   
Reference:   
* [Building out the infrastructure for Graph Search](https://www.facebook.com/notes/facebook-engineering/under-the-hood-building-out-the-infrastructure-for-graph-search/10151347573598920)
* [Indexing and ranking in Graph Search](https://www.facebook.com/notes/facebook-engineering/under-the-hood-indexing-and-ranking-in-graph-search/10151361720763920) 
* [The natural language interface of Graph Search](https://www.facebook.com/notes/facebook-engineering/under-the-hood-the-natural-language-interface-of-graph-search/10151432733048920) and [Erlang at Facebook](http://www.erlang-factory.com/upload/presentations/31/EugeneLetuchy-ErlangatFacebook.pdf)

**Design a picture sharing system**   
Reference:   
* [Flickr Architecture](http://highscalability.com/flickr-architecture) 
* [Instagram Architecture](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)

**Design a search engine**   
Reference:  
* [How would you implement Google Search?](http://programmers.stackexchange.com/questions/38324/interview-question-how-would-you-implement-google-search)  
* [Implementing Search Engines](http://www.ardendertat.com/2012/01/11/implementing-search-engines/)

**Design a recommendation system**  
Reference:  
* [Hulu’s Recommendation System](http://tech.hulu.com/blog/2011/09/19/recommendation-system.html)  
* [Recommender Systems](http://ijcai13.org/files/tutorial_slides/td3.pdf)

**Design a tinyurl system**    
Reference: 
* [System Design for Big Data-tinyurl](http://n00tc0d3r.blogspot.com/) 
* [URL Shortener API](https://developers.google.com/url-shortener/?csw=1)

**Design a garbage collection system**    
Reference:   
* [Baby's First Garbage Collector](http://journal.stuffwithstuff.com/2013/12/08/babys-first-garbage-collector/)
 
**Design a scalable web crawling system**    
Reference:  
* [How can I build a web crawler from scratch?](https://www.quora.com/How-can-I-build-a-web-crawler-from-scratch)

**Design the Facebook chat function**    
Reference:   
* [Erlang at Facebook](http://www.erlang-factory.com/upload/presentations/31/EugeneLetuchy-ErlangatFacebook.pdf)  
* [Facebook Chat](https://www.facebook.com/note.php?note_id=14218138919&id=9445547199&index=0)

**Design a trending topic system**    
Reference:  
* [Implementing Real-Time Trending Topics With a Distributed Rolling Count Algorithm in Storm](http://www.michael-noll.com/blog/2013/01/18/implementing-real-time-trending-topics-in-storm/)   
* [Early detection of Twitter trends explained](http://snikolov.wordpress.com/2012/11/14/early-detection-of-twitter-trends/)
 
**Design a cache system**    
Reference:   
* [Introduction to Memcached](http://www.slideshare.net/oemebamo/introduction-to-memcached)

