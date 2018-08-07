# Variables

una variable es un fragmento de memoria que es reservada para guardar información (datos) y que pueden ser utilizados a lo largo de un programa.

En JavaScript, las variables se pueden declarar colocando primero la palabra "var" o "let"

## Tipos de valores

JS tiene varios tipos de valores; boolean, numeros, string, undefined, objeto y null

Casi todos los tipos de valores son objetos (number, string, array, object inclusive, function), por lo cual cuenta tienen propiedades y metodos.

```javascript
var a; // valor indefinido
typeof undefned; // "undefined"
undefned = "hello world";
typeof string; // "string"
numb = 42;
typeof numb; // "number"
booolano = true;
typeof booolano; // "boolean"
nulo = null;
typeof nulo; // "object" -- weird. Bug
unde_2 = undefined;
typeof unde_2; // "undefined"
a = { b: "c" };
typeof a; // "object"
```

Las variables pueden devolver un valor de tipo undefined, si por ejemplo esta no tiene ningún valor.

*typeof* devuelve el tipo de valor. Más no devuelve el tipo de variable, ya que las variables son simplemente contenedores de información. Es el tipo de valor que se guarda en ella, que determina la variedad. Ya que las variables en JavaScript son debilmente tipados.

además por un error antiguo de JS, una variable de valor "null" devolvera que es ''object".

```javascript
var a = {propiedad: "jeje"};
var str = typeof a;

console.log(str); // devuelve "object" (en un array)

```

Que estas altura no se puede arreglar, ya que los programadores tendrian que cambiar mucho código y se les romperia todos los proyectos.