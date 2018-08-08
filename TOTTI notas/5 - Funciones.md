# Funciones

una función son un conjunto de instrucciones reutilizables, que son guardadas en memoria como una variable. Su estructura basica es:

```javascript
function myFuncion() {
    ....
}
```



------

### Parametros y argumentos

**Parametro**: son las variables "locales", por asi decirlo, de las funciones.

```javascript
function my(params1,params2) {
    ...
}
```

**Argumento**: son los elementos que son pasados a esa función.

```javascript
var f = my(argum1,argum2);
```

En JS, no pasa nada si colocas un par de argumentos de más (es decir, que la funcione necesite 1 y tu les ponga 2), ya que el resto los ignorará. Sin embargo, si falta un argumento (necesita 2 y tu le pones 1) el faltante lo interpretara como "undefined".

#### Object Arguments

cabe recordar que todo en JS es un objeto, de manera que una funcion también es un objeto, que a su vez contiene a otro objeto llamado "arguments", que guarda los argumentos pasados a una función, en un array de argumentos. Ejemplo de uso

```javascript
function suma() {
	var l = arguments.length;
	var sumaT = 0, i = 0;

	while(i < l) {
		sumaT += arguments[i];
		i++;
	} 

	return sumaT;
}

var sumando = suma(20,123,41);
console.log(sumando);
```

------

### Tipos de funciones

#### Normales

son las declaradas por nombre regularmente o anónimas

```javascript
function name() {
    ...
}
// anónimas
function () {
    ...
}
    
```

#### Autoejecutables

son aquellas que podemos hacer que su contenido sea autoejecutable. Simplemente envolviendo la función entre parentesis y colocando al final el operador de invocación ().

```javascript
(function holis() {
	console.log("hola");
})();

```

#### Expresion (literal)

son aquellas funciones que son guardadas dentro de una variable.

```JavaScript
var holis = function() { // suelen ser funciones anónimas
	console.log("hola");
}
```

que también puede ser llamada por el operador de invocación. La diferencia entre las expresiones y las funciones normales, es que la primera no es elevada (hoisting). Ya que recuerda que primero es declarada la variable y luego asignado su valor (cuando esta es llamada). Por ende, representa una carga menos en la memoria.

------

### Closures

son funciones internas de una función principal...