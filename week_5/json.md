# json

- a subset of javascript
- must be valid javacript syntax
- ordered list of values
- name / value pairs
- *language indepedant*

useful for storing config settings (package.json)


names: always "double-quoted"
values: can be numbers, strings or objects 

**serialization**
  -> turns an object into a string
  -> JSON.stringify();

**deserialization** 
  -> the reverse (string -> object)
  -> JSON.parse();

```javascript 
> const jsonString = '{"a":1, "b":2, "foo":"bar"}';
undefined
> jsonString
'{"a":1, "b":2, "foo":"bar"}'
> JSON.parse(jsonString)
{ a: 1, b: 2, foo: 'bar' }
> jsonString
'{"a":1, "b":2, "foo":"bar"}'
> const obj = JSON.parse(jsonString);
undefined
> obj
{ a: 1, b: 2, foo: 'bar' }
> delete obj.foo
true
> obj
{ a: 1, b: 2 }
> JSON.stringify(obj)
'{"a":1,"b":2}'
```

## json media type

HTTP headers will be labled as applicaton/json for JSON
text/html for HTML

```

}vagrant [w5]> curl -i ipinfo.io
...
content-type: application/json; charset=utf-8

{
  "ip": "x.x.x.x",
  "hostname": "sans@serif.ca",
  "region": "British Columbia",
  "timezone": "America/Vancouver",
  "readme": "https://ipinfo.io/missingauth"
}

```



# a p i

apis allow systems to work together
[bonus](https://maggieappleton.com/api)


**r e s t** 

