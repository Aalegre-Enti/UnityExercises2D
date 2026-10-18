# 200 ejercicios cortos para aprender Unity 2D y C# desde cero

Una progresión para personas que nunca han programado. Los ejercicios alternan el uso del editor con pequeños programas en C#: primero observarás y modificarás objetos; después crearás comportamientos y combinarás lo aprendido en escenas interactivas.

## Preparación y alcance

Se toma **Unity 6** como referencia. Necesitarás Unity Hub, el editor con soporte para crear ejecutables de tu sistema y un editor de C# conectado a Unity. Utiliza un proyecto con plantilla **2D**; los nombres de algunos menús pueden variar entre versiones.

Todo el trabajo es en **2D**: sprites, cámara ortográfica, movimiento en X/Y, rotación dentro del plano, `Rigidbody2D`, colisionadores 2D, Tilemap, interfaz y audio en modo 2D. La posición de los sprites mantendrá Z en 0 y la cámara conservará su Z inicial. Aunque `Transform` almacene tres coordenadas internamente, solo modificaremos las necesarias para trabajar en el plano; no se introducen mecánicas ni recursos de 3D.

Se introduce **Input System** en U081 y se mantiene ese mismo sistema para teclado, ratón y botones. En física se distinguirá entre mover un objeto visual y controlar un cuerpo físico.

## Recorrido

| Bloque | Ejercicios | Tema |
|---|---|---|
| 1 | U001-U010 | Primer contacto con el editor |
| 2 | U011-U020 | Primeros scripts y variables |
| 3 | U021-U030 | Sprites y organización visual |
| 4 | U031-U040 | Números y datos |
| 5 | U041-U050 | Decisiones |
| 6 | U051-U060 | Azar y repeticiones |
| 7 | U061-U070 | Métodos, referencias y arrays |
| 8 | U071-U080 | Tiempo y movimiento automático |
| 9 | U081-U090 | Teclado y ratón |
| 10 | U091-U100 | Seguimiento y cámara |
| 11 | U101-U110 | Física 2D |
| 12 | U111-U120 | Control de cuerpos físicos |
| 13 | U121-U130 | Zonas e interacciones |
| 14 | U131-U140 | Interfaz y puntuación |
| 15 | U141-U150 | Prefabs y creación de objetos |
| 16 | U151-U160 | Mapas y animación |
| 17 | U161-U170 | Áreas, enemigos y objetivos |
| 18 | U171-U180 | Sonido y música |
| 19 | U181-U190 | Escenas, pausa y guardado |
| 20 | U191-U200 | Pequeños retos y ejecutable |

## 1. Primer contacto con el editor (U001-U010)

Base: ninguna experiencia previa. Estas actividades se realizan sin scripts.

### U001. Tu primer proyecto

Crea desde Unity Hub un proyecto con plantilla 2D. Abre el editor y guarda la escena como `U001_Inicio` dentro de `Assets/Ejercicios/U001/`.

**Pista:** una escena es el espacio donde colocas objetos. **Comprueba:** cierra la escena y vuelve a abrirla desde Project.

### U002. Localizar las ventanas

Selecciona la cámara en Hierarchy y localiza sus propiedades en Inspector. Alterna entre Scene y Game, y encuentra Project y Console. Escribe una frase sobre para qué sirve cada ventana.

**Pista:** Scene permite editar; Game muestra la vista de la cámara. **Comprueba:** puedes localizar las seis ventanas sin ayuda.

### U003. Un cuadrado en pantalla

Añade un sprite cuadrado desde el menú de objetos 2D. Renómbralo `Jugador`, sitúalo en X=0, Y=0, Z=0 y cambia su color desde Sprite Renderer.

**Pista:** un GameObject reúne componentes; Sprite Renderer dibuja el sprite. **Comprueba:** el cuadrado aparece en Game con el color elegido.

### U004. Mover con coordenadas

Mueve el cuadrado cambiando X e Y en Transform. Prueba X=2 y después Y=-1. Devuélvelo al origen utilizando los campos numéricos, sin arrastrarlo.

**Pista:** X indica izquierda/derecha; Y, abajo/arriba. **Comprueba:** sabes anticipar hacia dónde se moverá antes de cambiar cada valor.

### U005. Cambiar el tamaño

Modifica Scale X e Y para obtener un rectángulo ancho y después uno alto. Termina con un cuadrado que mida el doble que el inicial.

**Pista:** escala 1 conserva el tamaño original. **Comprueba:** cambiar la escala no modifica los valores de Position.

### U006. Girar dentro del plano

Restaura la escala y gira el sprite usando únicamente Rotation Z: prueba 0, 45 y 90 grados. Mantén Rotation X e Y en 0.

**Pista:** Rotation Z gira la imagen dentro de la pantalla. **Comprueba:** a 45 grados el cuadrado parece un rombo.

### U007. Duplicar y nombrar

Duplica el cuadrado dos veces. Llama a los objetos `Rojo`, `Verde` y `Azul`, cambia sus colores y colócalos separados en una fila.

**Pista:** cada copia tiene sus propios componentes. **Comprueba:** cambiar el color de uno no cambia el de los demás.

### U008. Encuadrar la escena

Selecciona la cámara, confirma que su proyección es Orthographic y ajusta Size para ver los tres cuadrados. Cambia también el color del fondo.

**Pista:** una Size mayor permite ver más espacio. **Comprueba:** el encuadre de Game contiene los tres objetos completos.

### U009. Distinguir edición y ejecución

Entra en Play, mueve un cuadrado y detén la ejecución. Observa qué ocurre. Después realiza el mismo cambio fuera de Play y guarda la escena.

**Pista:** los cambios de objetos de escena durante Play normalmente no se conservan al detenerlo. **Comprueba:** el cambio guardado fuera de Play permanece.

### U010. Preparar una carpeta de trabajo

Crea carpetas para escenas, scripts e imágenes dentro de `Assets/Ejercicios/U010/`. Guarda allí una copia de la escena anterior y vuelve a abrir la original para distinguir ambas.

**Pista:** mueve los recursos desde Project para conservar sus referencias. **Comprueba:** puedes abrir las dos escenas y reconocer cuál estás editando.

## 2. Primeros scripts y variables (U011-U020)

Base: la escena con un cuadrado. Un script es un archivo de instrucciones; Unity ejecuta las de los componentes adjuntos a objetos activos.

### U011. Crear y adjuntar un script

Crea un script de componente C# llamado `U011_PrimerScript`, ábrelo y localiza la clase y sus llaves. Añádelo al cuadrado desde Inspector. Conserva la estructura creada por Unity.

**Pista:** el nombre de la clase debe coincidir con el archivo. **Comprueba:** el componente aparece en el objeto sin errores en Console.

### U012. Hello World

**Origen: PDF E02.**

Añade a `Start()` una instrucción que escriba `Hello World` en Console. Ejecuta la escena durante varios segundos y detén Play.

**Pista:** utiliza `Debug.Log`, comillas para el texto y punto y coma al terminar. **Comprueba:** aparece un solo mensaje por ejecución.

### U013. Reconocer un error de sintaxis

En una copia del script anterior, elimina el punto y coma del mensaje. Guarda, localiza el error en Console y abre la línea indicada. Repón el signo y vuelve a ejecutar.

**Pista:** corrige primero el primer error de la lista. **Comprueba:** el mensaje vuelve a aparecer y ya no hay errores rojos.

### U014. Leer las instrucciones en orden

Escribe tres mensajes en `Start()` que indiquen inicio, preparación y fin. Añade un comentario con `//` para explicar uno de ellos. Intercambia dos instrucciones.

**Pista:** los comentarios sirven para las personas y no se ejecutan. **Comprueba:** el orden de los mensajes coincide con el del código.

### U015. Guardar un nombre

Declara dentro de la clase, fuera de los métodos, una variable `string` llamada `nombreJugador`. Asígnale tu nombre y úsala para mostrar un saludo en `Start()`.

**Pista:** una variable guarda un dato; `string` guarda texto. **Comprueba:** al cambiar solo la variable cambia el saludo.

### U016. Guardar un número entero

Declara una variable `int` llamada `vidas` con valor 3. Muestra su valor al iniciar la escena. Cambia después el valor inicial a 5 y prueba de nuevo.

**Pista:** los números no llevan comillas. **Comprueba:** Console muestra el valor que has asignado a `vidas`.

### U017. Guardar un número con decimales

Declara una variable `float` llamada `velocidad` con valor `2.5f` y muéstrala al iniciar. Compara su declaración con la variable entera del ejercicio anterior.

**Pista:** en el código, los decimales usan punto y los literales `float` llevan `f`. **Comprueba:** el valor conserva la parte decimal.

### U018. Guardar verdadero o falso

Declara una variable `bool` llamada `tieneLlave`. Prueba primero `false` y después `true`, mostrando su valor en Console. Escribe qué podría representar en un juego.

**Pista:** un booleano solo guarda dos posibilidades. **Comprueba:** no necesitas escribir esas palabras entre comillas.

### U019. Editar datos desde Inspector

Expón las variables de nombre, vidas y velocidad como campos `public`. Modifica sus valores desde Inspector antes de Play y muestra los tres al iniciar la escena.

**Pista:** Unity conserva los valores guardados en el componente; cambiar el valor inicial en código no siempre los sustituye. **Comprueba:** se imprimen los valores del Inspector.

### U020. Una vez o en cada fotograma

Coloca un mensaje en `Start()` y otro diferente en `Update()`. Ejecuta durante dos segundos, detén Play y compara cuántas veces se ha escrito cada uno. Después desactiva el mensaje repetido.

**Pista:** `Update()` se llama cada fotograma; Console puede agrupar mensajes con Collapse. **Comprueba:** distingues una acción inicial de una repetida.

## 3. Sprites y organización visual (U021-U030)

Base: manejo del editor. Trabaja sin scripts para preparar recursos que reutilizarás después.

### U021. Importar una imagen transparente

**Origen: PDF E49.**

Importa un PNG con transparencia que no sea pixel art. Configura Texture Type como Sprite, aplica los cambios y arrastra la imagen a una escena.

**Pista:** deja visible un fondo de color detrás. **Comprueba:** las zonas transparentes muestran el fondo y no un rectángulo opaco.

### U022. Conservar los píxeles

**Origen: PDF E50.**

Importa un pequeño PNG de pixel art con transparencia. Configúralo como Sprite, usa filtrado Point y desactiva la compresión. Amplía el objeto para observar sus bordes.

**Pista:** compara el resultado con el filtrado Bilinear. **Comprueba:** los píxeles se distinguen sin el suavizado de sus bordes.

### U023. Relacionar píxeles y unidades

Duplica el archivo de una imagen y configura distintos valores de Pixels Per Unit en las dos importaciones. Coloca ambos sprites con escala 1 en la escena.

**Pista:** más píxeles por unidad producen una imagen más pequeña en el mundo. **Comprueba:** explicas por qué los tamaños son distintos.

### U024. Ordenar objetos superpuestos

Superpón tres sprites y modifica Order in Layer para decidir cuál se dibuja delante. Mantén la posición Z de los tres en 0.

**Pista:** el orden visual se controla desde Sprite Renderer. **Comprueba:** puedes cambiar qué imagen tapa a las otras sin moverlas.

### U025. Cambiar la transparencia

Coloca un sprite sobre otro. Modifica el canal A del color del sprite delantero para hacerlo semitransparente y después completamente transparente.

**Pista:** A significa alfa, la opacidad. **Comprueba:** puedes ver el sprite posterior a través del delantero.

### U026. Preparar una hoja de sprites

