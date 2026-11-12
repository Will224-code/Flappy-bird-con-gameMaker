# Requerimientos Funcionales

## Propósito
El propósito es listar todas las funcionalidades del videojuego *Flappy Bird*, dividiéndolas en 4 secciones. Las 3 primeras se enfocan específicamente en las funcionalidades de una sala en particular. En total se tienen contempladas 3 salas:

* `RM_Inicio` (Menú Principal)
* `RM_Juego` (Gameplay)
* `RM_Final` (Game Over)

La última sección se concentra en los elementos globales. Como son globales, pueden estar repartidos entre las 3 salas, por ende su separación en una sección aparte.

Los requerimientos sobre qué se muestra al jugador y cómo se presenta (títulos, textos, puntajes en pantalla) se encuentran en [requisitos de diseño.md](requisitos%20de%20dise%C3%B1o.md).

## Alcance
El documento abarca todos los elementos y funciones que se aplicarán. Gracias al listado de **Catálogo de Elementos** se tiene una visión muy amplia, además de que se basa en los demás documentos: **Lógica y Reglas** y **Pantallas**.

## Referencias

| Documento | Descripción | Ubicación |
|---|---|---|
| Catálogo de Elementos | Lista de objetos, sprites, fuentes, sonidos y salas, y qué elementos tiene cada sala. | [Catalogo de Elementos.md](../juego/elementos/Catalogo%20de%20Elementos.md) |
| Pantallas | Descripción de las salas (`RM_Inicio`, `RM_Juego`, `RM_Final`), su navegación, elementos interactivos y visuales. | [Pantallas.md](../juego/salas/Pantallas.md) |
| Lógica y Reglas | Generación de obstáculos, velocidad, sistema de puntuación y persistencia de datos. | [logica y reglas.md](../juego/logica%20y%20reglas.md) |
| Requisitos de diseño | Requerimientos de presentación visual por sala. | [requisitos de diseño.md](requisitos%20de%20dise%C3%B1o.md) |

## Requerimientos Funcionales

### RM_Inicio

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-01 \| Cambiar aspecto del personaje |
|**Descripción**| El sistema deberá permitir al jugador cambiar el aspecto (skin) del personaje mediante un botón especializado para ello. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al momento que el jugador dé clic al botón, el sistema cambiará el aspecto del personaje. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-02 \| Ir a la sala [RM_Juego] |
|**Descripción**| El sistema deberá cambiar de sala y guiar al jugador a la sala [RM_Juego] para iniciar la partida. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al momento de que el jugador dé clic al botón, el sistema lo guiará a la sala [RM_Juego]. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-03 \| Cargar el récord al iniciar el juego |
|**Descripción**| El sistema deberá leer el puntaje más alto guardado en el archivo [.ini] al iniciar el juego y asignarlo al [Récord]. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al iniciar el juego, si el archivo [.ini] existe, el sistema carga el valor guardado en el [Récord]; si no existe, el [Récord] inicia en 0. |

