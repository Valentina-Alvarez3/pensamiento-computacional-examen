# pensamiento-computacional-examen
Proceso de p5js de sistema inetractivo avanzado
# PAC-ORANGE
**Autor/a:** Valentina Alvarez  
**Asignatura:** Pensamiento Computacional  
**Carrera:** Diseño, Facultad de Arquitectura, Arte y Diseño (FAAD) UDP  

---

## 🔗 Enlaces del Proyecto
* [cite_start]**[Link para ejecutar el proyecto en p5.js]([(https://editor.p5js.org/vale.alvarez/full/46FhGmMk4])))** 
* [cite_start]**[Link editable para revisar el código]([(https://editor.p5js.org/vale.alvarez/sketches/46FhGmMk4])** 

---

## 📄 Descripción General

### [cite_start]Descripción Objetiva [cite: 104]
[cite_start]**PAC-ORANGE** es un sistema visual interactivo desarrollado en p5.js que reinterpreta la mecánica clásica de persecución del videojuego Pac-Man[cite: 15, 105]. [cite_start]El software está diseñado bajo una arquitectura de máquina de estados que transiciona a través de 4 escenas diferenciadas: una pantalla de inicio, la experiencia interactiva principal, una pantalla de celebración y un desenlace abstracto conceptual[cite: 38]. 

En la pantalla principal, el usuario visualiza un lienzo oscuro cubierto por una grilla geométrica automatizada. [cite_start]Los elementos visuales principales son una gran elipse naranja (Pac-Orange) y un círculo amarillo que representa su objetivo (la comida)[cite: 106]. [cite_start]El sistema utiliza como inputs las coordenadas de movimiento del mouse, pulsaciones del teclado y el flujo de video de la webcam en tiempo real[cite: 108]. [cite_start]Como outputs, genera transformaciones gráficas continuas, escalamiento de figuras, feedback sonoro interactivo y la superposición de píxeles mediante composición cromática avanzada[cite: 109].

### [cite_start]Descripción Conceptual [cite: 110]
* [cite_start]**Idea Central:** El proyecto explora la pérdida progresiva de control del usuario humano frente a las lógicas y algoritmos autónomos del software computacional[cite: 111].
* [cite_start]**Referente de Diseño / Corriente:** El proyecto se adscribe conceptualmente al **Expresionismo** y a la estética cinematográfica **Neón-Noir**[cite: 112]. 
* [cite_start]**Interpretación mediante Lógica Computacional:** En lugar de copiar una simple apariencia gráfica, se traduce la lógica de tensión expresionista a un sistema interactivo[cite: 24]. [cite_start]Al inicio, el usuario tiene el control del objetivo (el mouse), pero la Inteligencia Artificial (Pac-Orange) lo persigue implacablemente aumentando su tamaño a medida que "consume" las interacciones (puntos)[cite: 35]. El paso hacia la pantalla final disuelve la interfaz clara en un caos visual gobernado por un remolino gráfico y transparencias distorsionadas, simbolizando cómo el usuario queda atrapado de forma irreversible dentro de la lógica de la máquina.
* [cite_start]**Principio de Diseño Explorado:** Proporción, contraste cromático y dinamismo reactivo a través del espacio bidimensional[cite: 114].

---

## [cite_start]⚙️ Sistema Computacional [cite: 115]

### [cite_start]Explicación de la Interacción [cite: 122]
[cite_start]El sistema opera capturando datos continuos del entorno físico y digital[cite: 123]. [cite_start]El movimiento del cursor del usuario es mapeado directamente sobre las coordenadas de la comida[cite: 124]. Al mismo tiempo, la computadora calcula continuamente la distancia geométrica entre el círculo del jugador y el ente autónomo. [cite_start]Cuando se detecta una colisión bajo un umbral matemático, los datos se transforman incrementando una variable de puntaje global, la cual a su vez reconfigura el tamaño del personaje principal mediante una función de escalado proporcional[cite: 125, 126].

* [cite_start]**Inputs (Entradas):** [cite: 116]
    * Coordenadas bidimensionales del mouse (`mouseX`, `mouseY`).
    * Pulsación de la tecla `ENTER` en el teclado.
    * Clic físico del mouse (`mousePressed`).
    * Captura de video en vivo de la webcam del usuario (`createCapture`).
* [cite_start]**Procesos:** [cite: 117]
    * Evaluación condicional de la máquina de estados (`if / else if`).
    * Cálculo algorítmico de persecución autónoma (fórmula de proximidad en ejes X e Y).
    * Traducción lineal de rangos mediante la función `map()` para escalar objetos según variables.
    * Cálculo de distancias euclidianas mediante la función `dist()` para la detección de colisiones circulares.
    * Estructuras iterativas repetitivas (`for`) para la automatización de grillas y puntos simétricos de fondo.
* [cite_start]**Estados:** [cite: 118]
    * `Estado 0`: Pantalla de inicio (Espera de interacción y bienvenida).
    * `Estado 1`: Experiencia principal (Juego activo, persecución de IA, webcam activa y conteo de puntos).
    * `Estado 2`: Pantalla intermedia (Celebración del triunfo y feedback sonoro estático).
    * `Estado 3`: Pantalla final (Composición abstracta, desenlace conceptual y distorsión por hardware).
* [cite_start]**Eventos:** [cite: 119]
    * Gatillado asincrónico por teclado (`ENTER`) para iniciar el sistema.
    * Gatillado por colisión matemática para sumar puntaje y reposicionar objetos con `random()`.
    * Gatillado por alcance de puntaje límite (`puntaje >= 10`) para cambiar el estado al de victoria y alterar los flujos de audio.
    * Gatillado por clic del mouse para transicionar de la pantalla de éxito al desenlace estético.
* [cite_start]**Outputs (Respuestas):** [cite: 120]
    * Renderizado de la webcam integrada en la esquina de la interfaz.
    * Crecimiento dinámico reactivo en píxeles de la elipse persecutora.
    * Activación, bucle y detención selectiva de archivos de audio (`.mp3`).
    * Composición visual con modos de fusión avanzados (`blendMode(SCREEN)`) e interacción de paralaje invertido en la escena final.

---

## [cite_start]📷 Recursos Multimedia Utilizados [cite: 127]

1.  [cite_start]**Audio (`juego.mp3`):** [cite: 128]
    * [cite_start]*Función:* Cumple un rol de inmersión ambiental continuo durante el gameplay (Estado 1) actuando en modo bucle (`loop`) para generar tensión rítmica coherente con el neón-noir[cite: 129].
2.  [cite_start]**Audio (`champion.mp3`):** [cite: 128]
    * [cite_start]*Función:* Proporciona una retroalimentación auditiva clara e instantánea de éxito cuando el sistema procesa que se ha alcanzado la meta de puntuación[cite: 129].
3.  [cite_start]**Imagen (`remolino.jpg`):** [cite: 128]
    * *Función:* Actúa como la matriz visual en la pantalla final. [cite_start]Se duplica en dos capas mezcladas cromáticamente para representar el colapso gráfico del sistema[cite: 129].
4.  [cite_start]**Flujo de Video/Webcam (`createCapture`):** [cite: 128]
    * [cite_start]*Función:* Integra el rostro del usuario en tiempo real en la interfaz de juego, rompiendo la barrera de la pantalla y transformando al espectador en un elemento observado y controlado por el software[cite: 129].

---

## [cite_start]🗺️ Diagrama de Flujo [cite: 84]

[cite_start]*(Asegúrate de exportar tu diagrama desde Figma en formato PNG, guardarlo en la carpeta de tu repositorio y enlazarlo aquí correctamente) [cite: 94, 97]*

[cite_start]![Diagrama de Flujo del Sistema](diagrama.png) [cite: 98]

---

## [cite_start]🎨 Registro Visual del Proceso [cite: 130]

### [cite_start]Referentes [cite: 131]
*(Menciona o añade imágenes de películas Neón-Noir como Blade Runner o pinturas expresionistas que inspiraron tus colores cian/magenta).*

### [cite_start]Bocetos e Iteraciones [cite: 132, 133]
*(Sube las capturas de tus primeros dibujos o esquemas de cómo ibas a distribuir las pantallas).*

### [cite_start]Capturas del Proceso [cite: 134]
*(Coloca aquí al menos 2 capturas de pantalla de tu proyecto p5.js en funcionamiento).*

---

## [cite_start]💬 Reflexión Final [cite: 135]

* [cite_start]**Principales Decisiones Tomadas:** Se optó por un diseño de código altamente modularizado en funciones independientes para asegurar que el ciclo de actualización (`draw`) se mantuviera limpio y ordenado[cite: 136]. La inclusión de estructuras de bucle `for` permitió resolver de manera automatizada tanto la ambientación reticular (grilla) como la decoración geométrica abstracta final sin sobreescribir líneas de código de forma redundante.
* [cite_start]**Dificultades Encontradas:** El mayor desafío técnico residió en la sincronización del audio al cambiar de estados, ya que los sonidos tendían a encimarse o reproducirse de forma infinita[cite: 137]. Esto se solucionó implementando detenciones explícitas (`.stop()`) dentro de los condicionales lógicos de transición. Asimismo, el control del renderizador al usar modos de fusión avanzados requirió aislar el comando `blendMode` con su respectivo cierre para salvaguardar la legibilidad del texto en pantalla.
* [cite_start]**Aprendizajes Obtenidos:** La materialización de este proyecto consolidó la comprensión de que la programación creativa no consiste en aplicar efectos decorativos aislados, sino en construir arquitecturas lógicas e interactivas integradas donde cada input genera un impacto estructural en el comportamiento global del sistema[cite: 138].
