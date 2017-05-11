# Adding an API operation rate limit {#apigw_configuringoperationratelimit .task}

How to add an operation rate limit to override the rate limit scheme for an API operation.

By default, the rate limit schemes that you configure for a plan is enforced on all APIs that are packaged in the plan. To override the rate limit schemes for an operation, define an API operation rate limit configuration.

1.   In the search field, enter API. 
2.   From the search results, click **API Operation Rate Limit**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the API operation that you want to override rate limit for. 
6.   Specify the rate limit schemes to enforce on the operation. To add a rate limit scheme, do the following steps: 
    1.   Click **Add**. 
    2.   Specify the maximum rate to allow. 
    3.   Specify the time interval for the rate limit. 
    4.   Specify the time unit for the rate limit. 
    5.   Specify whether to enable hard limit. 
    6.   Click **Done**. 
7.   Specify the burst limit schemes to enforce on the operation. To add a burst limit scheme, do the following steps: 
    1.   Click **Add**. 
    2.   Specify the maximum burst rate to allow. 
    3.   Specify the time interval for the burst limit. 
    4.   Specify the time unit for the burst limit. 
    5.   Click **Done**. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an API plan](apigw_configuringapiplan.md)

