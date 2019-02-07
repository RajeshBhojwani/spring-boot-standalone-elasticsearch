
# Overview
In this project, We will show how Spring boot can intract with Elasticsearch Engine using TransportClient.
This project uses elasticsearch client jar 5.0.0 version with ElasticSearch Engine 5.5.0.
Don't use ElasticSearch 5.x and above with spring-data-elasticsearch as it is not updated yet with 
If you want to see how spring-data-elasticsearch interact with Elasticsearch Engine, check this blog for details -https://www.rajeshbhojwani.co.in/2018/12/overview-elasticsearch-real-time.html


## Step 1 Download the code from github
```git clone https://github.com/RajeshBhojwani/spring-boot-standalone-elasticsearch.git ```

## Step 2 Build the project
```mvn clean install```

## Step 3 Launch the application
```java -jar target\standalone-elasticsearch-0.0.1-SNAPSHOT.jar```

## Step 4  Use Curl or Postman to test the REST apis created. 


## APIs for ElastisearchTemplate usage
1. POST call for creating new Index "users", type "employee" and document.
http://localhost:8102/rest/users/create

### JSON data
```
{
  "userId":"1",
  "name": "Sumit",
   "userSettings": {
   	"gender" : "male",
   	"occupation" : "CA",
   	"hobby" : "chess"
   }
}
```

2. GET call to retrive particular User with id.

http://localhost:8102/rest/users/view/1

3. update field of the document by user id.
http://localhost:8102/rest/users/update/1

4. delete field of the document by user id.
http://localhost:8102/rest/users/delete/1



For detail explanation of this project check this blog - https://www.rajeshbhojwani.co.in/2018/12/spring-boot-elasticsearch.html



