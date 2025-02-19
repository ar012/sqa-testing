# JMeter load-testing

## Test-Cases: jmeter/bin/src/{scripts, reports, data, assets, custom-templates}


### Necessary Topics for Performance Testing with JMeter
        Necessary Links:
        https://jmeter.apache.org/usermanual/index.html
        https://www.softwaretestinghelp.com/jmeter-tutorials/
        https://www.guru99.com/jmeter-tutorials.html
        https://www.youtube.com/watch?v M-iAXz8vs48&list PLhW3qG5bs-L-zox1h3eIL7CZh5zJmci4c&index 1
        https://www.youtube.com/watch?v xAnSZMGO-xE&list PLIMhDiITmNrLcYc00erJ9T36rxShFHuIS
        https://www.youtube.com/watch?v hzoZmaeT4ww&list PL9ooVrP1hQOHa3W8GRZjZxGoiBfeWKmvL&index 30

1. How to install Jmeter?
2. How to create first Jmeter Test?
3. How to use Assertions?
4. How to use Listeners?
5. How to record a UI (web) Test?
6. How to create a Database Test Plan?
7. How to run jmeter from Command Line (non GUI mode)?
8. How to test FTP upload and download?
9. How to test Web Services API?
10. How to create assertions for JDBC (Database) Test?
11. How to create HTML Dashboard Reports from command?
12. How to use Plugins Manager?
13. How to read data from CSV file (Parameterisation)?
14. Functions and Variables?
15. How to setup realistic performance test-PACING?
16. TIMERS (How to add Think Time)?
17. How to parameterize FTP test?
18. How to run Scheduled Sequential execution?
19. Correlation (with Regular Expression Extractor)
20. How to use TEMPLATES?
21. How to use Test Script Recorder?
22. How to test File Upload?
23. How to test File Download?
24. How to DEBUG?
25. How to record login test?
26. How to Monitor Server Health with PerfMon _ How to a?
27. How to install JMeter on Linux | amazon aws ec2?
28. JMeter Remote Testing | Master Slave Distributed Testing
29. How To Use Recording?
30. JMeter Selenium Webdriver sampler


### JMeter Tips and Tricks

How to change Timestamp format in csv

1. How to install Jmeter
Step 1: Check java is installed on your system
    java.version

Step 2: Download Jmeter from internet
    https://www-eu.apache.org/dist//jmeter/binaries/apache-jmeter-5.1.1.zip

Step 3: Unzip and keep Jmeter folder at any location

Step 4: Start Jmeter
```shell
    Windows. jmeter/bin. jmeter.bat
    Linux or Mac. open terminal. jmeter/bin. sh jmeter.sh
```


2: How to create first Jmeter Test
                                  

Step 1. Start Jmeter

Step 2. Create a TestPlan

Step 3. Create a Thread Group (Users)

Step 4. Add a Sampler (Http)

Step 5. Add Listeners


3: Assertions
               

Assertions    checks on the Response

1. Response Assertion

2. Duration Assertion

3. Size Assertion

4. HTML Assertion

5. XML Assertion

6. XPATH Assertion

7. Listeners
               

listener   elements that gather information about the performance test

used to view results / metrics of the test

latency   time to first byte

1. View Results in Table
2. View Results Tree
3. Aggregate Report
4. Graph Results
5. Summary Report
6. Simple Data Writer


 5. How to record UI Test
                           

1. Tools available for recording Jmeter ui test
   . Badboy software (Windows)
   . Blazemeter. Chrome Plugin. (Windows and Mac)

2. Record a Test

3. Export as Jmeter (.jmx) Script

4. Open the script in Jmeter

5. Add listeners

6. Run and validate

6. How to create a Database Test Plan
                                       

Step 1. Add mysql jdbc jar to Jmeter lib folder | Restart Jmeter
       https://dev.mysql.com/downloads/conne...

How to create free DB. https://www.youtube.com/watch?v NkaJu...

Step 2. Add Thread Group

Step 3. Add JDBC Conn Config | Provide the details of our DB

JDBC URL Format


