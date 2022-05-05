# Get Key

This endpoint return a session key that should be used to start a authentication process with SPID, CIE or EIDAS.
The following http GET call must be made to start the authentication round. Since the call is protected, the ssl certificate provided during [Assessment](../configuration.md) must be used.


> **GET sslprotected/environment_name/getKey.php**

#### Parameters

Name | Description
------------- | -------------
 **domain_uri** | The ESP domain uri
 **environment_name** | The environment path
 **level** | It's the authentication level (1-2-3)
 **attributes** | It's the attribute level (Base-Full)
 **spidType** | It's the spid purpose value (optional -  default is [physical person](https://www.agid.gov.it/sites/default/files/repository_files/spid-avviso-n18_v.2-_autenticazione_persona_giuridica_o_uso_professionale_per_la_persona_giuridica.pdf))

### N.B.
The spidType parameter is usefull only for SPID AUTHENTICATION


## Result

The response of the api is a string that must be used in the [login](./login.md) at the `authnKey` parameter.