Importa la hoja de imágenes de Pixel Platformer Blocks enlazada al final. Configura Sprite Mode como Multiple y abre Sprite Editor; instala el paquete 2D Sprite desde Package Manager si falta.

**Pista:** una hoja reúne varias imágenes en un archivo. **Comprueba:** puedes ver la textura completa en Sprite Editor.

### U027. Separar una hoja en sprites

**Origen: PDF E52.**

Recorta la hoja de U026 en Sprite Editor utilizando una cuadrícula adecuada al archivo o recortes manuales. Aplica los cambios y coloca al menos dos sprites distintos en la escena.

**Pista:** despliega la textura en Project para ver sus sprites. **Comprueba:** cada objeto muestra una pieza y no toda la hoja.

### U028. Crear un objeto con hijos

Crea un objeto vacío llamado `Personaje` y coloca dos sprites como hijos: cuerpo y adorno. Mueve y gira el padre para observar qué ocurre con ambos.

**Pista:** arrastra los objetos dentro del padre en Hierarchy. **Comprueba:** el conjunto se mueve sin perder la colocación de sus piezas.

### U029. Entender la posición local

Selecciona el adorno de U028 y cambia su posición respecto al padre. Después mueve el padre. Anota la posición que muestra Inspector para el hijo antes y después.

**Pista:** en una jerarquía, Inspector muestra la posición local del hijo. **Comprueba:** mover el padre no cambia esos valores locales.

### U030. Activar y desactivar un conjunto

Desactiva el objeto padre de U028 con la casilla superior de Inspector. Reactívalo y desactiva solo el adorno. Guarda una copia de esta escena para usarla más adelante.

**Pista:** desactivar un padre también deja inactivos a sus hijos. **Comprueba:** sabes ocultar todo el personaje o solo una pieza.

## 4. Números y datos (U031-U040)

Base: los scripts de U015-U020. Escribe los resultados en `Start()` y utiliza campos del Inspector para probar diferentes datos.

### U031. Sumar dos números

**Origen: PDF E05.**

Crea dos campos `float`, suma sus valores y muestra el resultado una vez. Prueba con 2.5 y 1.25, y después con un número negativo.

**Pista:** utiliza el operador `+`; los decimales requieren un tipo adecuado. **Comprueba:** el primer resultado es 3.75.

### U032. Calcular lo que queda

Declara `monedasIniciales` y `precio` como enteros. Calcula cuántas monedas quedan después de una compra y muestra los tres valores en una frase.

**Pista:** el operador `-` resta. **Comprueba:** con 10 monedas y precio 4 quedan 6; con precio 12 obtienes -2.

### U033. Calcular un coste total

Declara un precio decimal y una cantidad entera. Multiplica ambos para calcular el coste de varias unidades. Prueba también con cantidad 0.

**Pista:** el operador `*` multiplica. **Comprueba:** tres unidades de precio 1.5 cuestan 4.5 y cero unidades cuestan 0.

### U034. Repartir sin perder decimales

Divide 5 entre 2 usando primero dos variables `int` y después dos `float`. Muestra ambos resultados y explica la diferencia en un comentario. Usa divisores distintos de cero.

**Pista:** el tipo de los operandos determina cómo se hace la división. **Comprueba:** obtienes 2 en la primera prueba y 2.5 en la segunda.

### U035. Encontrar el resto

Usa dos enteros para calcular cuántas monedas sobran al formar grupos del mismo tamaño. Prueba con 11 monedas en grupos de 3 y con 12 en grupos de 3.

**Pista:** `%` devuelve el resto; usa un tamaño de grupo mayor que cero. **Comprueba:** los restos son 2 y 0.

### U036. Hacer una media

**Origen: PDF E06.**

Expón tres números enteros en Inspector y calcula su media, conservando la parte decimal. Muestra el resultado una sola vez al iniciar la escena.

**Pista:** suma primero y divide entre `3f`. **Comprueba:** con 1, 2 y 2 el resultado es aproximadamente 1.67, no 1.

### U037. Decidir el orden de las operaciones

Calcula `2 + 3 * 4` y `(2 + 3) * 4`. Antes de ejecutar, escribe como comentario el resultado que esperas. Comprueba después tu predicción.

**Pista:** los paréntesis cambian qué operación se hace primero. **Comprueba:** los resultados son 14 y 20.

### U038. Aumentar un contador

Declara una puntuación inicial de 0. Auméntala una unidad tres veces en `Start()`, mostrando el valor después de cada cambio. Repite la prueba con una puntuación inicial de 10.

**Pista:** `++` incrementa una variable entera. **Comprueba:** los mensajes son 1, 2, 3 en la primera prueba y 11, 12, 13 en la segunda.

### U039. Guardar un vector del plano

**Origen: PDF E04. Adaptado de Vector3 a Vector2 para trabajar solo en 2D.**

Crea un campo `Vector2` editable desde Inspector y muestra sus dos componentes al iniciar. Prueba los valores X=3 e Y=-2 sin mover todavía ningún objeto.

**Pista:** un vector reúne dos números relacionados, accesibles con `.x` y `.y`. **Comprueba:** modificar una componente no cambia la otra.

### U040. Dar nombres claros a los resultados

Calcula el perímetro de un rectángulo a partir de ancho y alto configurables. Guarda el resultado en una variable con un nombre claro y muestra los datos junto al resultado.

**Pista:** el perímetro suma los cuatro lados. **Comprueba:** ancho 3 y alto 2 producen 10; no aparece un número sin contexto.

## 5. Decisiones (U041-U050)

Base: variables y operaciones. Una condición decide si se ejecuta un grupo de instrucciones encerrado entre llaves.

### U041. Tu primera condición

Crea un campo `vidas`. Usa `if` para mostrar `Sin vidas` solo cuando valga 0. Ejecuta una vez con 0 y otra con 3.

**Pista:** `==` compara; `=` asigna un valor. **Comprueba:** con 3 vidas no aparece el mensaje.

### U042. Elegir entre dos respuestas

Amplía U041 con `else` para mostrar `Puedes jugar` cuando queden vidas. Limita las pruebas a valores de 0 en adelante.

**Pista:** `else` se ejecuta cuando la condición del `if` es falsa. **Comprueba:** en cada ejecución aparece exactamente una respuesta.

### U043. Comparar cantidades

Usa `monedas` y `precio` para mostrar si puedes comprar un objeto. Considera que tener exactamente su precio también permite comprarlo.

**Pista:** compara con `>=`. **Comprueba:** con precio 5, las cantidades 4, 5 y 6 producen las respuestas esperadas.

### U044. Exigir dos condiciones

Declara `tieneLlave` y `puertaDesbloqueada`. Muestra `Puedes pasar` únicamente si ambas son verdaderas. Prueba las cuatro combinaciones posibles.

**Pista:** `&&` exige que se cumplan las dos condiciones. **Comprueba:** solo una de las cuatro combinaciones permite pasar.

### U045. Aceptar una alternativa

Declara `tieneEntrada` y `estaEnLaLista`. Permite entrar si se cumple al menos una condición. Prueba también el caso en que se cumplen ambas.

**Pista:** `||` significa que basta una de las condiciones. **Comprueba:** solo se deniega la entrada cuando ambas son falsas.

### U046. Cambiar un estado al contrario

Declara `luzEncendida`, muestra su valor y cámbialo al contrario con `!`. Vuelve a mostrarlo. Repite partiendo del valor opuesto.

**Pista:** negar un booleano intercambia verdadero y falso. **Comprueba:** el segundo mensaje siempre es distinto del primero.

### U047. Clasificar con varios casos

Clasifica una puntuación como baja si es menor que 5, media entre 5 y 9, y alta a partir de 10. Utiliza `if`, `else if` y `else`.

**Pista:** revisa las condiciones en orden. **Comprueba:** prueba 4, 5, 9 y 10; aparece una sola categoría por valor.

### U048. Elegir con switch

Crea un campo de texto `accion`. Usa `switch` para mostrar respuestas diferentes a `jugar`, `ayuda` y `salir`, y una respuesta por defecto para cualquier otra palabra.

**Pista:** cada `case` termina con `break`; `default` cubre valores desconocidos. **Comprueba:** una palabra inventada también recibe respuesta.

### U049. Una calculadora pequeña

**Origen: PDF E07.**

Crea dos números decimales y un símbolo de operación editables en Inspector. Usa `switch` para sumar, restar, multiplicar, dividir o calcular el resto (`+`, `-`, `*`, `/`, `%`). Muestra el resultado una vez.

**Pista:** rechaza divisor cero en `/` y `%`, y símbolos desconocidos. **Comprueba:** prueba las cinco operaciones y ambos errores.

### U050. Comprobar un intervalo

Crea un valor `energia` y muestra si está dentro del intervalo permitido, de 0 a 100 incluidos. Si está fuera, muestra un mensaje que explique el problema.

**Pista:** combina comparaciones con `&&`. **Comprueba:** prueba -1, 0, 50, 100 y 101 sin dejar casos sin respuesta.

## 6. Azar y repeticiones (U051-U060)

Base: condiciones y `Update()`. Un bucle repite instrucciones dentro de una misma llamada; no equivale a esperar al siguiente fotograma.

### U051. Un decimal aleatorio por fotograma

**Origen: PDF E09.**

Genera en `Update()` un número decimal entre -10 y 10 y escríbelo en Console. Ejecuta solo unos segundos y desactiva después el mensaje para evitar llenar la consola.

**Pista:** usa `Random.Range` con límites `float`. **Comprueba:** aparecen valores con decimales y ninguno queda fuera del intervalo.

### U052. Tirar un dado

Genera en `Start()` un entero entre 1 y 6. Reinicia varias veces la escena. Compara los límites utilizados con los del ejercicio anterior.

**Pista:** con enteros, el límite superior de `Random.Range` queda excluido. **Comprueba:** el dado nunca muestra 0 ni 7.

### U053. Calcular una operación al azar

**Origen: PDF E10.**

Reutiliza U049: genera dos números decimales y elige al azar una de sus cinco operaciones. Muestra una vez los operandos, el símbolo y el resultado. Conserva la comprobación de división o resto entre cero.

**Pista:** un entero de 0 a 4 puede representar la operación. **Comprueba:** puedes verificar a mano el cálculo mostrado.

### U054. Piedra, papel o tijera

**Origen: PDF E11.**

Elige desde Inspector 1 para piedra, 2 para papel o 3 para tijera. Genera la elección del ordenador y muestra ambas jugadas y el resultado: victoria, derrota o empate.

**Pista:** comprueba primero el empate y rechaza elecciones fuera de 1-3. **Comprueba:** verifica las nueve combinaciones posibles fijando temporalmente la jugada rival.

### U055. Contar del 1 al 100

**Origen: PDF E12.**

Escribe un bucle `for` en `Start()` que muestre todos los enteros del 1 al 100. Identifica su valor inicial, condición de continuación e incremento.

**Pista:** el contador debe avanzar hacia el final del intervalo. **Comprueba:** hay 100 mensajes, empezando por 1 y terminando en 100.

### U056. Una tabla de multiplicar

**Origen: PDF E08.**

Recibe un número decimal desde Inspector y muestra su tabla del 1 al 10. Reutiliza el `for` de U055 y muestra en cada línea los factores y el producto.

**Pista:** el contador actúa como segundo factor. **Comprueba:** para 2.5, la primera línea termina en 2.5 y la última en 25.

### U057. Cien números con while

**Origen: PDF E13.**

Usa un bucle `while` para mostrar exactamente 100 números aleatorios entre -10 y 10. Lleva la cuenta de cuántos has generado mediante una variable independiente.

