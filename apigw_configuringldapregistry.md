# Creating an API LDAP registry {#apigw_configuringldapregistry .task}

Create an API LDAP registry to define the LDAP server to authenticate incoming API requests.

LDAP registries can be used to authenticate users to APIs. You must provide the following data.

-   The LDAP host name and port
-   Optionally, the SSL client profile to secure connections
-   The LDAP version, DN, and password alias of the LDAP administrator password for the bind operation
-   The LDAP search parameters to retrieve user information from the LDAP server
-   The time to wait for a response from the LDAP server

1.   In the search field, enter API. 
2.   From the search results, select **API LDAP Registry**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Enter the host name or IP address of the LDAP server. 
6.   Enter the listening port on the LDAP server. 
7.   Select the SSL client profile to secure connections between the API Gateway and the LDAP server. 
8.   Select the LDAP version to use for the bind operation. 
9.   Enter the distinguished name \(DN\) to bind to the LDAP server for the LDAP search. 
10.  Select the password alias of the LDAP administrator password to bind to the LDAP server for the LDAP search. 
11.  Specify the LDAP search parameters to perform an LDAP search to retrieve the user DN. 
12.  Enter the time to wait for a response from the LDAP server before the API Gateway closes the LDAP connection. A value of 0 indicates that the connection never times out.
13.  Click **Apply** to save the changes to the running configuration. 
14.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

Associate the LDAP registry to a basic authentication security definition.

**Parent topic:** [API security](apigw_securitydefinitions.md)

**Related information**  


[Creating LDAP search parameters](ldapsearchparameters.html)

[Creating a basic authentication security definition](apigw_securitydefinitions_basicauth.md)

