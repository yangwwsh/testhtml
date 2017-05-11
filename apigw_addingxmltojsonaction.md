# Adding a convert XML to JSON action {#apigw_addingxmltojsonaction .task}

An XML to JSON action converts the payload of an API context from the extensible markup language \(XML\) format to JavaScript Object Notation \(JSON\) object.

The XML to JSON conversion is based on BadgerFish. The XML content is preserved, including the attributes and namespaces. .

When this action is triggered, it reads input from the message.body context variable if this context exists. Otherwise, it reads input from the request.body context variable. No additional configuration is required. The conversion output is stored in the message.body context variable.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly XML to JSON Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 

## Examples { .example}

-   The `<a>hello</a>` XML-formatted document is converted to the following JSON-formatted object.

    ```
    { "a": { "$" : "hello" } }
    ```

-   The `<a type="world">hello</a>` XML-formatted document with an attribute is converted to the following JSON-formatted object.

    ```
    { "a": { "$" : "hello", "@type" : "world" } }
    ```


**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

**Related information**  


[BadgerFish](http://badgerfish.ning.com)

[Variables in the API context](apigw_contextvariables.md)

