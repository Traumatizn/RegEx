***Version: 1.1.2***

# URL RegEx Pattern Matchers

Regular Expression for Matching URLs (EXPERIMENTAL):
```
((?:(?<=[^a-zA-Z0-9]){0,}(?:(?:https?\:\/\/){0,1}(?:[a-zA-Z0-9\%]{1,}\:[a-zA-Z0-9\%]{1,}[@]){,1})(?:(?:\w{1,}\.{1}){1,5}(?:(?:[a-zA-Z]){1,})|(?:[a-zA-Z]{1,}\/[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\:[0-9]{1,4}){1})){1}(?:(?:(?:\/{0,1}(?:[a-zA-Z0-9\-\_\=\-]){1,})*)(?:[?][a-zA-Z0-9\=\%\&\_\-]{1,}){0,1})(?:\.(?:[a-zA-Z0-9]){0,}){0,1})
```


Matches with:
- https://example.com/first/second?q=something
- https://example.com/first/second2
- www.example.io/
- http://subdomain.example.com/
- subdomain.example.com
- https://www.subdomain.example.com
- example.com/14awOx4
- https://goo.gl
- https://example.com/first/6718633/python-regular-expression
- https://example.com/first/6718633/python-regular-expression/something?q=search
- example.com/foo/bar?baz=true&something=%20alsotrue
- http://username:password@example.com/
- https://username:password@localhost/10.0.0.1:8080
- https://localhost/10.0.0.1:8080
- localhost/10.0.0.1:8080
- https://example.com/first/second/file.html
- https://www.youtube.com/watch?v=4XL74eIIRkM&t=1s

---

### Known Issues:
- These patterns do not check for numeric min/max values (ie, max of '255' in IP Address). This may come in an update later, if requested.
- More testing is required to further identify and understand any other issues, if any.
