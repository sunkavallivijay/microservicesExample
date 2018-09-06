# microservicesExample
Example code of Microservices implementation using Zuul proxy, Eureka service registy & Spring boot rest implementation

stock-service calls db-service using restTemplate by getting the service from Eureka
Zuul and Eureka are created as a single application

Eureka Service admin URL: http://localhost:8761/
Stock service endpoint: http://localhost:8301/rest/stock/
DB Service endpoint: http://localhost:8300/rest/db/
Calling through Zuul proxy url: http://localhost:8761/api/stock-service/rest/stock/

In zuul proxy url, api is configured in zuul config with routes configuration pointing to the other service url's.
