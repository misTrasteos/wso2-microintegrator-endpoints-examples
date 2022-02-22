# Context
Let's play with microintegrator endpoints

## Example

```
curl -kis 'header1:hi' -H 'header2:bye' http://localhost:8290/api1/failover          
HTTP/1.1 200 OK
activityid: fcc771ce-573d-4be5-877e-73de7fd3f6fc
Server: nginx/1.19.8
Access-Control-Allow-Methods: GET
Access-Control-Allow-Headers: 
Content-Type: applicaion/json
Date: Mon, 21 Feb 2022 14:48:07 GMT
Transfer-Encoding: chunked

{
   "Accept" : "*/*",
   "Connection" : "Keep-Alive",
   "Host" : "backend1-service:18080",
   "User-Agent" : "Synapse-PT-HttpComponents-NIO",
   "activityid" : "09bda7fa-1df4-456f-9b28-296486ed04d7",
   "header0" : "micro-integrator",
   "header2" : "bye"
}
```

* *header0* is added during mediation
* *header1* is removed during mediation
* *header2* is left untouched during mediaton

* *Host* contains backend answering the request