7. How to run jmeter from Command Line (non GUI mode)
                                                       

Why to execute non-gui mode ?
-gui . consumes more resources / memory
-gui. not recommended for heavy load testing
-command line. can be integrated with other systems .Jenkins/CI �

Step 1: Goto command line. goto jmeter. bin

Step 2: Command:

jmeter.n.t (location of your jmeter test script).l (location of the result file)

  -n -> non gui mode
  -t -> location of jmeter script
  -l -> location of result file


jmeter.h . to get help on jmeter commands

jmeter.? . to get information on jmeter command options


8. How to test FTP upload and download
                                         

Step 1: Add a FTP Request Sampler

Step 2: Add FTP connection parameters

https://www.swfwmd.state.fl.us/data/ftp/
Server: ftp.swfwmd.state.fl.us
User Name: Anonymous
(use your email address as password)

If the above site is down you can find more options here:
https://stackoverflow.com/questions/7...

Step 3: Test a FTP GET and validate (get file from ftp server to local system)

Step 4: Test a FTP PUT and validate (transfer file from local to ftp server)


(FileZilla client is used in this demo for physical validation of file transfer.
You can use other FTP clients like WinSCP)


9. Performance Test of Web Services (API)
                                           
An Update:
JMeter ver 3.2 onwards.  SOAP/XML-RPC Request has been removed as part of Bug 60727. Use HTTP Request element as a replacement. See Building a WebService Test Plan http://jmeter.apache.org/usermanual/b...



API   Application Programming Interface
example-
Restaurant.  table  � WAITER �  kitchen

real world example. makemytrip.com

WebServices. client  � API �  server

REST | SOAP

How to test REST API
--------------------
Step 1: Add HTTP Request Sampler
  OR
  Add SOAP/XML-RPC Request Sampler

Step 2: Add REST API details

