## Deploy an application from our Bootstrap a Simple Application using Spring Boot tutorial to AWS Elastic Beanstalk.
- As part of this we'll:
	- Install and configure AWS CLI tools
	- Create a Beanstalk project and MySQL deployment
	- Configure the application for MySQL in AWS RDS
	- Deploy, test, and scale the application
- AWS Elastic Beanstalk Configuration
	- As a pre-requisite, we should have registered ourselves on AWS and created a Java 8 environment on Elastic Beanstalk. 
	- We also need to install the AWS CLI which will allow us to connect to our environment.
- So, given that, we need to log in and initialize our application:
	- cd .../spring-boot-bootstrap
	- eb init
- Select a default region
1) us-east-1 : US East (N. Virginia)
2) us-west-1 : US West (N. California)
3) us-west-2 : US West (Oregon)
4) eu-west-1 : EU (Ireland)
5) eu-central-1 : EU (Frankfurt)
6) ap-south-1 : Asia Pacific (Mumbai)
7) ap-southeast-1 : Asia Pacific (Singapore)
8) ap-southeast-2 : Asia Pacific (Sydney)
9) ap-northeast-1 : Asia Pacific (Tokyo)
10) ap-northeast-2 : Asia Pacific (Seoul)
11) sa-east-1 : South America (Sao Paulo)
12) cn-north-1 : China (Beijing)
13) cn-northwest-1 : China (Ningxia)
14) us-east-2 : US East (Ohio)
15) ca-central-1 : Canada (Central)
16) eu-west-2 : EU (London)
17) eu-west-3 : EU (Paris)
18) eu-north-1 : EU (Stockholm)
- Select an application to use
1) demo
2) [ Create new Application ]
- At this time, the CLI will create a file named .elasticbeanstalk/config.yml. 
- This file will retain the defaults for the project.

- Database
	- Now, we can create the database on the AWS Web Console or with the CLI using:
	- eb create --single --database
	- We'll need to follow the instructions to provide a username and password.
	- With our database created, let's configure now the RDS credentials for our application. 
	- We'll do so in a Spring profile named beanstalk by creating src/main/resources/application-beanstalk.properties in our application:
		- spring.datasource.url=jdbc:mysql://${rds.hostname}:${rds.port}/${rds.db.name}
		- spring.datasource.username=${rds.username}
		- spring.datasource.password=${rds.password}
	- Spring will search for the property named rds.hostname as an environmental variable called RDS_HOSTNAME. 
	- The same logic will apply to the rest.
- Application
	- Now, we'll add a Beanstalk–specific Maven profile to pom.xml:
<profile>
    <id>beanstalk</id>
    <build>
        <finalName>${project.name}-eb</finalName>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <configuration>
                    <excludes>
                        <exclude>**/cloud/config/*.java</exclude>
                    </excludes>
                </configuration>
            </plugin>
        </plugins>
    </build>
</profile>
	- Next, we'll specify the artifact into the Elastic Beanstalk configuration file .elasticbeanstalk/config.yml:
- deploy:
	- artifact: target/spring-boot-bootstrap-eb.jar
	- And finally, we'll include two environmental variables into Elastic Beanstalk. 
	- The first one will specify the active Spring profiles, and the second one will ensure the use of the default port 5000 expected by Beanstalk:
		- eb setenv SPRING_PROFILES_ACTIVE=beanstalk,mysql
		- eb setenv SERVER_PORT=5000
- Deployment and Testing
- Now we are ready to build and deploy:
	- mvn clean package spring-boot:repackage
	- eb deploy
- Next, we'll check the status and determine the DNS name of the deployed application:
	- eb status
- And our output should be something like:
	- Environment details for: BaeldungDemo-env
		- Application name: demo
		- Region: us-east-2
		- Deployed Version: app-181216_154233
		- Environment ID: e-42mypzuc2x
		- Platform: arn:aws:elasticbeanstalk:us-east-2::platform/Java 8 running on 64bit Amazon Linux/2.7.7
		- Tier: WebServer-Standard-1.0
		- CNAME: Demo-env.uv3tr7qfy9.us-east-2.elasticbeanstalk.com
		- Updated: 2018-12-16 13:43:22.294000+00:00
		- Status: Ready
		- Health: Green
We can now test the application – notice the use of the CNAME field as DNS to complete the URL.

Let's add a book to our library now:

1
http POST http://demo-env.uv3tr7qfy9.us-east-2.elasticbeanstalk.com/api/books title="The Player of Games" author="Iain M. Banks"
And, if all is well, we should get something like:

HTTP/1.1 201 
Cache-Control: no-cache, no-store, max-age=0, must-revalidate
Connection: keep-alive
Content-Type: application/json;charset=UTF-8
Date: Wed, 19 Dec 2018 15:36:31 GMT
Expires: 0
Pragma: no-cache
Server: nginx/1.12.1
Transfer-Encoding: chunked
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
 
{
    "author": "Iain M. Banks",
    "id": 5,
    "title": "The Player of Games"
}
6. Scaling the Application
Lastly, we scale the deployment to run two instances:

1
eb scale 2
Beanstalk will now run 2 instances of the application and load balance traffic across both instances.

Automatic scaling for production is a bit more involved, so we'll leave that for another day.

7. Conclusion
In this tutorial, we:

Installed and configured the AWS Beanstalk CLI and configured an online environment
Deployed a MySQL service and configured the database connection properties
Built and deployed our configured Spring Boot application, and
Tested and scaled the application
For more details, check out the Beanstalk Java documentation.

As always, the complete source code of our examples is here, over on GitHub.