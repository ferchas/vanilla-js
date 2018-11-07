
## Seleccionar elementos del DOM

```javascript
var element = document.getElementById( 'element' );
var links = document.getElementsByClassName( 'some-class' );
var articles = document.getElementsByTagName( 'article' );

var elemCarrots = document.querySelector( '[data-snack="carrots"]' );
var elemRed = document.querySelector( '.bg-red' );
var elemsByClass = document.getElementsByClassName( 'some-class' );
```

####  Array of elements

```javascript
var links = document.querySelectorAll( '.some-class' );
var articles = document.querySelectorAll( 'article' ); 
```

## Moverte por el DOM

```javascript
var firstElement = document.getElementById( 'list' ).getElementsByTagName( 'li' )[0];
var nextElement = firstElement.nextElementSibling;
```

## Set y Get de atributos

```javascript
var element = document.getElementById( 'element' );

var scale = element.getAttribute( 'data-scale' );
element.setAttribute( 'data-scale', scale + 10 );

var classAttr = element.getAttribute( 'class' );
element.setAttribute( 'class', classAttr + ' some-class' );
```

## Operaciones con múltiples nodos

```javascript
var links = document.getElementById( 'post' ).getElementsByTagName( 'a' );
for ( i = 0; i < links.length; ++i ) {
  links[ i ].className += ' post-link';
}
```

## Operaciones con arrays

```javascript
var list = ['a', 'b', 'c'];

list.forEach( (e, index) => console.log(e, index) );

var newList = list.map( e => e+1 );

var value = list.reduce((valorAnterior, valorActual, indice, vector) => valorAnterior + valorActual );

var bool = list.every( e => isNaN(e) );

var bool = list.some( (e, index, array) =>  e >10 );

document
  .querySelectorAll( '#post a' )
  .forEach( a => a.className += ' post-link' );
```

## Operaciones con objetos

```javascript
var an_obj = { 100: 'a', 2: 'b', 7: 'c' };
console.log(Object.keys(an_obj)); // console: ['2', '7', '100']

Object.keys( object ).length;

Object.keys( object ).map( key => object[ key ] );
```



