# Adding a parse action to the assembly {#apigw_addingparseaction .task}

An assembly parse action controls the parsing of an input document which can be an XML or JSON document, or binary data from the API context. When a parse action is configured for an assembly rule, the parse settings that are associated with the parse action override the corresponding parser limits for input documents that are set by the XML manager.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Parse Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   In the **URL reference** field, specify the URL to retrieve parse settings. 
6.   In the **Literal configuration** field, specify parse settings with an XML or JSON text string with parameters and their values. 
7.   From the **Object reference** list, select the parse settings configuration object from which to retrieve its properties as the default settings for this action. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

