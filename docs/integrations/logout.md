# Logout

This page contains the reference for the logout SPID method (NOT NECESSARY FOR SECOND LEVEL AUTHENTICATIONS!)

> **GET environment_name/logout**

#### Parameters

Name | Description
------------- | -------------
 **domain_uri** | The ESP domain uri
 **environment_name** | The environment path
 **final** | It's the redirect url called at the end of the authentication process (It should be comunicated during the assessment phase)

## Result

The address that is constructed must then be copied and pasted into the address bar of a browser. The page that opens can be
- logout screen for SPID identity provider

## Logout Succeded

After a succeded logout the user will be redirected to the final url parameter.
