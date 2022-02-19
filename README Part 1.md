# Cryptos-Application

PROJECT 4 (95702) – TASK 1 
Name: Kiran Gajanan Solapure                                       
Submitted Zip Files: 
CryptosProjTask1
CryptosAppTask1

Design & Implementation :
I have created my webservice based on MVC using Java SpringBoot as it provides several annotations (@SpringBootApplication, @RestController, @EnableAutoConfiguration, @Service, @ Repository, @RequestMapping, @ResponseBody, @ComponentScan @Autowired, @EnableAutoConfiguration, @CrossOrigin @Qualifier  etc.)which in turn take care of configuration, binding , dependency injection, request mapping and handling and other navigations.

File Structure - Task 1:

•	system.properties & appliocation.properties : Configuration files
•	CyptosProjApplication.java: The entry point of a Spring Boot application is the class which is annotated with @SpringBootApplication
•	ServletInitializer.java : This will take care of binding the Servlet, Filter, and ServletContextInitializer.
•	pom.xml: All the Spring & SpringBoot dependencies added
•	CyptosController.java:  Inside directory com.crypos
•	MyGETRequest.java :  Inside directory com.crypos
•	Constants.java: :  Inside directory com.crypos

The Spring framework provides comprehensive infrastructure support for developing Java applications. Spring Boot is basically an extension of the Spring framework, which eliminates the boilerplate configurations required for setting up a Spring application.
By default, Spring Boot uses an embedded container to run the application. In this case, Spring Boot uses the public static void main entry point to launch an embedded web server (CyptosProjApplication.java) It also takes care of the binding of the Servlet, Filter, and ServletContextInitializer beans from the application context to the embedded servlet container.
Another feature of Spring Boot is that it automatically scans all the classes in the same package or sub packages of the Main-class for components. Additionally, Spring Boot provides the option of deploying it as a web archive in an external container. 
          Documentation Guides for Reference:
          https://www.baeldung.com/spring-vs-spring-boot
         https://www.journaldev.com/spring
         https://docs.spring.io/spring-boot/docs/



Description:
My application (Cryptos) takes a Crypto Code as string input from the user and uses it to fetch and displays the live rate of the requested Crypto-Currency.
Reference for documentation of API & Crypto Codes available: 
https://coinlayer.com/
https://coinlayer.com/documentation


Here is how my application meets the task requirements:
1. Implement a native Android application 
The name of my native Android application project in Android Studio is:
For Whole( Task 1+ Task 2): CryptosAppTask2
For Task 1: CryptosAppTask1 (For backup Zipped as 2 App tasks separately)
If running using CryptosAppTask2 replace host in the URL of the MainActivity.java file’s callExternalApi() method to “myapp-cryptos.herokuapp.com ” to just check functionality of part 1.


Cryptos APP:

 1.1. Has at least two different kinds of views in your Layout 
My application uses TextView, EditText, ProgressBar, Button, and ImageView.
Here is a screenshot of the layout before any input has been entered:

 
1.2. Requires input from the user
Here is a screenshot of the user searching for live rate of Crypto Currency-

 

1.3. Makes an HTTP request (using an appropriate HTTP method) to your web-service
My application does an HTTP GET request in mainactivtiy.java. The search method makes this request of my web application, parses type of crypto searched and then returns the Price. The HTTP request makes to the below URL, here the user's search crypto code – BTC (BITCOIN). 
Example:
https://myapp-cryptos.herokuapp.com/api/getPrice?code=BTC – Task 1
https://app2-cryptos.herokuapp.com/api/getPrice?code=BTC – Task 2
Web-Service Endpoints:
https://myapp-cryptos.herokuapp.com/ – Task 1 Web Service on heroku
https://app2-cryptos.herokuapp.com/ - Task 2 Web-Service on heroku

