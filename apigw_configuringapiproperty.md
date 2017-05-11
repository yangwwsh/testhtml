# Adding a custom API property entry {#apigw_configuringapiproperty .task}

Based on the purpose of your APIs, you can add custom API properties. The information instructs how to add a custom API property entry.

The value of an API property is collection-specific. A custom property entry specifies one property and the property value for one collection. To add another custom property, or to specify a different property value for another collection, add another entry.

To add a custom API property, provide the following information:

-   The name of the property. The assembly actions reference the property through the property name.
-   The name of the API collection that the property value applies to. When the property value applies to all collections, use the default value asterisk \(`*`\).
-   The value of the property for the specified collection.

1.   From the API definition configuration, locate the **Custom properties** setting. 
2.   Click **Add** or **New**. 
3.   Specify the property name. 
4.   Specify the collection name. 
5.   Specify the value for the collection. 
6.   Repeat step [2](#add) - [5](#value) to add another entry. 

After an API property is created, you can access or manipulate the property value by referencing the property in the assembly actions.

**Parent topic:** [API properties](apigw_properties.md)

**Related information**  


[Accessing and manipulating an API context variable](apigw_referencingapicontextvariable.md)

