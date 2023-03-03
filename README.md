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
### return hostname
```
        <return-response>
            <set-status code="200" reason="Ok" />
            <set-body>@(context.Request.OriginalUrl.Host)</set-body>
        </return-response>
```
### return hostname
```
        <return-response>
            <set-status code="200" reason="Ok" />
            <set-body>@(context.Request.Url.Path)</set-body>
        </return-response>
```
```
        <return-response>
            <set-status code="200" reason="Ok" />
            <set-body>@(context.Request.Headers.GetValueOrDefault("x-original-host","notfound"))</set-body>
        </return-response>
```

