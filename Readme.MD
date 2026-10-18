# 200 ejercicios cortos para aprender Unity 2D y C# desde cero

Una progresión para personas que nunca han programado. Los ejercicios alternan el uso del editor con pequeños programas en C#: primero observarás y modificarás objetos; después crearás comportamientos y combinarás lo aprendido en escenas interactivas.

## Preparación y alcance

Se toma **Unity 6** como referencia. Necesitarás Unity Hub, el editor con soporte para crear ejecutables de tu sistema y un editor de C# conectado a Unity. Utiliza un proyecto con plantilla **2D**; los nombres de algunos menús pueden variar entre versiones.

Todo el trabajo es en **2D**: sprites, cámara ortográfica, movimiento en X/Y, rotación dentro del plano, `Rigidbody2D`, colisionadores 2D, Tilemap, interfaz y audio en modo 2D. La posición de los sprites mantendrá Z en 0 y la cámara conservará su Z inicial. Aunque `Transform` almacene tres coordenadas internamente, solo modificaremos las necesarias para trabajar en el plano; no se introducen mecánicas ni recursos de 3D.

Se introduce **Input System** en U081 y se mantiene ese mismo sistema para teclado, ratón y botones. En física se distinguirá entre mover un objeto visual y controlar un cuerpo físico.

<a name="indice"></a>

## Índice de ejercicios

Pulsa un código para ir directamente a ese ejercicio o un tema para abrir su bloque. Las etiquetas bajo cada título indican qué conceptos se trabajan; puedes buscarlas con el buscador del navegador.

