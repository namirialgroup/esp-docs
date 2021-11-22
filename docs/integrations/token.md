# Token

Once the authentication with the IDP service is done, ESP takes care of making a redirect to the final_url specified in the login call, with two parameters the key and id that refer to the user's session on ESP.
The third method allows receiving a JWT token containing the user's information.

> **GET sslprotected/environment_name/getUser.php**

#### Parameters

Name | Description
------------- | -------------
 **ID** | The ESP user identifier
 **key** | The ESP session key



 The [JWT](https://jwt.io/introduction) is a signed token that contains the user information. Signed tokens can verify the integrity of the claims contained within it. JSON Web Tokens are a good way of securely transmitting information between parties.
 A sample of GET-USER-JWT content is the following:


``` js
{
  "dateOfBirth": "1900-11-19",
  "domicileMunicipality": "ANCONA",
  "domicileNation": "IT",
  "placeOfBirth": "A271",
  "expirationDate": "2023-09-10",
  "domicileStreetAddress": "via sample, 11",
  "familyName": "ROSSI",
  "mobilePhone": "00393400000000",
  "address": "via sample, 11 60120 ANCONA AN",
  "email": "m.rossi@email.com",
  "domicilePostalCode": "60120",
  "name": "MARIO",
  "countyOfBirth": "AN",
  "spidCode": "NAMI0000000000",
  "gender": "M",
  "fiscalNumber": "TINIT-RSSMRA00S19A271B",
  "domicileProvince": "AN",
  "digitalAddress": "",
  "idCard": "",
  "level": null,
  "reqId": "_e709d704aa3b47eda307203119a987ac",
  "assertionId": "_71ce2354dd3222a0db8477dcb1441fec"
}

```


You can check from the JWT content using the [jwt-io-debugger](https://jwt.io/#debugger-io). You can copy and paste the token and you can see its content.