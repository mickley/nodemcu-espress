# Sample simple-api

This sample serves custom endpoints configured in routes_custom.lc, and secured by an api-key.


## Procedure
Upload the following files to your NodeMCU:

1. Espress base files
 * espress.lc  
 * espress_init.lc  
 * http_default_handler.lc  
 * http_getondata.lc
 * http_prototypes.lc
 * http_request.lc  
 * http_request_buffer.lc
 * http_request_processor.lc  
 * http_response.lc  
 * http_response_send.lc
 * http_response_sendfile.lc  
 * plugins/auth_api_key.lc => auth_api_key.lc
 * plugins/router.lc => router.lc
 
2. Relevant Espress status-codes
 * status-codes/http-200 => http-200
 * status-codes/http-401 => http-401
 * status-codes/http-404 => http-404
 * status-codes/http-405 => http-405

3. Sample files
 * **init.lua**  
 * server.lua => server.lc  
 * routes_custom.lua => routes_custom.lc  
 * routes/askme.post.lua  => routes/askme.post.lc
 * routes/hello.get.lua  => routes/hello.get.lc
 
Replace the wifi settings with your own in **init.lua**

Access both resources like this:  

[POST] http://IP/question  
[GET] http://IP/hello 

**N.B.: Don't forget to add an Api-Key header (default value is 1234-my-key)**