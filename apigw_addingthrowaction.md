# Adding a throw action for a custom error message {#apigw_addingthrowaction .task}

A throw action throws a custom error. This action ends the current assembly rule.

You can customize an error in the throw action. When the throw action is triggered, a custom error is thrown. After the throw action is triggered, the API Gateway does not run the subsequent assembly actions and the current assembly rule is ended. The thrown error, which includes an error identifier and text for the error message, is saved in the API context.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Throw Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the error identifier. 
6.   Specify the text for the error message. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

