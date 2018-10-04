# Busqueda y filtrado en el DOM

**Ejemplo:** Buscar y filtrar elementos

```JavaScript
$(document).ready(fucntion(){
    // Forma 1 : Selecciona el primer parrafo seguido del hijo de section
    // con la clase contenido
    $('section.contenido p:first-of-type');

    // Forma 2 : Realiza lo mismo que lo anterior pero con una sintaxis 
    // mas comoda
    $('.contenido').find('p').first();

    // Aplica estilo css al 3 parrafo encontrado
    $('.contenido').find('p').eq(2).css('color', 'red');
});
```