**Pista:** inicializa el contador e increméntalo dentro del bucle. **Comprueba:** el bucle termina y Unity sigue respondiendo.

### U058. Todas las tablas

**Origen: PDF E14.**

Usa dos bucles `for` anidados para mostrar las tablas del 1 al 10, con multiplicadores del 1 al 10. Identifica qué contador elige la tabla y cuál el multiplicador.

**Pista:** el bucle interior se completa por cada vuelta del exterior. **Comprueba:** aparecen 100 operaciones, desde 1 × 1 hasta 10 × 10.

### U059. El primero que consigue cinco victorias

**Origen: PDF E15.**

Reutiliza las reglas de U054 para enfrentar a dos jugadores automáticos. Repite rondas aleatorias hasta que uno logre cinco victorias; los empates no suman. Muestra cada ronda, el marcador y el ganador final.

**Pista:** controla victorias, no cinco rondas. Añade un límite de seguridad de 1000 intentos que informe de interrupción. **Comprueba:** solo anuncias ganador si alcanza cinco victorias.

### U060. Acumular dentro de un bucle

Calcula la suma de los enteros del 1 al 10 con un bucle. Muestra cómo cambia el acumulador y después el total final. Reinicia la escena para comprobar el valor inicial.

**Pista:** inicializa la suma fuera del bucle y añade cada número con `+=`. **Comprueba:** el total final es 55 en cada ejecución.

## 7. Métodos, referencias y arrays (U061-U070)

Base: variables, condiciones y bucles. Ahora organizarás instrucciones y guardarás referencias a objetos de la escena.

### U061. Dar nombre a un grupo de instrucciones

Crea un método `MostrarBienvenida()` que escriba dos mensajes. Llámalo desde `Start()`. Después elimina temporalmente la llamada, manteniendo la definición del método.

**Pista:** un método propio se ejecuta cuando lo llamas; `void` indica que no devuelve un resultado. **Comprueba:** sin llamada no aparecen sus mensajes.

### U062. Pasar un dato a un método

Crea `Saludar(string nombre)` y úsalo desde `Start()` para saludar a dos nombres distintos. Utiliza el parámetro dentro del mensaje, en lugar de escribir un nombre fijo.

**Pista:** un parámetro permite reutilizar instrucciones con datos diferentes. **Comprueba:** el mismo método produce dos saludos distintos.

### U063. Devolver un resultado

Convierte la suma de U031 en un método que reciba dos `float` y devuelva otro `float`. Guarda el valor devuelto en una variable y muéstralo desde `Start()`.

**Pista:** `return` devuelve el resultado a quien llamó al método. **Comprueba:** el método calcula y la instrucción que lo llama decide cómo mostrarlo.

### U064. Referirse a otro objeto

Crea un campo `Transform` llamado `objetivo` y asigna un sprite arrastrándolo desde Hierarchy al Inspector. Muestra su posición X/Y al iniciar. Cambia la referencia por otro sprite.

**Pista:** una referencia permite acceder a un objeto que ya existe. **Comprueba:** el mensaje corresponde al objeto asignado, aunque renombres el objeto.

### U065. Detectar una referencia sin asignar

Vacía el campo de U064. Añade una condición que compruebe si `objetivo` es `null` antes de acceder a su posición. En ese caso, escribe un mensaje que explique qué falta.

**Pista:** `null` indica ausencia de referencia. **Comprueba:** tanto el campo vacío como el asignado se gestionan sin errores rojos.

### U066. Acceder al color desde código

Obtén el `SpriteRenderer` del mismo objeto al iniciar usando `GetComponent<SpriteRenderer>()`. Guarda la referencia y cambia su color a uno elegido en un campo `Color` del Inspector.

**Pista:** el componente debe estar en el objeto que lleva el script. **Comprueba:** cambiar el campo de color cambia el resultado de la siguiente ejecución.

### U067. Guardar varios números juntos

Declara un array de enteros con tres puntuaciones editables en Inspector. Muestra su tamaño y el primer elemento. Antes de leerlo, comprueba que contiene al menos un valor.

**Pista:** los arrays usan `[]`, el primer índice es 0 y `Length` indica su tamaño. **Comprueba:** un array vacío no produce errores.

### U068. Recorrer varios sprites

Guarda tres referencias `SpriteRenderer` en un array del Inspector. Recorre el array con `foreach` y cambia todos los colores al iniciar. Omite las posiciones que no tengan referencia.

**Pista:** `foreach` visita cada elemento sin escribir su índice. **Comprueba:** los tres sprites cambian y un hueco vacío no interrumpe el recorrido.

### U069. Elegir un elemento por su índice

Añade al array de U067 un campo `indiceElegido`. Muestra la puntuación de esa posición únicamente si el índice es válido. En caso contrario, explica el problema en Console.

**Pista:** el índice debe ser mayor o igual que 0 y menor que `Length`. **Comprueba:** prueba -1, 0 y el propio tamaño del array.

### U070. Elegir un color de una paleta

Crea un array de tres colores. Obtén un índice aleatorio válido y aplica el color elegido a un sprite al iniciar. Comprueba antes que la paleta no esté vacía.

**Pista:** combina U052, U066 y U069. **Comprueba:** el sprite solo utiliza colores de la paleta, aunque a veces repita uno.

## 8. Tiempo y movimiento automático (U071-U080)

Base: `Update()`, números, condiciones y `Vector2`. Usa sprites sin cuerpos físicos en este bloque.

### U071. Contar fotogramas

Incrementa un contador en `Update()` y muestra un mensaje al llegar a 100. Déjalo seguir aumentando sin repetir ese mensaje. Compara lo que cuenta con los segundos de un reloj.

**Pista:** un fotograma es una actualización de la imagen, no un segundo. **Comprueba:** no interpretas el contador como tiempo transcurrido.

### U072. Observar deltaTime

**Origen: PDF E03.**

Escribe `Time.deltaTime` en Console en cada fotograma durante unos segundos. Detén Play y compara varios valores. Después desactiva el mensaje repetido.

**Pista:** expresa en segundos el tiempo entre fotogramas. **Comprueba:** sus valores suelen ser fracciones pequeñas, no un contador creciente.

### U073. Esperar tres segundos sin bloquear

Acumula `Time.deltaTime` en un `float`. Al alcanzar tres segundos, muestra `Tiempo cumplido` una sola vez usando un booleano para recordar que ya lo has anunciado.

**Pista:** comprueba `>= 3`, no igualdad exacta. **Comprueba:** Unity sigue respondiendo durante la espera y solo aparece un aviso.

### U074. Mover hacia abajo y a la derecha

**Origen: PDF E16.**

En cada `Update()`, incrementa ligeramente X y reduce ligeramente Y de un sprite. Conserva Z en 0. Observa cómo cambia su posición durante Play.

**Pista:** modifica una copia de `transform.position` y vuelve a asignarla. **Comprueba:** se desplaza hacia la esquina inferior derecha; aún depende de los fotogramas.

### U075. Ajustar el paso desde Inspector

**Origen: PDF E17.**

Haz que el sprite se mueva hacia abajo y a la izquierda. Expón un valor para regular cuánto avanza en cada fotograma y compara dos valores distintos.

**Pista:** multiplica la dirección por el paso configurable. **Comprueba:** un valor mayor lo desplaza más deprisa; sigue siendo un paso por fotograma.

### U076. Medir la velocidad por segundo

**Origen: PDF E18.**

Mueve el sprite hacia arriba y a la izquierda con velocidad configurable. Multiplica el desplazamiento por `Time.deltaTime`. Normaliza la dirección con `.normalized` para que su longitud sea 1.

**Pista:** el desplazamiento resulta de dirección × velocidad × tiempo. **Comprueba:** en dos segundos recorre aproximadamente el doble que en uno.

### U077. Elegir la dirección desde Inspector

Amplía U076 con un campo `Vector2` para elegir dirección. Prueba derecha, arriba y diagonal. Si la dirección vale cero, el sprite debe permanecer quieto.

**Pista:** usa la dirección normalizada al calcular el desplazamiento. **Comprueba:** cambiar su orientación no cambia la velocidad total elegida.

### U078. Reaparecer al otro lado

Haz que un sprite avance hacia la derecha. Cuando su X supere 5, colócalo en X=-5 conservando Y. Mantén el movimiento basado en tiempo.

**Pista:** combina movimiento y una condición. **Comprueba:** puedes observar tres vueltas completas sin que el sprite desaparezca definitivamente.

### U079. Girar a velocidad constante

Haz que un sprite gire dentro del plano a una velocidad configurable en grados por segundo. Modifica únicamente la rotación Z y utiliza `Time.deltaTime`.

**Pista:** `Transform.Rotate` permite aplicar un pequeño giro. **Comprueba:** a 90 grados por segundo tarda unos cuatro segundos en completar una vuelta.

### U080. Crecer y detenerse

Aumenta progresivamente Scale X e Y de un sprite desde 1 hasta 2. Detén el crecimiento al alcanzar el tamaño máximo y conserva su posición.

**Pista:** guarda una escala común y limita el resultado con `Mathf.Min`. **Comprueba:** el sprite crece de forma uniforme y nunca supera el doble.

## 9. Teclado y ratón (U081-U090)

Base: movimiento sin física. Se usará Input System en todas las actividades siguientes; da el foco a la ventana Game para probar controles.

### U081. Preparar la entrada de teclado

Instala Input System desde Package Manager y activa su sistema de entrada cuando Unity lo solicite. Guarda antes de reiniciar el editor. Añade `using UnityEngine.InputSystem;` a un script nuevo.

**Pista:** revisa Active Input Handling en los ajustes de Player. **Comprueba:** el script reconoce `Keyboard` sin errores de compilación.

### U082. Detectar una pulsación

Muestra un mensaje al pulsar espacio. Comprueba la tecla dentro de `Update()` y evita acceder a un teclado inexistente comprobando `Keyboard.current != null`.

**Pista:** usa `spaceKey.wasPressedThisFrame`. **Comprueba:** mantener espacio pulsado produce un solo mensaje hasta que lo sueltes y vuelvas a pulsar.

### U083. Mantener una tecla pulsada

Haz que un sprite se mueva hacia la derecha mientras mantienes D. Debe detenerse al soltarla y conservar la velocidad por segundo de U076.

**Pista:** `dKey.isPressed` indica si la tecla sigue presionada. **Comprueba:** una pulsación larga desplaza más que una breve.

### U084. Detectar el ratón

Muestra mensajes distintos al pulsar los botones izquierdo y derecho del ratón. Comprueba primero que `Mouse.current` no sea `null`.

**Pista:** consulta `leftButton` y `rightButton` con `wasPressedThisFrame`. **Comprueba:** cada clic genera un mensaje del botón correcto.

### U085. Movimiento con WASD y position

**Origen: PDF E19.**

Construye una dirección `Vector2` a partir de W, A, S y D, empezando de cero en cada `Update()`. Mueve un sprite con `transform.position`, velocidad configurable y `Time.deltaTime`.

**Pista:** las teclas opuestas deben compensarse. **Comprueba:** el sprite se mueve en las cuatro direcciones y se detiene al soltar las teclas.

### U086. Movimiento con Translate

**Origen: PDF E20.**

Copia U085 y sustituye la modificación de posición por `transform.Translate`. Conserva WASD, velocidad configurable y tiempo entre fotogramas. Usa el espacio del mundo para mantener los controles aunque gires el sprite.

**Pista:** el parámetro `Space.World` evita que la orientación cambie la dirección. **Comprueba:** W sigue subiendo tras girar la imagen.

