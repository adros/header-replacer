# pro-xy-header-replace

Plugin for pro-xy, that performs user defined replaces in request or response headers.

TODO document config

	"pro-xy-header-replace" : [{
		"urlPattern": ".*",
		"request" : false,
		"response" : true,
		"header" : "Set-Cookie",
		"pattern": "mycookie",
		"replacement": "newcookie"
	}],
