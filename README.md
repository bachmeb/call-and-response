# call and response

## Plan
* Make stuff
* Deploy it
* Test
* Use

## Details
### Stuff
* Something to call
* Something that processes the call
* Something that responds to the call
* Something that waits for another call

## Detail details
### What gets called? 
An API
### What provides that?
* Tomcat on an EC2 instance
* Or Spring Boot in an ECS container
* Or an AWS API Gateway
### What processes the call? 
* Some code
  * Written in Java for Tomcat
  * Written in Java for Spring Boot
  * Written in Python for a Lambda function
  * Written in Go for a Lambda function
  * Written in NodeJS for a Lambda function
  * Written in Java for a Lambda function
### What is the process? 
* Get the request
* Identify the properties of the request
  * Size
  * Data type
* Parse the request
* Do something based on some property of the request
* Create a response
* Send the response
### What does a request look like?
```
Hey
```
### What does a response look like
```
What's up?
```
### How does a request get sent? 
```
curl url 'Hey'
```
### How does the API know who is sending it a request?
It doesn't
### Could the API know who is sending it a request? 
Sure
### How? 
It could look at the IP address of the sender
### Can the call-and-response system know how many requests it has received? 
Yes, it can read the log of previous requests
### What does the logging?
The API can log. The processing component can log. 
### Where do the logs go? 
Either into CloudWatch or to the file system of the EC2 instance, 
or the container. 
### Can the system run on any PC? 
Any Linux host.
Or any host that will run the runtime for the API and the processor.
### What can the system tell the client about the client? 
Anything it can figure out, like the IP address or the number of
times the client has visited, or what the client has sent before,
or aggregated stats about what the client has done before. 
### Can the system tell the client about things the client hasn't done? 
It could guess, or predict. It would have to use some kind of profliing and
modelling techniques to give somewhat accurate predictions. Or it could 
just guess without any regard for accuracy or usefulness. 
### What is the primary interface for the system? 
HTTP
### Can the system return responses in HTML? 
Maybe. If it were asked to. 
