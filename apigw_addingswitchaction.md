# Adding a switch action to choose which rule to use {#apigw_addingswitchaction .task}

An assembly switch action evaluates the input context against a list of conditions and runs the corresponding API rule of the first condition that matches. Provide conditions with JavaScript expression and use an "otherwise" clause to run a designated rule when no condition matches.

You can define a list of case statements. The order of case statements is important. The case statements are evaluated in their order and the API rule of the first condition that matches is run. The designated rule can define further switch actions.

The match condition must evaluate to true for the corresponding rule to run. The following values evaluate to false, which is also known as falsy values. All other values, including all objects, evaluate to true.

-   `false`
-   `undefined`
-   `null`
-   `0`
-   `NaN`
-   The empty string \(""\)

Do not confuse the primitive boolean values `true` and `false` with the true and false values of the Boolean object.

When no condition matches, you can use an "otherwise" clause to define the API rule to run.

-   When defined, the designated API rule runs.
-   When not defined, the DataPower® Gateway executes the next action that follows the switch action in the assembly.

When an error occurs during the execution of the selected rule, the transaction is aborted.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Switch Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify a case. 
    1.   Click **Add** or **New**. 
    2.   Enter the condition. 
    3.   Specify the API rule to run when the condition matches. 
    4.   Click **Apply**. 
6.   Repeat the previous step to add another case. 
7.   Specify the API rule to run when no condition matches. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

