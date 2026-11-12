# Requerimientos de Diseño

## Propósito
Listar los requerimientos respecto al diseño del videojuego *Flappy Bird* (qué se muestra al jugador y cómo se presenta), dividiéndolos en 3 secciones, cada una enfocada en una sala:

* `RM_Inicio` (Menú Principal)
* `RM_Juego` (Gameplay)
* `RM_Final` (Game Over)

Este documento trabaja en conjunto con [requisitos funcionales.md](requisitos%20funcionales.md): los requerimientos funcionales definen **qué hace** el sistema y los de diseño definen **qué se muestra y cómo se presenta**. El campo *Relacionado con* indica el requerimiento funcional que aporta el dato o la acción que se muestra.

## Referencias

| Documento | Descripción | Ubicación |
|---|---|---|
| Requisitos funcionales | Funcionalidades del sistema por sala. | [requisitos funcionales.md](requisitos%20funcionales.md) |
| Pantallas | Descripción de las salas, su navegación, elementos interactivos y visuales. | [Pantallas.md](../juego/salas/Pantallas.md) |
| Catálogo de Elementos | Lista de objetos, sprites, fuentes, sonidos y salas. | [Catalogo de Elementos.md](../juego/elementos/Catalogo%20de%20Elementos.md) |

## Glosario de identificadores

Cada requerimiento de diseño usa el formato `RD-CAT-NN`:

* **RD**: **R**equisito de **D**iseño (equivalente a **RF** en los requerimientos funcionales).
* **CAT**: categoría del requisito, de tres letras.
* **NN**: número consecutivo, que reinicia en cada categoría.

| Código | Categoría | Qué cubre |
| :--- | :--- | :--- |
| `RD-VIS-NN` | Visual / Mostrar | Textos, títulos, puntajes en pantalla, sprites y avisos. |
| `RD-ANI-NN` | Animación | Animaciones de selección, no selección, clic y movimiento del personaje. |
| `RD-SON-NN` | Sonido | Efectos de sonido y música (clic, punto, colisión). |

Si más adelante surge otra categoría (por ejemplo `RD-DIS` para la disposición y posición de elementos), se agrega a esta tabla sin renumerar los requisitos existentes.

## Requerimientos de Diseño

### RM_Inicio

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-01 \| Mostrar animación del fondo del juego |
|**Descripción**| El sistema deberá mostrar la animación del fondo del juego en la sala [RM_Inicio]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra la animacion de fondo del juego. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-02 \| Mostrar la animación del suelo de fondo del juego |
|**Descripción**| El sistema deberá mostrar la animación del fondo del juego en la sala [RM_Inicio]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra la animacion del suelo del juego. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-03 \| Mostrar título del juego |
|**Descripción**| El sistema deberá mostrar la imagen del título del juego en la sala [RM_Inicio]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra el título del juego con la fuente del videojuego. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-04 \| Mostrar el botón para cambiar aspecto |
|**Descripción**| El sistema deberá mostrar el botón de cambio de aspecto en la sala [RM_Inicio]. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra el botón de cambiar aspecto. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-05 \| Mostrar el botón de pasar a la sala Juego |
|**Descripción**| El sistema deberá mostrar el botón de pasar a la sala Juego en la sala [RM_Inicio]. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra el botón de Pasar a la sala Juego.

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-06 \| Mostrar el botón de pasar a la sala Juego |
|**Descripción**| El sistema deberá mostrar el botón de pasar a la sala Juego en la sala [RM_Inicio]. |
|**Prioridad**| Alta |
|**Criterio de aceptación**| Al cargar la sala [RM_Inicio], el sistema muestra el botón de Pasar a la sala Juego.




### RM_Juego

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-02 \| Mostrar puntaje del contador |
|**Descripción**| El sistema tomará el puntaje guardado y lo mostrará en pantalla. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Siempre se toma el puntaje guardado más actual para mostrarlo en pantalla. |

### RM_Final

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-03 \| Mostrar texto de derrota |
|**Descripción**| El sistema deberá mostrar el texto de derrota en la sala [RM_Final]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al cargar la sala [RM_Final], el sistema muestra el texto de derrota. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-04 \| Mostrar puntaje obtenido |
|**Descripción**| El sistema deberá mostrar el puntaje obtenido por el jugador en la ronda que acaba de terminar. |
|**Prioridad**| Media |
|**Criterio de aceptación**| Al cargar la sala [RM_Final], el sistema muestra el puntaje obtenido en la última partida. |

| Campo | Detalle |
| :--- | :--- |
|**Nombre**| RD-VIS-05 \| Mostrar Récord |
|**Descripción**| El sistema deberá mostrar el [Récord]. |
|**Prioridad**| Baja |
|**Criterio de aceptación**| Al momento de pasar a [RM_Final], el sistema mostrará el puntaje más alto guardado [Récord]. |

---