### U087. Igualar la velocidad diagonal

Compara el recorrido de U085 al mantener D y al mantener W+D durante el mismo tiempo. Normaliza la dirección antes de mover para evitar que las diagonales sean más rápidas.

**Pista:** conserva la dirección cero cuando no hay teclas. **Comprueba:** la distancia total recorrida es aproximadamente igual en ambos casos.

### U088. Correr mientras mantienes Shift

Amplía U087 con una velocidad normal y otra de carrera, ambas editables. Usa la segunda únicamente mientras mantengas Shift izquierdo; al soltarlo debe recuperarse la primera.

**Pista:** consulta `leftShiftKey.isPressed` y elige una velocidad antes de mover. **Comprueba:** pulsar Shift sin dirección no desplaza al personaje.

### U089. No salir de un rectángulo

Limita el movimiento del centro del sprite a X entre -5 y 5 e Y entre -3 y 3. Calcula la nueva posición y ajusta sus componentes antes de asignarla.

**Pista:** `Mathf.Clamp` mantiene un valor entre dos límites. **Comprueba:** sostener una tecla contra el borde no permite sobrepasarlo.

### U090. Voltear un sprite

**Origen: PDF E51.**

Usa una imagen asimétrica. Al pulsar espacio, invierte su orientación horizontal; al hacer clic derecho, invierte la vertical. Cada pulsación debe alternar el valor anterior.

**Pista:** combina `SpriteRenderer.flipX`, `flipY` y `!`. **Comprueba:** dos pulsaciones del mismo control restauran la orientación inicial.

## 10. Seguimiento y cámara (U091-U100)

Base: referencias de U064-U065 y jugador WASD de U087. Usa sprites sin física; la cámara permanece ortográfica.

### U091. Seguir de forma instantánea

**Origen: PDF E21.**

Añade un segundo sprite y asígnale el jugador como objetivo. Copia su posición X/Y en cada fotograma. Usa tamaños o transparencias diferentes para distinguir ambos aunque estén superpuestos.

**Pista:** comprueba que la referencia al objetivo está asignada. **Comprueba:** ambos ocupan siempre las mismas coordenadas del plano.

### U092. Seguir con una separación

**Origen: PDF E44.**

Amplía U091 con un desplazamiento `Vector2` editable desde Inspector. El seguidor debe ocupar la posición del objetivo más ese desplazamiento.

**Pista:** prueba una separación de X=2 e Y=1. **Comprueba:** la distancia relativa se mantiene al mover al jugador en cualquier dirección.

### U093. Acercarse con velocidad limitada

Haz que un sprite alcance al jugador sin superar una velocidad configurable por segundo. Cuando llegue, debe detenerse sin atravesar ni sobrepasar su posición.

**Pista:** utiliza `Vector2.MoveTowards` con velocidad multiplicada por `Time.deltaTime`. **Comprueba:** un objetivo lejano no provoca un salto instantáneo.

### U094. Seguir con suavidad

**Origen: PDF E22.**

Haz que un sprite siga al jugador con aceleración y frenado suaves. Expón un tiempo de suavizado y compara valores pequeños y grandes al arrancar, cambiar de dirección y detenerte.

**Pista:** `Vector2.SmoothDamp` conserva una variable de velocidad pasada con `ref`. **Comprueba:** el seguidor alcanza gradualmente al objetivo al detenerlo.

### U095. Seguir solo en horizontal

**Origen: PDF E48.**

Copia U091 y haz que el seguidor copie únicamente X. Guarda su propia altura inicial y consérvala aunque el jugador suba o baje.

**Pista:** combina la X del objetivo con la Y fija del seguidor. **Comprueba:** un movimiento exclusivamente vertical del jugador no lo desplaza.

### U096. Seguir únicamente desde cerca

**Origen: PDF E47.**

Amplía U093 para que el seguidor se mueva solo cuando la distancia entre ambos sea menor que 5 unidades. Cuando sea igual o mayor, debe quedarse quieto.

**Pista:** usa `Vector2.Distance` antes de calcular el desplazamiento. **Comprueba:** prueba distancias menores, iguales y mayores que 5.

### U097. Una cámara que sigue al jugador

Copia X/Y del jugador a la cámara en `LateUpdate()`, conservando la Z inicial de la cámara. Coloca varios sprites fijos para reconocer el desplazamiento del escenario.

**Pista:** `LateUpdate()` permite seguir después del movimiento hecho en `Update()`. **Comprueba:** el jugador permanece centrado y la cámara conserva su profundidad inicial.

### U098. Limitar la velocidad de la cámara

**Origen: PDF E35.**

Reutiliza el jugador WASD con velocidad configurable e independiente de los fotogramas. Cambia U097 para que la cámara lo alcance con una velocidad máxima configurable, en lugar de copiar instantáneamente su posición.

**Pista:** aplica `MoveTowards` a X/Y en `LateUpdate()` y conserva Z. **Comprueba:** una separación grande tarda en recuperarse.

### U099. Poner límites a la cámara

Amplía U098 para limitar el centro de la cámara a un rectángulo configurable. Prueba un escenario mayor que ese rectángulo y mueve al jugador hasta los extremos.

**Pista:** limita X/Y con `Mathf.Clamp`. **Comprueba:** el centro de la cámara no sobrepasa los límites, aunque el jugador siga avanzando.

### U100. Un fondo con tres capas

**Origen: PDF E45.**

Prepara tres capas de sprites con distintos órdenes visuales. Haz que sigan el desplazamiento X/Y de la cámara con factores diferentes y separaciones configurables para simular paralaje.

**Pista:** conserva posiciones iniciales y aplica una fracción del desplazamiento de cámara. **Comprueba:** al desplazarte, las tres capas se mueven a ritmos distintos.


## 11. Primeros experimentos con física 2D (U101-U110)

**Base y prerrequisitos:** Crea una escena de pruebas con cámara ortográfica; reutiliza los conocimientos de componentes, referencias, métodos, coordenadas y aleatoriedad.

### U101. Una caja que cae

**Origen: PDF E01.**

Crea una cápsula horizontal con CapsuleCollider2D que funcione como suelo estático. Coloca encima una caja con BoxCollider2D y Rigidbody2D de tipo Dynamic. Sin escribir scripts, ejecuta la escena y observa cómo cae la caja hasta apoyarse en la cápsula.

**Pista:** Comprueba los componentes de ambos objetos en el Inspector. **Comprueba:** La caja cae, queda apoyada y la cápsula permanece inmóvil.

### U102. Cambiar la intensidad de la gravedad

Duplica la caja y sitúa ambas a la misma altura, separadas horizontalmente. Asigna distintos valores positivos a Gravity Scale de sus Rigidbody2D. Ejecuta varias veces y después prueba un valor cero para descubrir qué controla esta propiedad.

**Pista:** Cambia una sola propiedad entre pruebas. **Comprueba:** Identificas qué caja acelera más al caer y qué sucede con gravedad cero.

### U103. Evitar que una caja vuelque

Añade una pequeña rampa al suelo y deja caer una caja sobre ella. Observa su rotación. Activa Freeze Rotation Z en las restricciones de su Rigidbody2D y repite la prueba para mantener su orientación mientras puede seguir desplazándose.

**Pista:** En un juego 2D, el giro visible ocurre alrededor de Z. **Comprueba:** La caja puede trasladarse sin girar.

### U104. Un cuerpo con dos colliders

**Origen: PDF E23.**

Añade un círculo como hijo de la caja y desplázalo hacia un lado. Ponle CircleCollider2D, pero ningún Rigidbody2D. Sin scripts, deja caer el conjunto sobre la cápsula y observa cómo los dos colliders pertenecen al cuerpo físico de la caja.

**Pista:** El cuerpo del padre reúne también los colliders de sus hijos. **Comprueba:** El círculo acompaña la posición y rotación de la caja y también choca con la cápsula.

### U105. Una caja que rebota

**Origen: PDF E24.**

Crea un suelo plano estático y un Physics Material 2D para el collider de la caja. Sin scripts, modifica su Bounciness para conseguir un rebote visible al caer sobre el suelo. Compara el resultado con otra caja que tenga un material sin rebote.

**Pista:** Mantén iguales las alturas iniciales y la gravedad. **Comprueba:** El material cambia el rebote sin modificar ningún script.

### U106. Superficies con distinto rozamiento

Prepara dos rampas iguales y dos cajas sin rebote. Crea materiales físicos 2D con valores de Friction diferentes y aplícalos a cada pareja de caja y rampa. Observa cómo cambia el deslizamiento usando siempre la misma posición inicial.

**Pista:** Evita cambiar la inclinación mientras comparas materiales. **Comprueba:** Puedes explicar cuál de las dos superficies dificulta más el deslizamiento.

### U107. Observar Update y FixedUpdate

Añade dos contadores a un script: uno aumenta en Update y otro en FixedUpdate. Muestra sus valores una vez por segundo en la Console. Observa que los fotogramas dibujados y los pasos de simulación física no tienen por qué coincidir.

**Pista:** Reutiliza el temporizador ya aprendido para limitar los mensajes. **Comprueba:** Distingues la actualización visual de la actualización de la física.

### U108. Guardar una referencia al cuerpo físico

En el script de la caja, declara una variable de tipo Rigidbody2D. Obtén su componente mediante GetComponent en Start y guarda la referencia. Utilízala para cambiar Gravity Scale a un valor configurable desde el Inspector, sin buscar el componente continuamente.

**Pista:** El componente buscado debe estar en el mismo objeto que el script. **Comprueba:** La gravedad de la caja adopta el valor indicado.

### U109. Un impulso inicial hacia arriba

**Origen: PDF E25.**

Coloca una caja apoyada sobre un suelo plano. Usando su referencia a Rigidbody2D, aplica una única fuerza hacia arriba en Start mediante AddForce y ForceMode2D.Impulse. Expón la intensidad en el Inspector y compara tres valores sin cambiar la gravedad.

**Pista:** Un impulso se aplica una vez, no cada fotograma. **Comprueba:** La caja sube y después vuelve a caer por gravedad.

### U110. Caer desde una posición aleatoria

**Origen: PDF E29.**

Construye varios obstáculos estáticos bajo la caja. En Start, elige aleatoriamente su coordenada X entre dos límites del Inspector y conserva una altura fija en la parte superior de la pantalla. Asigna esa posición inicial al Rigidbody2D y deja que la gravedad determine el resto del recorrido.

**Pista:** Reutiliza Random.Range con límites de tipo float. **Comprueba:** Al reiniciar, la caja aparece dentro del intervalo y choca con los obstáculos.

## 12. Controlar personajes mediante física 2D (U111-U120)

**Base y prerrequisitos:** Reutiliza la escena física, el Input System, las referencias a Rigidbody2D, los booleanos y la diferencia entre Update y FixedUpdate.

### U111. Saltar al pulsar espacio

**Origen: PDF E26.**

Transforma el impulso inicial en un salto al pulsar espacio. Detecta la pulsación en Update y guarda una solicitud booleana; consúmela una sola vez en FixedUpdate para aplicar el impulso. Por ahora permite saltar incluso cuando la caja está en el aire.

**Pista:** Utiliza Keyboard.current y una pulsación nueva, no una tecla mantenida. **Comprueba:** Cada pulsación genera exactamente un impulso.

### U112. Detectar el contacto con el suelo

Crea la etiqueta Suelo y asígnala a un único suelo plano. Añade OnCollisionEnter2D y OnCollisionExit2D al personaje para escribir mensajes cuando empieza y termina el contacto con ese objeto. Comprueba la etiqueta antes de mostrar cada mensaje.

