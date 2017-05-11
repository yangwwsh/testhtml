# Creating an API Gateway {#apigw_configuringapigw .task}

How to configure an API Gateway. This information is the high-level procedure to create an API Gateway.

To create an API Gateway, provide the following settings:

-   The protocol handlers to receive API requests. An API Gateway can receive requests only through HTTP and HTTPS handlers.
-   The API collections. Each API collection packages the subscribers and plans to make a collection of APIs available on the API Gateway.
-   The XML manager to manage the compilation and caching of style sheets, the caching of documents, and enforce constraints on document parsing.

1.   In the search field, enter API. 
2.   From the search results, click **API Gateway**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the protocol handlers to use to receive API requests. 
6.   Specify the API collections to include in the API Gateway. 
7.   Specify the XML manager. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

-   **[Creating an API collection](apigw_configuringapicollection.md)**  
An API collection packages the plans and subscribers to make APIs available to a specific group of API clients. The information instructs how to create an API collection.
-   **[Creating an API plan](apigw_configuringapiplan.md)**  
An API is not exposed for access unless you add the API into a plan. The information instructs how to configure an API plan to package a list of APIs to expose for access.
-   **[Creating an API subscription](apigw_configuringapisubscription.md)**  
A client can access only the APIs in the plans that the client subscribes to. An API subscription is a list of plans that a subscriber subscribes to. The information instructs how to create an API subscription.

**Parent topic:** [API Gateway](apigw_overview.md)

**Related information**  


[Configuring an HTTP handler](handler_http.html)

[Configuring an HTTPS handler](handler_https.html)

[XML managers](xmlmanager.html)