### RM_Juego

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-04 \| Salto del Personaje Jugador con clic |
|**Descripción**| El sistema deberá hacer que el personaje jugador salte cuando se le dé clic en la pantalla. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al momento que se dé clic en la pantalla, el personaje jugador salta; esto será aplicable mientras el personaje jugador siga con vida. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-05 \| Salto del Personaje Jugador con la barra espaciadora |
|**Descripción**| El sistema deberá hacer que el personaje jugador salte cuando el jugador presione la barra espaciadora. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al presionar la barra espaciadora, el personaje jugador salta; esto será aplicable mientras el personaje jugador siga con vida. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-06 \| Gravedad del Personaje Jugador |
|**Descripción**| El sistema deberá aplicar gravedad de forma continua al personaje jugador mientras siga con vida. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Si el jugador no hace clic, el personaje jugador desciende de forma constante hasta colisionar con un obstáculo. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-07 \| Colisión y Derrota del Personaje Jugador |
|**Descripción**| El sistema deberá finalizar la partida cuando el personaje jugador colisione con un obstáculo [tubo, suelo]. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al colisionar con un tubo o con el suelo, se reproduce el sonido de colisión y el sistema lleva al jugador a [RM_Final]. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-08 \| Creación de objetos Tubo |
|**Descripción**| El sistema deberá crear los objetos Tubo cada determinado tiempo. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al pasar un determinado tiempo, el sistema genera un objeto Tubo. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-09 \| Altura aleatoria y par de objetos Tubo |
|**Descripción**| El sistema deberá generar cada par de objetos Tubo (inferior y superior) con una altura aleatoria, manteniendo una separación fija entre ambos. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al generarse un par de tubos, la posición Y del tubo inferior es aleatoria y el tubo superior se posiciona en Y - 100. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-10 \| Movimiento del objeto Tubo |
|**Descripción**| El objeto Tubo creado por el sistema tendrá un movimiento horizontal; este objeto siempre avanzará hacia la izquierda. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al ser generado por el sistema, el objeto Tubo avanza hacia la izquierda de forma horizontal. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-11 \| Autodestrucción del objeto Tubo |
|**Descripción**| En el momento en que el objeto Tubo creado llegue a una determinada coordenada x (fuera de la pantalla), se autodestruirá para no saturar la memoria. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al llegar a una determinada coordenada x, el objeto Tubo se autodestruye. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-12 \| Creación de objetos de Puntaje |
|**Descripción**| El sistema generará los objetos de Puntaje al mismo tiempo y en la misma coordenada que los objetos Tubo. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al llegar al mismo tiempo de generación del objeto Tubo, el sistema genera el objeto de Puntaje. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-13 \| Movimiento del objeto de Puntaje |
|**Descripción**| El objeto de Puntaje creado por el sistema tendrá un movimiento horizontal hacia la izquierda, a la misma velocidad que los objetos Tubo. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al ser generado, el objeto de Puntaje avanza hacia la izquierda junto con su par de tubos. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-14 \| Autodestrucción del objeto de Puntaje |
|**Descripción**| Si el objeto de Puntaje llega a una determinada coordenada x (fuera de la pantalla) sin haber colisionado con el personaje jugador, se autodestruirá. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al llegar a una determinada coordenada x, el objeto de Puntaje se autodestruye. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-15 \| Destrucción de objetos de Puntaje |
|**Descripción**| Si el personaje jugador colisiona con el objeto de Puntaje, este se destruye. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al colisionar con el personaje jugador, el objeto de Puntaje se destruye. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-16 \| Entrega de Puntaje |
|**Descripción**| Cuando el personaje jugador colisione con un objeto de Puntaje, este enviará el puntaje al contador. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al colisionar con el personaje jugador, el objeto de Puntaje manda puntos al contador. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-17 \| Guardar puntaje en el contador |
|**Descripción**| Cuando le manden el puntaje de cada tubo, el contador guarda esa información para no perder el progreso del jugador. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Cuando el objeto de Puntaje manda puntos al contador, este los guarda para no perder el progreso. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-18 \| Reiniciar el puntaje al iniciar la partida |
|**Descripción**| El sistema deberá reiniciar el puntaje de la ronda en 0 cada vez que inicie una partida. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al cargar la sala [RM_Juego], el contador muestra 0. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-19 \| Desplazamiento del Suelo |
|**Descripción**| El sistema deberá desplazar el objeto Suelo horizontalmente hacia la izquierda de forma continua para simular el avance del personaje jugador. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Mientras la partida esté en curso, el suelo se desplaza hacia la izquierda a la misma velocidad que los objetos Tubo. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-20 \| Aplicar el aspecto seleccionado |
|**Descripción**| El sistema deberá asignar al personaje jugador el aspecto (skin) seleccionado en la sala [RM_Inicio]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Juego], el personaje jugador se muestra con el aspecto elegido por el jugador. |

### RM_Final

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-21 \| Mostrar aviso de nuevo récord |
|**Descripción**| El sistema deberá mostrar un aviso de nuevo récord cuando el puntaje obtenido supere el [Récord] actual. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Final], si el puntaje obtenido > [Récord], el sistema muestra el aviso de nuevo récord; en caso contrario, no lo muestra. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-22 \| Guardar el puntaje en memoria [.ini] |
|**Descripción**| El sistema deberá almacenar el puntaje más alto en un archivo [.ini] para no perder el [Récord]. La comparación se hace antes de actualizar el [Récord], para que el aviso de nuevo récord (RF-21) pueda mostrarse. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al llegar a [RM_Final], si puntaje obtenido > [Récord], el sistema guarda el nuevo [Récord] en el archivo [.ini]; si no es mayor, no modifica el archivo. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-23 \| Ir a la sala [RM_Inicio] |
|**Descripción**| Una vez que el usuario termine de visualizar, puede regresar a la sala [RM_Inicio] cuando interactúe con un botón. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al momento de que el usuario interactúe con el botón para regresar a [RM_Inicio], el sistema automáticamente lo guiará a esa sala. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RF-24 \| Ir a la sala [RM_Juego] |
|**Descripción**| Una vez que el usuario termine de visualizar, puede regresar a la sala [RM_Juego] cuando interactúe con un botón. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al momento de que el usuario interactúe con el botón para regresar a [RM_Juego], el sistema automáticamente lo guiará a esa sala. |

---
