# Adding an invoke action to retrieve documents {#apigw_addinginvokeaction .task}

An invoke action retrieves a document from a specified target URL from within the assembly. The invoke action sends a request that can include a payload to the target and stores the response in the specified variable in the API context.

For a PUT or POST request, the invoke action retrieves the headers and payload from the API context and sends the retrieved data to the target URL. For a GET request, the headers are retrieved from the API context, but no payload is sent. After the invoke action receives the response, it stores the response back into the variable that is specified by the **Output** property. By default, the response is stored in the `message` context variable.

When multiple invoke actions are used within the same assembly, the output of each invoke task might have a different variable name based on your need.

You can set whether to enable the **Stop on error** property.

-   When enabled, the assembly flow can stop on the following type of errors.

     Connection error
     :   The invoke action cannot establish a connection to the target URL. For example, the host is not reachable or the service is not available.

      SOAP error
     :   The the invoke action receives a 500 SOAP fault as response.

      Operation error
     :   The invoke action establishes the connection and receives a non-2xx response in return.

     -   When such an error occurs during the API call, an error is thrown. The invoke action stores the error message into the API context and aborts the assembly execution. Here is a sample error message.

        ```
        {
          name: 'ConnectionError',
          message: 'Invalid URL'
        }
        ```

    -   When no error is of the specified type, the invoke action completes and executes the next action in the assembly.
-   When disabled, the assembly flow continues regardless of an error.

With the cache type, you can set whether and how to cache documents in the response.

 No cache
 :   Does not cache any documents.

  Protocol
 :   Uses the cache behavior that is defined by the Cache-Control headers on the request and response. When used, the invoke action forwards the Cache-Control header from the client to the target and sends the Cache-Control header from the target back to the client.

  Time to live
 :   Keeps documents in the cache for a specified time. When used, you must specify the validity period for documents in the cache.

 When the cache type is **Protocol** or **Time to live**, you can specify a cache key, or unique identifier, for the document cache entry. By default, the URL is used as the key.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Invoke Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the URL to be invoked. 
6.   Specify the SSL client profile to secure connections between the DataPower® Gateway and the target URL. 
7.   Specify the time to wait before the DataPower Gateway receives a reply from the target. 
8.   Specify the user name to use for HTTP basic authentication. 
9.   Specify the password alias of the user password to use for HTTP basic authentication. 
10.  Specify the HTTP method to use for the invocation. When you set the method to **Keep**, the HTTP method from the incoming request is used.
11.  Set whether to enable HTTP compression. 
12.  Define the document cache settings. 
    1.   Set the cache type. This property takes effect only when a response is received from the target. When it is set, the invoke action always returns the non-expired response that is previously saved in cache.
    2.   When the cache type is set to **Time to Live**, specify the validity period for documents in the cache. 
    3.   When the cache type is set to **Time to Live** or **Protocol**, specify a unique identifier to use as a key for the document cache entry. When omitted, the entire URL string is used as the key. 
13.  Set whether the flow stops when a particular type of error occurs during the assembly execution. 
14.  When the flow is set to stop on error, specify the type of errors on which the flow stops. 
15.  Specify the name of a variable to store the invoke action output. By default, the output is stored in the `message.body` , `message.headers` , `message.statuscode` respectively in the API context.
16.  Click **Apply** to save the changes to the running configuration. 
17.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

