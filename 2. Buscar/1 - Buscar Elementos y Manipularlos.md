# Buscar elementos en el DOM y manipularlos

jQuery en si es un motor de selección, en base a selectores css

**Ejemplo:** Ejecutar algo cuando el DOM este listo
```javascript
$(document).ready(function(){
    console.log('El DOM se ha cargador con exito');
})
```

## Seleccionar elementos del DOM
**Ejemplos**
```javascript
$(document).ready(function(){
    // Seleccion descendientes directos: Seleccionara el elemento img
    // que se encuentra seguido de aside
    $('aside > img').fadeOut('slow'); // Tendrá un efecto de desvanecimiento

    // Busqueda de elemento y asigna estilo css
    $('a span').css('color', 'blue');

    // Seleccion múltiple
    $('a, spna, p').slideToggle(); // Tendra un efecto de compresion

    // Pseudo Clases: Selecciona el primer elemento parrafo que encuentre
    $('p:first').css({
        'font-weight': 'bold',
        'color':'goldenrod'
    });

    // Selecciona el ultimo parrafo
    $('p:last').css({
        'font-weight': 'bold',
        'color':'goldenrod'
    });

    // Selecciona los parrafos pares
    $('p:even').css({
        'font-weight': 'bold',
        'color':'goldenrod'
    });

    // selecciona los parrafos impares
    $('p:add').css({
        'font-weight': 'bold',
        'color':'goldenrod'
    });
});
```