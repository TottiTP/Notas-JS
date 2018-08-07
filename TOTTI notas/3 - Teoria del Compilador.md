# Teoria del Compilador

Si bien se dice que JS es un lenguaje interpretado, realmente tiene un compilador que se ejcuta segundos antes y luego procesa el código. Por ello es que muchos navegadores usan técnica para optimizar y ahorrar energia.

El compilador cuenta con un par de fases primordiales para la conversión de código a lenguaje maquina.

Tokenizing (o seperacion de elemento): rompe una cadena de caracteres en pedazos significativos (llamados tokens) que luego en otro proceso guarda en un array de tokens. Ejemplo 

```javascript
var variable = 2;
/*
	es dividido en
	var
	variable
	=
	2
	;
*/
```

Arbol de Sintaxis Abstrato (AST en ingles): toma ese array de tokens y los coloca en forma de arbol anidado, construyendo asi la gramatica estructural del programa. Convirtiendo finalmente el código a lenguaje maquina

Siguiendo el ejemplo anterior, todos esos tokens son anidados de manera gramatical de la siguiente manera

```javascript
// variable es guardado en un nodo
// = 2 es guardado en otro
```

------

El motor de JS, a la hora de buscar información trabaja de la siguiente manera

RHS (busca la fuente del lado derecho). Por ejemplo *var tt = 2;* aqui buscó y tomo el número 2.

LHS (quien es el destino de la asginado del lado izquierdo). Por ejemplo *var tt = 2;* aqui buscó y tomo "tt"

lo mismo pasa con los objetos.

Ejemplo (examen)

```javascript
function foo(a) { 
    var b = a; 
    return a + b; 
} 
var c = foo( 2 ); 
```

1. Identifique todas las consultas LHS (hay 3!). 
   - a = 2
   - c = ...
   - b 
2. Identifique todas las consultas RHS (hay 4!). 
   - = a
   - +b 
   - a+
   - foo(a)