1.4. Receives and parses an XML or JSON formatted reply from the web service
An example of the JSON reply is:
2021-11-12T17:19:26.295864+00:00 app[web.1]: JSON String Result
2021-11-12T17:19:26.295887+00:00 app[web.1]: {"success":true,"terms":"https:\/\/coinlayer.com\/terms","privacy":"https:\/\/coinlayer.com\/privacy","timestamp":1636737548,"target":"USD","rates":{"ABC":59.99,"ACP":0.014931,"ACT":0.012903,"ACT*":0.017178,"ADA":2.029979,"ADCN":0.00013,"ADL":0.01515,"ADX":0.795422,"ADZ":0.0023,"AE":0.1523,"AGI":0,"AIB":0.005626,"AIDOC":0.000691,"AION":0.1726,"AIR":0.001506,"ALT":0.565615,"AMB":0.041606,"AMM":0.01553,"ANT":5.1867,"APC":0.0017,"APPC":0.091884,"ARC":0.0169,"ARCT":0.00061,"ARDR":0.319547,"ARK":5.68884,"ARN":0.061501,"ASAFE2":0.4,"AST":0.518142,"ATB":0.017,"ATM":15.4822,"AURS":0.352867,"AVT":0,"BAR":14.255,"BASH":0.0056,"BAT":1.121202,"BAY":0.0644,"BBP":0.0005,"BCD":2.00276,"BCH":656.987221,"BCN":0.000392,"BCPT":0.003194,"BEE":1.0e-6,"BIO":0.0008,"BLC":0.072132,"BLOCK":1.153,"BLU":0.00054,"BLZ":0.3323,"BMC":0.037495,"BNB":612.5357,"BNT":4.500699,"BOST":0.048,"BQ":7.775e-5,"BQX":2.720931,"BRD":0.211201,"BRIT":0.03,"BT1":0,"BT2":0,"BTC":63182.319776,"BTCA":0.00036,"BTCS":0.01201,"BTCZ":0.000749,"BTG":63.829623,"BTLC":9,"BTM":0.078282,"BTM*":0.122609,"BTQ":0.01,"BTS":0.05284,"BTX":0.378535,"BURST":0.017348,"CALC":0.0006,"CAS":0.007,"CAT":0.194478,"CCRB":0.08888,"CDT":0.046736,"CESC":0.0037,"CHAT":0.002479,"CJ":0.000898,"CL":0.028,"CLD":0.02,"CLOAK":10,"CMT*":0.03954,"CND":0.016268,"CNX":1.996594,"CPC":0.0005,"CRAVE":0.4,"CRC":0.08475,"CRE":1.316485,"CRW":0.06102,"CTO":0.005,"CTR":0.017,"CVC":0.444656,"DAS":0.937816,"DASH":217.946856,"DAT":0.13833,"DATA":0.13833,"DBC":0.00895,"DBET":0.027656,"DCN":2.87904e-5,"DCR":106.958183,"DCT":0.00059,"DEEP":0.001,"DENT":0.006597,"DGB":0.061159,"DGD":878.34198,"DIM":9.4957e-5,"DIME":3.0e-5,"DMD":0.58782,"DNT":0.18255,"DOGE":0.255287,"DRGN":0.176449,"DRZ":3,"DSH":252.13175,"DTA":0.000373,"EC":50,"EDG":0.036273,"EDO":1.00965,"EDR":0,"EKO":0.000875,"ELA":5.311,"ELF":0.505193,"EMC":0.079274,"EMGO":0.43382,"ENG":0.067084,"ENJ":2.991976,"EOS":4.761717,"ERT":0.2054,"ETC":54.704285,"ETH":4575.708324,"ETN":0.02032,"ETP":0.308004,"ETT":2.9,"EVR":0.104931,"EVX":0.732249,"FCT":1.62704,"FLP":0.0093,"FOTA":0.000518,"FRST":0.78001,"FUEL":0.000817,"FUN":0.021164,"FUNC":0.00061,"FUTC":0.004,"GAME":0.21615,"GAS":8.412371,"GBYTE":39.106501,"GMX":6.467e-5,"GNO":458.49,"GNT":0.51271,"GNX":0.02847,"GRC":0.0067,"GRS":10,"GRWI":10000,"GTC":9.020237,"GTO":0.04765,"GUP":0.001482,"GVT":0.534601,"GXS":0.39381,"HAC":0.001521,"HNC":0,"HSR":1.8723,"HST":0.0027,"HVN":0.03529,"ICN":0.1452,"ICOS":17,"ICX":2.078664,"IGNIS":0.02586,"ILC":0.098703,"INK":0.001822,"INS":0.394836,"INSN":0.0473,"INT":0.01083,"IOP":15.455555,"IOST":0.046978,"ITC":0.08144,"KCS":22.057016,"KICK":0.000324,"KIN":9.80805e-5,"KLC":0.000703,"KMD":0.991174,"KNC":1.824307,"KRB":6,"LA":0.098516,"LEND":3.007499,"LEO":3.166575,"LINDA":0.000271,"LINK":33.296606,"LOC":3.450163,"LOG":0.060174,"LRC":2.941204,"LSK":3.332327,"LTC":248.304585,"LUN":0.066488,"LUX":2.09e-6,"MAID":0.502366,"MANA":3.206053,"MCAP":0.005398,"MCO":10.71,"MDA":0.673831,"MDS":0.004915,"MIOTA":1.2602,"MKR":2824.663415,"MLN":126.613181,"MNX":0.028649,"MOD":1.3556,"MOIN":0.033073,"MONA":1.672,"MTL":3.333,"MTN*":0.009575,"MTX":0.03,"NAS":0.5196,"NAV":0.520842,"NBT":270.808373,"NDC":0.008989,"NEBL":1.406843,"NEO":46.590258,"NEU":0.154972,"NEWB":0.002604,"NGC":0.429,"NKC":0.002946,"NLC2":0.599935,"NMC":5.867998,"NMR":42.762682,"NULS":0.555,"NVC":10,"NXT":0.018459,"OAX":0.289721,"OBITS":0.015,"OC":0.001171,"OCN":0.000808,"ODN":0.5,"OK":0.022376,"OMG":12.915647,"OMNI":3.4,"ORE":0,"ORME":1.235715,"OST":0.005143,"OTN":0,"OTX":0.023,"OXY":2.16,"PART":3.951477,"PAY":0.09,"PBT":879.049188,"PCS":0.019961,"PIVX":0.779977,"PIZZA":0.001,"PLBT":20,"PLR":0.03134,"POE":0.000192,"POLY":0.642,"POSW":0.48712,"POWR":0.364415,"PPC":1.707327,"PPT":0.799,"PPY":5.45,"PRC":3.0e-5,"PRES":0.219998,"PRG":0.612149,"PRL":0.061361,"PRO":2.910798,"PURA":0.25,"PUT":0,"QASH":0.07965,"QAU":0,"QSP":0.058139,"QTUM":15.681493,"QUN":0.008318,"R":1,"RBIES":1,"RCN":0.022265,"RDD":0.00268,"RDN":0,"RDN*":0.324446,"REBL":0.004882,"REE":1.0e-5,"REP":23.384,"REQ":0.2136,"REV":0.01475,"RGC":0.001,"RHOC":0.178417,"RIYA":0.090025,"RKC":5,"RLC":4.278482,"RPX":0.143205,"RUFF":0.0052,"SALT":0.768708,"SAN":0.5571,"SBC":7,"SC":0.019308,"SENT":0.005443,"SHIFT":0,"SIB":5.177,"SMART":0.004904,"SMLY":6.0e-5,"SMT*":0.011226,"SNC":0.031916,"SNGLS":0.000402,"SNM":0.545615,"SNT":0.090691,"SPK":0.0084,"SRN":0.013662,"STEEM":0.576225,"STK":0.001278,"STORJ":1.592584,"STRAT":0.327025,"STU":0.00019,"STX":0.01055,"SUB":0.003544,"SUR":0.358535,"SWFTC":0.002635,"SYS":0.440484,"TAAS":10,"TESLA":0.019139,"THC":0.012147,"THETA":7.004196,"THS":0.00171,"TIO":0.085,"TKN":0,"TKY":0.001315,"TNB":0.002513,"TNT":0.015,"TOA":0.002397,"TRC":6.2,"TRIG":1.265831,"TRST":0.04799,"TRUMP":0.055,"TRX":0.106267,"UBQ":0.22537,"UNO":107.2443,"UNRC":6.0e-5,"UQC":18.303,"USDT":1.005644,"UTK":0.42617,"UTT":0.325855,"VEE":0.020657,"VEN":8.904521,"VERI":23.736235,"VIA":0.273624,"VIB":0.0531,"VIBE":0.033861,"VOISE":0.00018,"VOX":1833.93226,"VRS":0.1375,"VTC":0.648259,"VUC":9.9e-5,"WABI":0.19616,"WAVES":23.425908,"WAX":0.5499,"WC":0.045,"WGR":0.053063,"WINGS":0.035801,"WLK":0.0058,"WOP":0.046453,"WPR":0.011545,"WRC":0.00055,"WTC":0.9805,"XAUR":0.10301,"XBP":0.0027,"XBY":0.2889,"XCP":12.786809,"XCXT":0.095658,"XDN":0.000995,"XEM":0.186468,"XGB":0.0015,"XHI":0.001325,"XID":0.010924,"XLM":0.372034,"XMR":258.920247,"XNC":0.00018,"XRB":59.080769,"XRP":1.171443,"XTO":0.324858,"XTZ":5.660285,"XUC":0.104703,"XVG":0.033523,"XZC":4.96985,"YEE":0.003528,"YOC":0.00012,"YOYOW":0.021083,"ZBC":0,"ZCL":0.147045,"ZEC":195.339776,"ZEN":97.241723,"ZIL":0.098969,"ZNY":0.02,"ZRX":1.25733,"ZSC":0.000318,"611":0.389165}}

