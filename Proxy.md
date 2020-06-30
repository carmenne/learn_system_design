### Proxy
#### Forward Proxy
```
Client 
Client     Proxy    Internet    Backend-servers
Client 

```

An intermediate server between the client and backend server.
Usage: filter requests, transfor requests (adding headers), log requests, cache.
#### Reverse Proxy
A reverse proxy retrieves resources on behalf of a client from one or more servers. 
These resources are then returned to the client, 
appearing as if they originated from the proxy server itself

```
                                Backend-servers
Client   Internet    Proxy      Backend-servers
                                Backend-servers

```