**Pista:** Usa CompareTag sobre el objeto recibido en la colisión. **Comprueba:** Saltar produce una salida y aterrizar produce una entrada.

### U113. Saltar solamente cuando hay apoyo

Añade un booleano que indique si el personaje está tocando el suelo de la prueba anterior. Actualízalo con los eventos de colisión y exige que sea verdadero antes de aceptar un salto. Desactívalo también al aplicar el impulso para evitar solicitudes repetidas.

**Pista:** Mantén un único suelo plano en esta primera versión. **Comprueba:** Pulsar espacio repetidamente en el aire no añade impulsos.

### U114. Experimentar con Transform y gravedad

**Origen: PDF E27.**

En una copia de la escena, mueve el personaje con WASD modificando transform.position en Update. Expón la velocidad y utiliza deltaTime; conserva Rigidbody2D, gravedad y colliders. Prueba paredes y suelo para observar las limitaciones de combinar desplazamientos directos con simulación física.

**Pista:** Registra movimientos bruscos, penetraciones o correcciones que observes. **Comprueba:** Explicas por qué esta mezcla puede interferir con la física.

### U115. Repetir el experimento en FixedUpdate

**Origen: PDF E28.**

Copia el experimento anterior y conserva la lectura del teclado en Update. Guarda la dirección y aplica el desplazamiento por transform.position en FixedUpdate usando Time.fixedDeltaTime. Compara el resultado: cambiar de método no convierte esos desplazamientos directos en un controlador físico correcto.

**Pista:** Usa el tiempo correspondiente al método que aplica el movimiento. **Comprueba:** Comparas ambos experimentos sin asumir que FixedUpdate elimina sus limitaciones.

### U116. Avanzar con velocidad física horizontal

Vuelve a la escena de salto y sustituye el desplazamiento directo por control de Rigidbody2D.linearVelocity. Lee A y D en Update; en FixedUpdate modifica solamente la componente X según la velocidad del Inspector y conserva la componente Y que produce la física.

**Pista:** Copia la velocidad a un Vector2 antes de cambiar X. **Comprueba:** Puedes avanzar, detenerte y saltar sin anular la gravedad.

### U117. Movimiento físico en vista cenital

Crea una escena vista desde arriba con paredes 2D y un personaje con Gravity Scale cero. Controla su linearVelocity mediante WASD en FixedUpdate, con velocidad configurable. Ajusta la dirección diagonal para que no sea más rápida y bloquea la rotación del cuerpo.

**Pista:** La velocidad física ya expresa distancia por segundo: no la multipliques por deltaTime. **Comprueba:** El personaje conserva su rapidez y choca con paredes.

### U118. Un seguidor que camina por el suelo

**Origen: PDF E46.**

Adapta el seguimiento a un personaje que avanza horizontalmente sobre suelo, con gravedad y colisiones. Asígnale un objetivo y una velocidad horizontal máxima en el Inspector. Ajusta solamente su velocidad X para acercarse y detenerse a una pequeña distancia, conservando su velocidad vertical.

**Pista:** Esta adaptación de E46 sigue al objetivo sobre suelo, sin perseguir su altura. **Comprueba:** El seguidor frena cerca y respeta las paredes.

### U119. Mover una plataforma cinemática

Crea una plataforma con collider y Rigidbody2D de tipo Kinematic. Define dos posiciones del recorrido y una velocidad. Desplázala con MovePosition en FixedUpdate hasta cada extremo y cambia de dirección al llegar; prueba primero el recorrido libre, sin transportar al jugador.

**Pista:** Calcula cada paso con Time.fixedDeltaTime. **Comprueba:** La plataforma recorre el mismo trayecto de ida y vuelta sin saltos de posición.

### U120. Comparar movimiento a 30 y 60 FPS

En la escena cenital, mide cuánto avanza el personaje durante diez segundos sin obstáculos. Compara límites de 30 y 60 FPS mediante Application.targetFrameRate, desactivando VSync durante la prueba. Comprueba la tasa real y registra si la distancia recorrida cambia de forma apreciable.

**Pista:** Un límite solicitado no garantiza que el equipo lo alcance. **Comprueba:** Relacionas las medidas con el tiempo transcurrido y los FPS observados.

## 13. Zonas, contactos y consecuencias (U121-U130)

**Base y prerrequisitos:** Reutiliza U117: WASD con velocidad del Inspector independiente de los fotogramas; cada interacción requiere Collider2D en ambos objetos y Rigidbody2D en al menos uno.

### U121. Entrar en una zona invisible

Crea una zona con BoxCollider2D y activa Is Trigger. Desde un script de la zona, detecta OnTriggerEnter2D y muestra un mensaje únicamente cuando entre el personaje, identificado con la etiqueta Jugador. Comprueba que el área permite atravesarla sin bloquear el movimiento.

**Pista:** Un trigger detecta solapamientos sin funcionar como una pared. **Comprueba:** Recibes un mensaje al entrar y puedes seguir caminando.

### U122. Detectar entrada y salida

**Origen: PDF E30.**

Amplía la zona anterior con OnTriggerExit2D. Muestra mensajes diferentes cuando el personaje entra y sale, indicando el nombre de la zona. Recorre sus bordes varias veces y observa cuándo se producen los eventos respecto al collider completo del personaje.

**Pista:** Mantén el filtro de etiqueta en los dos métodos. **Comprueba:** Cada recorrido completo produce un mensaje de entrada y otro de salida.

### U123. Cambiar de color dentro de la zona

**Origen: PDF E31.**

Haz que el personaje se vuelva rojo al entrar en una zona y recupere el blanco al salir. Guarda una referencia a su SpriteRenderer y cambia su color desde los eventos correspondientes. Utiliza una única zona para observar el comportamiento sin solapamientos.

**Pista:** Reutiliza los cambios de color y las referencias ya aprendidos. **Comprueba:** Permanecer dentro mantiene el rojo y salir devuelve el blanco.

### U124. Distinguir dos zonas por su etiqueta

**Origen: PDF E32.**

Crea dos zonas separadas con etiquetas diferentes. Coloca el detector en el personaje y utiliza condiciones para escribir qué zona acaba de atravesar. Incluye en cada mensaje el nombre del objeto que entra y la etiqueta de la zona detectada.

**Pista:** El collider recibido identifica el otro objeto de la interacción. **Comprueba:** La Console distingue las dos zonas y al personaje que entra.

### U125. Destruir objetos al tocarlos

**Origen: PDF E41.**

Distribuye varios objetos con colliders de tipo trigger y una etiqueta común. Desde el personaje, detecta el contacto con esos objetos y destruye únicamente el objeto encontrado. Conserva las paredes y las zonas anteriores para comprobar que el filtro distingue cada interacción.

**Pista:** Destroy debe recibir el objeto detectado, no el personaje. **Comprueba:** Puedes eliminar varios objetos sin hacer desaparecer paredes ni jugador.

### U126. Contar entradas en una zona

**Origen: PDF E42.**

Añade un contador entero que aumente cada vez que el personaje entra en una zona. Muestra el total actualizado en la Console. La zona debe permanecer activa para poder salir y volver a entrar; quedarse quieto dentro no debe incrementar continuamente el contador.

**Pista:** Incrementa el valor en el evento de entrada, no en Update. **Comprueba:** Tres entradas completas producen un total de tres.

### U127. Un portal de derecha a izquierda

**Origen: PDF E62.**

Coloca un portal de entrada a la derecha y una marca de destino a la izquierda. Al entrar el personaje, cambia la posición de su Rigidbody2D al destino mediante una referencia. El destino izquierdo no debe teletransportar de vuelta: el recorrido funciona en un único sentido.

**Pista:** Mantén el destino separado del trigger de entrada. **Comprueba:** Entrar por la derecha lleva a la izquierda sin provocar un bucle.

### U128. Perder vida al entrar en peligro

Añade una variable de vida al personaje y una zona etiquetada como peligrosa. Cada entrada debe restar una cantidad configurable y mostrar la vida restante en la Console. Limita el resultado para que nunca sea negativo y prueba varias entradas consecutivas.

**Pista:** Reutiliza las condiciones y la resta de valores. **Comprueba:** El daño solo afecta al personaje y la vida termina en cero.

### U129. Dejar tiempo entre dos daños

Modifica la zona peligrosa para causar daño mientras el personaje permanece dentro, usando OnTriggerStay2D. Añade un temporizador que permita recibir daño como máximo una vez por segundo, aunque llegue más de una detección. Mantén el temporizador en el personaje para compartirlo entre peligros.

**Pista:** Reduce el tiempo restante y acepta daño cuando haya terminado. **Comprueba:** Permanecer dentro no resta vida en cada paso físico.

### U130. Volver al último punto de control

Crea una zona de punto de control que guarde su posición en el personaje. Añade otra zona que represente una caída o derrota; al entrar, devuelve el Rigidbody2D a la posición guardada, reinicia su velocidad y recupera la vida inicial.

**Pista:** Guarda la posición inicial como primer punto de control. **Comprueba:** Puedes reaparecer antes y después de activar un punto nuevo.

## 14. Interfaz para mostrar y cambiar valores (U131-U140)

**Base y prerrequisitos:** Reutiliza métodos públicos, referencias, contadores y vida; conserva el Input System y aprende a conectar la interfaz desde el Inspector.

### U131. Preparar una interfaz en pantalla

Crea un Canvas con Render Mode Screen Space - Overlay y añade un texto TextMeshPro de interfaz. Si Unity solicita TMP Essential Resources, impórtalos. Comprueba que exista un único EventSystem con InputSystemUIInputModule. Distingue los objetos de la interfaz de los sprites de la escena.

**Pista:** Selecciona el Canvas y revisa sus componentes en el Inspector. **Comprueba:** El texto permanece en pantalla aunque muevas la cámara.

### U132. Cinco cuadrados que se adaptan

**Origen: PDF E36.**

Sin scripts, coloca cinco imágenes cuadradas de colores: una en cada esquina y otra en el centro. Configura Canvas Scaler con Scale With Screen Size y referencia 1920 × 1080. Ajusta anclas y márgenes para conservar su colocación al cambiar la resolución de Game.

**Pista:** Cada cuadrado necesita anclas acordes con su posición. **Comprueba:** Las cuatro esquinas y el centro siguen siendo reconocibles en dos resoluciones.

### U133. Comparar tres alineaciones de texto

**Origen: PDF E37.**

Sin scripts, crea tres textos TextMeshPro de interfaz con rectángulos del mismo tamaño. Copia en los tres el siguiente párrafo del documento original. Alinea uno a izquierda, otro centrado y otro a derecha.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam sed eros sollicitudin, porttitor nulla ac, venenatis augue. Duis lacinia hendrerit tellus, sit amet ornare ante blandit in. Nam sollicitudin felis a ultrices placerat. Nunc sed dictum ante.

**Pista:** Mantén iguales la fuente y su tamaño para comparar. **Comprueba:** El contenido coincide y solamente cambia la alineación del párrafo.

### U134. Un botón que escribe un mensaje

**Origen: PDF E38.**

Coloca un botón en el centro de la pantalla y cambia su texto. Crea un método público sin parámetros que escriba un mensaje en la Console. Conecta el evento On Click del botón con ese método mediante el Inspector y prueba varios clics.

**Pista:** Arrastra al evento el objeto que contiene el script. **Comprueba:** Cada clic produce un único mensaje con el texto elegido.

### U135. Mostrar y ocultar un panel sin scripts

**Origen: PDF E39.**

