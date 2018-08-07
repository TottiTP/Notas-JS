# Como funciona el Scope y Hoisting

Primero debemos entender como funciona JS para procesar todo el código. Por ejemplo

```javascript
var variable = 2:
```

Primero el compilador divide eso en tokens y luego los organiza con el AST. Posteriormente le pregunta  al Scope (ámbito) si en su lista de variables declaradas ya existe, si es asi, entonces ignora su compilación, caso contrario le pide al scope que la registre. Luego viene el Motor (responsable de la compilacion y la ejecusion del codigo) si ve que existe tal variable en el Scope, le asigna el valor de = 2. Si no, pues salta un error.

En definitiva, la primera "lectura" del código se basa en registrar o verificar que la variable exista y luego cuando esta vaya a ser llamada o ejecuta, se le asigna el valor correspondiente (con ayuda del AST).

**Hoisting (elevación)**

cuando el compilador encuentra un *var* lo eleva al máximo nivel de su ámbito, por ejemplo en una funcion lo pone de primero. Si es por ejemplo una funcion, primero la eleva y luego la declara.

He aqui un ejemplo raro (que es mala practica, por cierto, pero puede explicar un poco)

```javascript
test(); // es declarada, pero anteriormente ya el motor de JS la habia elevado. Por lo cual se puede usar antes de haberse creado.

// esta función es puesta por delaante de lo anterior (lo eleva)
function test() {
    x = 2; // cuando es solicitada la variable, es que se le asigna el valor a x.
    
    var x; // esta variable es puesta en la primera linea de la funcion
    return x; // 2
}

```

**Importante**

toda variable declara con "var" estara disponibles en los ambitos inferiores. Pero si se declara una variable con "let", dicha variable solo estara disponible en el ámbito o bloque de ({}) donde se encuentre.