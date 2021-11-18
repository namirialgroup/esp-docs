# Token

Once the authentication with the IDP service is done, ESP takes care of making a redirect to the final_url specified in the login call, with two parameters the key and id that refer to the user's session on ESP.
The third method allows receiving a JWT token containing the user's information.

> **GET sslprotected/<environment_name>/getUser.php**

#### Parameters

Name | Description
------------- | -------------
 **ID** | The ESP user identifier
 **key** | The ESP session key