PROJECT 4– TASK 2
Name: Kiran Gajanan Solapure                                       
Submitted Zip Files:
CryptosProjTask2
CryptosAppTask2
CryptosUICode
Design & Implementation :
I have created my webservice based on MVC using Java SpringBoot as it provides several annotations (@SpringBootApplication, @RestController, @EnableAutoConfiguration, @Service, @ Repository, @RequestMapping, @ResponseBody, @ComponentScan @Autowired, @EnableAutoConfiguration, @CrossOrigin @Qualifier  etc.)which in turn take care of configuration, binding , dependency injection, request mapping and handling and other navigations.




File Structure - Task 2:

•	system.properties & appliocation.properties : Configuration files
•	CyptosProjApplication.java: The entry point of a Spring Boot application is the class which is annotated with @SpringBootApplication
•	ServletInitializer.java : This will take care of binding the Servlet, Filter, and ServletContextInitializer.
•	pom.xml: All the Spring & SpringBoot dependencies added
•	CyptosController.java:  Inside directory com.crypos.controllers
•	CyptosService.java:  :  Inside directory com.crypos.services
•	MyGETRequest.java :  Inside directory com.crypos.services
•	CyptosDAO.java: :  Inside directory com.crypos.dao
•	Constants.java: :  Inside directory com.crypos.util

The Spring framework provides comprehensive infrastructure support for developing Java applications. Spring Boot is basically an extension of the Spring framework, which eliminates the boilerplate configurations required for setting up a Spring application.
By default, Spring Boot uses an embedded container to run the application. In this case, Spring Boot uses the public static void main entry point to launch an embedded web server (CyptosProjApplication.java) It also takes care of the binding of the Servlet, Filter, and ServletContextInitializer beans from the application context to the embedded servlet container.
Another feature of Spring Boot is that it automatically scans all the classes in the same package or sub packages of the Main-class for components. Additionally, Spring Boot provides the option of deploying it as a web archive in an external container. 
          Documentation Guides for Reference:
          https://www.baeldung.com/spring-vs-spring-boot
         https://www.journaldev.com/spring
         https://docs.spring.io/spring-boot/docs/
1. Log useful information
My android application (Cryptos) displays the live rates of the crypto currency as per the Crypto Code entered by user.
Reference for documentation of API & Crypto Codes available: 
https://coinlayer.com/
https://coinlayer.com/documentation

Thus, I found the following 6 pieces of information useful and are logged for each request/reply with the mobile phone:

1)	Crypto Code: Crypto currency code entered by the user to get price.

2)	Phone Model: Mobile Phone Model/device used by the user to access the application.

3)	IP Address: IP address of the user.


4)	Date: Date on which user accessed application and requested for the live rate of the currency.

5)	Time: Time at which the request was placed by user.


6)	Price: The price(live rate) returned to the user on the requested day.



2. Store the log information in a database
Web-Service (https://app2-cryptos.herokuapp.com/) connects, stores, and retrieves the information from a MongoDB database in the cloud.
The functioning for the same is implemented in CyptosDAO.java: (Inside directory com.crypos.dao)
Ref. Code : Logged the paarmeters mentioned in step 1 to the database.
Document cryptos = new Document("_id", new ObjectId());cryptos.append("Crypto_code", code)
       .append("Phone_Model", model)
       .append("Ip_Address", ip)
       .append("Date", date)
       .append("Time", time)
       .append("Reply", responsePrice);

MangoDB Credentials (in case verification is needed): 
Login Using email: ksolapur.andrew.cmu.edu Password: Kira*2323
ConnectionString("mongodb+srv://kiran:2323@cluster0.q68oe.mongodb.net/test?retryWrites=true&w=majority")


3. Display operations analytics and full logs on a web-based dashboard
a. A unique URL addresses a web interface dashboard for the web service.
https://cryptos-ui.herokuapp.com/
(Sometimes lag is found: maybe Heroku problem; please do refresh till the page appears!)

UI Description:

For the dashboard UI part, I have used bootstrap and angular framework. Calls have been made to the below endpoints to get the respective response.
In apiService.service.ts, making api calls to the different backend service endpoints that we have developed in springboot and deployed to heroku.
For example:
In logs page: Call is done using apiService service to make call to "https://app2-cryptos.herokuapp.com/api/getLogData" and getting all DB data from this URL in json form which we display in form of table in logs page.
Similarly, for analytics page1: Calling “https://app2-cryptos.herokuapp.com/api/getTopCryptocurrencies”
for analytics page2: Calling “https://app2-cryptos.herokuapp.com/api/getNumofRequests”
for analytics page3: Calling “https://app2-cryptos.herokuapp.com/api/getTopAndroidModels”
and displaying the data received in tables as well as passing data to chart.js component to display it as pie chart, line chart and bar chart.




3.b. The dashboard displays at least 3 interesting operations analytics.

3.b. Analytics 1:
Top 5 Cryptocurrencies Rates Searched by the User:

3.b. Analytics 2:
Number of requests that came in last 7 days:

3.c. The dashboard displays formatted full logs.
Dashboard Snippets: Log Page 
http://cryptos-ui.herokuapp.com/logs 

 

4. Deploy the web service to Heroku
https://app2-cryptos.herokuapp.com/ - Task 2 Web-Service
https://myapp-cryptos.herokuapp.com/ - Task 1 Web-Service
https://cryptos-ui.herokuapp.com/ - Dashboad URL: 

This web service satisfies all the functionalities of Task 1 and does additional logging, to and retrieving from database, and 3 dashboard analytics functions have also been implemented along with log formatting on the dashboard!


  
 
   







