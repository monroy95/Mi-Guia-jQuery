# Manipular el DOM sin jQuery (Eventos)

## Primeros pasos
No siempre puede llegar a ser necesario utilizar jQuery, en estos ejemplos mostrare que se puede hacer con vanilla JS.
### EVENTOS

**Ejemplo**: Escuchar evento del DOM cuando el documento se ha cargado 'DOM Content Loaded'
```javascript
document.addEventLister('DOMContentLoaded', function () {
  console.log('DOM Cargado');
});
```
**Ejemplo**: Para capturar un elemento del HTML podemos utilizar `querySelector` 
```javascript
// Capturara todos los elementos con la etiqueta 'a'
var enlace = document.querySelector('a');

console.log(enlace);
```
Nos mostrara el elemento que estamos consultado de la siguiente manera:

```HTML
<a href='#'>Esto es un enlace</a>
```

**Ejemplo:** Agregar evento a un elemento seleccionado, utilizaremos el elemento seleccionado anteriormente
```javascript
// Cada vez que realizemos un click sobre el enlace, se mostrara el mensaje 'click'
enlace.addEventListener('click', function (event) {
  console.log('Click');
})
```
#### `preventDefault`
Sirve a prevenir el comportamiento por default.

**Ejemplo:** En este ejemplo se esta previniento el comportamiento por default de la etiqueta `a` que nos direcciona a una direccion en especifico.
```javascript
var mi_enlace = document.querySelector('a');

// Cada vez que realizemos un click sobre el enlace, se mostrara el mensaje 'click'
mi_enlace.addEventListener('click', function (event) {
  event.preventDefault();
  console.log('Click');
})
```
