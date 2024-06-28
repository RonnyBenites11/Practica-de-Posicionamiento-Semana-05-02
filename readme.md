# Posicionamiento
- Determina cómo se colocan los elementos en una página web. Existen varios valores que puedes utilizar con la propiedad position para controlar la disposición de los elementos.
## Position: Relative
- El elemento se posiciona de acuerdo con el flujo normal del documento, pero se puede desplazar utilizando top, right, bottom y left.
```css
div {
  position: relative;
  top: 10px; /* Desplaza 10 píxeles hacia abajo */
  left: 20px; /* Desplaza 20 píxeles hacia la derecha */
}
```
## Position : Absolut
-  El elemento se posiciona en relación a su contenedor más cercano que no tenga position: static. Si no hay tal contenedor, se posiciona en relación al elemento <html>.
```css
.container {
  position: relative; /* Contenedor para el elemento absoluto */
}

.elemento {
  position: absolute;
  top: 10px; /* 10 píxeles desde la parte superior del contenedor */
  left: 20px; /* 20 píxeles desde la parte izquierda del contenedor */
}
```
## Position : Fixed
- El elemento se posiciona en relación a la ventana de visualización. Permanece fijo en la misma posición incluso cuando se desplaza la página.
```css
.elemento {
  position: fixed;
  top: 10px; /* 10 píxeles desde la parte superior de la ventana */
  right: 0; /* Pegado al borde derecho de la ventana */
}
```
## Position : sticky
- El elemento se comporta como relative hasta que su posición de desplazamiento alcanza un umbral definido, momento en el cual se comporta como fixed.
```css
.elemento {
  position: sticky;
  top: 0; /* Se vuelve fijo al alcanzar la parte superior de la ventana */
}
```
# Propiedades del posicionamiento
### Top
- Define la distancia entre el borde superior del elemento y el borde superior de su contenedor de referencia.
- Desplaza el elemento hacia abajo cuando es positivo, y hacia arriba cuando es negativo.
### Right
- Define la distancia entre el borde derecho del elemento y el borde derecho de su contenedor de referencia.
- Desplaza el elemento hacia la izquierda cuando es positivo, y hacia la derecha cuando es negativo.
### Bottom
- Define la distancia entre el borde inferior del elemento y el borde inferior de su contenedor de referencia.
- Desplaza el elemento hacia arriba cuando es positivo, y hacia abajo cuando es negativo.
### Left
- Define la distancia entre el borde izquierdo del elemento y el borde izquierdo de su contenedor de referencia.
- Desplaza el elemento hacia la derecha cuando es positivo, y hacia la izquierda cuando es negativo.
# Propiedad de Amnpliamiento
### Z-Index
- Controla el orden de apilamiento de los elementos posicionados (es decir, qué elementos se superponen a otros).
- Los elementos con mayor valor de z-index se apilan por encima de los elementos con menor valor. Solo tiene efecto en elementos que tienen position diferente de static.
- Puede ser un número positivo, negativo, o cero. Los elementos con valores z-index más altos se muestran sobre aquellos con valores más bajos.
```css
.elemento1 {
  position: absolute;
  z-index: 1; /* Se apilará por debajo de .element2 */
}

.elemento2 {
  position: absolute;
  z-index: 2; /* Se apilará por encima de .element1 */
}
```