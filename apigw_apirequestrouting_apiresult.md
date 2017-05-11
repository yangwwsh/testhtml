# Response preparation {#apigw_apirequestrouting_apiresult .concept}

The API Gateway runs the API result action to prepare responses to the client based on the result from the API execute action.

The API result action examines whether the result of the API execute action contains unhandled errors:

-   If yes, the API result action prepares a JSON error object and sends the object to the client as the response. The error object takes the following format:

    ```
    { "name": <error name>, "message": <error message> }
    ```

-   If no, the API result action reads the API context and uses the variables `message.body`, `message.headers`, `message.status.code`, and `message.status.reason` to compose the response to the client.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)

