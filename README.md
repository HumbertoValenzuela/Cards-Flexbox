# Cards-Flexbox
Responsive Cards usando Flexbox

```javascript
body {
    box-sizing: border-box;
    background-color: #f2f2f2;
}
```
* Se agrega ancho máximo.
* Se agrega margin notar que se mueve a la derecha

```javascript
.contenedor {
    max-width: 1100px;
    margin: 0 auto;
}
.contenido-principal {
    display: flex; /*article quedan en row*/
   
} 
.contenido-principal {
    display: flex; /*article quedan en row*/
    flex-wrap: wrap;/*article queda en columna*/
} 
img {
    max-width: 100%;/*Con esto la imagen será Responsive*/
}
h2 {
    /* Para que este en la parte superior */
    flex: 0  1 100%; /* 0 para que no cresca y una base de 100%*/
}

```
* Agregando Media Queries a los Cards

```javascript
@media screen and (min-width:480px) {
    .contenido-principal {
        display: flex; /*article quedan en row*/
        flex-wrap: wrap;/*article queda en columna*/
    } 
}

```
* Al insertar el media query no cambiará hasta cuando le demos ancho a la class=”entrada”

```javascript
.entrada {
        /*grow 0 para que no crezca, shrink 1 y basis crecerá como minímo del 50%*/
        flex: 0 1 calc(50%);
    }

@media screen and (min-width:480px) {
    .contenido-principal {
        display: flex; /*article quedan en row*/
        flex-wrap: wrap;/*article queda en columna*/
        /* para separar las imagenes justify-content: space-between;*/       
        justify-content: space-between;
    } 
    .entrada {
        /*grow 0 para que no crezca, shrink 1 y basis crecerá como minímo del 50%*/
        flex: 0 1 50%;
    }
```

* Debido a que la separación se debe dar en el basis, usando la función calc(50% - 20px)
* Space-between, junto con basis calc(50% - 1rem)
```javascript
.contenido-principal {
        display: flex; /*article quedan en row*/
        flex-wrap: wrap;/*article queda en columna*/
        /* para separar las imagenes justify-content: space-between;*/       
        justify-content: space-between;
    } 
    .entrada {
        /*grow 0 para que no crezca, shrink 1 y basis crecerá como minímo del 50%*/
        flex: 0 1 calc(50% - 1rem);
    }

```

* Crear otro Media Query para escritorio. Para que muestre los Cards en 3 columna
```javascript
@media screen and (min-width:768px) {
/*3Columnas para Cards en modo Escritorio*/
    .entrada {
    /*grow 0 para que no crezca, shrink 1 y basis crecerá como mínimo del 33%*/
    flex: 0 1 calc(33% - 1rem);
    }
}

```
* Estilos a los cards
```javascript
h2 {
    /* Para que esté en la parte superior */
    flex: 0  1 100%; /* 0 para que no crezca y una base de 100%*/
    text-align: center;
}
h3 {
    /* font de google */
    font-family: Libre Baskerville, serif;
    /* font google por default trae margin */
    /* margin: 0; */
    font-size: 1.8rem;
}
.contenido h3 {    
    font-size: 0.9rem;
    /* Interlineado */
    line-height: 1.4rem;
    /* Mayusculas*/
    text-transform: uppercase;
}
.entrada {
    margin-bottom: 1rem;
    box-shadow: 10px 10px 5px rgba(15, 15, 15, 0.5);
}
.contenido {
    background-color: #fff;    
    /* centrar todos los elementos de Card */
    text-align: center;
    /* Separación entre elemento imagen*/
    padding: 2rem;
     /* Mayusculas*/
    text-transform: uppercase;
    
}

.contenido h3 {    
    font-size: 0.9rem;
    /* Interlineado */
    line-height: 1.6rem;
}
p { 
    line-height: 1.6rem;
}
a{
    line-height: 1.6rem;
    margin-top: 1rem;
}
.contenido span {
    color: rgb(248, 10, 220);
}

```
* Botón 
```javascript
.boton {
    background-color: #008fd1;
    color: #fff;
    padding: 0.6rem 3rem;
    display: inline-block; /* con esto respetara el padding definido*/
    text-decoration: none;
}
```
