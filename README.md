Connecting DataPower Gateway to Product Insights to report usage information
IBM® Cloud Product Insights, an IBM Bluemix® service, allows you to connect your DataPower Gateway to report registeration and usage information. When a DataPower Gateway is configured to connect to a Product Insights service instance, the following information is reported and can be viewed in Product Insights dashboards:

//Need to update and rephrase in English words
- hostName
- installDirectory: this should be the directory where the DataPower Gateway is installed
- instanceIdentifier
- environmentType
- startTime
- endTime
- Modules
- TOTAL_FREE_ENCRYPTED_FILE
- TOTAL_ENCRYPTED_FILE
- TOTAL_FREE_TEMPORARY_FILE
- TOTAL_TEMPORARY_FILE
- TOTAL_FREE_INTERNAL_FILE
- TOTAL_INTERNAL_FILE
- TIME
- UPTIME
- BOOTUPTIME
- MEMORY_USAGE  
- TOTAL_SYSTEM_MEMORY: Total system memory
- TOTAL_USED_MEMORY
- TOTAL_FREE_MEMORY


## Before you begin
Before you connect a DataPower Gateway to the Product Insights service, you must have an IBM Bluemix account and create the Product Insights service in an organization and space. Follow the [Product Insights getting started information](https://developer.ibm.com/product-insights/docs/getting-started/) to set up an account and create the service.

## Procedure
To report DataPower registeration and usage data to the Product Insights service, proceed as follows:
1. Copy the API key and API host values from your Product Insights service instance.
2. With the API key and host information, configure the DataPower Gateway to connect to the Product Insights service instance.
   a. In the DataPower GUI, search `Product Insights`.
   b. From the search result, click `Product Insights`.
   c. In the **Service Host** field, enter the API host that you copied from your Product Insights service instance.
   d. In the **Service credentials** field, enter the API key that you copied from your Product Insights service instance.
   e. In the **Interval** field, enter the interval to send data to the Product Insights service. //Under discussion whether to allow users to set the interval
   f. To connect through an HTTP proxy, provide the following settings:
      - Server name
      - User ID
      - Password
   g. Click **Apply** to save the changes to the running configuration.
   h. Click **Save configuration** or **Save config** to save the changes to the persisted configuration.

## Results
The DataPower registeration and usage data is sent to your Product Insights service instance.
You should be able to view the data through your Product Insight Service instance on Bluemix.

## More information
For details about how DataPower Gateway integrates with Product Insights, see the DataPower Gateway information on IBM Knowledge Center.
For information about how to use Product Insights at run time, see the Bluemix documentation at [About IBM Product Insights](https://console.ng.bluemix.net/docs/services/product-insights/product-insights_overview.html#about_product-insights?cm_sp=dw-bluemix-_-product-insights-_-devcenter).
