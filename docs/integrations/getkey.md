# Get Key

This endpoint return a session key that should be used to start a authentication process with SPID or CIE.
The following http GET call must be made to start the authentication round. Since the call is protected, the ssl certificate provided during [Assessment](../configuration.md) must be used.


> **GET sslprotected/environment_name/getKey.php**

#### Parameters

Name | Description
------------- | -------------
 **domain_uri** | The ESP domain uri
 **environment_name** | The environment path
 **level** | It's the authentication level (L1-L2-L3)
 **attributes** | It's the attribute level (Base-Full)


## Result

The response of the api is a string that must be used in the [login](./login.md) at the `authnKey` parameter.