(http://openweathermap.org/appid)
api.openweathermap.org/data/2.5/forecast/city?id 524901&APPID 1111111111

http://api.openweathermap.org/data/2....

api.openweathermap.org
/data/2.5/weather/
q NewDelhi
appid 5ad76b332e2fa27ea9859353e5fdd69d

Step 3: Run and Validate


How to test SOAP API
--------------------

Step 1: Add SOAP/XML-RPC Request Sampler

Step 2: Add details of the Soap API Request
(http://www.webservicex.net/New/Home/S...)

Step 3: Run and Validate


https://samples.openweathermap.org/data/2.5/weather?q Dhaka,bd&appid 5f73d2e69fbb526a4691f0ef5566ecb0


10. How to create assertions for JDBC (Database) Test Plan
                                                           

to watch before this video: Jmeter Beginner Tutorial 6. How to create a Database Test Plan
https://www.youtube.com/watch?v oy53K...

Step 1: Add a Response Assertion

Step 2: Add variable names in JDBC Request

Col1,Col2,Col3,Col4

Col1 Col2  Col3 Col4
                   
ID  Name  Age  Country
1  Raghav  30  India
2  Tom  40  New Zealand

Col4_2   NewZealand
Col2_2   Tom

Step 3: In Response Assertion add Jmeter Variable and Pattern to Test

Step 4: Add Listener Assertion Results

Step 5: Run and validate


11. How to create HTML Reports (Dashboard reports) from command line
                                                                    
(This feature will work in jmeter 3.0 and later ver.)

Step 1: Create Test Plan and save it (and close).

Step 2: Open command line and change dir to jmeter/bin

Step 3: Execute command:

  to create report at the end of the test
 --------------------------------------
  jmeter.n.t <location of the jmeter script>.l <location of result file>
 .e.o <location of the output folder>

  create report from a standalone csv file
 ---------------------------------------
  jmeter.g <location of csv file>.o <location of output folder>


Step 4: Analyse HTML (Dashboard) Reports


12. How to use Plugin Manager
                             
### Manage Plugins. Quick & Easy

Install new plugins
Remove old plugins
Upgrade existing plugins
Information on plugins

Step 1: Download jmeter plugin manager jar and add to jmeter/lib/ext folder
   (Restart Jmeter)

Step 2: Find Plugin Manager under options Menu



13. How to read data from csv file. Parameterisation
                                                      

Step 1: Add config element. CSV Data Set Config

Step 2: Add details in CSV Data Set Config

Step 3: Update value fields: ${variable_name}

Step 4: Run and validate



14. Functions and Variables
                             

functions: any method that can populate a field in any other element of a test plan
 syntax: ${__functionName}
                ${__functionName(var1, var2, ...)}

variable: container that can store a value which can be referenced by any other element within the thread. (local to a thread)
 syntax: ${variableName}

function. caseSensitive | camelCasing

Functions:
----------
1. log . ${__log("message")}
2. time.
3. threadNum
4. intSum

Options. Jmeter Function Helper


15. What is a real-world performance test
                                            
Think Time. simulate actual user actions with timings/delays

Pacing. controlled ramp-up and down of virtual users
    . control timing between iterations
    . achieve x iterations in y mins/sec

Step 1. Add Plugin. Stepping Thread Group
Step 2. Setup load with required settings
Step 3. Run and validate



16. TIMERS (How to add Think Time)
                                   


Purpose. to pause thread (v.user) for some time
  . to add delay between threads
  . to avoid over flooding the server and achieve real time          behaviour by pacing the load

 (to simulate v. user's THINK TIME)

Constant Timer
Uniform Random Timer

Random Delay Max
Constant Delay Offset

formula:
0.X * Random Delay Max + Constant Delay Offset

X: 0-9

example:
0.X * 100 + 0

0. 99 milli sec

17. How to parameterize FTP test
                                 


18. How to run Scheduled + Sequential execution
                                                 
HOW TO RUN A TEST FOR SPECIFIC DURATION
Thread Group. Forever. Scheduler. Duration

HOW TO RUN PERFORMANCE TEST SEQUENTIALLY
Test Plan. Run Thread Group Consecutively

HOW TO ADD WEBSITES SEQUENTIALLY TO A PERFORMANCE TEST
Thread Group. Forever. Scheduler. Duration + Startup Delay
_______________________________________________

HOW TO RUN A TEST FOR SPECIFIC DURATION
Thread Group. Forever. Scheduler. Duration

Step 1: Thread Group. make loop count   forever

Step 2: Select Scheduler checkbox

Step 3: Add duration (sec)


HOW TO RUN PERFORMANCE TEST SEQUENTIALLY
Test Plan. Run Thread Group Consecutively

Step 1: Test Plan. select Run Thread Groups consecutively


HOW TO ADD WEBSITES SEQUENTIALLY TO A PERFORMANCE TEST
Thread Group. Forever. Scheduler. Duration + Startup Delay

Step 1: Add duration (max) to first thread group. 30 sec

Step 2: To consecutive thread groups add delay

example (for a 30 sec test plan):
1st Thread Group: delay   0 sec  |  duration   max duration of the test   30 sec

2nd Thread Group: delay   10 sec  |  duration   max. delay   30. 10   20 sec

3rd Thread Group: delay   20 sec  |  duration   max. delay   30. 20   10 sec



19. Correlation (with Regular Expression Extractor)
                                                    
What is Correlation
Why is it required
How to use Regular Expression Extractor

Step 1: Create a Test Plan where you want to do dynamic referencing in JMeter

Step 2: Add Regular Expression Extractor in the Step from where response value(s) needs to be extracted

Step 3: Refer the extracted value (referred by Reference Name) into a subsequent step

Step 4: Run and validate

references: http://regexr.com/

20. How to use TEMPLATES                      

1. What are JMeter Templates
2. How to use Templates
3. How to create your own Template
____________________________________________

1 What are JMeter Templates

Reusable project scripts

User can select any template and it will generate a Test Plan with basic and necessary components
____________________________________________

2 How to use Templates

File. Templates. select a template and start building over it.
____________________________________________

3 How to create your own Template

Step 1: save your test plan as .jmx file

Step 2: place the .jmx inside jmeter/bin/templates

Step 3: edit templates.xml file to add your template

Step 4: restart JMeter and check
____________________________________________

templates.xml

template
isTestPlan "true"    :    template will create a new test plan
isTestPlan "false"   :    templat will be merged into existing test plan
name: Name of the template
fileName : location of .jmx file
description : description will be displayed in html


21. How to use Test Script Recorder
                                     
How to use Test Script Recorder
--------------------------------------------

Today we will learn:

1. What is Test Script Recorder
2. How to record your test with it

helpful tips

__________________________________________

1 What is Test Script Recorder

is a workbench element
used to record user actions on browser

__________________________________________

2 How to record with Test Script Recorder

Step 1: Add Test Script Recorder in WorkBench
              WorkBench. Non-Test Elements. HTTP(S) Test Script Recorder

Step 2: In a Thread Group add
              Logic Controller. Recording Controller

Step 3: Add the values in Test Script Recorder parameters

Step 4: Set Browser Proxy Configuration

Step 5: Install the certificate in your browser (if required)

Step 6: Start Recording

Step 7: Run and validate
__________________________________________

Helpful Tips:

Use JMeter's inbuilt Recording template
You can use the in-built template. Recording

to start quickly
to save time and effort


JMeter Beginner Tutorial 22. How to test File Upload
                                                     

Today we will learn:
1. How to create test for file upload
2. How to record test for file upload
____________________________________

1  How to create test for File Upload

Step 1: Create a Test Plan. Thread Group. HTTP Request

Step 2:  Add values in HTTP Request sampler

Step 3: Add File Upload details

Step 4: Add Listeners to view results

Step 5: Run and Validate
____________________________________

2  How to record test for File Upload

Step 1: Add Template. Recording

Step 2: Provide a port number (e.g. 8181)

Step 3: Set browser to listen to this port

Step 4: Start Recording

Step 5: Filter the samples you need from recorded samples

Step 6: Run and Validate
__________________________________________

Helpful Tips:

In case you face any issues..
Check the following:

Method is POST
Use multipart/form-data for POST Box is checked
File location | Parameter | Mime Type  are correct
Check the logs for any other error



JMeter Beginner Tutorial 23. How to test File Download
                                                       
How to test file download in JMeter
                             

Today we will learn:

1. How to create test for file download

Step 1: Add Thread Group. HTTP Request sampler

Step 2: Add values in HTTP Request sampler

Step 3: Add Listeners to view results

Step 4: Add Listener. Save Responses to a file

Step 5: Add values to this Listener

Step 6: Run and Validate
______________________________________

Helpful Tips

How to avoid overwriting downloaded files.
in a multi-user test

Use function: ${__threadNum} as Prefix

24. How to DEBUG
                 
1. How to debug and fix errors
2. How to use Debug Sampler
____________________________

Step 1: Analyse with Listener. View Results Tree

Step 2: Analyse information in Log Viewer

Step 3: Add Listner. Debug Sampler


25. Jmeter How to record login test
                                     

Step 1: add blazemeter plugin to chrome browser

Step 2: start blazemeter plugin and login to blazemeter

Step 3: Record your scenario. Stop Recording. Export .jmx

In case you find jmx option disabled export as json and use this link to convert to jmx
http://converter.blazemeter.com/

Step 4: Import imx file in JMeter

Step 5: Add listeners

Step 6: Run and validate

26: How to Monitor Server Health with PerfMon | How to add PerfMon
                                                                  
1. How to add PerfMon plugin in JMeter
2. How to start PerfMon server
3. How to monitor server health with JMeter PerfMon plugin

Response
Time
Avg Time
Connect Time
Size
Bytes

Server. machine where your test application is hosted
CPU, Memory, Disk I/O, Network

10000 users
9000 users, high CPU usage

Suggest hardware infrastructure



Step 1: Add perfmon plugin in JMeter
   1. Download and add to JMeter lib and ext folder    https://jmeter-plugins.org/wiki/PerfMon/
   2. Plugins Manager

Step 2: On server
   Download perform server agent   https://github.com/undera/perfmon-age...

Step 3: Start the perfmon server agent
   Mac/linux. terminal. sh startAgent.sh
   Windows. startAgent.bat

   Check client can talk to server via port 4444

Step 4: Create JMeter test to monitor Server Health

Step 5: Run and Validate



27: How to install JMeter on Linux | amazon aws ec2
                                                   
JMeter | Install on AWS Linux

Amazon AWS Linux

Step 1: Check java is installed

Step 2: Get JMeter
   wget http://www-eu.apache.org/dist//jmeter...

Step 3: Extract jmeter
   tar.xf apache-jmeter-4.0.tgz

Step 4: Run a sample test


28: JMeter | Remote Testing | Master Slave | Distributed Testing
                                                                 
Meter. How to do Remote Testing
How to do Distributed Testing
How to create Master Slave


Step 1: SetUp Master
   added remote system’s ip in jmeter.properties

Step 2: create keystore file
    run create-rmi-keystore.bat / create-rmi-keystore.sh
   name: rmi
   password: changeit

Step 3: run jmeter-server file on slave (remote) system

Step 4: Run and Validate
    GUI and Commandline


Helpful Tips:

. all systems (master and slaves) have same ver of JMeter
. all systems have java (preferably same ver)
. all systems can connect to each other (are in same subnet)

. no need to copy jmeter script (jmx) to slave systems

. If you want to have 100 users and using  2 slaves. Give no as 50



29: JMeter How To Use Recording
                               
Using JMeter's HTTP(s) Test Script Recorder
Using Blazemeter plugin


30: JMeter Beginners Tutorial. JMeter Selenium Webdriver sampler
                                                                 
JMeter. Selenium WebDriver integration

Client-side performance analysis using WebDriver sampler


Step 1: Open JMeter

Step 2: Add plugin
JMeter. Plugin Manager. Selenium/WebDriver Support   https://github.com/undera/jmeter-plug...
https://github.com/undera/jmeter-plug...


Step 3: Create a test plan. add thread group

Step 4: Add
   Config Element. jp@gc. Chrome Driver Config
                        Sampler. jp@gc. Web Driver Sampler
   Listener. View Results Tree

Step 5: Download chromedriver.exe and provide the location in   Chrome Driver Config   e.g.. D:\Desktop\drivers\chromedriver\chromedriver.exe

Step 6: Add scripts in Web Driver Sampler
   e.g:
    WDS.sampleResult.sampleStart()
    WDS.browser.get('https://google.com')
    WDS.sampleResult.sampleEnd()

    WDS.sampleResult.sampleStart()
    WDS.browser.get("https://www.google.com/");
    var searchBox   WDS.browser.findElement(org.openqa.selenium.By.name("q"));
    searchBox.click();
    searchBox.sendKeys('Test');
    searchBox.sendKeys(org.openqa.selenium.Keys.ENTER);
    WDS.sampleResult.sampleEnd()


Step 7: Run & Validate


Notes:
1. WebDriver Sampler automates the execution and collection of Performance metrics on the Browser (client-side)
2. While using WebDriver sampler each thread will have a single browser instance and each browser consumes significant amount of resources
                               

## commands
```shell       
.\jmeter.n.t .\learn-src\jmeter_cli_test.jmx.l .\learn-src\cli_report.csv

.\jmeter.n.t .\learn-src\html_dashboard_report_cli.jmx.l .\learn-src\html_dashboard_report.csv.e.o .\learn-src\html-report\

 .\jmeter.g .\learn-src\html_dashboard_report.csv.o .\learn-src\html-report2\
```
How to change Timestamp format in csv
                                      
Step 1: Goto jmeter bin folder
Step 2: Open jmeter.properties file
Step 3: Find the line
            #jmeter.save.saveservice.timestamp_format yyyy/MM/dd HH:mm:ss.SSS
             Uncomment and edit the format as required
Step 4: Restart JMeter

 How to use JSON Extractor
                          
 
## References:
- https://reqres.in/
- https://codebeautify.org/jsonviewer

What is JSON Extractor
How to use JSON Extractor
How to refer multiple values
How to refer json extracted values
