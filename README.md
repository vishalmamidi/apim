# apim
# return hello World 

```xml

<policies>
    <inbound>
        <base />
        <return-response>
            <set-status code="200" reason="Ok" />
            <set-body>Hello world!</set-body>
        </return-response>
    </inbound>
    <backend>
        <base />
    </backend>
    <outbound>
        <base />
    </outbound>
    <on-error>
        <base />
    </on-error>
</policies>

```
