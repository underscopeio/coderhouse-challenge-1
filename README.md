## Challenge

Transformar en la nueva sintaxis cada uno de los siguientes _snippets_


```js
var React = require('react')
var Component = React.Component
```


```js
// El valor de PI nunca debería cambiar
var PI = 3.141592

var acumulador = 0
if (true) {
  acumulador = acumulador + 10
}
```


```js
function sumar(a, b) {
  return a + b
}
```


```js
function sumar(a, b) {
  a = a === undefined ? 1 : a
  b = b === undefined ? 2 : b
  return a + b
}
```

```js
function procrear(nombre, edad) {
  return {
    nombre: nombre,
    edad: edad,
  }
}
```


```js
var hijo = {
  nombre: 'Juan',
  edad: 30,
  padre: {
    nombre: 'Pedro',
    edad: 90,
  },
}

var nombreHijo = hijo.nombre
var edadPadre = hijo.padre.edad
```


```js
var nombre = 'Juan'
var apellido = 'Perez'
var edad = 40

// Notar como se mezclan el operador + de strings con el + de números cuando hacemos (50 - edad)
console.log('El señor' + nombre + ' ' + apellido + ' va a cumplir 50 dentro de ' + (50 - edad) + ' años')
```
