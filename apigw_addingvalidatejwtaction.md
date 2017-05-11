# Adding a validate JWT action {#apigw_addingvalidatejwtaction .task}

A validate JWT action defines the cryptographic material and methods to validate a JSON Web Token \(JWT\) in an API call to secure access to your APIs.

The validate JWT action extracts the JWT in the API call, verifies and decrypts the JWT, validates the claims, and stores all the claims into a context variable for subsequent use when the JWT validation succeeds. In a validate JWT action, you define the following settings.

-   The JWT to be validated.

    **Note:** The format of the authorization header must be `Authorization: Bearer jwt-token`, where jwt-token indicates the encoded JWT.

-   Where to put all the claims that the JWT contains when the JWT validation succeeds.
-   Optionally, values to use to validate the issuer claim or audience claim in the JWT.
    -   When no value is specified, the action validates only the expiration "`exp`"claim and the not before "`nbf`" claim in the JWT.
    -   When any value is specified, the action also validates the specified claim. If any specified claim fails, the JWT validation fails.
-   The cryptographic material to decrypt or verify a JWT. The following guidelines apply.
    -   You can use a cryptographic object or a JWK to decrypt or verify the JWT. When both a cryptographic object and a JWK are specified, the cryptographic object is used.
    -   If the original message is signed with a shared secret key, the cryptographic object that is specified must also be a shared secret key.
    -   If the original message is signed with a private key, the cryptographic object that is specified must be a crypto certificate \(public certificate\).
    -   If a JWK header parameter is included in the header of the JWT, the parameter must match the cryptographic object or JWK that is specified in the action. Otherwise, the JWT validation fails.

When the JWT validation succeeds, all the claims that the JWT contains are written to the specified context variable. When an error occurs, the action throws an error.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly Validate JWT Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the context variable that contains the JWT to be validated. 
6.   Specify a context variable to store all the claims that the JWT contains. After processing, the output data type is object.
7.   Specify the value to use to validate the issuer "`iss`" claim. 
8.   Specify the value to use to validate the audience "`aud`" claim. 
9.   When the JWT is encrypted, specify the cryptographic material to decrypt the JWT. You can specify a cryptographic object \(a shared secret key or certificate\) or a context variable that contains the JWK to use to decrypt the JWT.
10.  When the JWT is signed, specify the cryptographic material to verify the JWT. You can specify a cryptographic object \(a shared secret key or certificate\) or a context variable that contains the JWK to use to verify the JWT.
11.  Click **Apply** to save the changes to the running configuration. 
12.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

