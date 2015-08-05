This guide provides information on:



## Handling Exceptions ##

Lets try with invalid ci-key (-9999)

```
curl -H "Xbrlware-ApiKey: my123key" http://www.xbrlware.com/api/entities/-9999
```

This will return JSON response as below

```
{
    "status":"fail",
    "error-code":"404",
    "error-desc":"No detail exist for ci_key -9999 "
}
```

## List of error codes and descriptions ##
|Error code                      |Description                                   |
|:-------------------------------|:---------------------------------------------|
|501                             |API Key is missing in request header under name Xbrlware-ApiKey|
|502                             |Maximum requests allowed per day for your API key exceeded. Contact us at support@xbrlware.com if you want to extend your limit|
|503                             |API Key is invalid                            |
|404                             |Resource not found. All valid resources are listed [here](RESTResources.md)|
|500                             |System error. Contact us at support@xbrlware.com|