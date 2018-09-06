# My Microservices Example
- Example code of Microservices implementation using Zuul proxy, Eureka service registy & Spring boot rest implementation
- All the projects in the zip are sping boot applications running on ports: 8300 (DB Service), 8301 (stockservice), 8761 (Eureka & Zuul)
- Eureka is forcing port 8761, it is not working with other ports

- stock-service calls db-service using restTemplate by getting the service name: db-service from Eureka
- Zuul and Eureka are created as a single application

- Eureka Service admin URL: http://localhost:8761/
- Stock service endpoint: http://localhost:8301/rest/stock/
- DB Service endpoint: http://localhost:8300/rest/db/
- Calling Stock service endpoint through Zuul proxy url: http://localhost:8761/api/stock-service/rest/stock/
- Calling DB Service through zuul proxy: http://localhost:8761/api/db-service/rest/db/
* Note: In zuul proxy url, */api* is configured in zuul config with routes configuration pointing to the other service url's.
* Zuul knows which service the call should be routed basing on the part after '/api' i.e. '/stock-service' and '/db-service' which are names of other service applications and are as configured in zuul config (check yml file of eureka project).
