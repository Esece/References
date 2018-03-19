## HTTP Status Codes Simplified

|Status Code|Description|Simplified Description|
|-----------|-----------|-----|
|200|OK|Generic "no-error" response| 
|201|Created|New record is created (Generally with POST or PUT)|
|202|Accepted|Async process is requested|
|400|Bad Request|User sent missing or malformed parameters
|401|Unauthorized|User must log in
|403|Forbidden|User must have the role
|404|Not Found|Bad path
|405|Method Not Allowed|Bad HTTP verb (Add "Allow" header in response (i.e. Allow: POST)
|406|Not Acceptable|Requested media type not supported/available
|415|Unsupported Media Type|Client media type (Content-Type) not supported
|500|Internal Server Error|Generic server runtime error

Details:

https://restfulapi.net/http-status-codes/

https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

https://tools.ietf.org/html/rfc7231
