## Broadly speaking, scalability can be defined as thus:
- Extensible: Scalable software is extensible at the most basic level. 
    - The design itself does not limit functionality, 
    - and instead allows multiple avenues to tie into the underlying services 
    - and systems to enable extensions and other services. 
    - An example is Amazon’s API Gateway.
- Built into the architecture: 
    - Scalability must be imbued into the foundational stages of the API itself. 
    - To put it simply, don’t build then adopt scalability later on, build for scalability from the onset. 
    - Third party solutions can be valuable for increasing scalability, especially when they assist a built-to-scale approach.
- Implies demand balancing: 
    - Just as important as extensibility is responding to demand. 
    - Scalability implies that the handling of traffic is done just as well with one hundred requests as with one million — it’s in the name, “scale.” 
    - The serious implication is that scalability naturally demands efficient performance, regardless of technique or methodology, at both extremely high traffic and extremely low traffic.
    
## Four Mantras for Scalability
- Now that we have a better understanding of what scalability means, here are four mantras to live by when designing scalable APIs.
- 1: Design for A Repeating Launch Day
    - The day a product launches is perhaps one of the most stressful days in the lifespan of development for a variety of reasons. 
        - One of these reasons is the fact that no matter how good your market planning, how effective your outreach, 
        - you simply cannot know the requirements your system might see.
    - When launching a service, what kind of traffic can we expect? 
        - Let’s say we’re launching a new social platform that ties into an API to join social profiles into a single “hub.” 
        - So far, so good. We’ve designed this API to handle a certain volume of calls — for simplicity’s sake, let’s say 200k calls an hour is the maximum our server can handle.
    - The problem is that we don’t know exactly what our system is going to have to deal with. 
        - Our hub could be featured in a Reddit post, shared on Facebook, mentioned in a YouTube video, and before you know it, 
        - our 200k an hour call rate has ballooned to several millions of calls.
    - Application
        - What does this mean for scalability? 
        - You need to address the foundation of your API as if you are always on the verge launching. 
        - Ensuring that you are using a proper load balancer is hugely important, 
        - and in many cases, can be the difference between success and failure. 
        - Ensuring that your API has failover paths and secondary functions can make a huge difference not only to your API’s usability, 
        - but towards general user experience.
    - In fact, in some cases the server issues can be skipped entirely. If we’re truly concerned with scalability and we anticipate that our service is going to have extreme fluctuations in traffic, we can decide to simply go for a serverless solution like Amazon Web Services. By tying into an extensible system and enabling our traffic to be off-loaded via hardcoded routes in the API architecture, we can dynamically scale to meet almost any demand — in essence, we can expect the unexpected.
    - Finally, one of the best ways you can plan for launch is to integrate analytics into your system. Launch day is a mystery, and there will never be a perfect prediction as to what it will mean for a product — that being said, you’re essentially playing an information game. And as such, any edge you can give yourself is valuable. Being able to see trends developing in real time can help you develop in an agile way and address deficiencies as they arise organically, while predicting further failures down the road.
- 2: Anticipate Success
    - Speaking of “expecting the unexpected,” you never truly know how successful you’re actually going to be. This isn’t a simple consideration of traffic, either — traffic might be high even if you’re the second or third most popular choice.
    - The fact is that a service might easily be the number one service in a matter of days, regardless of what the expectation is. Instances of the “Reddit Hug of Death”, which was previously called the “Slashdot Effect”, can instantly inundate sites with dramatic amounts of traffic, causing them to crash and burn. It is this “crashing and burning” that can prematurely kill the cost benefit argument for a service, and can directly cause loss of retention.
    - Simply put, a provider cannot know how much traffic they can expect, and thus when planning in scalability terms, providers should plan for the most extreme case possible within their means in order to enable the handling of these extremes. Another way to frame this would be to anticipate success.
    - Application
        - An API provider that under-builds could be dramatically stunting potential growth. Ensuring that an API has the proper ability to route traffic is one thing, but under-building the underlying architecture to such a point that success is self-restricted is another thing entirely.
    - How can we stop this from being a problem? First and foremost, building out support for alternative data formats and adopting additional language implementations is incredibly helpful. Not everybody is going to a JSON fan, and not everybody is going to want to use Ruby. Easing implementations in both common and esoteric languages opens your system to further development and iteration to match a constantly evolving industry.
