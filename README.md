# Vue 💻
## Indice 
- [Vue 💻](#vue-)
  - [Indice](#indice)
  - [Instalacion](#instalacion)
  - [Estructura de archivos](#estructura-de-archivos)
  - [Single File Components](#single-file-components)
  - [Sintaxis de plantilla](#sintaxis-de-plantilla)
  - [Interpolacion de texto](#interpolacion-de-texto)
  - [v-bind (Interpolacion de texto en atributos)](#v-bind-interpolacion-de-texto-en-atributos)
  - [Expresiones de Javascript con interpolacion de texto](#expresiones-de-javascript-con-interpolacion-de-texto)
  - [Directivas](#directivas)
    - [v-if, v-else-if y v-else](#v-if-v-else-if-y-v-else)
    - [v-show](#v-show)
    - [v-for](#v-for)
      - [Para arreglos](#para-arreglos)
      - [Para objetos](#para-objetos)
    - [v-for junto a v-if](#v-for-junto-a-v-if)
    - [v-on y modificadores de eventos](#v-on-y-modificadores-de-eventos)
    - [Reactividad](#reactividad)
      - [ref()](#ref)
        - [Pasos para usar](#pasos-para-usar)

## Instalacion
  Para trabajar con vue, es necesario tener instalado node.js y npm (node package manager). Luego se puede proceder a instalar la version de Vue con la cual vas a trabajar.

  * Con ```npm``` : 
    ```
      npm create vue@latest
    ```
    
  * con ```CDN``` : 
    ```javascript 
      <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    ```
  
## Estructura de archivos
  La estructura básica de un proyecto en VueJs es la siguiente:

  ![Imagen de la estructura de archivos](image-1.png)

  > **Nota** 
  > Nos damos cuenta que la estructura de archivos de VueJS es parecida a la estructura de archivos de otros frameworks como React o Astro.

## Single File Components
  Es una tecnica que nos permite separar la logica, la estructura y los estilos.
  ![Imagen del Single File Components](image-2.png)

## Sintaxis de plantilla
  Vue utiliza una sintaxis de plantilla basada en HTML que le permite vincular declarativamente el DOM.
  ![Imagen de Sintaxis de plantilla](image-3.png)

## Interpolacion de texto
  La interpolacion de texto (bigote o llaves dobles) se utiliza para mostrar valores en el DOM.
  ![Interpolacion de texto](image-4.png)

## v-bind (Interpolacion de texto en atributos)
  El atributo `v-bind` se utiliza para asignar valores a atributos.
  ![v-bind](image-5.png)

## Expresiones de Javascript con interpolacion de texto  
  Solo se puedn agregar ciertas expresiones de javascript utilizando la interpolacion de texto.
  ![expresiones de JS](image-6.png)

## Directivas
  Son atributos especiales con prefijo `v-` que permiten aplicar comportamientos reactivos a nuestro DOM.
  ### v-if, v-else-if y v-else
  Se encarga de renderizar u ocultar elementos dependiendo de si cumple o no una condicion.
  ![v-if, v-else-if y v-else](image-7.png)
  > **Nota** 
  > v-if, v-else-if y v-else son directivas que funcionan con la mimsa estructura que un if y un else en cualquier lenguaje de programacion.

  ### v-show
  En este caso, el elemento sigue siendo parte del DOM pero solo se muestra o no segun las condiciones.
  ![v-show](image-8.png)

  ### v-for
  Permite iterar sobre arreglos o propiedades de objetos.
  #### Para arreglos
  Si tenemos el siguiente arreglo: 
  ![arreglo de ejemplo](image-9.png)
  Y queremos imprimir todos sus nombres, podemos hacerlo de esta manera:
  ![arreglo impreso](image-10.png)
  #### Para objetos
  Si tenemos el siguiente objeto:
  ![objeto de ejemplo](image-11.png)
  Podemos acceder a las propiedades de un objeto de la siguiente forma:
  ![objeto impreso](image-12.png)

  ### v-for junto a v-if
  Si tenemos el siguiente arreglo de objetos: 
  ![arreglo de objetos](image-13.png)
  Queremos imprimir los nombres de los usuarios que tengan menos de 30 años.
  ![arreglo de objetos impreso](image-14.png)

  ### v-on y modificadores de eventos
  Es una directiva que nos permite escuchar eventos nativos del DOM como click, keypress, etc.

  `v-on:click="handler"` o `@click="handler"`

  Primero creamos una funcion que sera llamada por el evento click.
  ![funcion handler](image-15.png)

  luego llamamos la funcion para ser usada con el evento click y con los modificadores de eventos que nos permiten hacer click solo con un boton respectivo del mouse.
  ![evento click y modificadores](image-16.png)

  ### Reactividad
  #### ref()
  * es una de las formas de trabajar con la reactividad de Vue 3.
  * es una referencia reactiva que nos permite actualizar autoaticamente el DOM cuando muta el estado reactivo.
  * al utilizar ``ref()`` en un valor reactivo ,vue nos devuelve un objeto y para acceder a su valor real(valor inicial de la variable reactiva) tenemos que utiliza `.value` para realizar la mutacion(modificacion del valor inicial).
  ##### Pasos para usar 
  * importamos el metodo de la libreria de vue
    


