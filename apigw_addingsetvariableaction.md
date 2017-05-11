# Adding a set variable action {#apigw_addingsetvariableaction .task}

You can add an assembly set variable action to set, add, or clear the variables in the API context.

You can use the following action to set, add, or clear a variable in the API context:

-   The set action assigns value to a variable:
    -   When the specified variable does not exist, a new variable is created with assigned value.
    -   When the specified variable exists and it is not read-only, the configured value overrides the existing value.
-   The add action adds a variable. This action can add a new header or append a new entry of the same header.
-   The clear action deletes a variable. This action can remove a header when the data is processed in the assembly flow.

When you assign value to a variable, follow these rules. Otherwise, error occurs and the current set variable action is ended.

-   The value must match the specified data type, number, string, or boolean.
-   You cannot add the `message.status.code` variable. Instead, you can set it. The data type of this variable must be number, and the assigned value must be a three-digit integer from 100 through 999.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Set Variable Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the set variable actions. 

    |Action|What to do|
    |------|----------|
    |****Add****Set****|     1.  Specify the variable name.
    2.  \(Optional\) Specify the data type of the variable.
    3.  Assign proper value to the variable.
 |
    |****Clear****|Specify the variable name.|

6.   Click **Apply** to save the changes to the running configuration. 
7.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

**Related information**  


[Variables in the API context](apigw_contextvariables.md)

