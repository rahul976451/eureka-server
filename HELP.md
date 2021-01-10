#### This is a eureka discovery server. This is the place where the application servers register and deregister themselves for discovery by their clients. An application server shares its hostname, location, port no for its discovery.
Eureka servers constantly check the status of services whether they are healthy or not. Clients that are registered 
with the eureka server send heartbeats every 30 sec by default to update that they are healthy. The services are 
removed from the registry after 90 seconds of no heartbeats. Sending the heartbeat is a default configuration, but 
we can also configure the eureka server to hit an endpoint to check heartbeats. 

Eureka server was created with high availability in mind. So whenever a client requests a service, the eureka server 
sends the copy of the registry, in case the discovery server(i.e the eureka server) fails then the client can 
continue to operate with the latest update. Now not the entire registry is passed everytime, but only the changes 
are passed to the client.

Netflix is a heavy user of AWS, and hence there is an aws support included in the netflix implementation of microservices.





