# Pensamiento-computacional-examen
**Proceso de p5js de sistema inetractivo avanzado**
PAC-ORANGE

Autora: Valentina Álvarez

Asignatura: Pensamiento Computacional

Carrera: Diseño, Facultad de Arquitectura, Arte y Diseño (FAAD) UDP

 **Enlaces del Proyecto**

Link para el proyecto en pantalla completa
[https://editor.p5js.org/vale.alvarez/full/46FhGmMk4]
-----
Link editable para revisar el código del proyecto
[https://editor.p5js.org/vale.alvarez/sketches/46FhGmMk4]
-----


**1. DESCRIPCION DEL PROYECTO**

PAC-ORANGE es un sistema visual interactivo programado en JavaScript utilizando el entorno p5.js. El software reinterpreta la estructura dinámica del videojuego arcade clásico Pac-Man mediante un entorno gráfico responsivo. Su funcionamiento está controlado por una máquina de estados lógicos que divide la experiencia en 4 momentos independientes: interfaz de bienvenida, escena principal de juego interactivo, pantalla de victoria y un desenlace abstracto de cierre.

En la escena de interacción principal, el sistema renderiza un lienzo digital que combina una grilla vectorial automatizada con entidades geométricas en movimiento y la captura en tiempo real de la cámara del usuario. El objetivo operativo del sistema es guiar un elemento interactivo usando el cursor mientras se evade a un persecutor autónomo que se escala de manera directamente proporcional al éxito del usuario.

**2. Sistema Computacional**

El software opera como un sistema de procesamiento continuo que recolecta entradas de hardware, ejecuta cálculos algorítmicos matemáticos en cada fotograma y genera respuestas dinámicas visuales y sonoras.

**Inputs (Entradas)**

-Hardware de Video (createCapture(VIDEO)): Flujo continuo de fotogramas de la webcam de la usuaria.

-Coordenadas de Posición (mouseX, mouseY): Datos de entrada analógicos capturados mediante el movimiento físico del mouse.

-Periférico de Teclado (keyCode === ENTER): Evento síncrono por pulsación de tecla para el cambio de estado inicial.

-Disparador del Mouse (mousePressed): Entrada discreta por clic para progresar al final de la experiencia.

*Processes (Lógicas y Algoritmos)*

-Máquina de Estados Lógicos: Estructura condicional anidada (if / else if) que evalúa continuamente la variable estado a 60 FPS para seleccionar el bloque de dibujo actual.

-Algoritmo de Persecución Autónoma (IA Básica): Comparación condicional entre las coordenadas del personaje y el mouse en los ejes cartesianos, alterando la posición de Pacman sumando o restando píxeles de manera constante (pacmanX += 2.5).

-Traducción Proporcional de Rangos (map()): Función matemática que convierte el rango de puntaje (0 a 10) al rango de diámetro del enemigo (40 a 110 píxeles).

-Cálculo de Proximidad Física (dist()): Operación matemática basada en la distancia euclidiana para determinar colisiones circulares exactas.

-Estructuras Iterativas Automatizadas (for): * Bucle 1 (Grilla): Automatización matemática de líneas verticales en el fondo espaciadas cada 40 píxeles.

-Bucle 2 (Abstracción): Segmentación espacial equidistante (width / 7 * i) para dibujar puntos simétricos en el desenlace.

**Estados**

Estado 0 (Inicio): Menú de bienvenida estático y recepción del input de partida.

Estado 1 (Juego Activo): Núcleo interactivo. Procesamiento de la IA de persecución, render de webcam, cálculo de colisiones y acumulación de puntaje.

Estado 2 (Ganador): Interfaz intermedia de éxito total tras cumplir la condición de victoria.

Estado 3 (Final): Desenlace abstracto y distorsión gráfica controlada por el usuario.

**Eventos**

-Teclado: Presionar ENTER detiene el menú e inicia la música del gameplay.

-Juntes: Al interceptar los círculos, se aumenta la variable puntaje y se ejecuta random() para reubicar al objetivo.

-Victoria (puntaje >= 10): Detiene la música de juego (.stop()), activa el sonido de gala (.play()) y migra al Estado 2.

-Clic: Avanza del Estado 2 al Estado 3.

**Elementos Multimedia Utilizados**

-Imagen (remolino.jpg): Archivo rasterizado de fondo procesado mediante filtros numéricos en la escena final.

-Audio (juego.mp3): Archivo sonoro cargado en bucle permanente (.loop()) para dar identidad atmosférica al juego.

-Audio (champion.mp3): Efecto auditivo para proporcionar retroalimentación (feedback) inmediata de éxito.

-Captura de Video: Uso de la webcam para incorporar la presencia física del usuario dentro del diseño de la interfaz.

**Outputs (Respuestas/Salidas)**

-Modificación en tiempo real del tamaño de la elipse de Pacman.

-Reproducción selectiva y sincronizada de pistas de sonido.

-Renderizado de la webcam espejada en la esquina de la pantalla de juego.

-Composición visual avanzada mediante la alteración y reseteo de los modos de mezcla del procesador (blendMode(SCREEN) y blendMode(BLEND)) junto con tintes cromáticos alternados según la posición del mouse en la pantalla final.

 **3. Explicación Conceptual y Relación con el Referente**
 
El proyecto se describe conceptualmente al Expresionismo y a la corriente cinematográfica Neón-Noir (tomando como referentes las atmósferas visuales cargadas de luces intensas, colores cian/magenta y contrastes marcados de obras como Blade Runner) al final de las 4 partes del sistema visual interactivo, hibridado con la iconografía visual y sonora del videojuego Pac-Man (1980). El diseño no busca imitar una ilustración literal o estática, sino traducir la lógica formal, la tensión de persecución y la nostalgia del arcade a un comportamiento dinámico dentro de un sistema interactivo.

 **4. Registro Visual del Proceso**   
 ----
Diagrama de Flujo del Sistema
    <img width="2720" height="3680" alt="diagrama de flujo pacorange" src="https://github.com/user-attachments/assets/8c17852c-bda9-43c5-ac96-2336b7ca206e" />
----

**Referentes Visuales e Inspiración**

<img width="654" height="468" alt="image" src="https://github.com/user-attachments/assets/4c11b5b7-82a8-4772-823e-9a1d4e107cc1" />
<img width="624" height="468" alt="image" src="https://github.com/user-attachments/assets/bf31bc89-5639-4e91-b924-d3eec69f0162" />

----
**Bocetos e Iteraciones del Desarrollo**

<img width="1200" height="1600" alt="boseto" src="https://github.com/user-attachments/assets/13b3469f-d31a-4698-8e3d-c8d755c90fa7" />
<img width="1200" height="1600" alt="WhatsApp Image 2026-06-25 at 9 25 49 PM" src="https://github.com/user-attachments/assets/5b143a38-8bec-46a2-8cd4-e33af245785d" />
<img width="1300" height="1300" alt="remolino" src="https://github.com/user-attachments/assets/a4408292-642d-484e-8c6b-94ee81eb4c43" />


----
**Capturas del Software en Funcionamiento**

<img width="588" height="410" alt="Captura de pantalla 2026-06-25 213044" src="https://github.com/user-attachments/assets/d54de95d-8b90-43a2-8ade-5fa48fede77b" />
<img width="602" height="425" alt="Captura de pantalla 2026-06-25 213912" src="https://github.com/user-attachments/assets/355bed66-2657-4281-902f-b63de811c447" />

---
**5. Reflexión Final**

-Decisiones Tomadas-
Una de las decisiones arquitectónicas fundamentales fue la modularización absoluta del código mediante el uso de funciones personalizadas para cada pantalla (pantallaInicio, pantallaJuego, etc.). Esto evitó la saturación del bloque draw(), facilitando la lectura, depuración y mantenimiento de las variables del sistema interactivo. Asimismo, la distribución estratégica de los bucles for (uno para la cuadrícula espacial de juego y otro para los adornos abstractos del final) permitió cumplir con rigurosidad matemática los requisitos técnicos de automatización y optimización de código.

-Dificultades Encontradas-
El principal desafío técnico residió en el control asincrónico de los elementos multimedia y la estabilidad de los estados de p5.js. Específicamente, sincronizar el corte y la activación de los canales de audio al cambiar de escena generaba solapamientos de sonido. Se resolvió aplicando condicionales estrictos de detención (.stop()) justo en las funciones de eventos de clic y teclado (keyPressed/mousePressed). Otra complicación fue el uso del modo avanzado de procesamiento de píxeles blendMode(SCREEN), ya que afectaba la legibilidad del texto; esto se solucionó aislando completamente el efecto y aplicando un reseteo forzado inmediato mediante blendMode(BLEND).

-Aprendizajes Obtenidos-
El desarrollo de este sistema visual interactivo permitió consolidar el aprendizaje de que el pensamiento computacional aplicado al diseño va mucho más allá de aplicar un filtro visual decorativo. Programar implica diseñar el comportamiento latente de los objetos y estructurar arquitecturas lógicas e interactivas integradas, donde cada entrada (input) física del usuario modifica las propiedades internas del entorno digital en tiempo real de manera controlada y coherente.
