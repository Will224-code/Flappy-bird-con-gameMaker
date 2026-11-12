# Elementos a Objetos
En este documento se redactara todos los objetos indentificados en el desarollo del video juego flappy bird, cada objeto tendra su descripcion, la descripcion de los metodos y atributos, cabe aclarar que esto es la indentificación, por ende no tendra o hara referencia a documentos relacionados con la programacion, solo enlistaran la descripcion, y lo que va a hacer el propio objeto.
Ademas que enlistara las funcionales del documento de requerimientos funcionales, catalogo de elementos y pantallas, esto ya que es el analisis completo de esto y debe de respetar lo ya planeado.


Estos objetos estaran dividos en secciones, cada sección estara dividida en cada sala.

## RM_Inicio [documento Pantallas]
Objetos indentidicados en la room inicio, son un total de:

### Titulo del juego [documento pantallas]
El titulo del juego sera mostrado por medio de una imagen, no tendra ninguna acción o algun evento. (actualmente el documento de catalogo de elementos muestra que sera un texto, pero por el analicis y actualizacion, se opta que va ser un objeto con la imagen del titulo, ya que es la desicion mas optima)

| Título del juego  | 
|-----------|
|Atributos|
|sprites [imagen]|
|Metodos|
|mostrar titulo del juego|

### Botón para seleccionar aspecto del personaje [documento pantallas]
El boton para seleccionar el aspecto, sera un botón que se haga click directamente y este sera encargado para el cambio de la skin del propio personaje.

| Botón seleccionar aspecto del personaje  | 
|-----------|
|Atributos|
|sprites [imagen]|
|Metodos|
|Cambiar aspecto del personaje [rf-01]|
|Mandar el aspecto del personaje a algun controlador|
|Aplicar sonido al ser precionado|
|Aplicar animacion de no seleccion|
|Aplicar animacion de seleccion|
|Aplicar animacion de clic|

### Botón para pasar a la sala Juego
El boton se ecnarga de pazar a la siguiente sala que viene siendo la sala de juego o conocido como [RM_Juego].
| Botón Pasar a la sala Juego | 
|-----------|
|Atributos|
|sprites [imagen]|
|Metodos|
|Pasar a la siguiente sala [RM_Juego]|
|Aplicar sonido al ser precionado|
|Aplicar animacion de no seleccion|
|Aplicar animacion de seleccion|
|Aplicar animacion de clic|


## RM_Juego [documento Pantallas]

| Tubo  | 
|-----------|
|Atributos|
|sprites [imagen]|
|Metodos|
|mostrar titulo del juego|