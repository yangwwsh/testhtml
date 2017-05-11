# Viewing and deleting API rate limit enforcement records {#apigw_ratelimit_view_delete_records .task}

How to view and delete API rate limit enforcement records.

**Note:** When the data storage contains a large volume of API rate limit enforcement records, the display of results can take several minutes.

The API Gateway enforces rate limiting through the quota enforcement server. The rate limit enforcement records can be persisted on the RAID volume or stored in memory. In a quota enforcement peer group, you can view records from each DataPower® Gateway by using the **API Rate Limit Enforcement Metrics** status provider. However, to delete records, you must delete from the master.

The **API Rate Limit Enforcement Metrics** status provider shows the following information:

-   The name of the subscriber that triggers rate limiting.
-   The name of the API.
-   The name of the configuration in which the rate limit scheme is defined.
-   The level of the configuration in which the rate limit scheme is defined. A rate limit scheme can be defined at the API plan, API operation, and API collection level.
-   The rate that indicates the maximum number of API requests that is allowed within an interval.
-   The interval between enforcements of API rate limiting.
-   The hard limit that indicates whether to reject requests when the threshold is exceeded.
-   The starting time of an interval.
-   The remaining requests that indicates the maximum number of remaining API requests that can be accepted in the current interval.

You can delete records at different levels from an application domain or the `default` domain:

-   From the application domain:
    -   Delete individual record.
    -   Delete all records.
-   From the `default` domain.
    -   Delete individual record from a specific domain.
    -   Delete all records from a specific domain.
    -   Delete all record from all domains, including the `default` domain and all application domains.

1.   Enter the proper domain. 
2.   In the search field, enter API. 
3.   From the search results, select **API Rate Limit Enforcement Metrics**. 
4.   Delete records according to your needs. 

**Parent topic:** [API Gateway](apigw_overview.md)

**Related information**  


[Rate limiting](apigw_apirequestrouting_apiratelimit.md)

[Peer group for quota enforcement](quotaenforcement_peergroup.html)

