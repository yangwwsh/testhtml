# Creating an API plan {#apigw_configuringapiplan .task}

An API is not exposed for access unless you add the API into a plan. The information instructs how to configure an API plan to package a list of APIs to expose for access.

To configure an API plan, provide the following settings:

-   The rate limit schemes to enforce on all APIs that are packaged in the plan.
-   Optionally, the burst limit schemes to enforce on all APIs that are packaged in the plan. The burst limit scheme helps prevent usage spikes that might damage infrastructure. The burst limit takes higher priority than the rate limit, when a message arrives within an interval, the message is first checked against the burst limit scheme.
    -   When the burst limit is exceeded, the message is rejected.
    -   When the burst limit is not exceeded, the API Gateway proceeds to check the message against the rate limit scheme.
-   The APIs to package into the plan.
-   The operations to exclude. When an operation is excluded from the plan, API requests cannot access the API operation through the plan.
-   The rate limit schemes that are specific to certain operations. When an operation-specific rate limit scheme is defined, the operation-specific rate limit scheme is enforced instead of the rate scheme that is defined for the plan.

1.   In the search field, enter API. 
2.   From the search results, click **API Plan**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the rate limit schemes to enforce on the plan. To add a rate limit scheme, do the following steps: 
    1.   Click **Add**. 
    2.   Specify the maximum rate to allow. 
    3.   Specify the time interval for the rate limit. 
    4.   Specify the time unit for the rate limit. 
    5.   Specify whether to enable hard limit. 
    6.   Click **Done**. 
6.   Specify the burst limit schemes to enforce on the plan. To add a burst limit scheme, do the following steps: 
    1.   Click **Add**. 
    2.   Specify the maximum burst rate to allow. 
    3.   Specify the time interval for the burst limit. 
    4.   Specify the time unit for the burst limit. 
    5.   Click **Done**. 
7.   Specify a list of APIs to package into the plan. 
8.   Specify the operations to exclude from the plan. 
9.   Specify the operation rate limit configuration to override the rate limit scheme for certain operations. 
10.  Click **Apply** to save the changes to the running configuration. 
11.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

-   **[Adding an API operation rate limit](apigw_configuringoperationratelimit.md)**  
How to add an operation rate limit to override the rate limit scheme for an API operation.

**Parent topic:** [Creating an API Gateway](apigw_configuringapigw.md)

**Related information**  


[Developing APIs](apigw_configuringapi.md)