- 3: Non-Extensible is a Unitasker
    - Traffic management and scalable mindset is all for naught if the application itself is not extensible. While extensibility is indeed its own concept, with its own considerations and implications, whether or not a service is extensible can have a direct impact on whether or not it’s scalable.
    - While it’s a great practice to develop with scalability from the onset, there’s no way that a provider can know literally every possible future use and application of their service.
    - Application
        - Thankfully, developers don’t need to be clairvoyant. When a system is properly designed with scalability in mind, functions should be interrelated as much as they are interconnected and interfaceable. That sounds like a bunch of buzzwords, but we can see this exact type of solution in something like GraphQL.
        - In GraphQL, you get predictability by allowing users to define what they want, and get exactly that. While that’s helpful, that’s only the tip of the iceberg in terms of extensibility. Because GraphQL ties into the underlying structure of the API and its resources, many resources can be called in a variety of ways using a single call. What this means is that a system like GraphQL, compared to a traditional API, is better able to handle a variety of requests that the developer may never have anticipated.
        - Adopting extensibility adds value to your service. While many niche web services derive their power from specialization, making a truly extensible application, with the added benefit of being scalable to boot, is supremely valuable and grants amazing staying power.
- 4: Efficiency Is King
    - You cannot always decrease the complexity of the problem — your traffic will always be your traffic, and use cases will remain the same. What you can do, however, is simplify your API architecture and thus simplify the resultant solution applied to the problem. By increasing efficiency, you can drastically reduce the actual resources needed by an application.
    - The issue with scalability is that, in classic conception, an increase in power necessitates an increase in methodology. In the physical world, to carry more people, you need more buses, more taxis, etc. On the internet, in order to carry more data and do more calculations, you need more advanced protocols.
    - Application
        - A great example of this is the rejection of polling in favor of something like REST Hooks. According to REST Hooks developers Zapier, “On average, 98.5% of polls are wasted.” All of this polling is simply wasted processing power, and can drastically contribute to increased API overhead, thereby limiting the processing available to the actual functionality of your API.


### Why is Scalability Important?
- Finally, it’s important to contextualize exactly why scalability important. It sounds good in analogy form, but is this actually a significant enough issue to demand best practices? Well, consider this data supplied by HighScalability.com:
    - Netflix has 100 million subscribers;
    - 25% of US citizens won’t subscribe to traditional cable, favoring streaming solutions;
    - The largest Google Computer Engine job utilized 220,000 high-throughput cores;
    - Sling TV has 1.3 million subscribers; and
    - There are 10^5 data centers worldwide needed for cloud computing.
- Why is this data important? All of these data points are from services that started out small, and grew exponentially larger. Netflix started as a relatively small service, and grew extremely fast. Google started essentially as a small experiment, and became one of the largest organizations in the world. Sling TV had a small subscriber base, and has considerably and consistently grown.
- That the smallest, single-purpose solution is not going to stay that way forever. Designing for the traffic and function that you currently handle is fine, but intrinsically limits the future growth of the platform.
- Conclusion: Scalability is Critical For API Platform Growth
- Hopefully these mantras have helped establish a strong, long-term ethos for scalable API design. It should be apparent that scalability is all but a requirement for modern applications, especially in the current climate where an application can rush from relatively unknown to heavy use in a matter of hours. Failing to match modern standards means death, and even the best laid plans are essentially useless if the underlying system itself is not scalable.











## References
- https://nordicapis.com/tag/microservices/
- https://nordicapis.com/5-protocols-for-event-driven-api-architectures/            