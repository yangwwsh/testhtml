# API properties {#concept_qf2_my4_3z .concept}

An API property is a type of context variable whose value is dependent on the API collection that the API is provisioned in. Collection-specific API properties allow you to use the same API definition in different API collections when a property in a collection requires a unique or different value.

You can access and manipulate the API properties by referencing an API property in the assembly actions. For example, you might configure an assembly if action that executes its case when the API request is routed to a particular API collection, which determines the value of the API property for the case.

After an API property is created, the assembly actions can then reference the API property through the property name.

-   **[Adding a custom API property entry](apigw_configuringapiproperty.md)**  
Based on the purpose of your APIs, you can add custom API properties. The information instructs how to add a custom API property entry.

**Parent topic:** [Developing APIs](apigw_configuringapi.md)