| Bloque | Tema | Ejercicios |
|---|---|---|
| [1](#bloque-01) | [Primer contacto con el editor](#bloque-01) | [U001](#u001) · [U002](#u002) · [U003](#u003) · [U004](#u004) · [U005](#u005)<br>[U006](#u006) · [U007](#u007) · [U008](#u008) · [U009](#u009) · [U010](#u010) |
| [2](#bloque-02) | [Primeros scripts y variables](#bloque-02) | [U011](#u011) · [U012](#u012) · [U013](#u013) · [U014](#u014) · [U015](#u015)<br>[U016](#u016) · [U017](#u017) · [U018](#u018) · [U019](#u019) · [U020](#u020) |
| [3](#bloque-03) | [Sprites y organización visual](#bloque-03) | [U021](#u021) · [U022](#u022) · [U023](#u023) · [U024](#u024) · [U025](#u025)<br>[U026](#u026) · [U027](#u027) · [U028](#u028) · [U029](#u029) · [U030](#u030) |
| [4](#bloque-04) | [Números y datos](#bloque-04) | [U031](#u031) · [U032](#u032) · [U033](#u033) · [U034](#u034) · [U035](#u035)<br>[U036](#u036) · [U037](#u037) · [U038](#u038) · [U039](#u039) · [U040](#u040) |
| [5](#bloque-05) | [Decisiones](#bloque-05) | [U041](#u041) · [U042](#u042) · [U043](#u043) · [U044](#u044) · [U045](#u045)<br>[U046](#u046) · [U047](#u047) · [U048](#u048) · [U049](#u049) · [U050](#u050) |
| [6](#bloque-06) | [Azar y repeticiones](#bloque-06) | [U051](#u051) · [U052](#u052) · [U053](#u053) · [U054](#u054) · [U055](#u055)<br>[U056](#u056) · [U057](#u057) · [U058](#u058) · [U059](#u059) · [U060](#u060) |
| [7](#bloque-07) | [Métodos, referencias y arrays](#bloque-07) | [U061](#u061) · [U062](#u062) · [U063](#u063) · [U064](#u064) · [U065](#u065)<br>[U066](#u066) · [U067](#u067) · [U068](#u068) · [U069](#u069) · [U070](#u070) |
| [8](#bloque-08) | [Tiempo y movimiento automático](#bloque-08) | [U071](#u071) · [U072](#u072) · [U073](#u073) · [U074](#u074) · [U075](#u075)<br>[U076](#u076) · [U077](#u077) · [U078](#u078) · [U079](#u079) · [U080](#u080) |
| [9](#bloque-09) | [Teclado y ratón](#bloque-09) | [U081](#u081) · [U082](#u082) · [U083](#u083) · [U084](#u084) · [U085](#u085)<br>[U086](#u086) · [U087](#u087) · [U088](#u088) · [U089](#u089) · [U090](#u090) |
| [10](#bloque-10) | [Seguimiento y cámara](#bloque-10) | [U091](#u091) · [U092](#u092) · [U093](#u093) · [U094](#u094) · [U095](#u095)<br>[U096](#u096) · [U097](#u097) · [U098](#u098) · [U099](#u099) · [U100](#u100) |
| [11](#bloque-11) | [Física 2D](#bloque-11) | [U101](#u101) · [U102](#u102) · [U103](#u103) · [U104](#u104) · [U105](#u105)<br>[U106](#u106) · [U107](#u107) · [U108](#u108) · [U109](#u109) · [U110](#u110) |
| [12](#bloque-12) | [Control de cuerpos físicos](#bloque-12) | [U111](#u111) · [U112](#u112) · [U113](#u113) · [U114](#u114) · [U115](#u115)<br>[U116](#u116) · [U117](#u117) · [U118](#u118) · [U119](#u119) · [U120](#u120) |
| [13](#bloque-13) | [Zonas e interacciones](#bloque-13) | [U121](#u121) · [U122](#u122) · [U123](#u123) · [U124](#u124) · [U125](#u125)<br>[U126](#u126) · [U127](#u127) · [U128](#u128) · [U129](#u129) · [U130](#u130) |
| [14](#bloque-14) | [Interfaz y puntuación](#bloque-14) | [U131](#u131) · [U132](#u132) · [U133](#u133) · [U134](#u134) · [U135](#u135)<br>[U136](#u136) · [U137](#u137) · [U138](#u138) · [U139](#u139) · [U140](#u140) |
| [15](#bloque-15) | [Prefabs y creación de objetos](#bloque-15) | [U141](#u141) · [U142](#u142) · [U143](#u143) · [U144](#u144) · [U145](#u145)<br>[U146](#u146) · [U147](#u147) · [U148](#u148) · [U149](#u149) · [U150](#u150) |
| [16](#bloque-16) | [Mapas y animación](#bloque-16) | [U151](#u151) · [U152](#u152) · [U153](#u153) · [U154](#u154) · [U155](#u155)<br>[U156](#u156) · [U157](#u157) · [U158](#u158) · [U159](#u159) · [U160](#u160) |
| [17](#bloque-17) | [Áreas, enemigos y objetivos](#bloque-17) | [U161](#u161) · [U162](#u162) · [U163](#u163) · [U164](#u164) · [U165](#u165)<br>[U166](#u166) · [U167](#u167) · [U168](#u168) · [U169](#u169) · [U170](#u170) |
| [18](#bloque-18) | [Sonido y música](#bloque-18) | [U171](#u171) · [U172](#u172) · [U173](#u173) · [U174](#u174) · [U175](#u175)<br>[U176](#u176) · [U177](#u177) · [U178](#u178) · [U179](#u179) · [U180](#u180) |
| [19](#bloque-19) | [Escenas, pausa y guardado](#bloque-19) | [U181](#u181) · [U182](#u182) · [U183](#u183) · [U184](#u184) · [U185](#u185)<br>[U186](#u186) · [U187](#u187) · [U188](#u188) · [U189](#u189) · [U190](#u190) |
| [20](#bloque-20) | [Pequeños retos y ejecutable](#bloque-20) | [U191](#u191) · [U192](#u192) · [U193](#u193) · [U194](#u194) · [U195](#u195)<br>[U196](#u196) · [U197](#u197) · [U198](#u198) · [U199](#u199) · [U200](#u200) |

[Correspondencia con el PDF](#correspondencia-pdf) · [Recursos y referencias](#recursos)

<a name="bloque-01"></a>

## 1. Primer contacto con el editor (U001-U010)

Base: ninguna experiencia previa. Estas actividades se realizan sin scripts.

<a name="u001"></a>

### U001. Tu primer proyecto

**Etiquetas:** `Unity Hub` · `Proyecto 2D` · `Escenas`

Crea desde Unity Hub un proyecto con plantilla 2D. Abre el editor y guarda la escena como `U001_Inicio` dentro de `Assets/Ejercicios/U001/`.

**Pista:** una escena es el espacio donde colocas objetos. **Comprueba:** cierra la escena y vuelve a abrirla desde Project.

<a name="u002"></a>

### U002. Localizar las ventanas

**Etiquetas:** `Editor` · `Ventanas` · `Inspector`

Selecciona la cámara en Hierarchy y localiza sus propiedades en Inspector. Alterna entre Scene y Game, y encuentra Project y Console. Escribe una frase sobre para qué sirve cada ventana.

**Pista:** Scene permite editar; Game muestra la vista de la cámara. **Comprueba:** puedes localizar las seis ventanas sin ayuda.

<a name="u003"></a>

### U003. Un cuadrado en pantalla

**Etiquetas:** `GameObject` · `Sprites` · `SpriteRenderer`

Añade un sprite cuadrado desde el menú de objetos 2D. Renómbralo `Jugador`, sitúalo en X=0, Y=0, Z=0 y cambia su color desde Sprite Renderer.

**Pista:** un GameObject reúne componentes; Sprite Renderer dibuja el sprite. **Comprueba:** el cuadrado aparece en Game con el color elegido.

<a name="u004"></a>

### U004. Mover con coordenadas

**Etiquetas:** `Transform` · `Posición` · `Coordenadas X/Y`

Mueve el cuadrado cambiando X e Y en Transform. Prueba X=2 y después Y=-1. Devuélvelo al origen utilizando los campos numéricos, sin arrastrarlo.

**Pista:** X indica izquierda/derecha; Y, abajo/arriba. **Comprueba:** sabes anticipar hacia dónde se moverá antes de cambiar cada valor.

<a name="u005"></a>

### U005. Cambiar el tamaño

**Etiquetas:** `Transform` · `Escala` · `Inspector`

Modifica Scale X e Y para obtener un rectángulo ancho y después uno alto. Termina con un cuadrado que mida el doble que el inicial.

**Pista:** escala 1 conserva el tamaño original. **Comprueba:** cambiar la escala no modifica los valores de Position.

<a name="u006"></a>

### U006. Girar dentro del plano

**Etiquetas:** `Transform` · `Rotación Z` · `Grados`

Restaura la escala y gira el sprite usando únicamente Rotation Z: prueba 0, 45 y 90 grados. Mantén Rotation X e Y en 0.

**Pista:** Rotation Z gira la imagen dentro de la pantalla. **Comprueba:** a 45 grados el cuadrado parece un rombo.

<a name="u007"></a>

### U007. Duplicar y nombrar

**Etiquetas:** `Duplicación` · `Hierarchy` · `SpriteRenderer`

Duplica el cuadrado dos veces. Llama a los objetos `Rojo`, `Verde` y `Azul`, cambia sus colores y colócalos separados en una fila.

**Pista:** cada copia tiene sus propios componentes. **Comprueba:** cambiar el color de uno no cambia el de los demás.

<a name="u008"></a>

### U008. Encuadrar la escena

**Etiquetas:** `Cámara ortográfica` · `Encuadre` · `Color de fondo`

Selecciona la cámara, confirma que su proyección es Orthographic y ajusta Size para ver los tres cuadrados. Cambia también el color del fondo.

**Pista:** una Size mayor permite ver más espacio. **Comprueba:** el encuadre de Game contiene los tres objetos completos.

<a name="u009"></a>

### U009. Distinguir edición y ejecución

**Etiquetas:** `Modo Play` · `Edición` · `Guardar escenas`

Entra en Play, mueve un cuadrado y detén la ejecución. Observa qué ocurre. Después realiza el mismo cambio fuera de Play y guarda la escena.

**Pista:** los cambios de objetos de escena durante Play normalmente no se conservan al detenerlo. **Comprueba:** el cambio guardado fuera de Play permanece.

<a name="u010"></a>

### U010. Preparar una carpeta de trabajo

**Etiquetas:** `Project` · `Organización de recursos` · `Escenas`

Crea carpetas para escenas, scripts e imágenes dentro de `Assets/Ejercicios/U010/`. Guarda allí una copia de la escena anterior y vuelve a abrir la original para distinguir ambas.

**Pista:** mueve los recursos desde Project para conservar sus referencias. **Comprueba:** puedes abrir las dos escenas y reconocer cuál estás editando.

[Volver al índice](#indice)

<a name="bloque-02"></a>

## 2. Primeros scripts y variables (U011-U020)

Base: la escena con un cuadrado. Un script es un archivo de instrucciones; Unity ejecuta las de los componentes adjuntos a objetos activos.

<a name="u011"></a>

### U011. Crear y adjuntar un script

**Etiquetas:** `C#` · `Scripts` · `Clases` · `Componentes`

Crea un script de componente C# llamado `U011_PrimerScript`, ábrelo y localiza la clase y sus llaves. Añádelo al cuadrado desde Inspector. Conserva la estructura creada por Unity.

**Pista:** el nombre de la clase debe coincidir con el archivo. **Comprueba:** el componente aparece en el objeto sin errores en Console.

<a name="u012"></a>

### U012. Hello World

**Etiquetas:** `Start` · `Debug.Log` · `Console`

**Origen: PDF E02.**

Añade a `Start()` una instrucción que escriba `Hello World` en Console. Ejecuta la escena durante varios segundos y detén Play.

**Pista:** utiliza `Debug.Log`, comillas para el texto y punto y coma al terminar. **Comprueba:** aparece un solo mensaje por ejecución.

<a name="u013"></a>

### U013. Reconocer un error de sintaxis

**Etiquetas:** `Sintaxis` · `Console` · `Depuración`

En una copia del script anterior, elimina el punto y coma del mensaje. Guarda, localiza el error en Console y abre la línea indicada. Repón el signo y vuelve a ejecutar.

**Pista:** corrige primero el primer error de la lista. **Comprueba:** el mensaje vuelve a aparecer y ya no hay errores rojos.

<a name="u014"></a>

### U014. Leer las instrucciones en orden

**Etiquetas:** `Secuencia de instrucciones` · `Comentarios` · `Start`

Escribe tres mensajes en `Start()` que indiquen inicio, preparación y fin. Añade un comentario con `//` para explicar uno de ellos. Intercambia dos instrucciones.

**Pista:** los comentarios sirven para las personas y no se ejecutan. **Comprueba:** el orden de los mensajes coincide con el del código.

<a name="u015"></a>

### U015. Guardar un nombre

**Etiquetas:** `Variables` · `string` · `Texto`

Declara dentro de la clase, fuera de los métodos, una variable `string` llamada `nombreJugador`. Asígnale tu nombre y úsala para mostrar un saludo en `Start()`.

**Pista:** una variable guarda un dato; `string` guarda texto. **Comprueba:** al cambiar solo la variable cambia el saludo.

<a name="u016"></a>

### U016. Guardar un número entero

**Etiquetas:** `Variables` · `int` · `Asignación`

Declara una variable `int` llamada `vidas` con valor 3. Muestra su valor al iniciar la escena. Cambia después el valor inicial a 5 y prueba de nuevo.

**Pista:** los números no llevan comillas. **Comprueba:** Console muestra el valor que has asignado a `vidas`.

<a name="u017"></a>

### U017. Guardar un número con decimales

**Etiquetas:** `Variables` · `float` · `Decimales`

Declara una variable `float` llamada `velocidad` con valor `2.5f` y muéstrala al iniciar. Compara su declaración con la variable entera del ejercicio anterior.

**Pista:** en el código, los decimales usan punto y los literales `float` llevan `f`. **Comprueba:** el valor conserva la parte decimal.

<a name="u018"></a>

### U018. Guardar verdadero o falso

**Etiquetas:** `Variables` · `bool` · `Estados`

Declara una variable `bool` llamada `tieneLlave`. Prueba primero `false` y después `true`, mostrando su valor en Console. Escribe qué podría representar en un juego.

**Pista:** un booleano solo guarda dos posibilidades. **Comprueba:** no necesitas escribir esas palabras entre comillas.

<a name="u019"></a>

### U019. Editar datos desde Inspector

**Etiquetas:** `Campos public` · `Inspector` · `Serialización`

Expón las variables de nombre, vidas y velocidad como campos `public`. Modifica sus valores desde Inspector antes de Play y muestra los tres al iniciar la escena.

**Pista:** Unity conserva los valores guardados en el componente; cambiar el valor inicial en código no siempre los sustituye. **Comprueba:** se imprimen los valores del Inspector.

<a name="u020"></a>

### U020. Una vez o en cada fotograma

**Etiquetas:** `Start` · `Update` · `Fotogramas`

Coloca un mensaje en `Start()` y otro diferente en `Update()`. Ejecuta durante dos segundos, detén Play y compara cuántas veces se ha escrito cada uno. Después desactiva el mensaje repetido.

**Pista:** `Update()` se llama cada fotograma; Console puede agrupar mensajes con Collapse. **Comprueba:** distingues una acción inicial de una repetida.

[Volver al índice](#indice)

<a name="bloque-03"></a>

## 3. Sprites y organización visual (U021-U030)

Base: manejo del editor. Trabaja sin scripts para preparar recursos que reutilizarás después.

<a name="u021"></a>

### U021. Importar una imagen transparente

**Etiquetas:** `Importación` · `Sprites` · `Transparencia`

**Origen: PDF E49.**

Importa un PNG con transparencia que no sea pixel art. Configura Texture Type como Sprite, aplica los cambios y arrastra la imagen a una escena.

**Pista:** deja visible un fondo de color detrás. **Comprueba:** las zonas transparentes muestran el fondo y no un rectángulo opaco.

<a name="u022"></a>

### U022. Conservar los píxeles

**Etiquetas:** `Pixel art` · `Filtrado Point` · `Compresión`

**Origen: PDF E50.**

Importa un pequeño PNG de pixel art con transparencia. Configúralo como Sprite, usa filtrado Point y desactiva la compresión. Amplía el objeto para observar sus bordes.

**Pista:** compara el resultado con el filtrado Bilinear. **Comprueba:** los píxeles se distinguen sin el suavizado de sus bordes.

<a name="u023"></a>

### U023. Relacionar píxeles y unidades

**Etiquetas:** `Pixels Per Unit` · `Sprites` · `Unidades`

Duplica el archivo de una imagen y configura distintos valores de Pixels Per Unit en las dos importaciones. Coloca ambos sprites con escala 1 en la escena.

**Pista:** más píxeles por unidad producen una imagen más pequeña en el mundo. **Comprueba:** explicas por qué los tamaños son distintos.

<a name="u024"></a>

### U024. Ordenar objetos superpuestos

**Etiquetas:** `SpriteRenderer` · `Order in Layer` · `Orden visual`

Superpón tres sprites y modifica Order in Layer para decidir cuál se dibuja delante. Mantén la posición Z de los tres en 0.

**Pista:** el orden visual se controla desde Sprite Renderer. **Comprueba:** puedes cambiar qué imagen tapa a las otras sin moverlas.

<a name="u025"></a>

### U025. Cambiar la transparencia

**Etiquetas:** `SpriteRenderer` · `Canal alfa` · `Transparencia`

Coloca un sprite sobre otro. Modifica el canal A del color del sprite delantero para hacerlo semitransparente y después completamente transparente.

**Pista:** A significa alfa, la opacidad. **Comprueba:** puedes ver el sprite posterior a través del delantero.

<a name="u026"></a>

### U026. Preparar una hoja de sprites

**Etiquetas:** `Hoja de sprites` · `Sprite Editor` · `Package Manager`

Importa la hoja de imágenes de Pixel Platformer Blocks enlazada al final. Configura Sprite Mode como Multiple y abre Sprite Editor; instala el paquete 2D Sprite desde Package Manager si falta.

**Pista:** una hoja reúne varias imágenes en un archivo. **Comprueba:** puedes ver la textura completa en Sprite Editor.

<a name="u027"></a>

### U027. Separar una hoja en sprites

**Etiquetas:** `Sprite Editor` · `Recorte de sprites` · `Cuadrícula`

**Origen: PDF E52.**

Recorta la hoja de U026 en Sprite Editor utilizando una cuadrícula adecuada al archivo o recortes manuales. Aplica los cambios y coloca al menos dos sprites distintos en la escena.

**Pista:** despliega la textura en Project para ver sus sprites. **Comprueba:** cada objeto muestra una pieza y no toda la hoja.

<a name="u028"></a>

### U028. Crear un objeto con hijos

**Etiquetas:** `Jerarquía` · `Padres e hijos` · `Transform`

Crea un objeto vacío llamado `Personaje` y coloca dos sprites como hijos: cuerpo y adorno. Mueve y gira el padre para observar qué ocurre con ambos.

**Pista:** arrastra los objetos dentro del padre en Hierarchy. **Comprueba:** el conjunto se mueve sin perder la colocación de sus piezas.

<a name="u029"></a>

### U029. Entender la posición local

**Etiquetas:** `Jerarquía` · `Posición local` · `Transform`

Selecciona el adorno de U028 y cambia su posición respecto al padre. Después mueve el padre. Anota la posición que muestra Inspector para el hijo antes y después.

**Pista:** en una jerarquía, Inspector muestra la posición local del hijo. **Comprueba:** mover el padre no cambia esos valores locales.

<a name="u030"></a>

### U030. Activar y desactivar un conjunto

**Etiquetas:** `Activación de objetos` · `Jerarquía` · `Inspector`

Desactiva el objeto padre de U028 con la casilla superior de Inspector. Reactívalo y desactiva solo el adorno. Guarda una copia de esta escena para usarla más adelante.

**Pista:** desactivar un padre también deja inactivos a sus hijos. **Comprueba:** sabes ocultar todo el personaje o solo una pieza.

[Volver al índice](#indice)

<a name="bloque-04"></a>

## 4. Números y datos (U031-U040)

Base: los scripts de U015-U020. Escribe los resultados en `Start()` y utiliza campos del Inspector para probar diferentes datos.

<a name="u031"></a>

### U031. Sumar dos números

**Etiquetas:** `float` · `Suma` · `Inspector`

**Origen: PDF E05.**

Crea dos campos `float`, suma sus valores y muestra el resultado una vez. Prueba con 2.5 y 1.25, y después con un número negativo.

**Pista:** utiliza el operador `+`; los decimales requieren un tipo adecuado. **Comprueba:** el primer resultado es 3.75.

<a name="u032"></a>

### U032. Calcular lo que queda

**Etiquetas:** `int` · `Resta` · `Texto con variables`

Declara `monedasIniciales` y `precio` como enteros. Calcula cuántas monedas quedan después de una compra y muestra los tres valores en una frase.

**Pista:** el operador `-` resta. **Comprueba:** con 10 monedas y precio 4 quedan 6; con precio 12 obtienes -2.

<a name="u033"></a>

### U033. Calcular un coste total

**Etiquetas:** `float` · `int` · `Multiplicación`

Declara un precio decimal y una cantidad entera. Multiplica ambos para calcular el coste de varias unidades. Prueba también con cantidad 0.

**Pista:** el operador `*` multiplica. **Comprueba:** tres unidades de precio 1.5 cuestan 4.5 y cero unidades cuestan 0.

<a name="u034"></a>

### U034. Repartir sin perder decimales

**Etiquetas:** `División` · `int` · `float`

Divide 5 entre 2 usando primero dos variables `int` y después dos `float`. Muestra ambos resultados y explica la diferencia en un comentario. Usa divisores distintos de cero.

**Pista:** el tipo de los operandos determina cómo se hace la división. **Comprueba:** obtienes 2 en la primera prueba y 2.5 en la segunda.

<a name="u035"></a>

### U035. Encontrar el resto

**Etiquetas:** `Operador %` · `Resto` · `int`

Usa dos enteros para calcular cuántas monedas sobran al formar grupos del mismo tamaño. Prueba con 11 monedas en grupos de 3 y con 12 en grupos de 3.

**Pista:** `%` devuelve el resto; usa un tamaño de grupo mayor que cero. **Comprueba:** los restos son 2 y 0.

<a name="u036"></a>

### U036. Hacer una media

**Etiquetas:** `Media aritmética` · `División` · `Decimales`

**Origen: PDF E06.**

Expón tres números enteros en Inspector y calcula su media, conservando la parte decimal. Muestra el resultado una sola vez al iniciar la escena.

**Pista:** suma primero y divide entre `3f`. **Comprueba:** con 1, 2 y 2 el resultado es aproximadamente 1.67, no 1.

<a name="u037"></a>

### U037. Decidir el orden de las operaciones

**Etiquetas:** `Precedencia de operadores` · `Paréntesis` · `Comentarios`

Calcula `2 + 3 * 4` y `(2 + 3) * 4`. Antes de ejecutar, escribe como comentario el resultado que esperas. Comprueba después tu predicción.

**Pista:** los paréntesis cambian qué operación se hace primero. **Comprueba:** los resultados son 14 y 20.

<a name="u038"></a>

### U038. Aumentar un contador

**Etiquetas:** `Contadores` · `Incremento ++` · `int`

Declara una puntuación inicial de 0. Auméntala una unidad tres veces en `Start()`, mostrando el valor después de cada cambio. Repite la prueba con una puntuación inicial de 10.

**Pista:** `++` incrementa una variable entera. **Comprueba:** los mensajes son 1, 2, 3 en la primera prueba y 11, 12, 13 en la segunda.

<a name="u039"></a>

### U039. Guardar un vector del plano

**Etiquetas:** `Vector2` · `Coordenadas X/Y` · `Inspector`

**Origen: PDF E04. Adaptado de Vector3 a Vector2 para trabajar solo en 2D.**

Crea un campo `Vector2` editable desde Inspector y muestra sus dos componentes al iniciar. Prueba los valores X=3 e Y=-2 sin mover todavía ningún objeto.

**Pista:** un vector reúne dos números relacionados, accesibles con `.x` y `.y`. **Comprueba:** modificar una componente no cambia la otra.

<a name="u040"></a>

### U040. Dar nombres claros a los resultados

**Etiquetas:** `Variables` · `Nombres descriptivos` · `Operaciones aritméticas`

Calcula el perímetro de un rectángulo a partir de ancho y alto configurables. Guarda el resultado en una variable con un nombre claro y muestra los datos junto al resultado.

**Pista:** el perímetro suma los cuatro lados. **Comprueba:** ancho 3 y alto 2 producen 10; no aparece un número sin contexto.

[Volver al índice](#indice)

<a name="bloque-05"></a>

## 5. Decisiones (U041-U050)

Base: variables y operaciones. Una condición decide si se ejecuta un grupo de instrucciones encerrado entre llaves.

<a name="u041"></a>

### U041. Tu primera condición

**Etiquetas:** `Condicionales` · `if` · `Igualdad ==`

Crea un campo `vidas`. Usa `if` para mostrar `Sin vidas` solo cuando valga 0. Ejecuta una vez con 0 y otra con 3.

**Pista:** `==` compara; `=` asigna un valor. **Comprueba:** con 3 vidas no aparece el mensaje.

<a name="u042"></a>

### U042. Elegir entre dos respuestas

**Etiquetas:** `Condicionales` · `if` · `else`

Amplía U041 con `else` para mostrar `Puedes jugar` cuando queden vidas. Limita las pruebas a valores de 0 en adelante.

**Pista:** `else` se ejecuta cuando la condición del `if` es falsa. **Comprueba:** en cada ejecución aparece exactamente una respuesta.

<a name="u043"></a>

### U043. Comparar cantidades

**Etiquetas:** `Condicionales` · `Comparaciones` · `Operador >=`

Usa `monedas` y `precio` para mostrar si puedes comprar un objeto. Considera que tener exactamente su precio también permite comprarlo.

**Pista:** compara con `>=`. **Comprueba:** con precio 5, las cantidades 4, 5 y 6 producen las respuestas esperadas.

<a name="u044"></a>

### U044. Exigir dos condiciones

**Etiquetas:** `bool` · `Operadores lógicos` · `Operador &&`

Declara `tieneLlave` y `puertaDesbloqueada`. Muestra `Puedes pasar` únicamente si ambas son verdaderas. Prueba las cuatro combinaciones posibles.

**Pista:** `&&` exige que se cumplan las dos condiciones. **Comprueba:** solo una de las cuatro combinaciones permite pasar.

<a name="u045"></a>

### U045. Aceptar una alternativa

**Etiquetas:** `bool` · `Operadores lógicos` · `Operador ||`

Declara `tieneEntrada` y `estaEnLaLista`. Permite entrar si se cumple al menos una condición. Prueba también el caso en que se cumplen ambas.

**Pista:** `||` significa que basta una de las condiciones. **Comprueba:** solo se deniega la entrada cuando ambas son falsas.

<a name="u046"></a>

### U046. Cambiar un estado al contrario

**Etiquetas:** `bool` · `Negación !` · `Estados`

Declara `luzEncendida`, muestra su valor y cámbialo al contrario con `!`. Vuelve a mostrarlo. Repite partiendo del valor opuesto.

**Pista:** negar un booleano intercambia verdadero y falso. **Comprueba:** el segundo mensaje siempre es distinto del primero.

<a name="u047"></a>

### U047. Clasificar con varios casos

**Etiquetas:** `Condicionales` · `else if` · `Intervalos`

Clasifica una puntuación como baja si es menor que 5, media entre 5 y 9, y alta a partir de 10. Utiliza `if`, `else if` y `else`.

**Pista:** revisa las condiciones en orden. **Comprueba:** prueba 4, 5, 9 y 10; aparece una sola categoría por valor.

<a name="u048"></a>

### U048. Elegir con switch

**Etiquetas:** `switch` · `case` · `default` · `break`

Crea un campo de texto `accion`. Usa `switch` para mostrar respuestas diferentes a `jugar`, `ayuda` y `salir`, y una respuesta por defecto para cualquier otra palabra.

**Pista:** cada `case` termina con `break`; `default` cubre valores desconocidos. **Comprueba:** una palabra inventada también recibe respuesta.

<a name="u049"></a>

### U049. Una calculadora pequeña

**Etiquetas:** `switch` · `Operaciones aritméticas` · `Validación de datos`

**Origen: PDF E07.**

Crea dos números decimales y un símbolo de operación editables en Inspector. Usa `switch` para sumar, restar, multiplicar, dividir o calcular el resto (`+`, `-`, `*`, `/`, `%`). Muestra el resultado una vez.

**Pista:** rechaza divisor cero en `/` y `%`, y símbolos desconocidos. **Comprueba:** prueba las cinco operaciones y ambos errores.

<a name="u050"></a>

### U050. Comprobar un intervalo

**Etiquetas:** `Intervalos` · `Comparaciones` · `Operador &&`

Crea un valor `energia` y muestra si está dentro del intervalo permitido, de 0 a 100 incluidos. Si está fuera, muestra un mensaje que explique el problema.

**Pista:** combina comparaciones con `&&`. **Comprueba:** prueba -1, 0, 50, 100 y 101 sin dejar casos sin respuesta.

[Volver al índice](#indice)

<a name="bloque-06"></a>

## 6. Azar y repeticiones (U051-U060)

Base: condiciones y `Update()`. Un bucle repite instrucciones dentro de una misma llamada; no equivale a esperar al siguiente fotograma.

<a name="u051"></a>

### U051. Un decimal aleatorio por fotograma

**Etiquetas:** `Random.Range` · `float` · `Update`

**Origen: PDF E09.**

Genera en `Update()` un número decimal entre -10 y 10 y escríbelo en Console. Ejecuta solo unos segundos y desactiva después el mensaje para evitar llenar la consola.

**Pista:** usa `Random.Range` con límites `float`. **Comprueba:** aparecen valores con decimales y ninguno queda fuera del intervalo.

<a name="u052"></a>

### U052. Tirar un dado

**Etiquetas:** `Random.Range` · `int` · `Límites de intervalos`

Genera en `Start()` un entero entre 1 y 6. Reinicia varias veces la escena. Compara los límites utilizados con los del ejercicio anterior.

**Pista:** con enteros, el límite superior de `Random.Range` queda excluido. **Comprueba:** el dado nunca muestra 0 ni 7.

<a name="u053"></a>

### U053. Calcular una operación al azar

**Etiquetas:** `Random.Range` · `switch` · `Operaciones aritméticas` · `Validación de datos`

**Origen: PDF E10.**

Reutiliza U049: genera dos números decimales y elige al azar una de sus cinco operaciones. Muestra una vez los operandos, el símbolo y el resultado. Conserva la comprobación de división o resto entre cero.

**Pista:** un entero de 0 a 4 puede representar la operación. **Comprueba:** puedes verificar a mano el cálculo mostrado.

<a name="u054"></a>

### U054. Piedra, papel o tijera

**Etiquetas:** `Random.Range` · `Condicionales` · `Validación de datos` · `Pruebas de casos`

**Origen: PDF E11.**

Elige desde Inspector 1 para piedra, 2 para papel o 3 para tijera. Genera la elección del ordenador y muestra ambas jugadas y el resultado: victoria, derrota o empate.

**Pista:** comprueba primero el empate y rechaza elecciones fuera de 1-3. **Comprueba:** verifica las nueve combinaciones posibles fijando temporalmente la jugada rival.

<a name="u055"></a>

### U055. Contar del 1 al 100

**Etiquetas:** `Bucles` · `for` · `Contadores`

**Origen: PDF E12.**

Escribe un bucle `for` en `Start()` que muestre todos los enteros del 1 al 100. Identifica su valor inicial, condición de continuación e incremento.

**Pista:** el contador debe avanzar hacia el final del intervalo. **Comprueba:** hay 100 mensajes, empezando por 1 y terminando en 100.

<a name="u056"></a>

### U056. Una tabla de multiplicar

**Etiquetas:** `for` · `Multiplicación` · `Texto con variables`

**Origen: PDF E08.**

Recibe un número decimal desde Inspector y muestra su tabla del 1 al 10. Reutiliza el `for` de U055 y muestra en cada línea los factores y el producto.

**Pista:** el contador actúa como segundo factor. **Comprueba:** para 2.5, la primera línea termina en 2.5 y la última en 25.

<a name="u057"></a>

### U057. Cien números con while

**Etiquetas:** `while` · `Random.Range` · `Contadores` · `Terminación de bucles`

**Origen: PDF E13.**

Usa un bucle `while` para mostrar exactamente 100 números aleatorios entre -10 y 10. Lleva la cuenta de cuántos has generado mediante una variable independiente.

**Pista:** inicializa el contador e increméntalo dentro del bucle. **Comprueba:** el bucle termina y Unity sigue respondiendo.

<a name="u058"></a>

### U058. Todas las tablas

**Etiquetas:** `Bucles anidados` · `for` · `Contadores`

**Origen: PDF E14.**

Usa dos bucles `for` anidados para mostrar las tablas del 1 al 10, con multiplicadores del 1 al 10. Identifica qué contador elige la tabla y cuál el multiplicador.

**Pista:** el bucle interior se completa por cada vuelta del exterior. **Comprueba:** aparecen 100 operaciones, desde 1 × 1 hasta 10 × 10.

<a name="u059"></a>

### U059. El primero que consigue cinco victorias

**Etiquetas:** `Bucles` · `Condicionales` · `Contadores` · `Random.Range` · `Terminación de bucles`

**Origen: PDF E15.**

Reutiliza las reglas de U054 para enfrentar a dos jugadores automáticos. Repite rondas aleatorias hasta que uno logre cinco victorias; los empates no suman. Muestra cada ronda, el marcador y el ganador final.

**Pista:** controla victorias, no cinco rondas. Añade un límite de seguridad de 1000 intentos que informe de interrupción. **Comprueba:** solo anuncias ganador si alcanza cinco victorias.

<a name="u060"></a>

### U060. Acumular dentro de un bucle

**Etiquetas:** `Bucles` · `Acumuladores` · `Operador +=`

Calcula la suma de los enteros del 1 al 10 con un bucle. Muestra cómo cambia el acumulador y después el total final. Reinicia la escena para comprobar el valor inicial.

**Pista:** inicializa la suma fuera del bucle y añade cada número con `+=`. **Comprueba:** el total final es 55 en cada ejecución.

[Volver al índice](#indice)

<a name="bloque-07"></a>

## 7. Métodos, referencias y arrays (U061-U070)

Base: variables, condiciones y bucles. Ahora organizarás instrucciones y guardarás referencias a objetos de la escena.

<a name="u061"></a>

### U061. Dar nombre a un grupo de instrucciones

**Etiquetas:** `Métodos` · `Llamadas` · `void`

Crea un método `MostrarBienvenida()` que escriba dos mensajes. Llámalo desde `Start()`. Después elimina temporalmente la llamada, manteniendo la definición del método.

**Pista:** un método propio se ejecuta cuando lo llamas; `void` indica que no devuelve un resultado. **Comprueba:** sin llamada no aparecen sus mensajes.

<a name="u062"></a>

### U062. Pasar un dato a un método

**Etiquetas:** `Métodos` · `Parámetros` · `Reutilización de código`

Crea `Saludar(string nombre)` y úsalo desde `Start()` para saludar a dos nombres distintos. Utiliza el parámetro dentro del mensaje, en lugar de escribir un nombre fijo.

**Pista:** un parámetro permite reutilizar instrucciones con datos diferentes. **Comprueba:** el mismo método produce dos saludos distintos.

<a name="u063"></a>

### U063. Devolver un resultado

**Etiquetas:** `Métodos` · `Parámetros` · `return` · `float`

Convierte la suma de U031 en un método que reciba dos `float` y devuelva otro `float`. Guarda el valor devuelto en una variable y muéstralo desde `Start()`.

**Pista:** `return` devuelve el resultado a quien llamó al método. **Comprueba:** el método calcula y la instrucción que lo llama decide cómo mostrarlo.

<a name="u064"></a>

### U064. Referirse a otro objeto

**Etiquetas:** `Referencias` · `Transform` · `Inspector`

Crea un campo `Transform` llamado `objetivo` y asigna un sprite arrastrándolo desde Hierarchy al Inspector. Muestra su posición X/Y al iniciar. Cambia la referencia por otro sprite.

**Pista:** una referencia permite acceder a un objeto que ya existe. **Comprueba:** el mensaje corresponde al objeto asignado, aunque renombres el objeto.

<a name="u065"></a>

### U065. Detectar una referencia sin asignar

**Etiquetas:** `Referencias` · `null` · `Validación de datos`

Vacía el campo de U064. Añade una condición que compruebe si `objetivo` es `null` antes de acceder a su posición. En ese caso, escribe un mensaje que explique qué falta.

**Pista:** `null` indica ausencia de referencia. **Comprueba:** tanto el campo vacío como el asignado se gestionan sin errores rojos.

<a name="u066"></a>

### U066. Acceder al color desde código

**Etiquetas:** `GetComponent` · `SpriteRenderer` · `Color` · `Referencias`

Obtén el `SpriteRenderer` del mismo objeto al iniciar usando `GetComponent<SpriteRenderer>()`. Guarda la referencia y cambia su color a uno elegido en un campo `Color` del Inspector.

**Pista:** el componente debe estar en el objeto que lleva el script. **Comprueba:** cambiar el campo de color cambia el resultado de la siguiente ejecución.

<a name="u067"></a>

### U067. Guardar varios números juntos

**Etiquetas:** `Arrays` · `Índices` · `Length` · `Validación de datos`

Declara un array de enteros con tres puntuaciones editables en Inspector. Muestra su tamaño y el primer elemento. Antes de leerlo, comprueba que contiene al menos un valor.

**Pista:** los arrays usan `[]`, el primer índice es 0 y `Length` indica su tamaño. **Comprueba:** un array vacío no produce errores.

<a name="u068"></a>

### U068. Recorrer varios sprites

**Etiquetas:** `Arrays` · `foreach` · `SpriteRenderer` · `null`

Guarda tres referencias `SpriteRenderer` en un array del Inspector. Recorre el array con `foreach` y cambia todos los colores al iniciar. Omite las posiciones que no tengan referencia.

**Pista:** `foreach` visita cada elemento sin escribir su índice. **Comprueba:** los tres sprites cambian y un hueco vacío no interrumpe el recorrido.

<a name="u069"></a>

### U069. Elegir un elemento por su índice

**Etiquetas:** `Arrays` · `Índices` · `Validación de datos`

Añade al array de U067 un campo `indiceElegido`. Muestra la puntuación de esa posición únicamente si el índice es válido. En caso contrario, explica el problema en Console.

**Pista:** el índice debe ser mayor o igual que 0 y menor que `Length`. **Comprueba:** prueba -1, 0 y el propio tamaño del array.

<a name="u070"></a>

### U070. Elegir un color de una paleta

**Etiquetas:** `Arrays` · `Random.Range` · `Color` · `SpriteRenderer`

Crea un array de tres colores. Obtén un índice aleatorio válido y aplica el color elegido a un sprite al iniciar. Comprueba antes que la paleta no esté vacía.

**Pista:** combina U052, U066 y U069. **Comprueba:** el sprite solo utiliza colores de la paleta, aunque a veces repita uno.

[Volver al índice](#indice)

<a name="bloque-08"></a>

## 8. Tiempo y movimiento automático (U071-U080)

Base: `Update()`, números, condiciones y `Vector2`. Usa sprites sin cuerpos físicos en este bloque.

<a name="u071"></a>

### U071. Contar fotogramas

**Etiquetas:** `Update` · `Fotogramas` · `Contadores` · `Condicionales`

Incrementa un contador en `Update()` y muestra un mensaje al llegar a 100. Déjalo seguir aumentando sin repetir ese mensaje. Compara lo que cuenta con los segundos de un reloj.

**Pista:** un fotograma es una actualización de la imagen, no un segundo. **Comprueba:** no interpretas el contador como tiempo transcurrido.

<a name="u072"></a>

### U072. Observar deltaTime

**Etiquetas:** `Tiempo` · `Time.deltaTime` · `Fotogramas` · `Console`

**Origen: PDF E03.**

Escribe `Time.deltaTime` en Console en cada fotograma durante unos segundos. Detén Play y compara varios valores. Después desactiva el mensaje repetido.

**Pista:** expresa en segundos el tiempo entre fotogramas. **Comprueba:** sus valores suelen ser fracciones pequeñas, no un contador creciente.

<a name="u073"></a>

### U073. Esperar tres segundos sin bloquear

**Etiquetas:** `Temporizadores` · `Time.deltaTime` · `bool` · `Condicionales`

Acumula `Time.deltaTime` en un `float`. Al alcanzar tres segundos, muestra `Tiempo cumplido` una sola vez usando un booleano para recordar que ya lo has anunciado.

**Pista:** comprueba `>= 3`, no igualdad exacta. **Comprueba:** Unity sigue respondiendo durante la espera y solo aparece un aviso.

<a name="u074"></a>

### U074. Mover hacia abajo y a la derecha

**Etiquetas:** `Movimiento` · `Transform` · `Coordenadas X/Y` · `Update`

**Origen: PDF E16.**

En cada `Update()`, incrementa ligeramente X y reduce ligeramente Y de un sprite. Conserva Z en 0. Observa cómo cambia su posición durante Play.

**Pista:** modifica una copia de `transform.position` y vuelve a asignarla. **Comprueba:** se desplaza hacia la esquina inferior derecha; aún depende de los fotogramas.

<a name="u075"></a>

### U075. Ajustar el paso desde Inspector

**Etiquetas:** `Movimiento` · `Inspector` · `Direcciones` · `Fotogramas`

**Origen: PDF E17.**

Haz que el sprite se mueva hacia abajo y a la izquierda. Expón un valor para regular cuánto avanza en cada fotograma y compara dos valores distintos.

**Pista:** multiplica la dirección por el paso configurable. **Comprueba:** un valor mayor lo desplaza más deprisa; sigue siendo un paso por fotograma.

<a name="u076"></a>

### U076. Medir la velocidad por segundo

**Etiquetas:** `Movimiento` · `Time.deltaTime` · `Velocidad` · `Normalización`

**Origen: PDF E18.**

Mueve el sprite hacia arriba y a la izquierda con velocidad configurable. Multiplica el desplazamiento por `Time.deltaTime`. Normaliza la dirección con `.normalized` para que su longitud sea 1.

**Pista:** el desplazamiento resulta de dirección × velocidad × tiempo. **Comprueba:** en dos segundos recorre aproximadamente el doble que en uno.

<a name="u077"></a>

### U077. Elegir la dirección desde Inspector

**Etiquetas:** `Movimiento` · `Vector2` · `Inspector` · `Normalización`

Amplía U076 con un campo `Vector2` para elegir dirección. Prueba derecha, arriba y diagonal. Si la dirección vale cero, el sprite debe permanecer quieto.

**Pista:** usa la dirección normalizada al calcular el desplazamiento. **Comprueba:** cambiar su orientación no cambia la velocidad total elegida.

<a name="u078"></a>

### U078. Reaparecer al otro lado

**Etiquetas:** `Movimiento` · `Coordenadas X/Y` · `Condicionales` · `Tiempo`

Haz que un sprite avance hacia la derecha. Cuando su X supere 5, colócalo en X=-5 conservando Y. Mantén el movimiento basado en tiempo.

**Pista:** combina movimiento y una condición. **Comprueba:** puedes observar tres vueltas completas sin que el sprite desaparezca definitivamente.

<a name="u079"></a>

### U079. Girar a velocidad constante

**Etiquetas:** `Rotación Z` · `Transform.Rotate` · `Time.deltaTime` · `Inspector`

Haz que un sprite gire dentro del plano a una velocidad configurable en grados por segundo. Modifica únicamente la rotación Z y utiliza `Time.deltaTime`.

**Pista:** `Transform.Rotate` permite aplicar un pequeño giro. **Comprueba:** a 90 grados por segundo tarda unos cuatro segundos en completar una vuelta.

<a name="u080"></a>

### U080. Crecer y detenerse

**Etiquetas:** `Escala` · `Transform` · `Límites` · `Mathf.Min`

Aumenta progresivamente Scale X e Y de un sprite desde 1 hasta 2. Detén el crecimiento al alcanzar el tamaño máximo y conserva su posición.

**Pista:** guarda una escala común y limita el resultado con `Mathf.Min`. **Comprueba:** el sprite crece de forma uniforme y nunca supera el doble.

[Volver al índice](#indice)

<a name="bloque-09"></a>

## 9. Teclado y ratón (U081-U090)

Base: movimiento sin física. Se usará Input System en todas las actividades siguientes; da el foco a la ventana Game para probar controles.

<a name="u081"></a>

### U081. Preparar la entrada de teclado

**Etiquetas:** `Input System` · `Package Manager` · `Configuración` · `Teclado`

Instala Input System desde Package Manager y activa su sistema de entrada cuando Unity lo solicite. Guarda antes de reiniciar el editor. Añade `using UnityEngine.InputSystem;` a un script nuevo.

**Pista:** revisa Active Input Handling en los ajustes de Player. **Comprueba:** el script reconoce `Keyboard` sin errores de compilación.

<a name="u082"></a>

### U082. Detectar una pulsación

**Etiquetas:** `Input System` · `Teclado` · `Pulsaciones` · `null`

Muestra un mensaje al pulsar espacio. Comprueba la tecla dentro de `Update()` y evita acceder a un teclado inexistente comprobando `Keyboard.current != null`.

**Pista:** usa `spaceKey.wasPressedThisFrame`. **Comprueba:** mantener espacio pulsado produce un solo mensaje hasta que lo sueltes y vuelvas a pulsar.

<a name="u083"></a>

### U083. Mantener una tecla pulsada

**Etiquetas:** `Teclado` · `Teclas mantenidas` · `Movimiento` · `Time.deltaTime`

Haz que un sprite se mueva hacia la derecha mientras mantienes D. Debe detenerse al soltarla y conservar la velocidad por segundo de U076.

**Pista:** `dKey.isPressed` indica si la tecla sigue presionada. **Comprueba:** una pulsación larga desplaza más que una breve.

<a name="u084"></a>

### U084. Detectar el ratón

**Etiquetas:** `Input System` · `Ratón` · `Pulsaciones` · `null`

Muestra mensajes distintos al pulsar los botones izquierdo y derecho del ratón. Comprueba primero que `Mouse.current` no sea `null`.

**Pista:** consulta `leftButton` y `rightButton` con `wasPressedThisFrame`. **Comprueba:** cada clic genera un mensaje del botón correcto.

<a name="u085"></a>

### U085. Movimiento con WASD y position

**Etiquetas:** `Teclado` · `Movimiento` · `Vector2` · `Transform` · `Time.deltaTime`

**Origen: PDF E19.**

Construye una dirección `Vector2` a partir de W, A, S y D, empezando de cero en cada `Update()`. Mueve un sprite con `transform.position`, velocidad configurable y `Time.deltaTime`.

**Pista:** las teclas opuestas deben compensarse. **Comprueba:** el sprite se mueve en las cuatro direcciones y se detiene al soltar las teclas.

<a name="u086"></a>

### U086. Movimiento con Translate

**Etiquetas:** `Teclado` · `Movimiento` · `Transform.Translate` · `Coordenadas globales`

**Origen: PDF E20.**

Copia U085 y sustituye la modificación de posición por `transform.Translate`. Conserva WASD, velocidad configurable y tiempo entre fotogramas. Usa el espacio del mundo para mantener los controles aunque gires el sprite.

**Pista:** el parámetro `Space.World` evita que la orientación cambie la dirección. **Comprueba:** W sigue subiendo tras girar la imagen.

<a name="u087"></a>

### U087. Igualar la velocidad diagonal

**Etiquetas:** `Movimiento` · `Normalización` · `Vector2` · `Velocidad`

Compara el recorrido de U085 al mantener D y al mantener W+D durante el mismo tiempo. Normaliza la dirección antes de mover para evitar que las diagonales sean más rápidas.

**Pista:** conserva la dirección cero cuando no hay teclas. **Comprueba:** la distancia total recorrida es aproximadamente igual en ambos casos.

<a name="u088"></a>

### U088. Correr mientras mantienes Shift

**Etiquetas:** `Teclado` · `Teclas mantenidas` · `Velocidad` · `Condicionales`

Amplía U087 con una velocidad normal y otra de carrera, ambas editables. Usa la segunda únicamente mientras mantengas Shift izquierdo; al soltarlo debe recuperarse la primera.

**Pista:** consulta `leftShiftKey.isPressed` y elige una velocidad antes de mover. **Comprueba:** pulsar Shift sin dirección no desplaza al personaje.

<a name="u089"></a>

### U089. No salir de un rectángulo

**Etiquetas:** `Movimiento` · `Coordenadas X/Y` · `Límites` · `Mathf.Clamp`

Limita el movimiento del centro del sprite a X entre -5 y 5 e Y entre -3 y 3. Calcula la nueva posición y ajusta sus componentes antes de asignarla.

**Pista:** `Mathf.Clamp` mantiene un valor entre dos límites. **Comprueba:** sostener una tecla contra el borde no permite sobrepasarlo.

<a name="u090"></a>

### U090. Voltear un sprite

**Etiquetas:** `SpriteRenderer` · `Volteo` · `Teclado` · `Ratón` · `bool`

**Origen: PDF E51.**

Usa una imagen asimétrica. Al pulsar espacio, invierte su orientación horizontal; al hacer clic derecho, invierte la vertical. Cada pulsación debe alternar el valor anterior.

**Pista:** combina `SpriteRenderer.flipX`, `flipY` y `!`. **Comprueba:** dos pulsaciones del mismo control restauran la orientación inicial.

[Volver al índice](#indice)

<a name="bloque-10"></a>

## 10. Seguimiento y cámara (U091-U100)

Base: referencias de U064-U065 y jugador WASD de U087. Usa sprites sin física; la cámara permanece ortográfica.

<a name="u091"></a>

### U091. Seguir de forma instantánea

**Etiquetas:** `Seguimiento` · `Referencias` · `Coordenadas X/Y` · `Transform`

**Origen: PDF E21.**

Añade un segundo sprite y asígnale el jugador como objetivo. Copia su posición X/Y en cada fotograma. Usa tamaños o transparencias diferentes para distinguir ambos aunque estén superpuestos.

**Pista:** comprueba que la referencia al objetivo está asignada. **Comprueba:** ambos ocupan siempre las mismas coordenadas del plano.

<a name="u092"></a>

### U092. Seguir con una separación

**Etiquetas:** `Seguimiento` · `Vector2` · `Desplazamiento relativo` · `Inspector`

**Origen: PDF E44.**

Amplía U091 con un desplazamiento `Vector2` editable desde Inspector. El seguidor debe ocupar la posición del objetivo más ese desplazamiento.

**Pista:** prueba una separación de X=2 e Y=1. **Comprueba:** la distancia relativa se mantiene al mover al jugador en cualquier dirección.

<a name="u093"></a>

### U093. Acercarse con velocidad limitada

**Etiquetas:** `Seguimiento` · `Vector2.MoveTowards` · `Velocidad` · `Time.deltaTime`

Haz que un sprite alcance al jugador sin superar una velocidad configurable por segundo. Cuando llegue, debe detenerse sin atravesar ni sobrepasar su posición.

**Pista:** utiliza `Vector2.MoveTowards` con velocidad multiplicada por `Time.deltaTime`. **Comprueba:** un objetivo lejano no provoca un salto instantáneo.

<a name="u094"></a>

### U094. Seguir con suavidad

**Etiquetas:** `Seguimiento` · `Vector2.SmoothDamp` · `Suavizado` · `Parámetros por referencia`

**Origen: PDF E22.**

Haz que un sprite siga al jugador con aceleración y frenado suaves. Expón un tiempo de suavizado y compara valores pequeños y grandes al arrancar, cambiar de dirección y detenerte.

**Pista:** `Vector2.SmoothDamp` conserva una variable de velocidad pasada con `ref`. **Comprueba:** el seguidor alcanza gradualmente al objetivo al detenerlo.

<a name="u095"></a>

### U095. Seguir solo en horizontal

**Etiquetas:** `Seguimiento` · `Coordenadas X/Y` · `Referencias` · `Movimiento horizontal`

**Origen: PDF E48.**

Copia U091 y haz que el seguidor copie únicamente X. Guarda su propia altura inicial y consérvala aunque el jugador suba o baje.

**Pista:** combina la X del objetivo con la Y fija del seguidor. **Comprueba:** un movimiento exclusivamente vertical del jugador no lo desplaza.

<a name="u096"></a>

### U096. Seguir únicamente desde cerca

**Etiquetas:** `Seguimiento` · `Vector2.Distance` · `Distancias` · `Condicionales`

**Origen: PDF E47.**

Amplía U093 para que el seguidor se mueva solo cuando la distancia entre ambos sea menor que 5 unidades. Cuando sea igual o mayor, debe quedarse quieto.

**Pista:** usa `Vector2.Distance` antes de calcular el desplazamiento. **Comprueba:** prueba distancias menores, iguales y mayores que 5.

<a name="u097"></a>

### U097. Una cámara que sigue al jugador

**Etiquetas:** `Cámara ortográfica` · `Seguimiento` · `LateUpdate` · `Coordenadas X/Y`

Copia X/Y del jugador a la cámara en `LateUpdate()`, conservando la Z inicial de la cámara. Coloca varios sprites fijos para reconocer el desplazamiento del escenario.

**Pista:** `LateUpdate()` permite seguir después del movimiento hecho en `Update()`. **Comprueba:** el jugador permanece centrado y la cámara conserva su profundidad inicial.

<a name="u098"></a>

### U098. Limitar la velocidad de la cámara

**Etiquetas:** `Cámara ortográfica` · `Seguimiento` · `Vector2.MoveTowards` · `Velocidad` · `LateUpdate`

**Origen: PDF E35.**

Reutiliza el jugador WASD con velocidad configurable e independiente de los fotogramas. Cambia U097 para que la cámara lo alcance con una velocidad máxima configurable, en lugar de copiar instantáneamente su posición.

**Pista:** aplica `MoveTowards` a X/Y en `LateUpdate()` y conserva Z. **Comprueba:** una separación grande tarda en recuperarse.

<a name="u099"></a>

### U099. Poner límites a la cámara

**Etiquetas:** `Cámara ortográfica` · `Coordenadas X/Y` · `Límites` · `Mathf.Clamp`

Amplía U098 para limitar el centro de la cámara a un rectángulo configurable. Prueba un escenario mayor que ese rectángulo y mueve al jugador hasta los extremos.

**Pista:** limita X/Y con `Mathf.Clamp`. **Comprueba:** el centro de la cámara no sobrepasa los límites, aunque el jugador siga avanzando.

<a name="u100"></a>

### U100. Un fondo con tres capas

**Etiquetas:** `Paralaje` · `Cámara ortográfica` · `Orden visual` · `Desplazamiento relativo`

**Origen: PDF E45.**

Prepara tres capas de sprites con distintos órdenes visuales. Haz que sigan el desplazamiento X/Y de la cámara con factores diferentes y separaciones configurables para simular paralaje.

**Pista:** conserva posiciones iniciales y aplica una fracción del desplazamiento de cámara. **Comprueba:** al desplazarte, las tres capas se mueven a ritmos distintos.

[Volver al índice](#indice)

<a name="bloque-11"></a>

## 11. Primeros experimentos con física 2D (U101-U110)

**Base y prerrequisitos:** Crea una escena de pruebas con cámara ortográfica; reutiliza los conocimientos de componentes, referencias, métodos, coordenadas y aleatoriedad.

<a name="u101"></a>

### U101. Una caja que cae

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Collider2D` · `Gravedad`

**Origen: PDF E01.**

Crea una cápsula horizontal con CapsuleCollider2D que funcione como suelo estático. Coloca encima una caja con BoxCollider2D y Rigidbody2D de tipo Dynamic. Sin escribir scripts, ejecuta la escena y observa cómo cae la caja hasta apoyarse en la cápsula.

**Pista:** Comprueba los componentes de ambos objetos en el Inspector. **Comprueba:** La caja cae, queda apoyada y la cápsula permanece inmóvil.

<a name="u102"></a>

### U102. Cambiar la intensidad de la gravedad

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Gravity Scale` · `Gravedad`

Duplica la caja y sitúa ambas a la misma altura, separadas horizontalmente. Asigna distintos valores positivos a Gravity Scale de sus Rigidbody2D. Ejecuta varias veces y después prueba un valor cero para descubrir qué controla esta propiedad.

**Pista:** Cambia una sola propiedad entre pruebas. **Comprueba:** Identificas qué caja acelera más al caer y qué sucede con gravedad cero.

<a name="u103"></a>

### U103. Evitar que una caja vuelque

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Restricciones` · `Rotación Z`

Añade una pequeña rampa al suelo y deja caer una caja sobre ella. Observa su rotación. Activa Freeze Rotation Z en las restricciones de su Rigidbody2D y repite la prueba para mantener su orientación mientras puede seguir desplazándose.

**Pista:** En un juego 2D, el giro visible ocurre alrededor de Z. **Comprueba:** La caja puede trasladarse sin girar.

<a name="u104"></a>

### U104. Un cuerpo con dos colliders

**Etiquetas:** `Física 2D` · `Collider2D` · `Rigidbody2D` · `Jerarquía`

**Origen: PDF E23.**

Añade un círculo como hijo de la caja y desplázalo hacia un lado. Ponle CircleCollider2D, pero ningún Rigidbody2D. Sin scripts, deja caer el conjunto sobre la cápsula y observa cómo los dos colliders pertenecen al cuerpo físico de la caja.

**Pista:** El cuerpo del padre reúne también los colliders de sus hijos. **Comprueba:** El círculo acompaña la posición y rotación de la caja y también choca con la cápsula.

<a name="u105"></a>

### U105. Una caja que rebota

**Etiquetas:** `Física 2D` · `Physics Material 2D` · `Rebote` · `Collider2D`

**Origen: PDF E24.**

Crea un suelo plano estático y un Physics Material 2D para el collider de la caja. Sin scripts, modifica su Bounciness para conseguir un rebote visible al caer sobre el suelo. Compara el resultado con otra caja que tenga un material sin rebote.

**Pista:** Mantén iguales las alturas iniciales y la gravedad. **Comprueba:** El material cambia el rebote sin modificar ningún script.

<a name="u106"></a>

### U106. Superficies con distinto rozamiento

**Etiquetas:** `Física 2D` · `Physics Material 2D` · `Rozamiento` · `Comparación de resultados`

Prepara dos rampas iguales y dos cajas sin rebote. Crea materiales físicos 2D con valores de Friction diferentes y aplícalos a cada pareja de caja y rampa. Observa cómo cambia el deslizamiento usando siempre la misma posición inicial.

**Pista:** Evita cambiar la inclinación mientras comparas materiales. **Comprueba:** Puedes explicar cuál de las dos superficies dificulta más el deslizamiento.

<a name="u107"></a>

### U107. Observar Update y FixedUpdate

**Etiquetas:** `Update` · `FixedUpdate` · `Contadores` · `Temporizadores` · `Física 2D`

Añade dos contadores a un script: uno aumenta en Update y otro en FixedUpdate. Muestra sus valores una vez por segundo en la Console. Observa que los fotogramas dibujados y los pasos de simulación física no tienen por qué coincidir.

**Pista:** Reutiliza el temporizador ya aprendido para limitar los mensajes. **Comprueba:** Distingues la actualización visual de la actualización de la física.

<a name="u108"></a>

### U108. Guardar una referencia al cuerpo físico

**Etiquetas:** `Rigidbody2D` · `GetComponent` · `Referencias` · `Inspector` · `Gravedad`

En el script de la caja, declara una variable de tipo Rigidbody2D. Obtén su componente mediante GetComponent en Start y guarda la referencia. Utilízala para cambiar Gravity Scale a un valor configurable desde el Inspector, sin buscar el componente continuamente.

**Pista:** El componente buscado debe estar en el mismo objeto que el script. **Comprueba:** La gravedad de la caja adopta el valor indicado.

<a name="u109"></a>

### U109. Un impulso inicial hacia arriba

**Etiquetas:** `Rigidbody2D` · `AddForce` · `Impulsos` · `Gravedad`

**Origen: PDF E25.**

Coloca una caja apoyada sobre un suelo plano. Usando su referencia a Rigidbody2D, aplica una única fuerza hacia arriba en Start mediante AddForce y ForceMode2D.Impulse. Expón la intensidad en el Inspector y compara tres valores sin cambiar la gravedad.

**Pista:** Un impulso se aplica una vez, no cada fotograma. **Comprueba:** La caja sube y después vuelve a caer por gravedad.

<a name="u110"></a>

### U110. Caer desde una posición aleatoria

**Etiquetas:** `Rigidbody2D` · `Random.Range` · `Coordenadas X/Y` · `Colisiones 2D`

**Origen: PDF E29.**

Construye varios obstáculos estáticos bajo la caja. En Start, elige aleatoriamente su coordenada X entre dos límites del Inspector y conserva una altura fija en la parte superior de la pantalla. Asigna esa posición inicial al Rigidbody2D y deja que la gravedad determine el resto del recorrido.

**Pista:** Reutiliza Random.Range con límites de tipo float. **Comprueba:** Al reiniciar, la caja aparece dentro del intervalo y choca con los obstáculos.

[Volver al índice](#indice)

<a name="bloque-12"></a>

## 12. Controlar personajes mediante física 2D (U111-U120)

**Base y prerrequisitos:** Reutiliza la escena física, el Input System, las referencias a Rigidbody2D, los booleanos y la diferencia entre Update y FixedUpdate.

<a name="u111"></a>

### U111. Saltar al pulsar espacio

**Etiquetas:** `Teclado` · `Salto` · `Impulsos` · `bool` · `FixedUpdate`

**Origen: PDF E26.**

Transforma el impulso inicial en un salto al pulsar espacio. Detecta la pulsación en Update y guarda una solicitud booleana; consúmela una sola vez en FixedUpdate para aplicar el impulso. Por ahora permite saltar incluso cuando la caja está en el aire.

**Pista:** Utiliza Keyboard.current y una pulsación nueva, no una tecla mantenida. **Comprueba:** Cada pulsación genera exactamente un impulso.

<a name="u112"></a>

### U112. Detectar el contacto con el suelo

**Etiquetas:** `Colisiones 2D` · `Detección del suelo` · `Etiquetas de objetos` · `CompareTag`

Crea la etiqueta Suelo y asígnala a un único suelo plano. Añade OnCollisionEnter2D y OnCollisionExit2D al personaje para escribir mensajes cuando empieza y termina el contacto con ese objeto. Comprueba la etiqueta antes de mostrar cada mensaje.

**Pista:** Usa CompareTag sobre el objeto recibido en la colisión. **Comprueba:** Saltar produce una salida y aterrizar produce una entrada.

<a name="u113"></a>

### U113. Saltar solamente cuando hay apoyo

**Etiquetas:** `Salto` · `Detección del suelo` · `bool` · `Condicionales`

Añade un booleano que indique si el personaje está tocando el suelo de la prueba anterior. Actualízalo con los eventos de colisión y exige que sea verdadero antes de aceptar un salto. Desactívalo también al aplicar el impulso para evitar solicitudes repetidas.

**Pista:** Mantén un único suelo plano en esta primera versión. **Comprueba:** Pulsar espacio repetidamente en el aire no añade impulsos.

<a name="u114"></a>

### U114. Experimentar con Transform y gravedad

**Etiquetas:** `Transform` · `Movimiento` · `Física 2D` · `Colisiones 2D` · `Comparación de resultados`

**Origen: PDF E27.**

En una copia de la escena, mueve el personaje con WASD modificando transform.position en Update. Expón la velocidad y utiliza deltaTime; conserva Rigidbody2D, gravedad y colliders. Prueba paredes y suelo para observar las limitaciones de combinar desplazamientos directos con simulación física.

**Pista:** Registra movimientos bruscos, penetraciones o correcciones que observes. **Comprueba:** Explicas por qué esta mezcla puede interferir con la física.

<a name="u115"></a>

### U115. Repetir el experimento en FixedUpdate

**Etiquetas:** `Transform` · `FixedUpdate` · `Time.fixedDeltaTime` · `Física 2D` · `Comparación de resultados`

**Origen: PDF E28.**

Copia el experimento anterior y conserva la lectura del teclado en Update. Guarda la dirección y aplica el desplazamiento por transform.position en FixedUpdate usando Time.fixedDeltaTime. Compara el resultado: cambiar de método no convierte esos desplazamientos directos en un controlador físico correcto.

**Pista:** Usa el tiempo correspondiente al método que aplica el movimiento. **Comprueba:** Comparas ambos experimentos sin asumir que FixedUpdate elimina sus limitaciones.

<a name="u116"></a>

### U116. Avanzar con velocidad física horizontal

**Etiquetas:** `Rigidbody2D` · `linearVelocity` · `Movimiento horizontal` · `FixedUpdate` · `Gravedad`

Vuelve a la escena de salto y sustituye el desplazamiento directo por control de Rigidbody2D.linearVelocity. Lee A y D en Update; en FixedUpdate modifica solamente la componente X según la velocidad del Inspector y conserva la componente Y que produce la física.

**Pista:** Copia la velocidad a un Vector2 antes de cambiar X. **Comprueba:** Puedes avanzar, detenerte y saltar sin anular la gravedad.

<a name="u117"></a>

### U117. Movimiento físico en vista cenital

**Etiquetas:** `Rigidbody2D` · `linearVelocity` · `Movimiento cenital` · `Normalización` · `Colisiones 2D`

Crea una escena vista desde arriba con paredes 2D y un personaje con Gravity Scale cero. Controla su linearVelocity mediante WASD en FixedUpdate, con velocidad configurable. Ajusta la dirección diagonal para que no sea más rápida y bloquea la rotación del cuerpo.

**Pista:** La velocidad física ya expresa distancia por segundo: no la multipliques por deltaTime. **Comprueba:** El personaje conserva su rapidez y choca con paredes.

<a name="u118"></a>

### U118. Un seguidor que camina por el suelo

**Etiquetas:** `Seguimiento` · `Rigidbody2D` · `Movimiento horizontal` · `Distancias` · `Gravedad`

**Origen: PDF E46.**

Adapta el seguimiento a un personaje que avanza horizontalmente sobre suelo, con gravedad y colisiones. Asígnale un objetivo y una velocidad horizontal máxima en el Inspector. Ajusta solamente su velocidad X para acercarse y detenerse a una pequeña distancia, conservando su velocidad vertical.

**Pista:** Esta adaptación de E46 sigue al objetivo sobre suelo, sin perseguir su altura. **Comprueba:** El seguidor frena cerca y respeta las paredes.

<a name="u119"></a>

### U119. Mover una plataforma cinemática

**Etiquetas:** `Rigidbody2D` · `Cuerpos cinemáticos` · `MovePosition` · `FixedUpdate` · `Movimiento`

Crea una plataforma con collider y Rigidbody2D de tipo Kinematic. Define dos posiciones del recorrido y una velocidad. Desplázala con MovePosition en FixedUpdate hasta cada extremo y cambia de dirección al llegar; prueba primero el recorrido libre, sin transportar al jugador.

**Pista:** Calcula cada paso con Time.fixedDeltaTime. **Comprueba:** La plataforma recorre el mismo trayecto de ida y vuelta sin saltos de posición.

<a name="u120"></a>

### U120. Comparar movimiento a 30 y 60 FPS

**Etiquetas:** `Fotogramas` · `Application.targetFrameRate` · `Tiempo` · `Velocidad` · `Comparación de resultados`

En la escena cenital, mide cuánto avanza el personaje durante diez segundos sin obstáculos. Compara límites de 30 y 60 FPS mediante Application.targetFrameRate, desactivando VSync durante la prueba. Comprueba la tasa real y registra si la distancia recorrida cambia de forma apreciable.

**Pista:** Un límite solicitado no garantiza que el equipo lo alcance. **Comprueba:** Relacionas las medidas con el tiempo transcurrido y los FPS observados.

[Volver al índice](#indice)

<a name="bloque-13"></a>

## 13. Zonas, contactos y consecuencias (U121-U130)

**Base y prerrequisitos:** Reutiliza U117: WASD con velocidad del Inspector independiente de los fotogramas; cada interacción requiere Collider2D en ambos objetos y Rigidbody2D en al menos uno.

<a name="u121"></a>

### U121. Entrar en una zona invisible

**Etiquetas:** `Triggers 2D` · `Collider2D` · `Etiquetas de objetos` · `Detección de entrada`

Crea una zona con BoxCollider2D y activa Is Trigger. Desde un script de la zona, detecta OnTriggerEnter2D y muestra un mensaje únicamente cuando entre el personaje, identificado con la etiqueta Jugador. Comprueba que el área permite atravesarla sin bloquear el movimiento.

**Pista:** Un trigger detecta solapamientos sin funcionar como una pared. **Comprueba:** Recibes un mensaje al entrar y puedes seguir caminando.

<a name="u122"></a>

### U122. Detectar entrada y salida

**Etiquetas:** `Triggers 2D` · `Detección de entrada` · `Detección de salida` · `Etiquetas de objetos`

**Origen: PDF E30.**

Amplía la zona anterior con OnTriggerExit2D. Muestra mensajes diferentes cuando el personaje entra y sale, indicando el nombre de la zona. Recorre sus bordes varias veces y observa cuándo se producen los eventos respecto al collider completo del personaje.

**Pista:** Mantén el filtro de etiqueta en los dos métodos. **Comprueba:** Cada recorrido completo produce un mensaje de entrada y otro de salida.

<a name="u123"></a>

### U123. Cambiar de color dentro de la zona

**Etiquetas:** `Triggers 2D` · `SpriteRenderer` · `Color` · `Referencias`

**Origen: PDF E31.**

Haz que el personaje se vuelva rojo al entrar en una zona y recupere el blanco al salir. Guarda una referencia a su SpriteRenderer y cambia su color desde los eventos correspondientes. Utiliza una única zona para observar el comportamiento sin solapamientos.

**Pista:** Reutiliza los cambios de color y las referencias ya aprendidos. **Comprueba:** Permanecer dentro mantiene el rojo y salir devuelve el blanco.

<a name="u124"></a>

### U124. Distinguir dos zonas por su etiqueta

**Etiquetas:** `Triggers 2D` · `Etiquetas de objetos` · `Condicionales` · `Identificación de objetos`

**Origen: PDF E32.**

Crea dos zonas separadas con etiquetas diferentes. Coloca el detector en el personaje y utiliza condiciones para escribir qué zona acaba de atravesar. Incluye en cada mensaje el nombre del objeto que entra y la etiqueta de la zona detectada.

**Pista:** El collider recibido identifica el otro objeto de la interacción. **Comprueba:** La Console distingue las dos zonas y al personaje que entra.

<a name="u125"></a>

### U125. Destruir objetos al tocarlos

**Etiquetas:** `Triggers 2D` · `Destroy` · `Etiquetas de objetos` · `Condicionales`

**Origen: PDF E41.**

Distribuye varios objetos con colliders de tipo trigger y una etiqueta común. Desde el personaje, detecta el contacto con esos objetos y destruye únicamente el objeto encontrado. Conserva las paredes y las zonas anteriores para comprobar que el filtro distingue cada interacción.

**Pista:** Destroy debe recibir el objeto detectado, no el personaje. **Comprueba:** Puedes eliminar varios objetos sin hacer desaparecer paredes ni jugador.

<a name="u126"></a>

### U126. Contar entradas en una zona

**Etiquetas:** `Triggers 2D` · `Contadores` · `Eventos` · `Console`

**Origen: PDF E42.**

Añade un contador entero que aumente cada vez que el personaje entra en una zona. Muestra el total actualizado en la Console. La zona debe permanecer activa para poder salir y volver a entrar; quedarse quieto dentro no debe incrementar continuamente el contador.

**Pista:** Incrementa el valor en el evento de entrada, no en Update. **Comprueba:** Tres entradas completas producen un total de tres.

<a name="u127"></a>

### U127. Un portal de derecha a izquierda

**Etiquetas:** `Triggers 2D` · `Teletransporte` · `Rigidbody2D` · `Referencias` · `Coordenadas X/Y`

**Origen: PDF E62.**

Coloca un portal de entrada a la derecha y una marca de destino a la izquierda. Al entrar el personaje, cambia la posición de su Rigidbody2D al destino mediante una referencia. El destino izquierdo no debe teletransportar de vuelta: el recorrido funciona en un único sentido.

**Pista:** Mantén el destino separado del trigger de entrada. **Comprueba:** Entrar por la derecha lleva a la izquierda sin provocar un bucle.

<a name="u128"></a>

### U128. Perder vida al entrar en peligro

**Etiquetas:** `Triggers 2D` · `Vida` · `Daño` · `Condicionales` · `Límites`

Añade una variable de vida al personaje y una zona etiquetada como peligrosa. Cada entrada debe restar una cantidad configurable y mostrar la vida restante en la Console. Limita el resultado para que nunca sea negativo y prueba varias entradas consecutivas.

**Pista:** Reutiliza las condiciones y la resta de valores. **Comprueba:** El daño solo afecta al personaje y la vida termina en cero.

<a name="u129"></a>

### U129. Dejar tiempo entre dos daños

**Etiquetas:** `Triggers 2D` · `OnTriggerStay2D` · `Temporizadores` · `Daño`

Modifica la zona peligrosa para causar daño mientras el personaje permanece dentro, usando OnTriggerStay2D. Añade un temporizador que permita recibir daño como máximo una vez por segundo, aunque llegue más de una detección. Mantén el temporizador en el personaje para compartirlo entre peligros.

**Pista:** Reduce el tiempo restante y acepta daño cuando haya terminado. **Comprueba:** Permanecer dentro no resta vida en cada paso físico.

<a name="u130"></a>

### U130. Volver al último punto de control

**Etiquetas:** `Puntos de control` · `Reaparición` · `Triggers 2D` · `Rigidbody2D` · `Vida`

Crea una zona de punto de control que guarde su posición en el personaje. Añade otra zona que represente una caída o derrota; al entrar, devuelve el Rigidbody2D a la posición guardada, reinicia su velocidad y recupera la vida inicial.

**Pista:** Guarda la posición inicial como primer punto de control. **Comprueba:** Puedes reaparecer antes y después de activar un punto nuevo.

[Volver al índice](#indice)

<a name="bloque-14"></a>

## 14. Interfaz para mostrar y cambiar valores (U131-U140)

**Base y prerrequisitos:** Reutiliza métodos públicos, referencias, contadores y vida; conserva el Input System y aprende a conectar la interfaz desde el Inspector.

<a name="u131"></a>

### U131. Preparar una interfaz en pantalla

**Etiquetas:** `Interfaz` · `Canvas` · `TextMeshPro` · `EventSystem` · `Input System`

Crea un Canvas con Render Mode Screen Space - Overlay y añade un texto TextMeshPro de interfaz. Si Unity solicita TMP Essential Resources, impórtalos. Comprueba que exista un único EventSystem con InputSystemUIInputModule. Distingue los objetos de la interfaz de los sprites de la escena.

**Pista:** Selecciona el Canvas y revisa sus componentes en el Inspector. **Comprueba:** El texto permanece en pantalla aunque muevas la cámara.

<a name="u132"></a>

### U132. Cinco cuadrados que se adaptan

**Etiquetas:** `Interfaz` · `Canvas Scaler` · `Anclas` · `Resoluciones` · `Imágenes`

**Origen: PDF E36.**

Sin scripts, coloca cinco imágenes cuadradas de colores: una en cada esquina y otra en el centro. Configura Canvas Scaler con Scale With Screen Size y referencia 1920 × 1080. Ajusta anclas y márgenes para conservar su colocación al cambiar la resolución de Game.

**Pista:** Cada cuadrado necesita anclas acordes con su posición. **Comprueba:** Las cuatro esquinas y el centro siguen siendo reconocibles en dos resoluciones.

<a name="u133"></a>

### U133. Comparar tres alineaciones de texto

**Etiquetas:** `Interfaz` · `TextMeshPro` · `Alineación de texto` · `RectTransform`

**Origen: PDF E37.**

Sin scripts, crea tres textos TextMeshPro de interfaz con rectángulos del mismo tamaño. Copia en los tres el siguiente párrafo del documento original. Alinea uno a izquierda, otro centrado y otro a derecha.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam sed eros sollicitudin, porttitor nulla ac, venenatis augue. Duis lacinia hendrerit tellus, sit amet ornare ante blandit in. Nam sollicitudin felis a ultrices placerat. Nunc sed dictum ante.

**Pista:** Mantén iguales la fuente y su tamaño para comparar. **Comprueba:** El contenido coincide y solamente cambia la alineación del párrafo.

<a name="u134"></a>

### U134. Un botón que escribe un mensaje

**Etiquetas:** `Interfaz` · `Botones` · `Eventos` · `Métodos públicos` · `Inspector`

**Origen: PDF E38.**

Coloca un botón en el centro de la pantalla y cambia su texto. Crea un método público sin parámetros que escriba un mensaje en la Console. Conecta el evento On Click del botón con ese método mediante el Inspector y prueba varios clics.

**Pista:** Arrastra al evento el objeto que contiene el script. **Comprueba:** Cada clic produce un único mensaje con el texto elegido.

<a name="u135"></a>

### U135. Mostrar y ocultar un panel sin scripts

**Etiquetas:** `Interfaz` · `Paneles` · `Botones` · `Eventos` · `SetActive`

**Origen: PDF E39.**

Crea un panel de pantalla completa y dos botones superpuestos arriba a la izquierda, fuera del panel y dibujados por delante. Sin scripts, configura On Click: A activa el panel y B, y se desactiva; B desactiva el panel, activa A y se desactiva. Empieza solo con A activo.

**Pista:** Usa tres llamadas a SetActive en cada botón; desactiva el propio botón al final. **Comprueba:** El mismo lugar permite abrir y cerrar repetidamente.

<a name="u136"></a>

### U136. Un botón para sumar puntos

**Etiquetas:** `Interfaz` · `Botones` · `Contadores` · `TextMeshPro` · `Conversión a texto`

**Origen: PDF E40.**

Sitúa un botón en el centro izquierdo y un contador TextMeshPro en el centro derecho. Cada clic debe incrementar una variable entera y actualizar el texto. Guarda una referencia al texto desde el Inspector y muestra cero antes de recibir el primer clic.

**Pista:** Usa `using TMPro;`, una referencia `TMP_Text` y su propiedad `.text`; convierte el número con `ToString()`. **Comprueba:** Cinco clics muestran cinco y reiniciar vuelve a cero.

<a name="u137"></a>

### U137. Reiniciar el contador desde otro botón

**Etiquetas:** `Interfaz` · `Contadores` · `Métodos` · `Reutilización de código` · `TextMeshPro`

Añade un botón para poner a cero el contador anterior. Crea un método que actualice su texto y reutilízalo tanto al sumar como al reiniciar. Comprueba que la variable y la interfaz siempre muestran el mismo resultado después de cualquier combinación de clics.

**Pista:** Centraliza la actualización del texto en un único método. **Comprueba:** Sumar, reiniciar y volver a sumar funciona sin valores desactualizados.

<a name="u138"></a>

### U138. Ajustar la velocidad con un deslizador

**Etiquetas:** `Interfaz` · `Slider` · `Eventos` · `Parámetros` · `Velocidad`

Añade un Slider con límites mínimo y máximo adecuados para la velocidad del personaje cenital. Conecta On Value Changed a un método público que reciba un float y actualice su velocidad. Prueba el efecto mientras mueves al personaje y conserva un valor inicial coherente.

**Pista:** Selecciona la llamada dinámica que utiliza el valor del deslizador. **Comprueba:** Cambiar el Slider modifica la rapidez sin editar el script.

<a name="u139"></a>

### U139. Mostrar la vida en una barra

**Etiquetas:** `Interfaz` · `Slider` · `Vida` · `Referencias`

Crea otro Slider para representar la vida del personaje. Configura su máximo con la vida inicial y actualiza su valor cuando reciba daño o reaparezca. Desactiva su interacción para que el jugador no pueda modificar la salud arrastrando la barra con el ratón.

**Pista:** Reutiliza la variable de vida; no mantengas dos contadores independientes. **Comprueba:** La barra baja con el daño y se recupera al reaparecer.

<a name="u140"></a>

### U140. Recoger objetos y ver el total

**Etiquetas:** `Triggers 2D` · `Recogida de objetos` · `Contadores` · `TextMeshPro` · `Destroy`

**Origen: PDF E43.**

Distribuye varios objetos estáticos con colliders de tipo trigger por la escena cenital. Al tocarlos con el personaje, hazlos desaparecer y suma uno al contador TextMeshPro. Reutiliza un método para actualizar el total y asegúrate de que cada objeto pueda contarse solamente una vez.

**Pista:** Desactiva su collider antes de destruir el objeto recogido. **Comprueba:** El total coincide con las recogidas y no aumenta por permanecer quieto.

[Volver al índice](#indice)

<a name="bloque-15"></a>

## 15. Crear y gestionar copias de objetos (U141-U150)

**Base y prerrequisitos:** Reutiliza el personaje cenital, sus entradas de teclado, los contadores de interfaz, los temporizadores, los arrays y los bucles.

<a name="u141"></a>

### U141. Guardar un objeto como prefab

**Etiquetas:** `Prefabs` · `Instancias` · `SpriteRenderer` · `Inspector`

Crea una ficha visual sencilla con SpriteRenderer y conviértela en prefab guardándola en una carpeta del proyecto. Arrastra dos copias a la escena y modifica el color del prefab para observar la relación con sus instancias. Mantén esta ficha sin componentes físicos.

**Pista:** Distingue el recurso de Project de sus copias en Hierarchy. **Comprueba:** Las dos instancias reciben el cambio de color del prefab.

<a name="u142"></a>

### U142. Crear una copia al pulsar espacio

**Etiquetas:** `Prefabs` · `Instanciación` · `Instantiate` · `Teclado`

**Origen: PDF E59.**

Añade al personaje una referencia al prefab de la ficha, asignada desde el Inspector. Mientras lo controlas con WASD, cada pulsación de espacio debe usar Instantiate para crear una copia en su posición actual. La copia debe permanecer donde apareció cuando el personaje siga avanzando.

**Pista:** Usa una pulsación nueva y crea la copia sin hacerla hija del personaje. **Comprueba:** Puedes dejar varias fichas separadas por la escena.

<a name="u143"></a>

### U143. Contar todas las copias creadas

**Etiquetas:** `Instanciación` · `Contadores` · `TextMeshPro` · `Métodos`

**Origen: PDF E60.**

Añade un contador TextMeshPro que muestre el número total de fichas creadas durante la partida. Incrementa el valor cuando Instantiate cree una copia y actualiza la interfaz. Este contador representa el total histórico, por lo que borrar una ficha no debe reducirlo.

**Pista:** Reutiliza el método que actualiza textos de contador. **Comprueba:** El valor aumenta una vez por copia y coincide con las pulsaciones aceptadas.

<a name="u144"></a>

### U144. Desaparecer después de tres segundos

**Etiquetas:** `Destrucción` · `Destroy` · `Retrasos` · `Instancias`

Añade al prefab un script que programe la destrucción de cada instancia tres segundos después de aparecer. Crea varias fichas en momentos diferentes y observa que cada una conserva su propio plazo. El contador de copias creadas debe seguir mostrando el total histórico.

**Pista:** Destroy permite indicar un retraso antes de eliminar el objeto. **Comprueba:** Cada ficha desaparece aproximadamente tres segundos después de su creación.

<a name="u145"></a>

### U145. Contar solamente las copias que siguen vivas

**Etiquetas:** `Contadores` · `Temporizadores` · `GetComponent` · `Referencias` · `Destrucción`

**Origen: PDF E61.**

Añade un segundo contador para las copias vivas. Al crear cada ficha, pásale una referencia al script contador. Sustituye su destrucción diferida por un temporizador propio: al cumplir tres segundos, debe avisar al contador antes de destruirse. Incrementa el total vivo al crearla.

**Pista:** Obtén el componente de la instancia con GetComponent y llama a un método de inicialización que reciba el contador. **Comprueba:** Sin nuevas creaciones, el contador vivo vuelve a cero.

<a name="u146"></a>

### U146. Crear fichas a intervalos regulares

**Etiquetas:** `Instanciación` · `Temporizadores` · `Métodos` · `Inspector`

Crea un generador fijo que produzca una ficha cada cierto intervalo configurable desde el Inspector. Reutiliza el método de creación y los contadores anteriores. Gestiona el intervalo con un temporizador para que la frecuencia dependa del tiempo transcurrido, no del número de fotogramas.

**Pista:** Reinicia el tiempo de espera después de cada creación. **Comprueba:** Cambiar el intervalo modifica la frecuencia y los contadores permanecen coherentes.

<a name="u147"></a>

### U147. Limitar las fichas presentes

**Etiquetas:** `Condicionales` · `Comparaciones` · `Contadores` · `Instanciación`

Añade al generador un límite máximo de fichas vivas. Antes de cada intento de creación, compara ese límite con el contador actual y crea solamente si queda espacio. Cuando una ficha desaparezca, el generador podrá volver a crear en su siguiente intervalo.

**Pista:** Realiza la comprobación también si mantienes la creación mediante espacio. **Comprueba:** El total vivo nunca supera el límite configurado.

<a name="u148"></a>

### U148. Construir una fila con un bucle

**Etiquetas:** `Bucles` · `for` · `Instanciación` · `Coordenadas X/Y`

En una copia de la escena, sustituye la generación periódica por una fila creada al iniciar. Usa un bucle for, una cantidad y una separación configurables. Calcula la posición de cada ficha desde un origen común y permite suficientes objetos vivos para completar la fila.

**Pista:** Multiplica el índice del bucle por la separación horizontal. **Comprueba:** Cambiar cantidad y distancia produce una fila regular sin duplicar instrucciones.

<a name="u149"></a>

### U149. Borrar una fila guardada en un array

**Etiquetas:** `Arrays` · `Bucles` · `Destrucción` · `null` · `Contadores`

Para esta prueba, utiliza una copia del prefab sin autodestrucción. Guarda las fichas de la fila en un array al crearlas. Añade una tecla que recorra ese array y destruya sus objetos; comprueba cada referencia para poder repetir la acción cuando ya no quede ninguno. Actualiza también el contador vivo.

**Pista:** Una referencia a un objeto destruido debe comprobarse antes de usarla. **Comprueba:** La fila desaparece y repetir la tecla no genera errores.

<a name="u150"></a>

### U150. Generar dentro de un área delimitada

**Etiquetas:** `Random.Range` · `Coordenadas X/Y` · `Límites` · `Instanciación`

Recupera el generador periódico con límite de objetos vivos. Define valores mínimos y máximos para X e Y en el Inspector y genera cada ficha en una posición aleatoria dentro de ese rectángulo. Coloca cuatro marcas visuales en sus esquinas para comprobar los límites.

**Pista:** Obtén aleatoriamente cada coordenada por separado. **Comprueba:** Las fichas aparecen dentro del área y siguen respetando el máximo de objetos vivos.

[Volver al índice](#indice)

<a name="bloque-16"></a>

## 16. Mapas y animaciones (U151-U160)

Base del bloque: reutiliza el spritesheet recortado de U027, las jerarquías de U028 y un jugador con movimiento 2D.

<a name="u151"></a>

### U151. Crear una paleta de piezas

**Etiquetas:** `Tile Palette` · `Tiles` · `Hoja de sprites` · `Package Manager`

Abre Tile Palette y crea una paleta con los sprites del spritesheet que recortaste en U027. Si falta la ventana, instala 2D Tilemap Editor desde Package Manager. Guarda los recursos Tile en una carpeta propia y coloca al menos seis piezas diferentes en la paleta.

**Pista:** una paleta reúne las piezas que usarás para pintar un mapa. **Comprueba:** seleccionas cada pieza sin volver al spritesheet original.

<a name="u152"></a>

### U152. Dibujar un mapa con Tilemap

**Etiquetas:** `Tilemap` · `Grid` · `Tile Palette` · `Diseño de niveles`

**Origen: PDF E53.**

Crea un Tilemap rectangular y dibuja un escenario pequeño utilizando la paleta anterior, sin escribir scripts. Incluye un suelo reconocible, varios obstáculos y una zona de inicio. Corrige al menos una pieza usando la herramienta de borrar.

**Pista:** Grid organiza las celdas y Tilemap contiene las piezas pintadas. **Comprueba:** el escenario se ve completo desde la cámara 2D.

<a name="u153"></a>

### U153. Hacer sólido el mapa

**Etiquetas:** `TilemapCollider2D` · `Colisiones 2D` · `Rigidbody2D` · `Tiles`

Añade TilemapCollider2D al mapa y prueba encima el jugador con Rigidbody2D que ya utilizaste. Ajusta el tipo de colisión de las piezas necesarias para que el suelo y los obstáculos detengan al jugador. Mantén el escenario inmóvil.

**Pista:** utiliza piezas con Collider Type distinto de None. **Comprueba:** el jugador se apoya en el suelo y no atraviesa los obstáculos.

<a name="u154"></a>

### U154. Separar fondo y obstáculos

**Etiquetas:** `Tilemap` · `Grid` · `Orden visual` · `Colisiones 2D`

Separa el escenario en dos Tilemaps dentro del mismo Grid: uno para decoración y otro para obstáculos. Mueve algunas piezas a su capa correspondiente y ajusta su orden de dibujo. Deja las colisiones únicamente en las piezas que deban bloquear al jugador.

**Pista:** revisa Order in Layer en cada Tilemap Renderer. **Comprueba:** el jugador atraviesa la decoración y sigue chocando con los obstáculos.

<a name="u155"></a>

### U155. Animar una transformación

**Etiquetas:** `Animación 2D` · `Transform` · `Fotogramas clave` · `Clips de animación`

**Origen: PDF E33.**

Selecciona un sprite y crea una animación con la ventana Animation, sin escribir scripts. Durante el clip, cambia su posición en X e Y, su rotación alrededor de Z y su escala en X e Y. Mantén el movimiento dentro del plano 2D.

**Pista:** añade fotogramas al principio, en medio y al final. **Comprueba:** al reproducir el clip se distinguen las tres transformaciones.

<a name="u156"></a>

### U156. Animar dos piezas juntas

**Etiquetas:** `Animación 2D` · `Jerarquía` · `Fotogramas clave` · `Clips de animación`

**Origen: PDF E34.**

Crea un objeto padre con dos sprites hijos, como un cuerpo y una antena. Desde el padre, graba un único clip que cambie posición, rotación Z y escala de sus hijos. Anima ambos sprites sin escribir scripts ni crear clips independientes.

**Pista:** selecciona cada hijo mientras grabas el clip del padre. **Comprueba:** una sola reproducción anima las dos piezas de forma coordinada.

<a name="u157"></a>

### U157. Crear una animación de carrera

**Etiquetas:** `Animación 2D` · `Hoja de sprites` · `Sprites` · `Repetición de clips`

**Origen: PDF E54.**

Descarga un personaje de [Dino Characters](https://arks.itch.io/dino-characters), importa su spritesheet y separa los fotogramas de carrera. Crea una animación que los reproduzca en orden y se repita, sin escribir scripts. Ajusta la velocidad hasta reconocer claramente el movimiento.

**Pista:** conserva el mismo tamaño de corte para todos los fotogramas. **Comprueba:** el dinosaurio corre sin saltos de tamaño ni imágenes mezcladas.

<a name="u158"></a>

### U158. Cambiar de animación con espacio

**Etiquetas:** `Animator` · `Transiciones` · `bool` · `Teclado`

**Origen: PDF E55.**

Prepara dos animaciones del mismo personaje, por ejemplo reposo y carrera, y colócalas en su Animator. Añade un parámetro booleano y las transiciones necesarias. Escribe un script que invierta ese parámetro cada vez que pulses espacio.

**Pista:** utiliza una pulsación nueva y revisa las condiciones de ambas transiciones. **Comprueba:** cada toque alterna una vez entre las dos animaciones.

<a name="u159"></a>

### U159. Animar según el movimiento

**Etiquetas:** `Animator` · `Vectores` · `Movimiento` · `Condicionales`

Reutiliza el personaje anterior y conecta el parámetro del Animator con el movimiento WASD. Activa la carrera cuando la entrada de movimiento tenga alguna dirección y vuelve a reposo cuando no la tenga. Comprueba también las combinaciones de dos teclas.

**Pista:** aprovecha el vector de movimiento que ya calcula tu script. **Comprueba:** la animación responde al empezar y al terminar de caminar.

<a name="u160"></a>

### U160. Mirar hacia donde caminas

**Etiquetas:** `SpriteRenderer` · `flipX` · `Movimiento` · `Condicionales`

Haz que el sprite mire a la derecha al caminar hacia la derecha y a la izquierda al caminar hacia la izquierda. Cuando el personaje se detenga, conserva la última orientación. Mantén el comportamiento de las animaciones que ya preparaste.

**Pista:** cambia flipX del SpriteRenderer solo cuando haya movimiento horizontal. **Comprueba:** girar al personaje no modifica sus colisiones ni invierte la interfaz.

[Volver al índice](#indice)

<a name="bloque-17"></a>

## 17. Acciones por proximidad y reglas de juego (U161-U170)

Base del bloque: reutiliza un jugador WASD, enemigos sencillos, colisiones 2D, contadores y la persecución cercana de U096.

<a name="u161"></a>

### U161. Medir distancias a varios enemigos

**Etiquetas:** `Arrays` · `Bucles` · `Distancias` · `Vector2` · `Depuración`

Coloca cinco enemigos inmóviles y guarda sus referencias en un array asignado desde el Inspector. Al pulsar una tecla, recorre el array y muestra en Console el nombre y la distancia 2D de cada enemigo respecto al jugador.

**Pista:** calcula cada distancia con posiciones tratadas como Vector2. **Comprueba:** al mover al jugador cambian las distancias de todos los enemigos.

<a name="u162"></a>

### U162. Encontrar objetos en un círculo

**Etiquetas:** `Physics2D.OverlapCircleAll` · `LayerMask` · `Capas físicas` · `Collider2D`

Añade un Collider2D a cada enemigo y crea una capa física desde Layer > Add Layer, distinta del orden visual. Asigna los enemigos a ella y selecciónala en un campo LayerMask. Consulta Physics2D.OverlapCircleAll con radio 3 y ese filtro; muestra cuántos detecta.

**Pista:** utiliza un único collider por enemigo y excluye al jugador de la capa. **Comprueba:** detectas solo enemigos cuyos colliders alcanzan el círculo.

<a name="u163"></a>

### U163. Destruir enemigos cercanos

**Etiquetas:** `Distancias` · `Comparaciones` · `Destrucción` · `null`

**Origen: PDF E56.**

Prepara varios enemigos estáticos y un jugador que se mueva con WASD. Al pulsar espacio, destruye todos los enemigos cuya distancia entre centros sea menor que 3 unidades. Conserva los que estén a 3 unidades o más y permite repetir la acción.

**Pista:** comprueba la distancia exacta de cada candidato y omite referencias vacías. **Comprueba:** una pulsación puede eliminar varios enemigos simultáneamente.

<a name="u164"></a>

### U164. Provocar una explosión de impulso

**Etiquetas:** `Rigidbody2D` · `AddForce` · `ForceMode2D.Impulse` · `Vectores` · `Distancias`

**Origen: PDF E57.**

Construye una habitación con suelo, paredes y techo estáticos, y varios cuerpos con Rigidbody2D dinámico. Mueve al jugador con WASD. Al pulsar espacio, aplica un impulso hacia fuera a los cuerpos cuyo centro esté a menos de 3 unidades del jugador.

**Pista:** Reutiliza el filtro de U162, resta posiciones y aplica AddForce con ForceMode2D.Impulse; usa un collider por cuerpo. **Comprueba:** Solo los cuerpos cercanos reciben impulso hacia fuera.

<a name="u165"></a>

### U165. Invertir la gravedad

**Etiquetas:** `Physics2D.gravity` · `Física 2D` · `Estado global` · `Ciclo de vida`

**Origen: PDF E58.**

Reutiliza la habitación cerrada con varios cuerpos físicos y haz que espacio invierta Physics2D.gravity. Guarda su valor original al entrar y restáuralo al desactivar el controlador, para no alterar otras escenas. Observa cómo los cuerpos pasan del suelo al techo.

**Pista:** la gravedad 2D afecta globalmente a los cuerpos dinámicos. **Comprueba:** dos pulsaciones recuperan la dirección inicial y salir restaura el valor guardado.

<a name="u166"></a>

### U166. Patrullar entre dos puntos

**Etiquetas:** `Movimiento` · `Patrullas` · `Referencias` · `Estados`

Crea dos objetos vacíos como extremos de una patrulla y asigna sus referencias a un enemigo visual sin Rigidbody2D. Haz que avance hacia el primer punto y cambie de destino al llegar. Repite el recorrido con una velocidad ajustable desde el Inspector.

**Pista:** guarda cuál de los dos puntos es el destino actual. **Comprueba:** el enemigo completa varias vueltas sin detenerse ni sobrepasar los extremos.

<a name="u167"></a>

### U167. Alternar patrulla y persecución

**Etiquetas:** `Patrullas` · `Persecución` · `Distancias` · `Condicionales`

Combina la patrulla anterior con la persecución cercana de U096. Mientras el jugador esté lejos, el enemigo patrulla; cuando entre en el radio elegido, lo persigue. Al alejarse el jugador, el enemigo retoma su recorrido entre los dos puntos.

**Pista:** Utiliza una condición para escoger un único comportamiento y conserva el enemigo sin física de U166. **Comprueba:** Acercarte y alejarte cambia su comportamiento.

<a name="u168"></a>

### U168. Abrir una puerta con una llave

**Etiquetas:** `Triggers 2D` · `bool` · `Condicionales` · `Colisiones 2D`

Coloca una llave con trigger y una puerta que bloquee el paso. Al recoger la llave, guarda ese hecho en una variable booleana. Cuando el jugador entre en una zona delante de la puerta, ábrela únicamente si ya tiene la llave.

**Pista:** separa el trigger de detección del collider que bloquea. **Comprueba:** sin llave no pasas y, después de recogerla, sí puedes cruzar.

<a name="u169"></a>

### U169. Ganar al recoger tres monedas

**Etiquetas:** `Contadores` · `Condiciones de victoria` · `Estados de partida` · `Interfaz`

Reutiliza el contador de monedas y coloca exactamente tres en una escena pequeña. Cuando el jugador recoja la tercera, muestra un mensaje de victoria y desactiva su movimiento. Evita que recoger cada moneda pueda sumar más de una vez.

**Pista:** Comprueba el total tras aumentarlo; bloquea nuevas entradas y deja la velocidad física en cero. **Comprueba:** La tercera moneda detiene al jugador.

<a name="u170"></a>

### U170. Perder al agotar las vidas

**Etiquetas:** `Vida` · `Condiciones de derrota` · `Estados de partida` · `Interfaz`

Reutiliza tu sistema de vida y añade una condición de derrota cuando llegue a cero. Muestra un mensaje y desactiva el movimiento. Impide que nuevos contactos con peligros sigan restando vida o repitan la presentación de la derrota.

**Pista:** guarda si la partida ha terminado antes de procesar más daño. **Comprueba:** la vida se mantiene en cero y el mensaje aparece una vez.

[Volver al índice](#indice)

<a name="bloque-18"></a>

## 18. Sonidos y música (U171-U180)

Base del bloque: reutiliza monedas, triggers, prefabs, botones y sliders, y prepara un efecto corto y una pista musical que puedas utilizar.

<a name="u171"></a>

### U171. Reproducir un sonido 2D

**Etiquetas:** `Audio 2D` · `AudioSource` · `AudioClip` · `AudioListener`

Importa un efecto de sonido corto y asigna el clip a un AudioSource de la escena. Configura Spatial Blend en 0 para reproducirlo como audio 2D. Activa Play On Awake y escucha el resultado al iniciar la escena.

**Pista:** revisa el volumen y que la cámara conserve su AudioListener. **Comprueba:** el efecto se escucha sin depender de la posición del jugador.

<a name="u172"></a>

### U172. Escuchar una moneda al entrar

**Etiquetas:** `Audio 2D` · `AudioSource` · `OnTriggerEnter2D` · `Triggers 2D`

**Origen: PDF E63.**

Coloca una zona con Collider2D marcado como trigger. Cuando el jugador entre, reproduce un sonido de moneda mediante un AudioSource, aunque no recoja ningún objeto. Permite volver a escucharlo si sale de la zona y entra otra vez.

**Pista:** filtra al jugador y reproduce el sonido desde OnTriggerEnter2D. **Comprueba:** quedarse dentro no dispara el efecto continuamente.

<a name="u173"></a>

### U173. Crear un objeto con sonido

**Etiquetas:** `Audio 2D` · `AudioSource` · `Prefabs` · `Instanciación`

**Origen: PDF E64.**

Reutiliza un prefab que aparezca al pulsar espacio y añade un sonido a cada aparición. Configura su AudioSource para reproducir el efecto al crearse o actívalo desde el código de creación. Mantén una sola reproducción por objeto generado.

**Pista:** elige una sola forma de iniciar el audio para evitar duplicados. **Comprueba:** tres pulsaciones generan tres objetos y tres sonidos.

<a name="u174"></a>

### U174. Repetir una música de fondo

**Etiquetas:** `Audio 2D` · `AudioSource` · `Música` · `Repetición de audio`

**Origen: PDF E65.**

Crea un objeto independiente para la música de fondo y asígnale un AudioSource 2D. Activa Loop y Play On Awake. Ajusta su volumen para que puedas distinguir los efectos de las monedas mientras la música continúa durante toda la escena.

**Pista:** empieza con un volumen moderado y escucha el final del clip. **Comprueba:** la música vuelve a empezar sin que tengas que pulsar nada.

<a name="u175"></a>

### U175. Ajustar el volumen con un slider

**Etiquetas:** `Slider` · `Eventos` · `AudioSource` · `Volumen`

Reutiliza un slider de interfaz y configura su rango entre 0 y 1. Conecta su cambio de valor con el volumen del AudioSource de música. Al iniciar, coloca el slider en el valor que realmente esté utilizando la música.

**Pista:** utiliza On Value Changed para transmitir el valor del slider. **Comprueba:** ambos extremos permiten silenciar la música y recuperar su volumen máximo.

<a name="u176"></a>

### U176. Silenciar sin perder el volumen

**Etiquetas:** `AudioSource.mute` · `bool` · `Botones` · `Textos de interfaz`

Añade un botón que alterne entre silenciar y recuperar la música. Utiliza la propiedad mute del AudioSource para conservar el volumen que elegiste con el slider. Cambia el texto del botón para indicar la acción disponible en cada momento.

**Pista:** invierte un estado booleano en cada pulsación. **Comprueba:** al recuperar el sonido se mantiene el volumen seleccionado antes de silenciar.

<a name="u177"></a>

### U177. Pausar y continuar la música

**Etiquetas:** `AudioSource.Pause` · `AudioSource.UnPause` · `Botones` · `Reproducción de audio`

Añade un botón para pausar la música y otro para continuarla desde el mismo instante. Conserva los controles de volumen y silencio. Escucha un fragmento reconocible antes de pausar para poder comprobar después que no vuelve al principio.

**Pista:** compara Pause y UnPause con el comportamiento de Stop. **Comprueba:** reanudar continúa el fragmento y no reinicia la pista musical.

<a name="u178"></a>

### U178. Dar sonido a un botón

**Etiquetas:** `Botones` · `Eventos` · `AudioSource` · `Audio 2D`

Añade un sonido corto a uno de tus botones de interfaz. Reprodúcelo desde un AudioSource independiente cuando llegue el evento On Click y conserva también la acción original del botón. Prueba varios clics sin mantener el botón pulsado.

**Pista:** un mismo evento puede ejecutar más de una acción. **Comprueba:** cada clic realiza su función y reproduce una sola confirmación sonora.

<a name="u179"></a>

### U179. Terminar el sonido de una moneda

**Etiquetas:** `AudioSource.PlayOneShot` · `Destrucción` · `Referencias` · `Contadores`

Haz que una moneda desaparezca al recogerla y que su sonido se escuche completo. Traslada la reproducción a un emisor independiente que permanezca en la escena, aunque la moneda se destruya inmediatamente. Reutiliza el contador de monedas existente.

**Pista:** reproduce el clip desde un AudioSource de la escena con PlayOneShot. **Comprueba:** la moneda desaparece sin cortar el final del sonido.

<a name="u180"></a>

### U180. Variar ligeramente un efecto

**Etiquetas:** `AudioSource.pitch` · `Random.Range` · `Audio 2D`

Reutiliza un efecto corto y cambia ligeramente su pitch antes de cada reproducción, eligiendo un valor aleatorio entre 0,9 y 1,1. Haz la prueba con pulsaciones separadas para escuchar cada variación completa. Mantén la música con su tono habitual.

**Pista:** cambia el pitch del AudioSource dedicado al efecto. **Comprueba:** las reproducciones se parecen, pero no suenan todas exactamente iguales.

[Volver al índice](#indice)

<a name="bloque-19"></a>

## 19. Escenas, pausa y datos guardados (U181-U190)

Base del bloque: reutiliza botones, temporizadores y música, y guarda una copia de las escenas antes de añadir navegación entre ellas.

<a name="u181"></a>

### U181. Preparar tres escenas de colores

**Etiquetas:** `Escenas` · `Cámara ortográfica` · `Build Profiles` · `Textos de interfaz`

Crea tres escenas llamadas e66_red, e66_blue y e66_green. Configura el fondo de sus cámaras ortográficas en rojo, azul y verde respectivamente, y añade un texto que identifique cada escena. Inclúyelas en la lista de escenas de Build Profiles.

**Pista:** guarda cada escena antes de añadirla a la lista. **Comprueba:** sus nombres coinciden exactamente y los tres fondos se distinguen al ejecutarlas.

<a name="u182"></a>

### U182. Cargar la escena roja con espacio

**Etiquetas:** `Escenas` · `SceneManager` · `Input System` · `Teclado`

**Origen: PDF E66.**

Añade a las tres escenas un controlador que cargue e66_red cuando pulses espacio. Utiliza SceneManager para realizar el cambio y una pulsación nueva del Input System. Prueba la acción empezando desde cada una de las tres escenas.

**Pista:** SceneManager pertenece a UnityEngine.SceneManagement. **Comprueba:** desde azul o verde pasas a rojo, y desde rojo recargas la misma escena.

<a name="u183"></a>

### U183. Cargar la escena azul con un botón

**Etiquetas:** `Escenas` · `SceneManager` · `Botones` · `Métodos públicos`

**Origen: PDF E66.**

Coloca un botón visible en cada una de las tres escenas y conecta su evento On Click con un método que cargue e66_blue. Mantén también la navegación con espacio y comprueba ambas acciones desde las tres escenas disponibles.

**Pista:** utiliza un método público sin parámetros para conectarlo desde el Inspector. **Comprueba:** cualquier botón lleva a azul y espacio sigue llevando a rojo.

<a name="u184"></a>

### U184. Cambiar tras diez segundos de inactividad

**Etiquetas:** `Temporizadores` · `Time.deltaTime` · `Input System` · `Escenas`

**Origen: PDF E66.**

Añade a las tres escenas un temporizador de inactividad que cargue e66_green al alcanzar diez segundos. Reinicia la cuenta al pulsar cualquier tecla, mover el ratón, usar su rueda o pulsar sus botones. Reutiliza tu temporizador con Time.deltaTime.

**Pista:** consulta Keyboard.current y Mouse.current comprobando que existan. **Comprueba:** nueve segundos de espera y una entrada reinician los diez segundos completos.

<a name="u185"></a>

### U185. Mantener la música al cambiar de escena

**Etiquetas:** `Escenas` · `DontDestroyOnLoad` · `Persistencia entre escenas` · `Música`

**Origen: PDF E67.**

Crea e67_red y e67_blue con sus fondos correspondientes. Inicia música en roja y conserva su objeto raíz con DontDestroyOnLoad. Al pulsar espacio, carga azul y comprueba que la misma pista sigue sonando desde el punto alcanzado, sin reiniciarse.

**Pista:** registra ambas escenas y deja el objeto de música sin padre. **Comprueba:** el cambio de color no interrumpe ni reinicia la canción.

<a name="u186"></a>

### U186. Evitar música duplicada al regresar

**Etiquetas:** `Persistencia entre escenas` · `static` · `Awake` · `Destrucción` · `AudioSource`

Añade un botón para volver de e67_blue a e67_red. Guarda una referencia compartida, mediante un campo static, al reproductor conservado. En Awake, conserva la primera instancia e inicia su audio con Play; destruye las nuevas copias sin reproducirlas. Mantén desactivado Play On Awake.

**Pista:** Awake prepara el objeto antes de Start; static comparte la referencia entre copias. **Comprueba:** Varios viajes conservan una sola canción, que no reinicia.

<a name="u187"></a>

### U187. Reiniciar la escena actual

**Etiquetas:** `Escenas` · `SceneManager.GetActiveScene` · `Reinicio de partida` · `Botones`

Añade un botón de reinicio a una escena de juego ya terminada. Carga de nuevo la escena activa usando su nombre y comprueba que recupera su estado inicial: posición del jugador, monedas presentes y contador. Mantén la música persistente si existe.

**Pista:** consulta el nombre con SceneManager.GetActiveScene(). **Comprueba:** reiniciar después de jugar recupera los valores iniciales sin crear otra copia de la música.

<a name="u188"></a>

### U188. Mostrar un menú de pausa

**Etiquetas:** `Time.timeScale` · `Pausa` · `Estados de partida` · `Interfaz` · `Ciclo de vida`

Añade un panel con un botón para continuar y alterna la pausa con Escape. Detén el tiempo del juego con Time.timeScale, bloquea las acciones del jugador y muestra el panel. Al continuar o abandonar la escena, restablece el tiempo a 1.

**Pista:** usa un booleano de pausa y restaura el tiempo al desactivar el controlador. **Comprueba:** los objetos se detienen y el botón permite continuar.

<a name="u189"></a>

### U189. Guardar una mejor puntuación

**Etiquetas:** `PlayerPrefs` · `Persistencia de datos` · `Puntuación` · `Comparaciones` · `Interfaz`

Reutiliza una escena con puntuación y guarda su mejor resultado mediante PlayerPrefs. Al terminar, compara la puntuación actual con el récord guardado y actualízalo solo si lo supera. Muestra el récord en un texto de interfaz al entrar.

**Pista:** usa una clave fija y un valor inicial de cero. **Comprueba:** una partida peor no sustituye el mejor resultado obtenido anteriormente.

<a name="u190"></a>

### U190. Comprobar la recuperación de datos

**Etiquetas:** `PlayerPrefs.Save` · `PlayerPrefs.DeleteKey` · `Persistencia de datos` · `Pruebas`

Prueba el récord anterior deteniendo y volviendo a iniciar Play. Añade un botón de prueba que borre únicamente la clave del récord y actualice su texto. Comprueba el valor inicial, una mejora y una puntuación inferior; repetirás la prueba en el ejecutable de U200.

**Pista:** utiliza Save para guardar y DeleteKey para borrar esa clave. **Comprueba:** reiniciar conserva el récord y el botón lo devuelve a cero.

[Volver al índice](#indice)

<a name="bloque-20"></a>

## 20. Pequeños retos y entrega del proyecto (U191-U200)

Base del bloque: combina escenas y prefabs ya terminados; centra cada ejercicio en una modificación pequeña y una prueba concreta.

<a name="u191"></a>

### U191. Abrir con tres interruptores

**Etiquetas:** `Triggers 2D` · `bool` · `Contadores` · `Condicionales` · `SpriteRenderer`

Reutiliza la puerta de U168 y sustituye la llave por tres interruptores con trigger. Cada interruptor debe activarse solo una vez y cambiar de color. Abre la puerta cuando los tres estén activados, sin exigir un orden específico.

**Pista:** guarda un booleano por interruptor y cuenta las activaciones nuevas. **Comprueba:** pisar varias veces el mismo interruptor no abre la puerta antes de tiempo.

<a name="u192"></a>

### U192. Recoger monedas antes de que termine el tiempo

**Etiquetas:** `Cuenta atrás` · `Contadores` · `Estados de partida` · `Condiciones de victoria` · `Condiciones de derrota`

Combina el temporizador de U073 con las monedas de U140 y la victoria de U169. Transforma el temporizador en una cuenta atrás desde treinta segundos. Muestra victoria al recoger las tres monedas o derrota al agotarse el tiempo, deteniendo la partida.

**Pista:** usa un único estado de partida terminada para resolver el resultado. **Comprueba:** después de ganar no aparece una derrota por el temporizador.

<a name="u193"></a>

### U193. Llegar a una meta saltando

**Etiquetas:** `Salto` · `Plataformas 2D` · `Triggers 2D` · `Condiciones de victoria`

Reutiliza el movimiento y salto de U116. Prepara dos plataformas con etiqueta Suelo, separadas para que el jugador no toque ambas simultáneamente. Coloca una meta con trigger después de la segunda y adapta la victoria de U169 para terminar al llegar.

**Pista:** ajusta las distancias utilizando el salto que ya funciona. **Comprueba:** puedes completar el recorrido y la victoria aparece únicamente al tocar la meta.

<a name="u194"></a>

### U194. Encontrar una referencia vacía

**Etiquetas:** `Depuración` · `Console` · `null` · `Inspector`

En una copia de una escena, deja sin asignar una referencia que utilice tu script, por ejemplo el texto del contador. Ejecuta la escena, localiza el error en Console y sigue su enlace hasta la línea afectada. Repara la asignación en el Inspector.

**Pista:** lee el nombre del script y qué objeto necesita esa línea. **Comprueba:** al repetir la misma acción desaparece el error y vuelve la función.

<a name="u195"></a>

### U195. Probar valores en los límites

**Etiquetas:** `Pruebas de límites` · `Comparaciones` · `Distancias` · `Depuración`

Revisa la acción de proximidad de U163 colocando enemigos a 2,9, 3 y 3,1 unidades del jugador. Anota qué debería pasar con cada uno y ejecuta la prueba. Corrige la comparación si el resultado no coincide con el requisito original.

**Pista:** conserva la condición estricta de distancia menor que 3. **Comprueba:** solo desaparece el enemigo situado a 2,9 unidades.

<a name="u196"></a>

### U196. Explicar cómo jugar en pantalla

**Etiquetas:** `Interfaz` · `Textos de interfaz` · `Botones` · `Usabilidad`

Añade a una escena terminada un panel breve con sus controles y objetivo. Indica solo las teclas que realmente funcionan en esa escena y permite ocultar el panel con un botón. Comprueba que no tapa al jugador ni los indicadores principales.

**Pista:** usa frases cortas y un tamaño de texto legible. **Comprueba:** otra persona puede identificar cómo moverse y qué debe conseguir sin explicaciones adicionales.

<a name="u197"></a>

### U197. Preparar un menú de selección

**Etiquetas:** `Scroll View` · `Prefabs` · `Vertical Layout Group` · `Content Size Fitter` · `Interfaz`

Crea una escena MainMenu con título y Scroll View. Diseña un botón con espacio para el nombre de un ejercicio y guárdalo como prefab. Prepara Content con un Vertical Layout Group para distribuir botones y ajusta el desplazamiento vertical.

**Pista:** Content Size Fitter puede adaptar la altura al contenido. **Comprueba:** al añadir varias copias, los botones quedan separados y puedes recorrer la lista.

<a name="u198"></a>

### U198. Generar botones a partir de una lista

**Etiquetas:** `Bucles` · `Instanciación` · `Escenas` · `Botones` · `SceneUtility`

Registra primero tres escenas de prueba. Recorre por índice las escenas incluidas en la compilación y crea un botón por escena dentro de Content, excepto MainMenu. El componente de cada botón guardará su propio nombre de escena y tendrá un método público para cargarla.

**Pista:** Usa `SceneManager.sceneCountInBuildSettings`, `SceneUtility.GetScenePathByBuildIndex` y `System.IO.Path.GetFileNameWithoutExtension`. **Comprueba:** Cada botón muestra su nombre y abre su propia escena.

<a name="u199"></a>

### U199. Acceder a todos los ejercicios

**Etiquetas:** `Build Profiles` · `Escenas` · `Persistencia entre escenas` · `Input System` · `Pruebas`

**Origen: PDF E68.**

Añade en grupo todas las escenas guardadas a Build Profiles y comprueba que el menú de U198 las enumera. Crea en MainMenu un único controlador persistente, reutilizando U185-U186, que permita regresar con F1 desde cualquier ejercicio. Prueba tres recorridos de ida y vuelta.

**Pista:** Coloca MainMenu primero y evita duplicar el controlador al regresar. **Comprueba:** El menú lista todas las escenas incluidas, sin configurar botones individualmente.

<a name="u200"></a>

### U200. Crear y probar el ejecutable

**Etiquetas:** `Compilación` · `Distribución` · `Pruebas` · `Persistencia de datos`

**Origen: PDF E68.**

Genera una compilación de escritorio del proyecto completo y ejecútala fuera del Editor. Copia la carpeta de salida completa a otro ordenador compatible. Prueba MainMenu, entrada, sonido y regreso con F1; cierra y abre el ejecutable para comprobar el récord. Anota cualquier fallo para corregirlo.

**Pista:** el otro ordenador debe usar un sistema compatible con la compilación. **Comprueba:** el proyecto funciona sin abrir Unity y conserva la navegación.

[Volver al índice](#indice)

<a name="correspondencia-pdf"></a>

## Correspondencia con los ejercicios del PDF

Los códigos E corresponden al documento original; los códigos U, a esta progresión. Las actividades preparatorias adicionales no necesitan una correspondencia.

| Ejercicio original | Ejercicio de esta lista |
|---|---|
| E01 | [U101](#u101) |
| E02 | [U012](#u012) |
| E03 | [U072](#u072) |
| E04 | [U039](#u039) |
| E05 | [U031](#u031) |
| E06 | [U036](#u036) |
| E07 | [U049](#u049) |
| E08 | [U056](#u056) |
| E09 | [U051](#u051) |
| E10 | [U053](#u053) |
| E11 | [U054](#u054) |
| E12 | [U055](#u055) |
| E13 | [U057](#u057) |
| E14 | [U058](#u058) |
| E15 | [U059](#u059) |
| E16 | [U074](#u074) |
| E17 | [U075](#u075) |
| E18 | [U076](#u076) |
| E19 | [U085](#u085) |
| E20 | [U086](#u086) |
| E21 | [U091](#u091) |
| E22 | [U094](#u094) |
| E23 | [U104](#u104) |
| E24 | [U105](#u105) |
| E25 | [U109](#u109) |
| E26 | [U111](#u111) |
| E27 | [U114](#u114) |
| E28 | [U115](#u115) |
| E29 | [U110](#u110) |
| E30 | [U122](#u122) |
| E31 | [U123](#u123) |
| E32 | [U124](#u124) |
| E33 | [U155](#u155) |
| E34 | [U156](#u156) |
| E35 | [U098](#u098) |
| E36 | [U132](#u132) |
| E37 | [U133](#u133) |
| E38 | [U134](#u134) |
| E39 | [U135](#u135) |
| E40 | [U136](#u136) |
| E41 | [U125](#u125) |
| E42 | [U126](#u126) |
| E43 | [U140](#u140) |
| E44 | [U092](#u092) |
| E45 | [U100](#u100) |
| E46 | [U118](#u118) |
| E47 | [U096](#u096) |
| E48 | [U095](#u095) |
| E49 | [U021](#u021) |
| E50 | [U022](#u022) |
| E51 | [U090](#u090) |
| E52 | [U027](#u027) |
| E53 | [U152](#u152) |
| E54 | [U157](#u157) |
| E55 | [U158](#u158) |
| E56 | [U163](#u163) |
| E57 | [U164](#u164) |
| E58 | [U165](#u165) |
| E59 | [U142](#u142) |
| E60 | [U143](#u143) |
| E61 | [U145](#u145) |
| E62 | [U127](#u127) |
| E63 | [U172](#u172) |
| E64 | [U173](#u173) |
| E65 | [U174](#u174) |
| E66 | [U182](#u182), [U183](#u183), [U184](#u184) |
| E67 | [U185](#u185) |
| E68 | [U199](#u199), [U200](#u200) |

<a name="recursos"></a>

## Recursos y referencias

Los recursos visuales propuestos en el PDF son [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks), para U026-U027 y U151-U152, y [Dino Characters, de Arks](https://arks.itch.io/dino-characters), para U157-U160. También puedes utilizar recursos equivalentes facilitados por el docente. Revisa las condiciones de uso del recurso que elijas.

Para resolver las actividades, consulta estas referencias oficiales según el concepto que estés practicando:

- **U081, entrada:** [Instalación y activación de Input System](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.17/manual/Installation.html). Utiliza la versión del paquete compatible que ofrezca Package Manager.
- **U094, suavizado:** [Vector2.SmoothDamp](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Vector2.SmoothDamp.html).
- **U116-U118, velocidad física:** [Rigidbody2D.linearVelocity](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D-linearVelocity.html). La velocidad ya se expresa en unidades por segundo.
- **U119, movimiento cinemático:** [Rigidbody2D.MovePosition](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D.MovePosition.html). Se utiliza en pasos de física y no sustituye el comportamiento de gravedad de un cuerpo dinámico.
- **U181 y U199, escenas incluidas:** [Lista de escenas de Build Profiles](https://docs.unity3d.com/6000.0/Documentation/Manual/build-profile-scene-list.html).
- **U198, menú automático:** [Cantidad de escenas incluidas](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneManager-sceneCountInBuildSettings.html) y [ruta de una escena por su índice](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneUtility.GetScenePathByBuildIndex.html).
