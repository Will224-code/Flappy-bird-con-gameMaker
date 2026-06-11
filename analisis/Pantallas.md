# Información de las ROOMS

 Actualmente, el juego *Flappy Bird* desarrollado por *wil224-code* hará uso de salas (**ROOMS**), cada una con el objetivo de dividir las responsabilidades del flujo de juego.

## ROOMS Planificadas

El videojuego está pensado para la implementación de **3 salas**. Cada una tendrá su propia responsabilidad para facilitar su manejo y acceso, siguiendo un flujo lineal de inicio-fin.

* `RM_Inicio` (Menú Principal)
* `RM_Juego` (Gameplay)
* `RM_Final` (Game Over)

---

## Navegación entre ROOMS

A continuación se muestra el diagrama de cómo interactúan las salas y qué acciones disparan los cambios de pantalla:

```
    A[RM_Inicio] -->|Botón Jugar| B(RM_Juego)
    B -->|Jugador Pierde| C(RM_Final)
    C -->|Botón Volver a Jugar| B
    C -->|Botón Menú Principal| A
```

## Detalles de las ROOMS
### RM_Inicio
#### Propósito: 
El objetivo de esta sala es ser el menú principal en donde el usuario podra ingresar, seleccionar el aspecto (skin) del personaje y acceder al juego por medio de un botón.

#### Elementos Interactivos [Botones]:
* Seleccionar personaje: Cambia el aspecto del personaje.
* Ir a la siguiente sala: Pasa a la siguiente sala [RM_juego].

#### Elementos Visuales:
* Fondo: Fondo con un cielo azul y con una ciudad al fondo [como el juego original].
* Titulo: Spretie con el Nombre del juego con la tipografia a usar.
* Botones: Cada botón con su sprite y respectivas animaciones.
    * Animacion de selección.
    * Animacion de **NO** selección.
    * Animacion para precionar el botón.
* Música: Musica de fondo en bucle.


### RM_Juego
#### Propósito: 
El objetivo de esta sala es ser la sección en donde el jugadador interactua con las mecanicas y el "gameplay". 

#### Elementos Interactivos
* La pantalla: Cada interacción con la pantalla hace que el personaje salte para elevarse.

#### Elementos Visuales:
* Fondo: Cielo azul y ciudad con movimiento de desplazamiento horizontal hacia la izquierda (scrolling) para simular velocidad.
* Contador: Sección en donde mostrara el puntaje obtenido en tiempo real.
* Suelo: Suelo de color verde con anaranjado con un movimiento horizontal hacia la izquierda.
* Tubos: Tuvos color verde con un movimiento horizontal a la izquierda. 
* Pesonaje: Personaje elegido por sala "RM_Juego".
* Música: Musica de fondo en bucle.

### RM_Final 
#### Propósito: 
Esta sala actúa como la pantalla de Game Over. Informa al jugador que ha perdido, despliega sus resultados y ofrece opciones para reintentar o salir.

#### Elementos Interactivos [Botones]
* Volver a jugar: Regresa a la sala "RM_Juego".
* Regresar al menu: Regresa a la sala "RM_Inicio"

#### Elementos Visuales
* Fondo: Con un cielo azul y con una ciudad al fondo [como el juego original].
* Puntaje optenido: Cantidad de puntos optenidos en la ronda. 
* Puntaje ALTO: Récord histórico guardado.
* Aviso de nuevo record: Texto dinámico con la tipografía del juego que se activa solo si el jugador supera su récord actual.
* Botones: Cada botón con su sprite y respectivas animaciones.
    * Animacion de selección.
    * Animacion de **NO** selección.
    * Animacion para precionar el botón.
* Música: Musica de fondo en bucle.
