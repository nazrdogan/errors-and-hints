
* ### [Discover single tables](https://github.com/nazrdogan/errors-and-hints/blob/master/discover-schema.js)
      https://github.com/strongloop/loopback.io/issues/347
      
* ### Primary key is missing for the *ModelName* model
   "id":true

```javascript
"idInjection": false,
"properties": {
    "contact_id": {
      "type": "number",
      "generated": true,
      "id":true,
      "required":false,
      "doc":"This is the primary ID used to identify a contact"
    },
```


### ID values incorrectly stored as plain strings in relation tables for mongodb 

https://github.com/strongloop/loopback/issues/274#issuecomment-182077347  

    
### Loopback before save 

```

Product.observe('before save', function setAutoData(context, next) {
		if (context.instance) {
			if (context.isNewInstance) {
				context.instance.created = Date.now();
				context.instance.ownerId = context.options.accessToken.userId;
			}
			context.instance.modified = Date.now();
		}
		next();
	});
      
```      
    
