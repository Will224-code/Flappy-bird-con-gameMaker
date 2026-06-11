# Lógica y Reglas

Este documento redacta detalladamente los comportamientos lógicos, los algoritmos de generación aleatoria y el flujo del juego.

## 1. Generación de Obstáculos
Esta sección explica detalladamente la automatización de la generación de los tubos.

* **Frecuencia:** La generación de cada tubo será cada 1.5 segundos.
* **Posicionamiento en el eje X:** Los tubos creados serán posicionados fuera del límite de la pantalla, para que no se vea en qué momento se crean. 
* **Algoritmo de altura:** La posición Y del tubo terrestre será aleatoria. Por medio de esa coordenada se le restarán 100 unidades, dando como resultado `Y - 100`, que vendría siendo la posición del tubo de arriba.
* **Margen de paso:** El tubo se moverá horizontalmente, desplazándose hacia la izquierda con una velocidad de 2.5.

---

## 2. Velocidad y Dificultad Progresiva

Para mantener el dinamismo y el reto en la partida, el juego implementa un control de movimiento lineal continuo:

* **Desplazamiento del Escenario:** Los tubos y el suelo se desplazan hacia la izquierda a una velocidad base inicial de `V` píxeles por fotograma (ej. `3px/frame`). Esto simula el avance del jugador hacia adelante.
* **Velocidad Constante:** La velocidad se mantiene fija durante toda la partida para respetar la experiencia arcade clásica.

---

## 3. Sistema de Puntuación (Score)
El cálculo y la validación de cada punto se realizan por medio de colisiones entre banderas.

* **Activación del Punto:** Cada par de tubos creados genera una línea o tubo bandera para la verificación de su colisión.
* **Condición de Éxito:** Cuando el jugador colisione con la bandera, ocurrirá lo siguiente:
    1. Se incrementa el puntaje en +1.
    2. Se genera un efecto de sonido para confirmar la colisión y el nuevo puntaje.
    3. La bandera se elimina porque ya cumplió su función.

---

## 4. Persistencia de Datos (Puntaje Alto)

El juego almacena de forma local el récord más alto del usuario para que no se pierda al cerrar la aplicación.

* **Estructura de Almacenamiento:** Se utiliza un sistema simple de archivos de texto o formato `.ini` provisto por GameMaker (ej. `save_data.ini`).
* **Lógica de Lectura (Al iniciar el juego):** El sistema busca el archivo local. Si existe, lee el valor de la clave `max_score` y lo asigna a la variable `global.highscore`. Si no existe, inicializa la variable en `0`.
* **Lógica de Escritura (Al perder):** En la pantalla de derrota (`RM_Derrota`), el sistema compara:
  - Si `global.score` > `global.highscore`: Se actualiza el nuevo valor en el archivo local y se guarda inmediatamente en el almacenamiento del dispositivo.
