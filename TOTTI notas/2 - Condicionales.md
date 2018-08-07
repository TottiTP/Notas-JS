# Condicionales

una condición, es la instrucción dada a las diferentes comparaciones que se puedan realizar a lo largo de un programa. Exsten las siguientes

### Operador Ternario

el operador de una sola linea u Operador Ternario, se basta simplemente de una estructura de true y false. Ejemplo:

```javascript
// estructura
condicion ? valor_true : valor_false;

(5 === 5) ? true : false; // true
```

------

### Sentencias if, else, y else-if.

Las condiciones mas usadas para comparar valores son:

```javascript
if(1 > 5) {
    // si es true
}
else if (1 === 5) {
    // si el anterior if fue false, pasa a este
}
else {
	// si ninguno de los dos dió true, entonces queda esto por ultimo (el caso false)
}
```

------

### Switch

esta condición, es una forma mas dinamica, por asi decirlo, de realizar if, else if, es decir que según el case, se ejecutara una instrucción ejemplo:

```javascript
switch(condicion) {
    case 0: {
        break;
    }
        
    case 1: {
   		break;     
    }
        
    default: console.log("ninguno");
}
```

cada "case" funciona como un else if (si no..) y default, funciona como un else final. Es necesario colocar un break, en caso de que queramos detener la ejecusión. Ya que si no lo hacemos, el switch funciona como especie de loop, en donde pasara por cada caso, independientemente de si es el correcto o no.