Crea un panel de pantalla completa y dos botones superpuestos arriba a la izquierda, fuera del panel y dibujados por delante. Sin scripts, configura On Click: A activa el panel y B, y se desactiva; B desactiva el panel, activa A y se desactiva. Empieza solo con A activo.

**Pista:** Usa tres llamadas a SetActive en cada botón; desactiva el propio botón al final. **Comprueba:** El mismo lugar permite abrir y cerrar repetidamente.

### U136. Un botón para sumar puntos

**Origen: PDF E40.**

Sitúa un botón en el centro izquierdo y un contador TextMeshPro en el centro derecho. Cada clic debe incrementar una variable entera y actualizar el texto. Guarda una referencia al texto desde el Inspector y muestra cero antes de recibir el primer clic.

**Pista:** Usa `using TMPro;`, una referencia `TMP_Text` y su propiedad `.text`; convierte el número con `ToString()`. **Comprueba:** Cinco clics muestran cinco y reiniciar vuelve a cero.

### U137. Reiniciar el contador desde otro botón

Añade un botón para poner a cero el contador anterior. Crea un método que actualice su texto y reutilízalo tanto al sumar como al reiniciar. Comprueba que la variable y la interfaz siempre muestran el mismo resultado después de cualquier combinación de clics.

**Pista:** Centraliza la actualización del texto en un único método. **Comprueba:** Sumar, reiniciar y volver a sumar funciona sin valores desactualizados.

### U138. Ajustar la velocidad con un deslizador

Añade un Slider con límites mínimo y máximo adecuados para la velocidad del personaje cenital. Conecta On Value Changed a un método público que reciba un float y actualice su velocidad. Prueba el efecto mientras mueves al personaje y conserva un valor inicial coherente.

**Pista:** Selecciona la llamada dinámica que utiliza el valor del deslizador. **Comprueba:** Cambiar el Slider modifica la rapidez sin editar el script.

### U139. Mostrar la vida en una barra

Crea otro Slider para representar la vida del personaje. Configura su máximo con la vida inicial y actualiza su valor cuando reciba daño o reaparezca. Desactiva su interacción para que el jugador no pueda modificar la salud arrastrando la barra con el ratón.

**Pista:** Reutiliza la variable de vida; no mantengas dos contadores independientes. **Comprueba:** La barra baja con el daño y se recupera al reaparecer.

### U140. Recoger objetos y ver el total

**Origen: PDF E43.**

Distribuye varios objetos estáticos con colliders de tipo trigger por la escena cenital. Al tocarlos con el personaje, hazlos desaparecer y suma uno al contador TextMeshPro. Reutiliza un método para actualizar el total y asegúrate de que cada objeto pueda contarse solamente una vez.

**Pista:** Desactiva su collider antes de destruir el objeto recogido. **Comprueba:** El total coincide con las recogidas y no aumenta por permanecer quieto.

## 15. Crear y gestionar copias de objetos (U141-U150)

**Base y prerrequisitos:** Reutiliza el personaje cenital, sus entradas de teclado, los contadores de interfaz, los temporizadores, los arrays y los bucles.

### U141. Guardar un objeto como prefab

Crea una ficha visual sencilla con SpriteRenderer y conviértela en prefab guardándola en una carpeta del proyecto. Arrastra dos copias a la escena y modifica el color del prefab para observar la relación con sus instancias. Mantén esta ficha sin componentes físicos.

**Pista:** Distingue el recurso de Project de sus copias en Hierarchy. **Comprueba:** Las dos instancias reciben el cambio de color del prefab.

### U142. Crear una copia al pulsar espacio

**Origen: PDF E59.**

Añade al personaje una referencia al prefab de la ficha, asignada desde el Inspector. Mientras lo controlas con WASD, cada pulsación de espacio debe usar Instantiate para crear una copia en su posición actual. La copia debe permanecer donde apareció cuando el personaje siga avanzando.

**Pista:** Usa una pulsación nueva y crea la copia sin hacerla hija del personaje. **Comprueba:** Puedes dejar varias fichas separadas por la escena.

### U143. Contar todas las copias creadas

**Origen: PDF E60.**

Añade un contador TextMeshPro que muestre el número total de fichas creadas durante la partida. Incrementa el valor cuando Instantiate cree una copia y actualiza la interfaz. Este contador representa el total histórico, por lo que borrar una ficha no debe reducirlo.

**Pista:** Reutiliza el método que actualiza textos de contador. **Comprueba:** El valor aumenta una vez por copia y coincide con las pulsaciones aceptadas.

### U144. Desaparecer después de tres segundos

Añade al prefab un script que programe la destrucción de cada instancia tres segundos después de aparecer. Crea varias fichas en momentos diferentes y observa que cada una conserva su propio plazo. El contador de copias creadas debe seguir mostrando el total histórico.

**Pista:** Destroy permite indicar un retraso antes de eliminar el objeto. **Comprueba:** Cada ficha desaparece aproximadamente tres segundos después de su creación.

### U145. Contar solamente las copias que siguen vivas

**Origen: PDF E61.**

Añade un segundo contador para las copias vivas. Al crear cada ficha, pásale una referencia al script contador. Sustituye su destrucción diferida por un temporizador propio: al cumplir tres segundos, debe avisar al contador antes de destruirse. Incrementa el total vivo al crearla.

**Pista:** Obtén el componente de la instancia con GetComponent y llama a un método de inicialización que reciba el contador. **Comprueba:** Sin nuevas creaciones, el contador vivo vuelve a cero.

### U146. Crear fichas a intervalos regulares

Crea un generador fijo que produzca una ficha cada cierto intervalo configurable desde el Inspector. Reutiliza el método de creación y los contadores anteriores. Gestiona el intervalo con un temporizador para que la frecuencia dependa del tiempo transcurrido, no del número de fotogramas.

**Pista:** Reinicia el tiempo de espera después de cada creación. **Comprueba:** Cambiar el intervalo modifica la frecuencia y los contadores permanecen coherentes.

### U147. Limitar las fichas presentes

Añade al generador un límite máximo de fichas vivas. Antes de cada intento de creación, compara ese límite con el contador actual y crea solamente si queda espacio. Cuando una ficha desaparezca, el generador podrá volver a crear en su siguiente intervalo.

**Pista:** Realiza la comprobación también si mantienes la creación mediante espacio. **Comprueba:** El total vivo nunca supera el límite configurado.

### U148. Construir una fila con un bucle

En una copia de la escena, sustituye la generación periódica por una fila creada al iniciar. Usa un bucle for, una cantidad y una separación configurables. Calcula la posición de cada ficha desde un origen común y permite suficientes objetos vivos para completar la fila.

**Pista:** Multiplica el índice del bucle por la separación horizontal. **Comprueba:** Cambiar cantidad y distancia produce una fila regular sin duplicar instrucciones.

### U149. Borrar una fila guardada en un array

Para esta prueba, utiliza una copia del prefab sin autodestrucción. Guarda las fichas de la fila en un array al crearlas. Añade una tecla que recorra ese array y destruya sus objetos; comprueba cada referencia para poder repetir la acción cuando ya no quede ninguno. Actualiza también el contador vivo.

**Pista:** Una referencia a un objeto destruido debe comprobarse antes de usarla. **Comprueba:** La fila desaparece y repetir la tecla no genera errores.

### U150. Generar dentro de un área delimitada

Recupera el generador periódico con límite de objetos vivos. Define valores mínimos y máximos para X e Y en el Inspector y genera cada ficha en una posición aleatoria dentro de ese rectángulo. Coloca cuatro marcas visuales en sus esquinas para comprobar los límites.

**Pista:** Obtén aleatoriamente cada coordenada por separado. **Comprueba:** Las fichas aparecen dentro del área y siguen respetando el máximo de objetos vivos.

## 16. Mapas y animaciones (U151-U160)

Base del bloque: reutiliza el spritesheet recortado de U027, las jerarquías de U028 y un jugador con movimiento 2D.

### U151. Crear una paleta de piezas

Abre Tile Palette y crea una paleta con los sprites del spritesheet que recortaste en U027. Si falta la ventana, instala 2D Tilemap Editor desde Package Manager. Guarda los recursos Tile en una carpeta propia y coloca al menos seis piezas diferentes en la paleta.

**Pista:** una paleta reúne las piezas que usarás para pintar un mapa. **Comprueba:** seleccionas cada pieza sin volver al spritesheet original.

### U152. Dibujar un mapa con Tilemap

**Origen: PDF E53.**

Crea un Tilemap rectangular y dibuja un escenario pequeño utilizando la paleta anterior, sin escribir scripts. Incluye un suelo reconocible, varios obstáculos y una zona de inicio. Corrige al menos una pieza usando la herramienta de borrar.

**Pista:** Grid organiza las celdas y Tilemap contiene las piezas pintadas. **Comprueba:** el escenario se ve completo desde la cámara 2D.

### U153. Hacer sólido el mapa

Añade TilemapCollider2D al mapa y prueba encima el jugador con Rigidbody2D que ya utilizaste. Ajusta el tipo de colisión de las piezas necesarias para que el suelo y los obstáculos detengan al jugador. Mantén el escenario inmóvil.

**Pista:** utiliza piezas con Collider Type distinto de None. **Comprueba:** el jugador se apoya en el suelo y no atraviesa los obstáculos.

### U154. Separar fondo y obstáculos

Separa el escenario en dos Tilemaps dentro del mismo Grid: uno para decoración y otro para obstáculos. Mueve algunas piezas a su capa correspondiente y ajusta su orden de dibujo. Deja las colisiones únicamente en las piezas que deban bloquear al jugador.

**Pista:** revisa Order in Layer en cada Tilemap Renderer. **Comprueba:** el jugador atraviesa la decoración y sigue chocando con los obstáculos.

### U155. Animar una transformación

**Origen: PDF E33.**

Selecciona un sprite y crea una animación con la ventana Animation, sin escribir scripts. Durante el clip, cambia su posición en X e Y, su rotación alrededor de Z y su escala en X e Y. Mantén el movimiento dentro del plano 2D.

**Pista:** añade fotogramas al principio, en medio y al final. **Comprueba:** al reproducir el clip se distinguen las tres transformaciones.

### U156. Animar dos piezas juntas

**Origen: PDF E34.**

Crea un objeto padre con dos sprites hijos, como un cuerpo y una antena. Desde el padre, graba un único clip que cambie posición, rotación Z y escala de sus hijos. Anima ambos sprites sin escribir scripts ni crear clips independientes.

**Pista:** selecciona cada hijo mientras grabas el clip del padre. **Comprueba:** una sola reproducción anima las dos piezas de forma coordinada.

### U157. Crear una animación de carrera

**Origen: PDF E54.**

