# Posicionando elementos con flexbox
Para este curso desde un principio se brindo el proyecto ya iniciado, una landing pages con estilos ya definidos pero los elementos aun no estaban posicionados ni se contaba con un diseño responsivo. Así que para lograr todo eso a lo largo de este curso se vio como utilizar flexbox.

## Objetivos:
* Aprender a utilizar Flexbox para posicionar los elementos en la página.
* Entender las diversas propiedades de Flexbox y como utilizarlas.
* Entender como las propiedades de Flexbox sustituyen float, inline e inline-block.
* Elaborar un sitio web responsivo con Flexbox.

## ¿Que se aprendió a lo largo de este curso?
* Utilizar el `display:flex`.
* Utilizar las propiedades `align-items` y `justify-content`.
* Utilizar la propiedad `width` para aumentar el espacio de nuestro elemento.
* Para que sirve el `space-around`, que nos permite poner espacio alrededor de los elementos.
* A utilizar la propiedad `flex-direction`, donde admite 4 valores, pero usualmente se suelen usar 2, los cuales son:
  * `column`: En forma de columna, hace que los elementos se pongan abajo uno del otro.
  * `row`: En forma de fila, hace que los elementos se pongan uno al lado del otro.
* A utilizar la propiedad `height` para setear la altura de nuestro elemento.
* A utilizar la propiedad `flex-wrap`, y con el valor `wrap` permite que cuando el contenido exceda el tamaño del padre, simplemente se rompa a la siguiente columna.
* La propiedad `flex-grow` permite establecer como se va a axpandir un elemento cada que el tamaño de pantalla también se vaya expandiendo, es decir, si establecemos como valor un número 2, el elemento se expandira 2 veces más que los otros elementos. No admite numeros negativos.
    * Por ejemplo, digamos que tenemos dos flex ítems y necesitamos que uno de esos elementos llene todo el espacio que queda del flex container1. Para decirle a un elemento/flex-item que crezca y ocupe todo el espacio que queda dentro del flex container debemos utilizar la propiedad flex-grow. Podemos poner el valor 1 para que este elemento ocupe todo el espacio.
    * Por ejemplo, si tenemos:
      Elemento 1: 200 px.
      Elemento 2: 200 px.
      Espacio vacío que restó del flex container: 600 px.
      Total: 1000 px.
      Se ponemos flex-grow: 1 en el primer elemento, este pasa a tener 800 px de ancho, es decir, espacio vacío + Elemento 1: 800 px.
      Y el segundo elemento sigue teniendo 200 px de ancho.
    * Otro ejemplo sería si tenemos 4 elementos y utilizan una misma clase, al asignar la propiedad `flex-grow` y darle el valor de 1, no se verá mucho el cambio, pero si solo al primer elemento le asignamos `flex-grow: 5`, entonces ahora el tamaño de pantalla se va a dividir entre 8 pero el primer elemento tomará 5, lo cuál lo hará ver 5 veces más grande que los otros elementos.
* La propiedad `flex-shrink` permite establecer como se va a reducir un elemento cada que el tamaño de pantalla también se vaya reduciendo, es decir, si establecemos como valor un número 2, el elemento se reducirá 2 veces más que los otros elementos. No admite numeros negativos. 
    * Se puede tomar como ejemplo, el ejemplo de `flex-grow` solo que aquí en vez de verse más grande, se verá más pequeño.
    * Por ejemplo, imaginemos que aunque el usuario reduzca la pantalla nuestro vídeo no debe disminuir de tamaño, esto se podría lograr aplicando la propiedad `flex-shrink: 0`
* La propiedad `flex-basis` permite establecer el ancho de un elemento, funciona como `width` pero solo dentro de flexbox. La propiedad `flex-basis` sirve para definir un ancho para el elemento en caso de que el "flex container" esté con `flex-direction: row` así como `flex-direction: column`.
* Una forma para utiliza las 3 propiedades juntas, es la siguiente: `flex: 1 1 300px`
  * Donde el orden de los valores es el siguiente: `flex-grow`, `flex-shrink` y `flex-basis`.