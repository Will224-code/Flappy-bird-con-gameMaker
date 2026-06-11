# Elementos a Implementar 

## Categorías 
Esta sección redactará los tipos de elementos que se implementarán en el videojuego *Flappy Bird*, para poder tenerlos enlistados y tomarlos en cuenta por cualquier cambio en el desarrollo; En *Game Maker* utilizan objetos principalmente para los elementos, por esta razón se categorizarán como objetos y por tipo de funcionalidad.

Los distintos Elementos a utilizar en *Game Maker* son:

* **Objetos**: Para la creación del personaje, creación de obstáculos, manejo de botones, control del juego y diseños UI.
* **Sprites**: Para la sección de *Arte* (Diseño) en los *Objetos* [Personaje, Obstáculos, Botones, Diseño UI].
* **Fuentes**: Para agregar textos con la fuente del videojuego *Flappy Bird*.
* **Sonidos**: Para añadirle efectos de sonidos a los *Objetos* [Personaje, Obstáculos, Botones y controladores].
* **Rooms**: Salas para agregar los distintos elementos y poder realizar el videojuego.

---

## Catálogo de Elementos 

### Objetos
Los objetos a utilizar cumplirán tareas específicas para tener un control y orden. 

#### Personaje
Objeto que el jugador controlará; El personaje será controlado por medio del mouse (clic izquierdo) o también por el teclado (botón espacio). Cada acción realizada por el jugador el personaje podrá saltar evitando caer por la gravedad, o en dado caso esquivar los obstáculos.

#### Obstáculos
Objetos con el objetivo de hacer que el personaje colisione y pierda la ronda.

* **Tubo**: El obstáculo se desplazará hacia la izquierda con una velocidad fija y una altura aleatoria.
* **Suelo**: Obstáculo sin movimiento, será el límite para que el jugador pierda al pasarse de los límites.

#### Contador
Objeto con el objetivo de llevar el puntaje de la ronda.

#### Puntaje
Objeto invisible con desplazamiento hacia la izquierda, con el objetivo de que colisione el jugador y sumarle puntos.

#### Botones
Objetos con el fin de que el usuario interactúe y agregarle más dinamismo al juego para implementar ciertas mecánicas; En el juego se tiene contemplado el uso de 3 botones.

* **seleccionar aspecto del personaje**: Botón que cambia el aspecto del personaje.
* **Pasar a la sala *Juego***: Botón que te guiará para empezar el juego.
* **pasar a la sala principal**: Botón que te regresa a la sala principal.

#### Controladores
Objetos que servirán para coordinar los elementos y casos especiales dentro del juego, además de implementar el control de lógica avanzada.

* **Controlador juego**: Encargado de controlar el juego, desde asignar el aspecto seleccionado, hasta identificar en qué momento el jugador perdió.
* **Controlador obstáculo**: Encargado de crear los obstáculos y asignarle su posición original.
 
#### Diseños UI
Secciones en donde mostrarán el logo del juego o animaciones decorativas para el videojuego.

* **Texto Título del juego**: Esta sección se encargará de mostrar el texto principal del título del videojuego.
* **Texto de Derrota**: Esta sección se encargará de mostrar el texto de derrota.
* **Texto de Nuevo Récord**: Esta sección se encargará de mostrar el mensaje de nuevo récord cuando el jugador tenga un puntaje alto.

### Sprites
Animaciones que tendrán los objetos, esta lista indicará qué elementos tendrán agregado alguna animación o diseño para que el juego sea atractivo visualmente.

* **Personaje**: El personaje tendrá implementado varios sprites para sus diferentes acciones; Tendrá para saltar, caer y colisionar.
* **Botones (todos)**: Los botones tendrán un total de 3 animaciones, cuando no lo seleccionen, cuando lo selecciones y cuando le den clic.
* **Tubo**: Los obstáculos tendrán un sprite fijo.
* **Fondo**: Sprite fijo.
* **Suelo**: Sprite fijo.

### Fuentes
Se utilizará una única fuente para que el juego tenga coherencia de diseño, la fuente a utilizar para mostrar el puntaje es "FlappyFont.fnt".

### Sonidos 
Sección para indicar qué objetos tendrán sonido para implementar en el videojuego.

* **Personaje**: El personaje tendrá implementado un efecto de sonido para su salto y cuando colisione con algún obstáculo.
* **Botones (todos)**: Los botones tendrán implementado un efecto de sonido cuando le hagan clic.
* **Fondo**: Habrá música de ambientación, música de fondo.

### Salas (ROOMS)
Salas enlistadas y explicadas en el documento anterior.

* `RM_Inicio` (Menú Principal)
* `RM_Juego` (Gameplay)
* `RM_Final` (Game Over)

---

## Elementos de cada Sala
Esta sección enlistará los elementos que tendrá cada sala sacado del *Catálogo de Elementos*

### `RM_Inicio`

#### Diseños UI
* **Texto Título del juego**

#### Botones
* **seleccionar aspecto del personaje**
* **Pasar a la sala *Juego***

### `RM_Juego`

#### Personaje
* Objeto que el jugador controlará.

#### Obstáculos
* **Tubo**
* **Suelo**

#### Controladores
* **Controlador juego**
* **Controlador obstáculo**

#### Contador
* Objeto con el objetivo de llevar el puntaje de la ronda.

### `RM_Final` 

#### Diseños UI
* **Texto de Derrota**
* **Texto de Nuevo Récord**

#### Botones
* **Pasar a la sala *Juego***
* **pasar a la sala principal**