# pro-xy-header-replace

Plugin for pro-xy, that performs user defined replaces in request or response headers.

Sample configuration

```
{
    "port": 8000,
    "logLevel": "INFO",
    "plugins": [
        "pro-xy-header-replace"
    ],
	"pro-xy-cookie-replace" : {
		"disabled": true,
		"replaces": [
			{
				"urlPattern": ".*",
				"request" : false,
				"response" : true,
				"header" : "Content-Type",
				"pattern": "text/html",
				"replacement": "text/plain"
		    }
		]
	}
}
```

Configuration consists of list of config objects with following properties:

- *urlPattern* - regular expression that will be used to test if current request will be processed by plugin
- *request* - if true, replace headers in request
- *response* - if true, replace headers in response
- *header* - name of header to replace value in
- *pattern* - regular expression to find part of header value to replace
- *replacement* - replacement value