1.5. Displays new information to the user

1.6. Is repeatable (I.e. the user can repeatedly reuse the application without
restarting it.)
The user can type in another search code\ clear code and hit Submit. Here is an example of having typed in "BTC", .

Can type in the same session without restarting:
Ex:
Typing LTC in the same window after getting result for BTC



2. Implement a web application, deployed to Heroku
The URL of my web service deployed to Heroku is:
https://dashboard.heroku.com/apps/myapp-cryptos
The Java project directory name is CryptosProjectTask1.

2.1. Using the MVC based Java SpringBoot  to implement a simple (can be a single path) API
In my project controller is present inside com.crypos directory. 
Controller: CryptosController.java        Model: myGetRequest.java
Request Mapping and handling to the deployed web service on heroku is handled by CryptosController.java file, myGetRequest.java class makes the request to the third-party API returns the JSON containing the data. 

2.2. Receives an HTTP request from the native Android application
Controller receives the HTTP GET request with the argument "get Price" and the input code entered by the user. 
HTTP request format:
https://myapp-cryptos.herokuapp.com/api/getPrice?code=BTC



2.3. Executes business logic appropriate to your application
Controller Upon getting request maps to its getPrice() method which further males call to the  makes call to the myGETRequestCall() method of myGetRequest.java class which returns the JSON data from third party API (coinlayer).
Controller then extracts the rate from the JSON as per the input Crypto code provided by user.

2.4. Replies to the Android application with an XML or JSON formatted response.
Controller replies to the user request with the response as price/live rate for the entered crypto currency. 
Example:
2021-11-12T17:19:26.296789+00:00 app[web.1]: Price: $63182.319776
2021-11-12T17:19:26.297476+00:00 heroku[router]: at=info method=GET path="/api/getPrice?code=BTC" host=myapp-cryptos.herokuapp.com request_id=5c9ea124-f335-4fae-87af-9c2ee3a9b95f fwd="117.194.17.105" dyno=web.1 connect=0ms service=37ms status=200 bytes=153 protocol=https





