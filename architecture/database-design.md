## Database Design Best Practices
- Good database design is essential to building scalable, high-performance applications. 
- A database is nothing more than a mass of information stored in a framework that makes it easier to search.
- Everything else is just details. If a database works well, bits of related information are filed automatically and details can be pulled out needed.
- It should be simple to draw new meaning from data by compiling it into reports and visualizations, then storing away those facts for later use.
- Within that simple definition, there is infinite variation. Small decisions in the beginning have a huge cumulative impact.



### Database Design Best Practices
- 1. Consider Every Viewpoint During Planning
    - Don’t start building a database without input from the project sponsor and other stakeholders.
    - Get consensus on precise expectations, and consider how hard it will be to train users on the search functions.
- 2. Choose A Database Type
    - This is usually as easy as deciding between SQL and NoSQL (though there are more specific types that may be appropriate for some projects).
    - SQL databases are the standard for structured data, when data integrity is absolutely important.
    - Emerging technology like machine learning or the Internet of Things (IoT) find the speed, scalability, and fluid requirements of NoSQL databases a better fit.
    - Web analytics, social networks and some other types of databases also work much better within the NoSQL framework.
    - Make the decision as early as possible.
- 3. Normalize Your Data
    - In reality, most companies today function in a hybrid world of SQL and NoSQL databases that work together in complex arrangements.
    - With such a complicated structure, it’s critical to normalize data to achieve minimum redundancy.
    - Eliminate multi-valued attributes and repeated attributes, then start in on the subkeys.
- 4. Make Structures Transparent
    - The database belongs to its future users, not its creator, so design with them in mind.
    - Stay away from shortcuts, abbreviations, or plurals. Use consistent naming conventions.
    - Don’t reinvent the wheel or make things difficult for those who may need to modify the database at some point, which will certainly happen.
- 5. Define Constraints to Maintain Data Integrity
    - Look into the full range of options to enforce business rules, such as foreign key, check, not null, and the like.
    - The application will prevent some bad data from getting in, but not all of it.
- 6. Document Everything
    - No matter how annoying it may seem, documentation is as essential as primary keys.
    - Take care to document the design, entity-relationship schemas, and triggers for future users.
- 7. Plan for Increasing Backup Time in the Build
    - Before delving too deeply into design, think about what happens during a natural or man-made disaster.
    - Plan for failover clustering, auto backups, replication and any other procedures necessary to ensure that the database structure remains intact.
    - As the saying goes, “Prepare and prevent, don’t repair and repent.”
- 8. Keep Privacy Primary
    - The GDPR signals an era of increasing privacy concerns.
    - Encrypt passwords, and don’t assign an administrator without privacy training and well-documented qualifications.
    - This can be a tricky rule to follow due to office politics, but as a good security practice the database should be as closed as possible.
    - Vulnerabilities impact data integrity, which impacts everything else in the enterprise.
- 9. Optimize for Speed
    - Create indexes for queries that will be used regularly. Use a database analyzer to determine if an index or a clustered index is necessary.
    - Consider incorporating tools like Elastisearch to speed up searches.
- 10. Keep the Database on Its Own Server
    - Put the database on a different server than the web to lower CPU usage.

In addition to freeing up compute resources, it also helps to keep the database out of the reach of unauthorized users.

Final Thoughts
Remember, database frameworks are not set in stone.

The current database workflows can be refined and directed, or even broken up, when it make sense.

Just as business directives change over time, the database will also need fine tuning to stay in line with the company’s current goals.

Too often, administrators get bogged down in thinking about how the database functions at the moment without considering what it is capable of doing in the future.

Instead of thinking, “It doesn’t work like that,” start from the viewpoint of “What is the end goal, and how can we get there?”