
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

```javascript
var array1 = ['a', 'b', 'c'];
var array2 = ['d', 'e', 'f'];

console.log(array1.concat(array2));
// expected output: Array ["a", "b", "c", "d", "e", "f"]
```

## Operaciones con objetos

```javascript
var an_obj = { 100: 'a', 2: 'b', 7: 'c' };
console.log(Object.keys(an_obj)); // console: ['2', '7', '100']

Object.keys( object ).length;

Object.keys( object ).map( key => object[ key ] );

var o1 = { a: 1 };
var o2 = { b: 2 };
var o3 = { c: 3 };

var obj = Object.assign({}, o1, o2, o3);
console.log(obj); // { a: 1, b: 2, c: 3 }
```

## String Transforms

```javascript
var text = '  This sentence has some whitespace at the beginning and end of it.  ';
var trimmed = text.trim();
// returns 'This sentence has some whitespace at the beginning and end of it.'
```

```javascript
var text = 'This sentence has some MIXED CASE LeTTeRs in it.';
var lower = text.toLowerCase();
// returns 'this sentence has some mixed case letters in it.'
```

```javascript
var text = 'This sentence has some MIXED CASE LeTTeRs in it.';
var upper = text.toUpperCase();
// returns 'THIS SENTENCE HAS SOME MIXED CASE LETTERS IN IT.'
```

```javascript
var text = '42px';
var integer = parseInt( text, 10 );
// returns 42
```

```javascript
var text = '3.14someRandomStuff';
var pointNum = parseFloat( text );
// returns 3.14
```

```javascript
var text = 'Cape Cod potato chips';
var startAtFive = text.slice( 5 );
var startAndEnd = text.slice( 5, 8 );
var sliceFromTheEnd = text.slice( 0, -6 );

// startAtFive: 'Cod potato chips'
// startAndEnd: 'Code'
// sliceFromTheEnd: 'Cape Cod potato'
```

## classes

```javascript
var elem = document.querySelector( '#some-elem' );

// Add a class
elem.classList.add( 'some-class' );

// Remove a class
elem.classList.remove( 'some-other-class' );

// Toggle a class
// (Add the class if it's not already on the element, remove it if it is.)
elem.classList.toggle( 'toggle-me' );

// Check if an element has a specfic class
if ( elem.classList.contains( 'yet-another-class' ) ) {
    // Do something...
}
```

```javascript
var elem = document.querySelector( 'div' );

// Get all of the classes on an element
var elemClasses = elem.className;

// Add a class to an element
elem.className += ' vanilla-js';

// Completely replace all classes on an element
elem.className = 'new-class';
```
## Styles

```javascript
var elem = document.querySelector( '#some-elem' );

// Get a style
// If this style is not set as an inline style directly on the element, it returns an empty string
var bgColor = elem.style.backgroundColor;

// Set a style
elem.style.backgroundColor = 'purple';
```

## Attributes

```javascript
var elem = document.querySelector( '#some-elem' );

// Get the value of an attribute
var sandwich = elem.getAttribute( 'data-sandwich' );

// Set an attribute value
elem.setAttribute( 'data-sandwich', 'turkey' );

// Check if an element has an attribute
if ( elem.hasAttribute( 'data-sandwich' ) ) {
    // do something...
}
```

```javascript
var elem = document.querySelector( '#some-elem' );

// Get attributes
var id = elem.id;
var name = elem.name;
var tabindex = elem.tabindex;

// Set attributes
elem.id = 'new-id';
elem.title = 'The title for this thing is awesome!';
elem.tabIndex = '-1';
```

## Event Listeners

[HTML DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)

```javascript
var btn = document.querySelector( '#click-me' );
btn.addEventListener('click', function ( event ) {
    console.log( event ); // The event details
    console.log( event.target ); // The clicked element
    
    // If the clicked element has the `.click-me` class, it's a match!
    if ( event.target.classList.contains( 'click-me' ) ) {
        // Do something...
    }
}, false);
```

## DOM Injection
```javascript
var div = document.createElement( 'div' );

// Add content to the new element
div.innerHTML = 'Your content, markup, etc.';
```

```javascript
var elem = document.querySelector('#some-element');
elem.style.display = 'none';

var elem = document.querySelector('#some-element');
elem.parentNode.removeChild( elem );
```

## Referencias
[vanilla-js-guidebook](https://zoxon.gitbooks.io/the-vanilla-js-guidebook/content/chapters/09%20-%20DOM%20Ready.html)
[neliosoftware](https://neliosoftware.com/es/blog/vanilla-javascript-es-el-futuro/)


