# js-web-sql

JS-we-sql this lib will help you save json values in sql web.

## add in your project


Import the directive into your app module.

```html
<script src="assets/lib/dati.js"></script>
```

## Usage

dati.initialize(function);

dati.insert(table, json, function);

dati.update(table, json, field, id, function);

dati.selectAll(table, function);

dati.delete(table, field, id, function);

dati.existRow(table, function);

## Example

```javascript
dati.initialize(function (status)
  {
    if (status==false)
    {
      alert('error.');
    } 
}) 
  
dati.insert("user", {"nome":"Thiago Feijór"}, function(codigo){
  //return
});
    
dati.update("user", {"nome":"Thiago Feijó"}, "CODIGO", 1, function(status){});

dati.selectAll("user", function(registros){
	//array in registros
})

dati.delete('user', "CODIGO", 1, function(){
});


dati.existRow("user", function(retorno){
    if(retorno === true){ 
      //your code
    } 
}) 
```

## Contribute

Any pull-request and issue is more than welcome.

## License

[The MIT License (MIT) Copyright (c) 2013](http://opensource.org/licenses/MIT) 
 
