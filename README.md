# spring-consuming-restfull-web-service
This guide walks you through the process of creating an application that consumes a RESTful web service. This example is based on the Spring guides, available in https://spring.io/guides/gs/consuming-rest/. 

## Build and Run project
To build this project, you need to have Gradle installed in your system because I decided to not use the Gradle wrapper commands.

In the root of the project execute:
```
gradle build
```
And then to start the embedded server execute:
```
java -jar build/libs/three-consume-rest-0.1.0.jar
```
The name of the jar is declared in the _build.gradle_ file in the _bootJar_ section. 


## Consuming a RESTfull Web Service

This project consumes a web service from this address http://gturnquist-quoters.cfapps.io/api/random that receives a random content in the JSON format, and then, convert to Java object, using the library called Jacskon JSON. 

JSON format received.
```
{
   type: "success",
   value: {
      id: 11,
      quote: "I have two hours today to build an app from scratch. @springboot to the rescue!"
   }
}
```
The Java object representation using its _toString_ method.
```java
Quote{ type=success 
       value=Value{ id=12 
                    quote=I have two hours today to build an app from scratch. @springboot to the rescue!
                  }  
    }
```
