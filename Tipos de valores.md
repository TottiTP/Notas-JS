# Tipos de valores

Casi todos los tipos de valores son objetos (number, string, array, object inclusive, function), por lo cual cuenta tienen propiedades y metodos.

JS tiene varios tipos de valores; boolean, numeros, string, undefined, objeto y null

```javascript
var a;
typeof a; // "undefined"
a = "hello world";
typeof a; // "string"
a = 42;
typeof a; // "number"
a = true;
typeof a; // "boolean"
a = null;
typeof a; // "object" -- weird, bug
a = undefined;
typeof a; // "undefined"
a = { b: "c" };
typeof a; // "object"
```

Las variables pueden devolver un valor de tipo undefined, si por ejemplo esta no tiene ningún valor.

*typeof* devuelve el tipo de valor en un string. Más no devuelve el tipo de variable, ya que las variables son simplemente contenedores de información. Es el tipo de valor que se guarda en ella, que determina la variedad.

además por un error antiguo de JS, una variable de valor "null" devolvera que es ''object".

```javascript
var a = {propiedad: "jeje"};
var str = typeof a;

console.log(str); // devuelve "object" (en un array)

```