Descarga un personaje de [Dino Characters](https://arks.itch.io/dino-characters), importa su spritesheet y separa los fotogramas de carrera. Crea una animación que los reproduzca en orden y se repita, sin escribir scripts. Ajusta la velocidad hasta reconocer claramente el movimiento.

**Pista:** conserva el mismo tamaño de corte para todos los fotogramas. **Comprueba:** el dinosaurio corre sin saltos de tamaño ni imágenes mezcladas.

### U158. Cambiar de animación con espacio

**Origen: PDF E55.**

Prepara dos animaciones del mismo personaje, por ejemplo reposo y carrera, y colócalas en su Animator. Añade un parámetro booleano y las transiciones necesarias. Escribe un script que invierta ese parámetro cada vez que pulses espacio.

**Pista:** utiliza una pulsación nueva y revisa las condiciones de ambas transiciones. **Comprueba:** cada toque alterna una vez entre las dos animaciones.

### U159. Animar según el movimiento

Reutiliza el personaje anterior y conecta el parámetro del Animator con el movimiento WASD. Activa la carrera cuando la entrada de movimiento tenga alguna dirección y vuelve a reposo cuando no la tenga. Comprueba también las combinaciones de dos teclas.

**Pista:** aprovecha el vector de movimiento que ya calcula tu script. **Comprueba:** la animación responde al empezar y al terminar de caminar.

### U160. Mirar hacia donde caminas

Haz que el sprite mire a la derecha al caminar hacia la derecha y a la izquierda al caminar hacia la izquierda. Cuando el personaje se detenga, conserva la última orientación. Mantén el comportamiento de las animaciones que ya preparaste.

**Pista:** cambia flipX del SpriteRenderer solo cuando haya movimiento horizontal. **Comprueba:** girar al personaje no modifica sus colisiones ni invierte la interfaz.

## 17. Acciones por proximidad y reglas de juego (U161-U170)

Base del bloque: reutiliza un jugador WASD, enemigos sencillos, colisiones 2D, contadores y la persecución cercana de U096.

### U161. Medir distancias a varios enemigos

Coloca cinco enemigos inmóviles y guarda sus referencias en un array asignado desde el Inspector. Al pulsar una tecla, recorre el array y muestra en Console el nombre y la distancia 2D de cada enemigo respecto al jugador.

**Pista:** calcula cada distancia con posiciones tratadas como Vector2. **Comprueba:** al mover al jugador cambian las distancias de todos los enemigos.

### U162. Encontrar objetos en un círculo

Añade un Collider2D a cada enemigo y crea una capa física desde Layer > Add Layer, distinta del orden visual. Asigna los enemigos a ella y selecciónala en un campo LayerMask. Consulta Physics2D.OverlapCircleAll con radio 3 y ese filtro; muestra cuántos detecta.

**Pista:** utiliza un único collider por enemigo y excluye al jugador de la capa. **Comprueba:** detectas solo enemigos cuyos colliders alcanzan el círculo.

### U163. Destruir enemigos cercanos

**Origen: PDF E56.**

Prepara varios enemigos estáticos y un jugador que se mueva con WASD. Al pulsar espacio, destruye todos los enemigos cuya distancia entre centros sea menor que 3 unidades. Conserva los que estén a 3 unidades o más y permite repetir la acción.

**Pista:** comprueba la distancia exacta de cada candidato y omite referencias vacías. **Comprueba:** una pulsación puede eliminar varios enemigos simultáneamente.

### U164. Provocar una explosión de impulso

**Origen: PDF E57.**

Construye una habitación con suelo, paredes y techo estáticos, y varios cuerpos con Rigidbody2D dinámico. Mueve al jugador con WASD. Al pulsar espacio, aplica un impulso hacia fuera a los cuerpos cuyo centro esté a menos de 3 unidades del jugador.

**Pista:** Reutiliza el filtro de U162, resta posiciones y aplica AddForce con ForceMode2D.Impulse; usa un collider por cuerpo. **Comprueba:** Solo los cuerpos cercanos reciben impulso hacia fuera.

### U165. Invertir la gravedad

**Origen: PDF E58.**

Reutiliza la habitación cerrada con varios cuerpos físicos y haz que espacio invierta Physics2D.gravity. Guarda su valor original al entrar y restáuralo al desactivar el controlador, para no alterar otras escenas. Observa cómo los cuerpos pasan del suelo al techo.

**Pista:** la gravedad 2D afecta globalmente a los cuerpos dinámicos. **Comprueba:** dos pulsaciones recuperan la dirección inicial y salir restaura el valor guardado.

### U166. Patrullar entre dos puntos

Crea dos objetos vacíos como extremos de una patrulla y asigna sus referencias a un enemigo visual sin Rigidbody2D. Haz que avance hacia el primer punto y cambie de destino al llegar. Repite el recorrido con una velocidad ajustable desde el Inspector.

**Pista:** guarda cuál de los dos puntos es el destino actual. **Comprueba:** el enemigo completa varias vueltas sin detenerse ni sobrepasar los extremos.

### U167. Alternar patrulla y persecución

Combina la patrulla anterior con la persecución cercana de U096. Mientras el jugador esté lejos, el enemigo patrulla; cuando entre en el radio elegido, lo persigue. Al alejarse el jugador, el enemigo retoma su recorrido entre los dos puntos.

**Pista:** Utiliza una condición para escoger un único comportamiento y conserva el enemigo sin física de U166. **Comprueba:** Acercarte y alejarte cambia su comportamiento.

### U168. Abrir una puerta con una llave

Coloca una llave con trigger y una puerta que bloquee el paso. Al recoger la llave, guarda ese hecho en una variable booleana. Cuando el jugador entre en una zona delante de la puerta, ábrela únicamente si ya tiene la llave.

**Pista:** separa el trigger de detección del collider que bloquea. **Comprueba:** sin llave no pasas y, después de recogerla, sí puedes cruzar.

### U169. Ganar al recoger tres monedas

Reutiliza el contador de monedas y coloca exactamente tres en una escena pequeña. Cuando el jugador recoja la tercera, muestra un mensaje de victoria y desactiva su movimiento. Evita que recoger cada moneda pueda sumar más de una vez.

**Pista:** Comprueba el total tras aumentarlo; bloquea nuevas entradas y deja la velocidad física en cero. **Comprueba:** La tercera moneda detiene al jugador.

### U170. Perder al agotar las vidas

Reutiliza tu sistema de vida y añade una condición de derrota cuando llegue a cero. Muestra un mensaje y desactiva el movimiento. Impide que nuevos contactos con peligros sigan restando vida o repitan la presentación de la derrota.

**Pista:** guarda si la partida ha terminado antes de procesar más daño. **Comprueba:** la vida se mantiene en cero y el mensaje aparece una vez.

## 18. Sonidos y música (U171-U180)

Base del bloque: reutiliza monedas, triggers, prefabs, botones y sliders, y prepara un efecto corto y una pista musical que puedas utilizar.

### U171. Reproducir un sonido 2D

Importa un efecto de sonido corto y asigna el clip a un AudioSource de la escena. Configura Spatial Blend en 0 para reproducirlo como audio 2D. Activa Play On Awake y escucha el resultado al iniciar la escena.

**Pista:** revisa el volumen y que la cámara conserve su AudioListener. **Comprueba:** el efecto se escucha sin depender de la posición del jugador.

### U172. Escuchar una moneda al entrar

**Origen: PDF E63.**

Coloca una zona con Collider2D marcado como trigger. Cuando el jugador entre, reproduce un sonido de moneda mediante un AudioSource, aunque no recoja ningún objeto. Permite volver a escucharlo si sale de la zona y entra otra vez.

**Pista:** filtra al jugador y reproduce el sonido desde OnTriggerEnter2D. **Comprueba:** quedarse dentro no dispara el efecto continuamente.

### U173. Crear un objeto con sonido

**Origen: PDF E64.**

Reutiliza un prefab que aparezca al pulsar espacio y añade un sonido a cada aparición. Configura su AudioSource para reproducir el efecto al crearse o actívalo desde el código de creación. Mantén una sola reproducción por objeto generado.

**Pista:** elige una sola forma de iniciar el audio para evitar duplicados. **Comprueba:** tres pulsaciones generan tres objetos y tres sonidos.

### U174. Repetir una música de fondo

**Origen: PDF E65.**

Crea un objeto independiente para la música de fondo y asígnale un AudioSource 2D. Activa Loop y Play On Awake. Ajusta su volumen para que puedas distinguir los efectos de las monedas mientras la música continúa durante toda la escena.

**Pista:** empieza con un volumen moderado y escucha el final del clip. **Comprueba:** la música vuelve a empezar sin que tengas que pulsar nada.

### U175. Ajustar el volumen con un slider

Reutiliza un slider de interfaz y configura su rango entre 0 y 1. Conecta su cambio de valor con el volumen del AudioSource de música. Al iniciar, coloca el slider en el valor que realmente esté utilizando la música.

**Pista:** utiliza On Value Changed para transmitir el valor del slider. **Comprueba:** ambos extremos permiten silenciar la música y recuperar su volumen máximo.

### U176. Silenciar sin perder el volumen

Añade un botón que alterne entre silenciar y recuperar la música. Utiliza la propiedad mute del AudioSource para conservar el volumen que elegiste con el slider. Cambia el texto del botón para indicar la acción disponible en cada momento.

**Pista:** invierte un estado booleano en cada pulsación. **Comprueba:** al recuperar el sonido se mantiene el volumen seleccionado antes de silenciar.

### U177. Pausar y continuar la música

Añade un botón para pausar la música y otro para continuarla desde el mismo instante. Conserva los controles de volumen y silencio. Escucha un fragmento reconocible antes de pausar para poder comprobar después que no vuelve al principio.

**Pista:** compara Pause y UnPause con el comportamiento de Stop. **Comprueba:** reanudar continúa el fragmento y no reinicia la pista musical.

### U178. Dar sonido a un botón

Añade un sonido corto a uno de tus botones de interfaz. Reprodúcelo desde un AudioSource independiente cuando llegue el evento On Click y conserva también la acción original del botón. Prueba varios clics sin mantener el botón pulsado.

**Pista:** un mismo evento puede ejecutar más de una acción. **Comprueba:** cada clic realiza su función y reproduce una sola confirmación sonora.

### U179. Terminar el sonido de una moneda

Haz que una moneda desaparezca al recogerla y que su sonido se escuche completo. Traslada la reproducción a un emisor independiente que permanezca en la escena, aunque la moneda se destruya inmediatamente. Reutiliza el contador de monedas existente.

**Pista:** reproduce el clip desde un AudioSource de la escena con PlayOneShot. **Comprueba:** la moneda desaparece sin cortar el final del sonido.

### U180. Variar ligeramente un efecto

Reutiliza un efecto corto y cambia ligeramente su pitch antes de cada reproducción, eligiendo un valor aleatorio entre 0,9 y 1,1. Haz la prueba con pulsaciones separadas para escuchar cada variación completa. Mantén la música con su tono habitual.

**Pista:** cambia el pitch del AudioSource dedicado al efecto. **Comprueba:** las reproducciones se parecen, pero no suenan todas exactamente iguales.

## 19. Escenas, pausa y datos guardados (U181-U190)

Base del bloque: reutiliza botones, temporizadores y música, y guarda una copia de las escenas antes de añadir navegación entre ellas.

### U181. Preparar tres escenas de colores

Crea tres escenas llamadas e66_red, e66_blue y e66_green. Configura el fondo de sus cámaras ortográficas en rojo, azul y verde respectivamente, y añade un texto que identifique cada escena. Inclúyelas en la lista de escenas de Build Profiles.

**Pista:** guarda cada escena antes de añadirla a la lista. **Comprueba:** sus nombres coinciden exactamente y los tres fondos se distinguen al ejecutarlas.

### U182. Cargar la escena roja con espacio

**Origen: PDF E66.**

Añade a las tres escenas un controlador que cargue e66_red cuando pulses espacio. Utiliza SceneManager para realizar el cambio y una pulsación nueva del Input System. Prueba la acción empezando desde cada una de las tres escenas.

**Pista:** SceneManager pertenece a UnityEngine.SceneManagement. **Comprueba:** desde azul o verde pasas a rojo, y desde rojo recargas la misma escena.

### U183. Cargar la escena azul con un botón

**Origen: PDF E66.**

Coloca un botón visible en cada una de las tres escenas y conecta su evento On Click con un método que cargue e66_blue. Mantén también la navegación con espacio y comprueba ambas acciones desde las tres escenas disponibles.

**Pista:** utiliza un método público sin parámetros para conectarlo desde el Inspector. **Comprueba:** cualquier botón lleva a azul y espacio sigue llevando a rojo.

### U184. Cambiar tras diez segundos de inactividad

**Origen: PDF E66.**

Añade a las tres escenas un temporizador de inactividad que cargue e66_green al alcanzar diez segundos. Reinicia la cuenta al pulsar cualquier tecla, mover el ratón, usar su rueda o pulsar sus botones. Reutiliza tu temporizador con Time.deltaTime.

**Pista:** consulta Keyboard.current y Mouse.current comprobando que existan. **Comprueba:** nueve segundos de espera y una entrada reinician los diez segundos completos.

### U185. Mantener la música al cambiar de escena

**Origen: PDF E67.**

Crea e67_red y e67_blue con sus fondos correspondientes. Inicia música en roja y conserva su objeto raíz con DontDestroyOnLoad. Al pulsar espacio, carga azul y comprueba que la misma pista sigue sonando desde el punto alcanzado, sin reiniciarse.

**Pista:** registra ambas escenas y deja el objeto de música sin padre. **Comprueba:** el cambio de color no interrumpe ni reinicia la canción.

### U186. Evitar música duplicada al regresar

Añade un botón para volver de e67_blue a e67_red. Guarda una referencia compartida, mediante un campo static, al reproductor conservado. En Awake, conserva la primera instancia e inicia su audio con Play; destruye las nuevas copias sin reproducirlas. Mantén desactivado Play On Awake.

**Pista:** Awake prepara el objeto antes de Start; static comparte la referencia entre copias. **Comprueba:** Varios viajes conservan una sola canción, que no reinicia.

### U187. Reiniciar la escena actual

Añade un botón de reinicio a una escena de juego ya terminada. Carga de nuevo la escena activa usando su nombre y comprueba que recupera su estado inicial: posición del jugador, monedas presentes y contador. Mantén la música persistente si existe.

**Pista:** consulta el nombre con SceneManager.GetActiveScene(). **Comprueba:** reiniciar después de jugar recupera los valores iniciales sin crear otra copia de la música.

### U188. Mostrar un menú de pausa

Añade un panel con un botón para continuar y alterna la pausa con Escape. Detén el tiempo del juego con Time.timeScale, bloquea las acciones del jugador y muestra el panel. Al continuar o abandonar la escena, restablece el tiempo a 1.

**Pista:** usa un booleano de pausa y restaura el tiempo al desactivar el controlador. **Comprueba:** los objetos se detienen y el botón permite continuar.

### U189. Guardar una mejor puntuación

Reutiliza una escena con puntuación y guarda su mejor resultado mediante PlayerPrefs. Al terminar, compara la puntuación actual con el récord guardado y actualízalo solo si lo supera. Muestra el récord en un texto de interfaz al entrar.

**Pista:** usa una clave fija y un valor inicial de cero. **Comprueba:** una partida peor no sustituye el mejor resultado obtenido anteriormente.

### U190. Comprobar la recuperación de datos

Prueba el récord anterior deteniendo y volviendo a iniciar Play. Añade un botón de prueba que borre únicamente la clave del récord y actualice su texto. Comprueba el valor inicial, una mejora y una puntuación inferior; repetirás la prueba en el ejecutable de U200.

**Pista:** utiliza Save para guardar y DeleteKey para borrar esa clave. **Comprueba:** reiniciar conserva el récord y el botón lo devuelve a cero.

## 20. Pequeños retos y entrega del proyecto (U191-U200)

Base del bloque: combina escenas y prefabs ya terminados; centra cada ejercicio en una modificación pequeña y una prueba concreta.

### U191. Abrir con tres interruptores

Reutiliza la puerta de U168 y sustituye la llave por tres interruptores con trigger. Cada interruptor debe activarse solo una vez y cambiar de color. Abre la puerta cuando los tres estén activados, sin exigir un orden específico.

**Pista:** guarda un booleano por interruptor y cuenta las activaciones nuevas. **Comprueba:** pisar varias veces el mismo interruptor no abre la puerta antes de tiempo.

### U192. Recoger monedas antes de que termine el tiempo

Combina el temporizador de U073 con las monedas de U140 y la victoria de U169. Transforma el temporizador en una cuenta atrás desde treinta segundos. Muestra victoria al recoger las tres monedas o derrota al agotarse el tiempo, deteniendo la partida.

**Pista:** usa un único estado de partida terminada para resolver el resultado. **Comprueba:** después de ganar no aparece una derrota por el temporizador.

### U193. Llegar a una meta saltando

Reutiliza el movimiento y salto de U116. Prepara dos plataformas con etiqueta Suelo, separadas para que el jugador no toque ambas simultáneamente. Coloca una meta con trigger después de la segunda y adapta la victoria de U169 para terminar al llegar.

**Pista:** ajusta las distancias utilizando el salto que ya funciona. **Comprueba:** puedes completar el recorrido y la victoria aparece únicamente al tocar la meta.

### U194. Encontrar una referencia vacía

En una copia de una escena, deja sin asignar una referencia que utilice tu script, por ejemplo el texto del contador. Ejecuta la escena, localiza el error en Console y sigue su enlace hasta la línea afectada. Repara la asignación en el Inspector.

**Pista:** lee el nombre del script y qué objeto necesita esa línea. **Comprueba:** al repetir la misma acción desaparece el error y vuelve la función.

### U195. Probar valores en los límites

Revisa la acción de proximidad de U163 colocando enemigos a 2,9, 3 y 3,1 unidades del jugador. Anota qué debería pasar con cada uno y ejecuta la prueba. Corrige la comparación si el resultado no coincide con el requisito original.

**Pista:** conserva la condición estricta de distancia menor que 3. **Comprueba:** solo desaparece el enemigo situado a 2,9 unidades.

### U196. Explicar cómo jugar en pantalla

Añade a una escena terminada un panel breve con sus controles y objetivo. Indica solo las teclas que realmente funcionan en esa escena y permite ocultar el panel con un botón. Comprueba que no tapa al jugador ni los indicadores principales.

**Pista:** usa frases cortas y un tamaño de texto legible. **Comprueba:** otra persona puede identificar cómo moverse y qué debe conseguir sin explicaciones adicionales.

### U197. Preparar un menú de selección

Crea una escena MainMenu con título y Scroll View. Diseña un botón con espacio para el nombre de un ejercicio y guárdalo como prefab. Prepara Content con un Vertical Layout Group para distribuir botones y ajusta el desplazamiento vertical.

**Pista:** Content Size Fitter puede adaptar la altura al contenido. **Comprueba:** al añadir varias copias, los botones quedan separados y puedes recorrer la lista.

### U198. Generar botones a partir de una lista

Registra primero tres escenas de prueba. Recorre por índice las escenas incluidas en la compilación y crea un botón por escena dentro de Content, excepto MainMenu. El componente de cada botón guardará su propio nombre de escena y tendrá un método público para cargarla.

**Pista:** Usa `SceneManager.sceneCountInBuildSettings`, `SceneUtility.GetScenePathByBuildIndex` y `System.IO.Path.GetFileNameWithoutExtension`. **Comprueba:** Cada botón muestra su nombre y abre su propia escena.

### U199. Acceder a todos los ejercicios

**Origen: PDF E68.**

Añade en grupo todas las escenas guardadas a Build Profiles y comprueba que el menú de U198 las enumera. Crea en MainMenu un único controlador persistente, reutilizando U185-U186, que permita regresar con F1 desde cualquier ejercicio. Prueba tres recorridos de ida y vuelta.

**Pista:** Coloca MainMenu primero y evita duplicar el controlador al regresar. **Comprueba:** El menú lista todas las escenas incluidas, sin configurar botones individualmente.

### U200. Crear y probar el ejecutable

**Origen: PDF E68.**

Genera una compilación de escritorio del proyecto completo y ejecútala fuera del Editor. Copia la carpeta de salida completa a otro ordenador compatible. Prueba MainMenu, entrada, sonido y regreso con F1; cierra y abre el ejecutable para comprobar el récord. Anota cualquier fallo para corregirlo.

**Pista:** el otro ordenador debe usar un sistema compatible con la compilación. **Comprueba:** el proyecto funciona sin abrir Unity y conserva la navegación.

## Correspondencia con los ejercicios del PDF

Los códigos E corresponden al documento original; los códigos U, a esta progresión. Las actividades preparatorias adicionales no necesitan una correspondencia.

| Ejercicio original | Ejercicio de esta lista |
|---|---|
| E01 | U101 |
| E02 | U012 |
| E03 | U072 |
| E04 | U039 |
| E05 | U031 |
| E06 | U036 |
| E07 | U049 |
| E08 | U056 |
| E09 | U051 |
| E10 | U053 |
| E11 | U054 |
| E12 | U055 |
| E13 | U057 |
| E14 | U058 |
| E15 | U059 |
| E16 | U074 |
| E17 | U075 |
| E18 | U076 |
| E19 | U085 |
| E20 | U086 |
| E21 | U091 |
| E22 | U094 |
| E23 | U104 |
| E24 | U105 |
| E25 | U109 |
| E26 | U111 |
| E27 | U114 |
| E28 | U115 |
| E29 | U110 |
| E30 | U122 |
| E31 | U123 |
| E32 | U124 |
| E33 | U155 |
| E34 | U156 |
| E35 | U098 |
| E36 | U132 |
| E37 | U133 |
| E38 | U134 |
| E39 | U135 |
| E40 | U136 |
| E41 | U125 |
| E42 | U126 |
| E43 | U140 |
| E44 | U092 |
| E45 | U100 |
| E46 | U118 |
| E47 | U096 |
| E48 | U095 |
| E49 | U021 |
| E50 | U022 |
| E51 | U090 |
| E52 | U027 |
| E53 | U152 |
| E54 | U157 |
| E55 | U158 |
| E56 | U163 |
| E57 | U164 |
| E58 | U165 |
| E59 | U142 |
| E60 | U143 |
| E61 | U145 |
| E62 | U127 |
| E63 | U172 |
| E64 | U173 |
| E65 | U174 |
| E66 | U182, U183, U184 |
| E67 | U185 |
| E68 | U199, U200 |

## Recursos y referencias

Los recursos visuales propuestos en el PDF son [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks), para U026-U027 y U151-U152, y [Dino Characters, de Arks](https://arks.itch.io/dino-characters), para U157-U160. También puedes utilizar recursos equivalentes facilitados por el docente. Revisa las condiciones de uso del recurso que elijas.

Para resolver las actividades, consulta estas referencias oficiales según el concepto que estés practicando:

- **U081, entrada:** [Instalación y activación de Input System](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.17/manual/Installation.html). Utiliza la versión del paquete compatible que ofrezca Package Manager.
- **U094, suavizado:** [Vector2.SmoothDamp](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Vector2.SmoothDamp.html).
- **U116-U118, velocidad física:** [Rigidbody2D.linearVelocity](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D-linearVelocity.html). La velocidad ya se expresa en unidades por segundo.
- **U119, movimiento cinemático:** [Rigidbody2D.MovePosition](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D.MovePosition.html). Se utiliza en pasos de física y no sustituye el comportamiento de gravedad de un cuerpo dinámico.
- **U181 y U199, escenas incluidas:** [Lista de escenas de Build Profiles](https://docs.unity3d.com/6000.0/Documentation/Manual/build-profile-scene-list.html).
- **U198, menú automático:** [Cantidad de escenas incluidas](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneManager-sceneCountInBuildSettings.html) y [ruta de una escena por su índice](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneUtility.GetScenePathByBuildIndex.html).
