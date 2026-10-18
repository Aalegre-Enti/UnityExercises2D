# 200 ejercicios cortos para aprender Unity 2D y C# desde cero

Una progresión para personas que nunca han programado. Los ejercicios alternan el uso del editor con pequeños programas en C#: primero observarás y modificarás objetos; después crearás comportamientos y combinarás lo aprendido en escenas interactivas.

## Cómo practicar y qué merece la pena guardar

Estos ejercicios son para practicar por tu cuenta: no se evalúan ni hay que entregarlos. Puedes trabajar en un proyecto de pruebas y modificar una misma escena tantas veces como necesites. No hace falta conservar cada resultado ni reunir las actividades en una aplicación.

Sigue el orden si partes de cero: cada bloque introduce conocimientos que se usan después. Cuando sustituyas un comportamiento, desactiva o retira el componente anterior para evitar que dos scripts muevan el mismo objeto o respondan a la misma tecla. Conserva activos los componentes que la nueva práctica siga necesitando.

**Comprueba** propone una observación para saber si has entendido el comportamiento; no es un criterio de calificación. Cuando una actividad retoma otra, puedes continuar en la misma sesión, recuperar una base que hayas conservado o reconstruir solo lo necesario.

La marca **★** del índice identifica resultados que **conviene guardar de forma opcional**. En cada uno encontrarás qué conservar y para qué:

- **Prácticas posteriores:** una base útil para retomar otros ejercicios; se indican sus enlaces.
- **Futuros proyectos:** un script, prefab, interfaz o recurso que puedes adaptar a otro juego. Son ejemplos de aprendizaje, que tendrás que ajustar y probar en su nuevo contexto.

Los ejercicios sin marca pueden quedarse como experimentos temporales. No necesitas guardar por separado todas las versiones intermedias: las recomendaciones priorizan resultados que reúnen varios pasos ya practicados.

Guardar un script para que Unity compile, crear un prefab o guardar escenas para probar su carga forma parte del funcionamiento de Unity. Eso no implica que debas archivar la práctica al terminar. Si decides conservar una pieza, incluye sus scripts y recursos necesarios y anota qué referencias debes asignar en el Inspector.

## Preparación y alcance

Se toma **Unity 6** como referencia. Necesitarás Unity Hub, el editor y un editor de C# conectado a Unity. Utiliza un proyecto con plantilla **2D**; los nombres de algunos menús pueden variar entre versiones.

Todo el trabajo es en **2D**: sprites, cámara ortográfica, movimiento en X/Y, rotación dentro del plano, `Rigidbody2D`, colisionadores 2D, Tilemap, interfaz y audio en modo 2D. La posición de los sprites mantendrá Z en 0 y la cámara conservará su Z inicial. Aunque `Transform` almacene tres coordenadas internamente, solo modificaremos las necesarias para trabajar en el plano; no se introducen mecánicas ni recursos de 3D.

Se introduce **Input System** en [U081](#u081) y se mantiene ese mismo sistema para teclado, ratón y botones. En física se distinguirá entre mover un objeto visual y controlar un cuerpo físico.

<a name="indice"></a>

## Índice de ejercicios

Pulsa un código para ir directamente a ese ejercicio o un tema para abrir su bloque. Las etiquetas bajo cada título indican qué conceptos se trabajan; puedes buscarlas con el buscador del navegador. **★** señala una recomendación opcional de guardado, explicada al final del ejercicio.

| Bloque | Tema | Ejercicios |
|---|---|---|
| [1](#bloque-01) | [Primer contacto con el editor](#bloque-01) | [U001](#u001) · [U002](#u002) · [U003](#u003) · [U004](#u004) · [U005](#u005)<br>[U006](#u006) · [U007](#u007) · [U008](#u008) · [U009](#u009) · [U010](#u010) |
| [2](#bloque-02) | [Primeros scripts y variables](#bloque-02) | [U011](#u011) · [U012](#u012) · [U013](#u013) · [U014](#u014) · [U015](#u015)<br>[U016](#u016) · [U017](#u017) · [U018](#u018) · [U019](#u019) · [U020](#u020) |
| [3](#bloque-03) | [Sprites y organización visual](#bloque-03) | [U021](#u021) · [U022](#u022) · [U023](#u023) · [U024](#u024) · [U025](#u025)<br>[U026](#u026) · [U027 ★](#u027) · [U028](#u028) · [U029](#u029) · [U030 ★](#u030) |
| [4](#bloque-04) | [Números y datos](#bloque-04) | [U031](#u031) · [U032](#u032) · [U033](#u033) · [U034](#u034) · [U035](#u035)<br>[U036](#u036) · [U037](#u037) · [U038](#u038) · [U039](#u039) · [U040](#u040) |
| [5](#bloque-05) | [Decisiones](#bloque-05) | [U041](#u041) · [U042](#u042) · [U043](#u043) · [U044](#u044) · [U045](#u045)<br>[U046](#u046) · [U047](#u047) · [U048](#u048) · [U049 ★](#u049) · [U050](#u050) |
| [6](#bloque-06) | [Azar y repeticiones](#bloque-06) | [U051](#u051) · [U052](#u052) · [U053](#u053) · [U054 ★](#u054) · [U055](#u055)<br>[U056](#u056) · [U057](#u057) · [U058](#u058) · [U059](#u059) · [U060](#u060) |
| [7](#bloque-07) | [Métodos, referencias y arrays](#bloque-07) | [U061](#u061) · [U062](#u062) · [U063](#u063) · [U064](#u064) · [U065 ★](#u065)<br>[U066](#u066) · [U067](#u067) · [U068 ★](#u068) · [U069](#u069) · [U070 ★](#u070) |
| [8](#bloque-08) | [Tiempo y movimiento automático](#bloque-08) | [U071](#u071) · [U072](#u072) · [U073 ★](#u073) · [U074](#u074) · [U075](#u075)<br>[U076](#u076) · [U077 ★](#u077) · [U078](#u078) · [U079](#u079) · [U080](#u080) |
| [9](#bloque-09) | [Teclado y ratón](#bloque-09) | [U081](#u081) · [U082](#u082) · [U083](#u083) · [U084](#u084) · [U085](#u085)<br>[U086](#u086) · [U087](#u087) · [U088 ★](#u088) · [U089](#u089) · [U090](#u090) |
| [10](#bloque-10) | [Seguimiento y cámara](#bloque-10) | [U091](#u091) · [U092](#u092) · [U093](#u093) · [U094 ★](#u094) · [U095](#u095)<br>[U096 ★](#u096) · [U097](#u097) · [U098](#u098) · [U099 ★](#u099) · [U100 ★](#u100) |
| [11](#bloque-11) | [Física 2D](#bloque-11) | [U101](#u101) · [U102](#u102) · [U103](#u103) · [U104](#u104) · [U105](#u105)<br>[U106](#u106) · [U107](#u107) · [U108](#u108) · [U109](#u109) · [U110](#u110) |
| [12](#bloque-12) | [Control de cuerpos físicos](#bloque-12) | [U111](#u111) · [U112](#u112) · [U113](#u113) · [U114](#u114) · [U115](#u115)<br>[U116 ★](#u116) · [U117 ★](#u117) · [U118 ★](#u118) · [U119 ★](#u119) · [U120](#u120) |
| [13](#bloque-13) | [Zonas e interacciones](#bloque-13) | [U121](#u121) · [U122](#u122) · [U123](#u123) · [U124](#u124) · [U125](#u125)<br>[U126](#u126) · [U127 ★](#u127) · [U128](#u128) · [U129](#u129) · [U130 ★](#u130) |
| [14](#bloque-14) | [Interfaz y puntuación](#bloque-14) | [U131](#u131) · [U132 ★](#u132) · [U133](#u133) · [U134](#u134) · [U135 ★](#u135)<br>[U136](#u136) · [U137 ★](#u137) · [U138 ★](#u138) · [U139 ★](#u139) · [U140 ★](#u140) |
| [15](#bloque-15) | [Prefabs y creación de objetos](#bloque-15) | [U141 ★](#u141) · [U142](#u142) · [U143](#u143) · [U144](#u144) · [U145](#u145)<br>[U146](#u146) · [U147](#u147) · [U148](#u148) · [U149](#u149) · [U150 ★](#u150) |
| [16](#bloque-16) | [Mapas y animación](#bloque-16) | [U151 ★](#u151) · [U152](#u152) · [U153](#u153) · [U154 ★](#u154) · [U155](#u155)<br>[U156](#u156) · [U157](#u157) · [U158](#u158) · [U159](#u159) · [U160 ★](#u160) |
| [17](#bloque-17) | [Áreas, enemigos y objetivos](#bloque-17) | [U161](#u161) · [U162 ★](#u162) · [U163 ★](#u163) · [U164](#u164) · [U165](#u165)<br>[U166](#u166) · [U167 ★](#u167) · [U168 ★](#u168) · [U169 ★](#u169) · [U170](#u170) |
| [18](#bloque-18) | [Sonido y música](#bloque-18) | [U171](#u171) · [U172 ★](#u172) · [U173](#u173) · [U174](#u174) · [U175](#u175)<br>[U176](#u176) · [U177 ★](#u177) · [U178](#u178) · [U179 ★](#u179) · [U180](#u180) |
| [19](#bloque-19) | [Escenas, pausa y guardado](#bloque-19) | [U181 ★](#u181) · [U182](#u182) · [U183](#u183) · [U184](#u184) · [U185](#u185)<br>[U186 ★](#u186) · [U187 ★](#u187) · [U188 ★](#u188) · [U189](#u189) · [U190 ★](#u190) |
| [20](#bloque-20) | [Prácticas combinadas y reutilización](#bloque-20) | [U191 ★](#u191) · [U192](#u192) · [U193](#u193) · [U194](#u194) · [U195](#u195)<br>[U196 ★](#u196) · [U197](#u197) · [U198 ★](#u198) · [U199 ★](#u199) · [U200](#u200) |

<a name="bloque-01"></a>

## 1. Primer contacto con el editor (U001-U010)

Base: ninguna experiencia previa. Estas actividades se realizan sin scripts.

<a name="u001"></a>

### U001. Tu primer proyecto

**Etiquetas:** `Unity Hub` · `Proyecto 2D` · `Escenas`

Crea desde Unity Hub un proyecto de pruebas con plantilla 2D. Abre el editor y localiza la escena inicial. Puedes utilizar este mismo proyecto para tantas prácticas como quieras.

<details>
<summary>Pista</summary>

una escena es el espacio donde colocas objetos.

</details>

**Comprueba:** reconoces la escena abierta y localizas su cámara en Hierarchy.

<a name="u002"></a>

### U002. Localizar las ventanas

**Etiquetas:** `Editor` · `Ventanas` · `Inspector`

Selecciona la cámara en Hierarchy y localiza sus propiedades en Inspector. Alterna entre Scene y Game, y encuentra Project y Console. Identifica para qué sirve cada ventana; puedes explicártelo en voz alta.

<details>
<summary>Pista</summary>

Scene permite editar; Game muestra la vista de la cámara.

</details>

**Comprueba:** puedes localizar las seis ventanas sin ayuda.

<a name="u003"></a>

### U003. Un cuadrado en pantalla

**Etiquetas:** `GameObject` · `Sprites` · `SpriteRenderer`

Añade un sprite cuadrado desde GameObject > 2D Object > Sprites > Square, o la opción equivalente de tu versión. Renómbralo `Jugador`, sitúalo en X=0, Y=0, Z=0 y cambia su color desde Sprite Renderer.

<details>
<summary>Pista</summary>

un GameObject reúne componentes; Sprite Renderer dibuja el sprite.

</details>

**Comprueba:** el cuadrado aparece en Game con el color elegido.

<a name="u004"></a>

### U004. Mover con coordenadas

**Etiquetas:** `Transform` · `Posición` · `Coordenadas X/Y`

Mueve el cuadrado cambiando X e Y en Transform. Prueba X=2 y después Y=-1. Devuélvelo al origen utilizando los campos numéricos, sin arrastrarlo.

<details>
<summary>Pista</summary>

X indica izquierda/derecha; Y, abajo/arriba.

</details>

**Comprueba:** sabes anticipar hacia dónde se moverá antes de cambiar cada valor.

<a name="u005"></a>

### U005. Cambiar el tamaño

**Etiquetas:** `Transform` · `Escala` · `Inspector`

Modifica Scale X e Y para obtener un rectángulo ancho y después uno alto. Termina con un cuadrado que mida el doble que el inicial.

<details>
<summary>Pista</summary>

escala 1 conserva el tamaño original.

</details>

**Comprueba:** cambiar la escala no modifica los valores de Position.

<a name="u006"></a>

### U006. Girar dentro del plano

**Etiquetas:** `Transform` · `Rotación Z` · `Grados`

Restaura la escala y gira el sprite usando únicamente Rotation Z: prueba 0, 45 y 90 grados. Mantén Rotation X e Y en 0.

<details>
<summary>Pista</summary>

Rotation Z gira la imagen dentro de la pantalla.

</details>

**Comprueba:** a 45 grados el cuadrado parece un rombo.

<a name="u007"></a>

### U007. Duplicar y nombrar

**Etiquetas:** `Duplicación` · `Hierarchy` · `SpriteRenderer`

Duplica el cuadrado dos veces. Llama a los objetos `Rojo`, `Verde` y `Azul`, cambia sus colores y colócalos separados en una fila.

<details>
<summary>Pista</summary>

cada copia tiene sus propios componentes.

</details>

**Comprueba:** cambiar el color de uno no cambia el de los demás.

<a name="u008"></a>

### U008. Encuadrar la escena

**Etiquetas:** `Cámara ortográfica` · `Encuadre` · `Color de fondo`

Selecciona la cámara, confirma que su proyección es Orthographic y ajusta Size para ver los tres cuadrados. Cambia también el color del fondo.

<details>
<summary>Pista</summary>

una Size mayor permite ver más espacio.

</details>

**Comprueba:** el encuadre de Game contiene los tres objetos completos.

<a name="u009"></a>

### U009. Distinguir edición y ejecución

**Etiquetas:** `Modo Play` · `Edición` · `Guardar escenas`

Entra en Play, mueve un cuadrado y detén la ejecución. Observa qué ocurre. Después realiza el mismo cambio fuera de Play y guarda la escena.

<details>
<summary>Pista</summary>

los cambios de objetos de escena durante Play normalmente no se conservan al detenerlo.

</details>

**Comprueba:** el cambio guardado fuera de Play permanece.

<a name="u010"></a>

### U010. Preparar una carpeta de trabajo

**Etiquetas:** `Project` · `Organización de recursos` · `Escenas`

Crea carpetas para escenas, scripts e imágenes dentro de `Assets/Practica/`. Prueba a guardar una copia de la escena y vuelve a abrir la anterior para distinguir ambas. Estas copias sirven para experimentar con la organización; no necesitas conservarlas después.

<details>
<summary>Pista</summary>

mueve los recursos desde Project para conservar sus referencias.

</details>

**Comprueba:** puedes abrir las dos escenas y reconocer cuál estás editando.

[Volver al índice](#indice)

<a name="bloque-02"></a>

## 2. Primeros scripts y variables (U011-U020)

Base: la escena con un cuadrado. Un script es un archivo de instrucciones; Unity ejecuta sus métodos de inicio y actualización cuando el componente está habilitado y su objeto está activo.

Puedes modificar el mismo script en estas prácticas. Si creas otro, usa un nombre nuevo para la clase y el archivo y desactiva el componente anterior para que sus mensajes no se mezclen. Después de editar código, guarda el archivo, vuelve a Unity y espera a que termine la compilación antes de Play. Usa Clear en Console antes de comparar los mensajes de dos pruebas. Unity compila todos los archivos C# del proyecto: corrige los errores aunque el script no esté adjunto a ningún objeto.

<a name="u011"></a>

### U011. Crear y adjuntar un script

**Etiquetas:** `C#` · `Scripts` · `Clases` · `Componentes`

En Project, utiliza Create > Scripting > MonoBehaviour Script, o la opción equivalente de tu versión, para crear `U011_PrimerScript`. Ábrelo, localiza `public class U011_PrimerScript : MonoBehaviour` y sus llaves. Arrastra el archivo al Inspector del cuadrado para añadirlo como componente. Conserva la estructura creada por Unity.

<details>
<summary>Pista</summary>

el nombre de la clase debe coincidir con el archivo. Si la plantilla no incluye `Start()` y `Update()`, utiliza esta estructura; si ya existen, no los dupliques:

```csharp
using UnityEngine;

public class U011_PrimerScript : MonoBehaviour
{
    void Start()
    {
    }

    void Update()
    {
    }
}
```

</details>

**Comprueba:** el componente aparece en el objeto sin errores en Console.

**Referencia:** [Crear scripts de componente en Unity](https://docs.unity3d.com/6000.0/Documentation/Manual/creating-scripts.html).


<a name="u012"></a>

### U012. Hello World

**Etiquetas:** `Start` · `Debug.Log` · `Console`

Añade a `Start()` una instrucción que escriba `Hello World` en Console. Ejecuta la escena durante varios segundos y detén Play.

<details>
<summary>Pista</summary>

escribe `Debug.Log("Hello World");` entre las llaves de `Start()`. Las mayúsculas, comillas, paréntesis y punto y coma forman parte de la instrucción.

</details>

**Comprueba:** aparece un solo mensaje por ejecución.

<a name="u013"></a>

### U013. Reconocer un error de sintaxis

**Etiquetas:** `Sintaxis` · `Console` · `Depuración`

En el script anterior, elimina el punto y coma del mensaje. Guarda, localiza el error en Console y abre la línea indicada. Repón el signo y vuelve a ejecutar.

<details>
<summary>Pista</summary>

corrige primero el primer error de la lista.

</details>

**Comprueba:** el mensaje vuelve a aparecer y ya no hay errores rojos.

<a name="u014"></a>

### U014. Leer las instrucciones en orden

**Etiquetas:** `Secuencia de instrucciones` · `Comentarios` · `Start`

Escribe tres mensajes en `Start()` que indiquen inicio, preparación y fin. Añade un comentario con `//` para explicar uno de ellos. Intercambia dos instrucciones.

<details>
<summary>Pista</summary>

los comentarios sirven para las personas y no se ejecutan.

</details>

**Comprueba:** el orden de los mensajes coincide con el del código.

<a name="u015"></a>

### U015. Guardar un nombre

**Etiquetas:** `Variables` · `string` · `Texto`

Declara dentro de la clase, fuera de los métodos, una variable `string` llamada `nombreJugador`. Asígnale tu nombre y úsala para mostrar un saludo en `Start()`.

<details>
<summary>Pista</summary>

una declaración como `string nombreJugador = "Ana";` reserva un dato de texto. En `Start()`, `Debug.Log("Hola, " + nombreJugador);` une el saludo y ese dato con `+`.

</details>

**Comprueba:** al cambiar solo la variable cambia el saludo.

<a name="u016"></a>

### U016. Guardar un número entero

**Etiquetas:** `Variables` · `int` · `Asignación`

Declara una variable `int` llamada `vidas` con valor 3. Muestra su valor al iniciar la escena. Cambia después el valor inicial a 5 y prueba de nuevo.

<details>
<summary>Pista</summary>

los números no llevan comillas.

</details>

**Comprueba:** Console muestra el valor que has asignado a `vidas`.

<a name="u017"></a>

### U017. Guardar un número con decimales

**Etiquetas:** `Variables` · `float` · `Decimales`

Declara una variable `float` llamada `velocidad` con valor `2.5f` y muéstrala al iniciar. Compara su declaración con la variable entera del ejercicio anterior.

<details>
<summary>Pista</summary>

en el código, los decimales usan punto y los literales `float` llevan `f`.

</details>

**Comprueba:** el valor conserva la parte decimal.

<a name="u018"></a>

### U018. Guardar verdadero o falso

**Etiquetas:** `Variables` · `bool` · `Estados`

Declara una variable `bool` llamada `tieneLlave`. Prueba primero `false` y después `true`, mostrando su valor en Console. Escribe qué podría representar en un juego.

<details>
<summary>Pista</summary>

un booleano solo guarda dos posibilidades.

</details>

**Comprueba:** no necesitas escribir esas palabras entre comillas.

<a name="u019"></a>

### U019. Editar datos desde Inspector

**Etiquetas:** `Campos public` · `Inspector` · `Serialización`

Expón las variables de nombre, vidas y velocidad como campos `public`. Modifica sus valores desde Inspector antes de Play y muestra los tres al iniciar la escena.

<details>
<summary>Pista</summary>

escribe, por ejemplo, `public int vidas = 3;` dentro de la clase y fuera de `Start()` o `Update()`. Unity conserva los valores del componente: cambiar el valor inicial en código no siempre sustituye lo guardado en Inspector.

</details>

**Comprueba:** se imprimen los valores del Inspector.

<a name="u020"></a>

### U020. Una vez o en cada fotograma

**Etiquetas:** `Start` · `Update` · `Fotogramas`

Coloca un mensaje en `Start()` y otro diferente en `Update()`. Ejecuta durante dos segundos, detén Play y compara cuántas veces se ha escrito cada uno. Después desactiva el mensaje repetido.

<details>
<summary>Pista</summary>

`Update()` se llama cada fotograma; Console puede agrupar mensajes con Collapse.

</details>

**Comprueba:** distingues una acción inicial de una repetida.

[Volver al índice](#indice)

<a name="bloque-03"></a>

## 3. Sprites y organización visual (U021-U030)

Base: manejo del editor. Trabaja sin scripts para preparar recursos que puedes reutilizar después.

<a name="u021"></a>

### U021. Importar una imagen transparente

**Etiquetas:** `Importación` · `Sprites` · `Transparencia`

Importa un PNG con transparencia que no sea pixel art. Configura Texture Type como Sprite, aplica los cambios y arrastra la imagen a una escena.

<details>
<summary>Pista</summary>

deja visible un fondo de color detrás.

</details>

**Comprueba:** las zonas transparentes muestran el fondo y no un rectángulo opaco.

<a name="u022"></a>

### U022. Conservar los píxeles

**Etiquetas:** `Pixel art` · `Filtrado Point` · `Compresión`

Importa un pequeño PNG de pixel art con transparencia. Configúralo como Sprite, usa filtrado Point y desactiva la compresión. Amplía el objeto para observar sus bordes.

<details>
<summary>Pista</summary>

compara el resultado con el filtrado Bilinear.

</details>

**Comprueba:** los píxeles se distinguen sin el suavizado de sus bordes.

<a name="u023"></a>

### U023. Relacionar píxeles y unidades

**Etiquetas:** `Pixels Per Unit` · `Sprites` · `Unidades`

Duplica el archivo de una imagen y configura distintos valores de Pixels Per Unit en las dos importaciones. Coloca ambos sprites con escala 1 en la escena.

<details>
<summary>Pista</summary>

más píxeles por unidad producen una imagen más pequeña en el mundo.

</details>

**Comprueba:** explicas por qué los tamaños son distintos.

<a name="u024"></a>

### U024. Ordenar objetos superpuestos

**Etiquetas:** `SpriteRenderer` · `Order in Layer` · `Orden visual`

Superpón tres sprites y modifica Order in Layer para decidir cuál se dibuja delante. Mantén la posición Z de los tres en 0.

<details>
<summary>Pista</summary>

el orden visual se controla desde Sprite Renderer.

</details>

**Comprueba:** puedes cambiar qué imagen tapa a las otras sin moverlas.

<a name="u025"></a>

### U025. Cambiar la transparencia

**Etiquetas:** `SpriteRenderer` · `Canal alfa` · `Transparencia`

Coloca un sprite sobre otro. Modifica el canal A del color del sprite delantero para hacerlo semitransparente y después completamente transparente.

<details>
<summary>Pista</summary>

A significa alfa, la opacidad.

</details>

**Comprueba:** puedes ver el sprite posterior a través del delantero.

<a name="u026"></a>

### U026. Preparar una hoja de sprites

**Etiquetas:** `Hoja de sprites` · `Sprite Editor` · `Package Manager`

Descarga y descomprime [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks). Importa a Project el PNG que reúne varias piezas en una hoja. Selecciónalo, configura Texture Type como Sprite y Sprite Mode como Multiple, aplica los cambios y abre Sprite Editor. Si falta, instala 2D Sprite desde Window > Package Manager.

<details>
<summary>Pista</summary>

una hoja reúne varias imágenes en un archivo.

</details>

**Comprueba:** puedes ver la textura completa en Sprite Editor.

**Material:** Puedes utilizar una hoja de sprites equivalente facilitada por el docente. Revisa las condiciones de uso del recurso que elijas.

<a name="u027"></a>

### U027. Separar una hoja en sprites

**Etiquetas:** `Sprite Editor` · `Recorte de sprites` · `Cuadrícula`

Recorta la hoja de [U026](#u026) en Sprite Editor utilizando una cuadrícula adecuada al archivo o recortes manuales. Aplica los cambios y coloca al menos dos sprites distintos en la escena.

<details>
<summary>Pista</summary>

las piezas de este recurso son de 18 × 18 píxeles. En Slice, configura una cuadrícula por tamaño de celda y revisa si la hoja incluye separación; también puedes delimitar dos piezas manualmente. Despliega la textura en Project para ver los sprites recortados.

</details>

**Comprueba:** cada objeto muestra una pieza completa y no toda la hoja.

**Recurso:** Reutiliza [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks), importado en [U026](#u026).

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva la hoja de sprites y su configuración de importación y recorte. Así podrás crear la paleta de piezas de [U151](#u151) y volver a usar esos sprites en otros mapas 2D. **Retómalo en:** [U151](#u151).

<a name="u028"></a>

### U028. Crear un objeto con hijos

**Etiquetas:** `Jerarquía` · `Padres e hijos` · `Transform`

Crea un objeto vacío llamado `Personaje` y coloca dos sprites como hijos: cuerpo y adorno. Mueve y gira el padre para observar qué ocurre con ambos.

<details>
<summary>Pista</summary>

arrastra los objetos dentro del padre en Hierarchy.

</details>

**Comprueba:** el conjunto se mueve sin perder la colocación de sus piezas.

<a name="u029"></a>

### U029. Entender la posición local

**Etiquetas:** `Jerarquía` · `Posición local` · `Transform`

Selecciona el adorno de [U028](#u028) y cambia su posición respecto al padre. Después mueve el padre. Compara la posición que muestra Inspector para el hijo antes y después.

<details>
<summary>Pista</summary>

en una jerarquía, Inspector muestra la posición local del hijo.

</details>

**Comprueba:** mover el padre no cambia esos valores locales.

<a name="u030"></a>

### U030. Activar y desactivar un conjunto

**Etiquetas:** `Activación de objetos` · `Jerarquía` · `Inspector`

Desactiva el objeto padre de [U028](#u028) con la casilla superior de Inspector. Reactívalo y desactiva solo el adorno.

<details>
<summary>Pista</summary>

desactivar un padre también deja inactivos a sus hijos.

</details>

**Comprueba:** sabes ocultar todo el personaje o solo una pieza.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva la escena con el personaje de dos piezas y su jerarquía, dejando activas ambas piezas. Así podrás partir de ese conjunto al animar dos sprites hijos en [U156](#u156). **Retómalo en:** [U156](#u156).

[Volver al índice](#indice)

<a name="bloque-04"></a>

## 4. Números y datos (U031-U040)

Base: los scripts de [U015](#u015)-[U020](#u020). Escribe los resultados en `Start()` y utiliza campos del Inspector para probar diferentes datos.

<a name="u031"></a>

### U031. Sumar dos números

**Etiquetas:** `float` · `Suma` · `Inspector`

Crea dos campos `float`, suma sus valores y muestra el resultado una vez. Prueba con 2.5 y 1.25, y después con un número negativo.

<details>
<summary>Pista</summary>

los datos de entrada pueden ser campos `public float a;` y `public float b;`; dentro de `Start()`, `float resultado = a + b;` calcula la suma antes de mostrarla.

</details>

**Comprueba:** el primer resultado es 3.75.

<a name="u032"></a>

### U032. Calcular lo que queda

**Etiquetas:** `int` · `Resta` · `Texto con variables`

Declara `monedasIniciales` y `precio` como enteros. Calcula cuántas monedas quedan después de una compra y muestra los tres valores en una frase.

<details>
<summary>Pista</summary>

el operador `-` resta.

</details>

**Comprueba:** con 10 monedas y precio 4 quedan 6; con precio 12 obtienes -2.

<a name="u033"></a>

### U033. Calcular un coste total

**Etiquetas:** `float` · `int` · `Multiplicación`

Declara un precio decimal y una cantidad entera. Multiplica ambos para calcular el coste de varias unidades. Prueba también con cantidad 0.

<details>
<summary>Pista</summary>

el operador `*` multiplica.

</details>

**Comprueba:** tres unidades de precio 1.5 cuestan 4.5 y cero unidades cuestan 0.

<a name="u034"></a>

### U034. Repartir sin perder decimales

**Etiquetas:** `División` · `int` · `float`

Divide 5 entre 2 usando primero dos variables `int` y después dos `float`. Muestra ambos resultados y explica la diferencia en un comentario. Usa divisores distintos de cero.

<details>
<summary>Pista</summary>

el tipo de los operandos determina cómo se hace la división.

</details>

**Comprueba:** obtienes 2 en la primera prueba y 2.5 en la segunda.

<a name="u035"></a>

### U035. Encontrar el resto

**Etiquetas:** `Operador %` · `Resto` · `int`

Usa dos enteros para calcular cuántas monedas sobran al formar grupos del mismo tamaño. Prueba con 11 monedas en grupos de 3 y con 12 en grupos de 3.

<details>
<summary>Pista</summary>

`%` devuelve el resto; usa un tamaño de grupo mayor que cero.

</details>

**Comprueba:** los restos son 2 y 0.

<a name="u036"></a>

### U036. Hacer una media

**Etiquetas:** `Media aritmética` · `División` · `Decimales`

Expón tres números enteros en Inspector y calcula su media, conservando la parte decimal. Muestra el resultado una sola vez al iniciar la escena.

<details>
<summary>Pista</summary>

agrupa la suma entre paréntesis antes de dividir: `(a + b + c) / 3f`.

</details>

**Comprueba:** con 1, 2 y 2 el resultado es aproximadamente 1.67, no 1.

<a name="u037"></a>

### U037. Decidir el orden de las operaciones

**Etiquetas:** `Precedencia de operadores` · `Paréntesis` · `Comentarios`

Calcula `2 + 3 * 4` y `(2 + 3) * 4`. Antes de ejecutar, escribe como comentario el resultado que esperas. Comprueba después tu predicción.

<details>
<summary>Pista</summary>

los paréntesis cambian qué operación se hace primero.

</details>

**Comprueba:** los resultados son 14 y 20.

<a name="u038"></a>

### U038. Aumentar un contador

**Etiquetas:** `Contadores` · `Incremento ++` · `int`

Declara una puntuación inicial de 0. Auméntala una unidad tres veces en `Start()`, mostrando el valor después de cada cambio. Repite la prueba con una puntuación inicial de 10.

<details>
<summary>Pista</summary>

`++` incrementa una variable entera.

</details>

**Comprueba:** los mensajes son 1, 2, 3 en la primera prueba y 11, 12, 13 en la segunda.

<a name="u039"></a>

### U039. Guardar un vector del plano

**Etiquetas:** `Vector2` · `Coordenadas X/Y` · `Inspector`

Crea un campo `Vector2` editable desde Inspector y muestra sus dos componentes al iniciar. Prueba los valores X=3 e Y=-2 sin mover todavía ningún objeto.

<details>
<summary>Pista</summary>

`public Vector2 coordenadas = new Vector2(3f, -2f);` crea un campo con dos números; `new Vector2(...)` construye ese vector. Accede a cada componente con `.x` y `.y`.

</details>

**Comprueba:** modificar una componente no cambia la otra.

<a name="u040"></a>

### U040. Dar nombres claros a los resultados

**Etiquetas:** `Variables` · `Nombres descriptivos` · `Operaciones aritméticas`

Calcula el perímetro de un rectángulo a partir de ancho y alto configurables. Guarda el resultado en una variable con un nombre claro y muestra los datos junto al resultado.

<details>
<summary>Pista</summary>

el perímetro suma los cuatro lados.

</details>

**Comprueba:** ancho 3 y alto 2 producen 10; no aparece un número sin contexto.

[Volver al índice](#indice)

<a name="bloque-05"></a>

## 5. Decisiones (U041-U050)

Base: variables y operaciones. Una condición decide si se ejecuta un grupo de instrucciones encerrado entre llaves.

<a name="u041"></a>

### U041. Tu primera condición

**Etiquetas:** `Condicionales` · `if` · `Igualdad ==`

Crea un campo `vidas`. Usa `if` para mostrar `Sin vidas` solo cuando valga 0. Ejecuta una vez con 0 y otra con 3.

<details>
<summary>Pista</summary>

escribe en `Start()` la estructura `if (vidas == 0) { /* escribe aquí el mensaje */ }`. La condición va entre paréntesis y las instrucciones dentro de llaves; `==` compara y `=` asigna.

</details>

**Comprueba:** con 3 vidas no aparece el mensaje.

<a name="u042"></a>

### U042. Elegir entre dos respuestas

**Etiquetas:** `Condicionales` · `if` · `else`

Amplía [U041](#u041) con `else` para mostrar `Puedes jugar` cuando queden vidas. Limita las pruebas a valores de 0 en adelante.

<details>
<summary>Pista</summary>

coloca `else { /* segundo mensaje */ }` justo después de la llave que cierra el `if`, sin añadir otra condición. Se ejecuta cuando la condición del `if` es falsa.

</details>

**Comprueba:** en cada ejecución aparece exactamente una respuesta.

<a name="u043"></a>

### U043. Comparar cantidades

**Etiquetas:** `Condicionales` · `Comparaciones` · `Operador >=`

Usa `monedas` y `precio` para mostrar si puedes comprar un objeto. Considera que tener exactamente su precio también permite comprarlo.

<details>
<summary>Pista</summary>

compara con `>=`.

</details>

**Comprueba:** con precio 5, las cantidades 4, 5 y 6 producen las respuestas esperadas.

<a name="u044"></a>

### U044. Exigir dos condiciones

**Etiquetas:** `bool` · `Operadores lógicos` · `Operador &&`

Declara `tieneLlave` y `puertaDesbloqueada`. Muestra `Puedes pasar` únicamente si ambas son verdaderas. Prueba las cuatro combinaciones posibles.

<details>
<summary>Pista</summary>

`&&` exige que se cumplan las dos condiciones.

</details>

**Comprueba:** solo una de las cuatro combinaciones permite pasar.

<a name="u045"></a>

### U045. Aceptar una alternativa

**Etiquetas:** `bool` · `Operadores lógicos` · `Operador ||`

Declara `tieneEntrada` y `estaEnLaLista`. Permite entrar si se cumple al menos una condición. Prueba también el caso en que se cumplen ambas.

<details>
<summary>Pista</summary>

`||` significa que basta una de las condiciones.

</details>

**Comprueba:** solo se deniega la entrada cuando ambas son falsas.

<a name="u046"></a>

### U046. Cambiar un estado al contrario

**Etiquetas:** `bool` · `Negación !` · `Estados`

Declara `luzEncendida`, muestra su valor y cámbialo al contrario con `!`. Vuelve a mostrarlo. Repite partiendo del valor opuesto.

<details>
<summary>Pista</summary>

negar un booleano intercambia verdadero y falso.

</details>

**Comprueba:** el segundo mensaje siempre es distinto del primero.

<a name="u047"></a>

### U047. Clasificar con varios casos

**Etiquetas:** `Condicionales` · `else if` · `Intervalos`

Clasifica una puntuación como baja si es menor que 5, media entre 5 y 9, y alta a partir de 10. Utiliza `if`, `else if` y `else`.

<details>
<summary>Pista</summary>

revisa las condiciones en orden.

</details>

**Comprueba:** prueba 4, 5, 9 y 10; aparece una sola categoría por valor.

<a name="u048"></a>

### U048. Elegir con switch

**Etiquetas:** `switch` · `case` · `default` · `break`

Crea un campo de texto `accion`. Usa `switch` para mostrar respuestas diferentes a `jugar`, `ayuda` y `salir`, y una respuesta por defecto para cualquier otra palabra.

<details>
<summary>Pista</summary>

empieza en `Start()` con este modelo y añade los casos de `ayuda` y `salir`. Todos los casos solo escriben mensajes; todavía no abren ni cierran pantallas.

```csharp
switch (accion)
{
    case "jugar":
        Debug.Log("Has elegido jugar");
        break;
    default:
        Debug.Log("Acción desconocida");
        break;
}
```

</details>

**Comprueba:** cada palabra conocida muestra su respuesta y una palabra inventada muestra la respuesta por defecto.

**Referencia:** [Condiciones y selección con `if` y `switch` en C#](https://learn.microsoft.com/es-es/dotnet/csharp/language-reference/statements/selection-statements).


<a name="u049"></a>

### U049. Una calculadora pequeña

**Etiquetas:** `switch` · `Operaciones aritméticas` · `Validación de datos`

Crea dos campos `float` y un campo `string` llamado `operacion`, editables en Inspector. En el texto escribe uno de estos símbolos: `+`, `-`, `*`, `/` o `%`. Usa `switch` para realizar la operación y muestra una vez el cálculo o el error detectado.

<details>
<summary>Pista</summary>

rechaza divisor cero en `/` y `%`, y símbolos desconocidos.

</details>

**Comprueba:** prueba las cinco operaciones y ambos errores.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva el script de la calculadora con sus comprobaciones de operaciones y divisores. Así podrás añadir operandos y operaciones aleatorios en [U053](#u053) sin volver a escribir la calculadora. **Retómalo en:** [U053](#u053).

<a name="u050"></a>

### U050. Comprobar un intervalo

**Etiquetas:** `Intervalos` · `Comparaciones` · `Operador &&`

Crea un valor `energia` y muestra si está dentro del intervalo permitido, de 0 a 100 incluidos. Si está fuera, muestra un mensaje que explique el problema.

<details>
<summary>Pista</summary>

combina comparaciones con `&&`.

</details>

**Comprueba:** prueba -1, 0, 50, 100 y 101 sin dejar casos sin respuesta.

[Volver al índice](#indice)

<a name="bloque-06"></a>

## 6. Azar y repeticiones (U051-U060)

Base: condiciones y `Update()`. Un bucle repite instrucciones dentro de una misma llamada; no equivale a esperar al siguiente fotograma.

<a name="u051"></a>

### U051. Un decimal aleatorio por fotograma

**Etiquetas:** `Random.Range` · `float` · `Update`

Genera en `Update()` un número decimal entre -10 y 10 y escríbelo en Console. Ejecuta solo unos segundos y desactiva después el mensaje para evitar llenar la consola.

<details>
<summary>Pista</summary>

`Random.Range(-10f, 10f)` utiliza límites `float` y puede incluir ambos extremos. Es distinto de pasar dos límites enteros.

</details>

**Comprueba:** aparecen valores con decimales y ninguno queda fuera del intervalo.

<a name="u052"></a>

### U052. Tirar un dado

**Etiquetas:** `Random.Range` · `int` · `Límites de intervalos`

Genera en `Start()` un entero entre 1 y 6. Reinicia varias veces la escena. Compara los límites utilizados con los del ejercicio anterior.

<details>
<summary>Pista</summary>

con enteros, el límite superior de `Random.Range` queda excluido.

</details>

**Comprueba:** el dado nunca muestra 0 ni 7.

<a name="u053"></a>

### U053. Calcular una operación al azar

**Etiquetas:** `Random.Range` · `switch` · `Operaciones aritméticas` · `Validación de datos`

Reutiliza [U049](#u049): genera dos números decimales y elige al azar una de sus cinco operaciones. Muestra una vez los operandos, el símbolo y el resultado. Conserva la comprobación de división o resto entre cero.

<details>
<summary>Pista</summary>

un entero de 0 a 4 puede representar la operación.

</details>

**Comprueba:** puedes verificar a mano el cálculo mostrado.

<a name="u054"></a>

### U054. Piedra, papel o tijera

**Etiquetas:** `Random.Range` · `Condicionales` · `Validación de datos` · `Pruebas de casos`

Elige desde Inspector 1 para piedra, 2 para papel o 3 para tijera. Genera la elección del ordenador y muestra ambas jugadas y el resultado: victoria, derrota o empate.

<details>
<summary>Pista</summary>

comprueba primero el empate y rechaza elecciones fuera de 1-3.

</details>

**Comprueba:** verifica las nueve combinaciones posibles fijando temporalmente la jugada rival.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva el script con las reglas y la resolución de una ronda de piedra, papel o tijera. Así podrás reutilizar las reglas al simular rondas hasta alcanzar cinco victorias en [U059](#u059). **Retómalo en:** [U059](#u059).

<a name="u055"></a>

### U055. Contar del 1 al 100

**Etiquetas:** `Bucles` · `for` · `Contadores`

Escribe un bucle `for` en `Start()` que muestre todos los enteros del 1 al 100. Identifica su valor inicial, condición de continuación e incremento.

<details>
<summary>Pista</summary>

utiliza `for (int i = 1; i <= 100; i++) { /* muestra i */ }` dentro de `Start()`. La primera parte se ejecuta una vez, la segunda decide si continúa y la tercera actualiza el contador tras cada vuelta.

</details>

**Comprueba:** hay 100 mensajes, empezando por 1 y terminando en 100.

**Referencia:** [Bucles `for`, `while` y `foreach` en C#](https://learn.microsoft.com/es-es/dotnet/csharp/language-reference/statements/iteration-statements).


<a name="u056"></a>

### U056. Una tabla de multiplicar

**Etiquetas:** `for` · `Multiplicación` · `Texto con variables`

Recibe un número decimal desde Inspector y muestra su tabla del 1 al 10. Reutiliza el `for` de [U055](#u055) y muestra en cada línea los factores y el producto.

<details>
<summary>Pista</summary>

el contador actúa como segundo factor.

</details>

**Comprueba:** para 2.5, la primera línea termina en 2.5 y la última en 25.

<a name="u057"></a>

### U057. Cien números con while

**Etiquetas:** `while` · `Random.Range` · `Contadores` · `Terminación de bucles`

Usa un bucle `while` para mostrar exactamente 100 números aleatorios entre -10 y 10. Lleva la cuenta de cuántos has generado mediante una variable independiente.

<details>
<summary>Pista</summary>

en `Start()`, declara `int generados = 0;` antes de `while (generados < 100) { /* genera un número y aumenta generados */ }`. Añade `generados++;` dentro de las llaves: sin ese avance, el editor podría quedarse atrapado en el bucle.

</details>

**Comprueba:** el bucle termina tras 100 números y Unity sigue respondiendo.

<a name="u058"></a>

### U058. Todas las tablas

**Etiquetas:** `Bucles anidados` · `for` · `Contadores`

Usa dos bucles `for` anidados para mostrar las tablas del 1 al 10, con multiplicadores del 1 al 10. Identifica qué contador elige la tabla y cuál el multiplicador.

<details>
<summary>Pista</summary>

el bucle interior se completa por cada vuelta del exterior.

</details>

**Comprueba:** aparecen 100 operaciones, desde 1 × 1 hasta 10 × 10.

<a name="u059"></a>

### U059. El primero que consigue cinco victorias

**Etiquetas:** `Bucles` · `Condicionales` · `Contadores` · `Random.Range` · `Terminación de bucles`

Reutiliza las reglas de [U054](#u054) para enfrentar a dos jugadores automáticos. Repite rondas aleatorias hasta que uno logre cinco victorias; los empates no suman. Muestra cada ronda, el marcador y el ganador final.

<details>
<summary>Pista</summary>

controla victorias, no cinco rondas. Añade un límite de seguridad de 1000 intentos que informe de interrupción.

</details>

**Comprueba:** solo anuncias ganador si alcanza cinco victorias.

<a name="u060"></a>

### U060. Acumular dentro de un bucle

**Etiquetas:** `Bucles` · `Acumuladores` · `Operador +=`

Calcula la suma de los enteros del 1 al 10 con un bucle. Muestra cómo cambia el acumulador y después el total final. Reinicia la escena para comprobar el valor inicial.

<details>
<summary>Pista</summary>

inicializa la suma fuera del bucle. `suma += i;` equivale a `suma = suma + i;`: añade el valor actual del contador al acumulador.

</details>

**Comprueba:** el total final es 55 en cada ejecución.

[Volver al índice](#indice)

<a name="bloque-07"></a>

## 7. Métodos, referencias y arrays (U061-U070)

Base: variables, condiciones y bucles. Ahora organizarás instrucciones y guardarás referencias a objetos de la escena.

<a name="u061"></a>

### U061. Dar nombre a un grupo de instrucciones

**Etiquetas:** `Métodos` · `Llamadas` · `void`

Crea un método `MostrarBienvenida()` que escriba dos mensajes. Llámalo desde `Start()`. Después elimina temporalmente la llamada, manteniendo la definición del método.

<details>
<summary>Pista</summary>

define `void MostrarBienvenida() { /* dos mensajes */ }` dentro de la clase y fuera de `Start()`. Para llamarlo, escribe `MostrarBienvenida();` dentro de `Start()`. `void` indica que no devuelve un resultado.

</details>

**Comprueba:** sin llamada no aparecen sus mensajes.

<a name="u062"></a>

### U062. Pasar un dato a un método

**Etiquetas:** `Métodos` · `Parámetros` · `Reutilización de código`

Crea `Saludar(string nombre)` y úsalo desde `Start()` para saludar a dos nombres distintos. Utiliza el parámetro dentro del mensaje, en lugar de escribir un nombre fijo.

<details>
<summary>Pista</summary>

la definición empieza con `void Saludar(string nombre)`; una llamada como `Saludar("Ana");` entrega el texto al parámetro `nombre`.

</details>

**Comprueba:** el mismo método produce dos saludos distintos.

<a name="u063"></a>

### U063. Devolver un resultado

**Etiquetas:** `Métodos` · `Parámetros` · `return` · `float`

Convierte la suma de [U031](#u031) en un método que reciba dos `float` y devuelva otro `float`. Guarda el valor devuelto en una variable y muéstralo desde `Start()`.

<details>
<summary>Pista</summary>

define `float Sumar(float a, float b)` y escribe `return a + b;` en su cuerpo. Una llamada como `float total = Sumar(2f, 3f);` recibe el resultado.

</details>

**Comprueba:** el método calcula y la instrucción que lo llama decide cómo mostrarlo.

<a name="u064"></a>

### U064. Referirse a otro objeto

**Etiquetas:** `Referencias` · `Transform` · `Inspector`

Crea un campo `Transform` llamado `objetivo` y asigna un sprite arrastrándolo desde Hierarchy al Inspector. Muestra su posición X/Y al iniciar. Cambia la referencia por otro sprite.

<details>
<summary>Pista</summary>

declara `public Transform objetivo;` fuera de los métodos. Una referencia permite acceder a un objeto que ya existe: `objetivo.position.x` y `objetivo.position.y` leen sus coordenadas.

</details>

**Comprueba:** el mensaje corresponde al objeto asignado, aunque renombres el objeto.

<a name="u065"></a>

### U065. Detectar una referencia sin asignar

**Etiquetas:** `Referencias` · `null` · `Validación de datos`

Vacía el campo de [U064](#u064). Añade una condición que compruebe si `objetivo` es `null` antes de acceder a su posición. En ese caso, escribe un mensaje que explique qué falta.

<details>
<summary>Pista</summary>

`null` indica ausencia de referencia.

</details>

**Comprueba:** tanto el campo vacío como el asignado se gestionan sin errores rojos.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el script que comprueba una referencia Transform antes de utilizarla. Así podrás tomar como base la referencia al objetivo del seguidor de [U091](#u091) y adaptar la comprobación a componentes que necesiten otro objeto. **Retómalo en:** [U091](#u091).

<a name="u066"></a>

### U066. Acceder al color desde código

**Etiquetas:** `GetComponent` · `SpriteRenderer` · `Color` · `Referencias`

Obtén el `SpriteRenderer` del mismo objeto al iniciar usando `GetComponent<SpriteRenderer>()`. Guarda la referencia y cambia su color a uno elegido en un campo `Color` del Inspector.

<details>
<summary>Pista</summary>

en `Start()`, `SpriteRenderer dibujo = GetComponent<SpriteRenderer>();` obtiene el componente del mismo objeto; `dibujo.color = colorElegido;` aplica un campo declarado como `public Color colorElegido = Color.white;`.

</details>

**Comprueba:** cambiar el campo de color cambia el resultado de la siguiente ejecución.

<a name="u067"></a>

### U067. Guardar varios números juntos

**Etiquetas:** `Arrays` · `Índices` · `Length` · `Validación de datos`

Declara un array de enteros con tres puntuaciones editables en Inspector. Muestra su tamaño y el primer elemento. Antes de leerlo, comprueba que contiene al menos un valor.

<details>
<summary>Pista</summary>

empieza con `public int[] puntuaciones = { 10, 20, 30 };`. `puntuaciones.Length` indica cuántos elementos hay y `puntuaciones[0]` accede al primero. Lee ese elemento solo cuando `Length > 0`; para la prueba vacía, pon el tamaño a 0 en Inspector.

</details>

**Comprueba:** un array vacío no produce errores.

<a name="u068"></a>

### U068. Recorrer varios sprites

**Etiquetas:** `Arrays` · `foreach` · `SpriteRenderer` · `null`

Guarda tres referencias `SpriteRenderer` en un array del Inspector. Recorre el array con `foreach` y cambia todos los colores al iniciar. Omite las posiciones que no tengan referencia.

<details>
<summary>Pista</summary>

declara `public SpriteRenderer[] sprites = new SpriteRenderer[3];` y asigna sus casillas en Inspector. `foreach (SpriteRenderer sprite in sprites) { /* comprueba y cambia el color */ }` visita cada elemento; usa `if (sprite != null)` antes de acceder a `sprite.color`; `!=` significa distinto de.

</details>

**Comprueba:** los tres sprites cambian y un hueco vacío no interrumpe el recorrido.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script que recorre referencias SpriteRenderer y cambia sus colores, omitiendo las vacías. Así podrás aplicar un color a un grupo de sprites, por ejemplo al activar un conjunto o destacar varios objetos.

<a name="u069"></a>

### U069. Elegir un elemento por su índice

**Etiquetas:** `Arrays` · `Índices` · `Validación de datos`

Añade al array de [U067](#u067) un campo `indiceElegido`. Muestra la puntuación de esa posición únicamente si el índice es válido. En caso contrario, explica el problema en Console.

<details>
<summary>Pista</summary>

el índice debe ser mayor o igual que 0 y menor que `Length`.

</details>

**Comprueba:** prueba -1, 0 y el propio tamaño del array.

<a name="u070"></a>

### U070. Elegir un color de una paleta

**Etiquetas:** `Arrays` · `Random.Range` · `Color` · `SpriteRenderer`

Crea un array de tres colores. Obtén un índice aleatorio válido y aplica el color elegido a un sprite al iniciar. Comprueba antes que la paleta no esté vacía.

<details>
<summary>Pista</summary>

combina [U052](#u052), [U066](#u066) y [U069](#u069).

</details>

**Comprueba:** el sprite solo utiliza colores de la paleta, aunque a veces repita uno.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script de elección aleatoria de color y su paleta configurada. Así podrás dar variaciones de color a objetos manteniendo una paleta común y controlando el caso de una paleta vacía.

[Volver al índice](#indice)

<a name="bloque-08"></a>

## 8. Tiempo y movimiento automático (U071-U080)

Base: `Update()`, números, condiciones y `Vector2`. Usa sprites sin cuerpos físicos en este bloque.

<a name="u071"></a>

### U071. Contar fotogramas

**Etiquetas:** `Update` · `Fotogramas` · `Contadores` · `Condicionales`

Incrementa un contador en `Update()` y muestra un mensaje al llegar a 100. Déjalo seguir aumentando sin repetir ese mensaje. Compara lo que cuenta con los segundos de un reloj.

<details>
<summary>Pista</summary>

un fotograma es una actualización de la imagen, no un segundo.

</details>

**Comprueba:** no interpretas el contador como tiempo transcurrido.

<a name="u072"></a>

### U072. Observar deltaTime

**Etiquetas:** `Tiempo` · `Time.deltaTime` · `Fotogramas` · `Console`

Escribe `Time.deltaTime` en Console en cada fotograma durante unos segundos. Detén Play y compara varios valores. Después desactiva el mensaje repetido.

<details>
<summary>Pista</summary>

expresa en segundos el tiempo entre fotogramas.

</details>

**Comprueba:** sus valores suelen ser fracciones pequeñas, no un contador creciente.

<a name="u073"></a>

### U073. Esperar tres segundos sin bloquear

**Etiquetas:** `Temporizadores` · `Time.deltaTime` · `bool` · `Condicionales`

Acumula `Time.deltaTime` en un `float`. Al alcanzar tres segundos, muestra `Tiempo cumplido` una sola vez usando un booleano para recordar que ya lo has anunciado.

<details>
<summary>Pista</summary>

comprueba `>= 3`, no igualdad exacta.

</details>

**Comprueba:** Unity sigue respondiendo durante la espera y solo aparece un aviso.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el script del temporizador con su aviso de una sola ejecución. Así podrás adaptarlo a esperas, generación periódica, inactividad o cuentas atrás. **Retómalo en:** [U107](#u107), [U145](#u145), [U146](#u146), [U184](#u184), [U192](#u192).

<a name="u074"></a>

### U074. Mover hacia abajo y a la derecha

**Etiquetas:** `Movimiento` · `Transform` · `Coordenadas X/Y` · `Update`

En cada `Update()`, incrementa ligeramente X y reduce ligeramente Y de un sprite. Conserva Z en 0. Observa cómo cambia su posición durante Play.

<details>
<summary>Pista</summary>

`Vector3 posicion = transform.position;` obtiene una copia con X, Y y Z. Modifica `posicion.x` y `posicion.y`, por ejemplo en pasos de `0.01f`, y termina con `transform.position = posicion;`.

</details>

**Comprueba:** se desplaza hacia la esquina inferior derecha; aún depende de los fotogramas.

<a name="u075"></a>

### U075. Ajustar el paso desde Inspector

**Etiquetas:** `Movimiento` · `Inspector` · `Direcciones` · `Fotogramas`

Haz que el sprite se mueva hacia abajo y a la izquierda. Expón un valor para regular cuánto avanza en cada fotograma y compara dos valores distintos.

<details>
<summary>Pista</summary>

multiplica la dirección por el paso configurable.

</details>

**Comprueba:** un valor mayor lo desplaza más deprisa; sigue siendo un paso por fotograma.

<a name="u076"></a>

### U076. Medir la velocidad por segundo

**Etiquetas:** `Movimiento` · `Time.deltaTime` · `Velocidad` · `Normalización`

Mueve el sprite hacia arriba y a la izquierda con velocidad configurable. Multiplica el desplazamiento por `Time.deltaTime`. Normaliza la dirección con `.normalized` para que su longitud sea 1.

<details>
<summary>Pista</summary>

el desplazamiento es dirección × velocidad × tiempo. Trabaja con una copia de la posición en `Vector2` y asígnala de nuevo al Transform; Z quedará en 0.

</details>

**Comprueba:** en dos segundos recorre aproximadamente el doble que en uno.

<a name="u077"></a>

### U077. Elegir la dirección desde Inspector

**Etiquetas:** `Movimiento` · `Vector2` · `Inspector` · `Normalización`

Amplía [U076](#u076) con un campo `Vector2` para elegir dirección. Prueba derecha, arriba y diagonal. Si la dirección vale cero, el sprite debe permanecer quieto.

<details>
<summary>Pista</summary>

usa la dirección normalizada al calcular el desplazamiento.

</details>

**Comprueba:** cambiar su orientación no cambia la velocidad total elegida.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el script de movimiento visual con dirección y velocidad configurables. Así podrás mover elementos sin física con la misma rapidez en cualquier dirección. **Retómalo en:** [U083](#u083), [U085](#u085).

<a name="u078"></a>

### U078. Reaparecer al otro lado

**Etiquetas:** `Movimiento` · `Coordenadas X/Y` · `Condicionales` · `Tiempo`

Haz que un sprite avance hacia la derecha. Cuando su X supere 5, colócalo en X=-5 conservando Y. Mantén el movimiento basado en tiempo.

<details>
<summary>Pista</summary>

combina movimiento y una condición.

</details>

**Comprueba:** puedes observar tres vueltas completas sin que el sprite desaparezca definitivamente.

<a name="u079"></a>

### U079. Girar a velocidad constante

**Etiquetas:** `Rotación Z` · `Transform.Rotate` · `Time.deltaTime` · `Inspector`

Haz que un sprite gire dentro del plano a una velocidad configurable en grados por segundo. Modifica únicamente la rotación Z y utiliza `Time.deltaTime`.

<details>
<summary>Pista</summary>

`Transform.Rotate` permite aplicar un pequeño giro.

</details>

**Comprueba:** a 90 grados por segundo tarda unos cuatro segundos en completar una vuelta.

<a name="u080"></a>

### U080. Crecer y detenerse

**Etiquetas:** `Escala` · `Transform` · `Límites` · `Mathf.Min`

Aumenta progresivamente Scale X e Y de un sprite desde 1 hasta 2 usando una velocidad de crecimiento por segundo y `Time.deltaTime`. Detén el crecimiento al alcanzar el tamaño máximo y conserva su posición.

<details>
<summary>Pista</summary>

guarda una escala común y limita el resultado con `Mathf.Min`.

</details>

**Comprueba:** el sprite crece de forma uniforme y nunca supera el doble.

[Volver al índice](#indice)

<a name="bloque-09"></a>

## 9. Teclado y ratón (U081-U090)

Base: movimiento sin física. Se usará Input System en todas las actividades siguientes; da el foco a la ventana Game para probar controles.

<a name="u081"></a>

### U081. Preparar la entrada de teclado

**Etiquetas:** `Input System` · `Package Manager` · `Configuración` · `Teclado`

Comprueba en Package Manager si Input System está instalado; instálalo si falta y activa su sistema de entrada cuando Unity lo solicite. Si quieres mantener los cambios de la sesión, guarda antes de reiniciar el editor. Añade `using UnityEngine.InputSystem;` a un script nuevo. Mantén Update Mode en `Process Events In Dynamic Update`.

<details>
<summary>Pista</summary>

Active Input Handling está en los ajustes de Player; Update Mode, en Project Settings > Input System Package.

</details>

**Comprueba:** el script reconoce `Keyboard` sin errores de compilación.

**Referencia:** [Instalación y activación de Input System](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.17/manual/Installation.html). Utiliza la versión del paquete compatible que ofrezca Package Manager.

<a name="u082"></a>

### U082. Detectar una pulsación

**Etiquetas:** `Input System` · `Teclado` · `Pulsaciones` · `null`

Muestra un mensaje al pulsar espacio. Comprueba la tecla dentro de `Update()` y evita acceder a un teclado inexistente comprobando `Keyboard.current != null`.

<details>
<summary>Pista</summary>

consulta `Keyboard.current.spaceKey.wasPressedThisFrame` dentro de la condición que comprueba que existe el teclado.

</details>

**Comprueba:** mantener espacio pulsado produce un solo mensaje hasta que lo sueltes y vuelvas a pulsar.

<a name="u083"></a>

### U083. Mantener una tecla pulsada

**Etiquetas:** `Teclado` · `Teclas mantenidas` · `Movimiento` · `Time.deltaTime`

Haz que un sprite se mueva hacia la derecha mientras mantienes D. Debe detenerse al soltarla y conservar la velocidad por segundo de [U076](#u076).

<details>
<summary>Pista</summary>

`dKey.isPressed` indica si la tecla sigue presionada.

</details>

**Comprueba:** una pulsación larga desplaza más que una breve.

<a name="u084"></a>

### U084. Detectar el ratón

**Etiquetas:** `Input System` · `Ratón` · `Pulsaciones` · `null`

Muestra mensajes distintos al pulsar los botones izquierdo y derecho del ratón. Comprueba primero que `Mouse.current` no sea `null`.

<details>
<summary>Pista</summary>

consulta `leftButton` y `rightButton` con `wasPressedThisFrame`.

</details>

**Comprueba:** cada clic genera un mensaje del botón correcto.

<a name="u085"></a>

### U085. Movimiento con WASD y position

**Etiquetas:** `Teclado` · `Movimiento` · `Vector2` · `Transform` · `Time.deltaTime`

Construye una dirección `Vector2` a partir de W, A, S y D, empezando de cero en cada `Update()`. Mueve un sprite con `transform.position`, velocidad configurable y `Time.deltaTime`.

<details>
<summary>Pista</summary>

las teclas opuestas deben compensarse.

</details>

**Comprueba:** el sprite se mueve en las cuatro direcciones y se detiene al soltar las teclas.

<a name="u086"></a>

### U086. Movimiento con Translate

**Etiquetas:** `Teclado` · `Movimiento` · `Transform.Translate` · `Coordenadas globales`

Copia [U085](#u085) y sustituye la modificación de posición por `transform.Translate`. Conserva WASD, velocidad configurable y tiempo entre fotogramas. Usa el espacio del mundo para mantener los controles aunque gires el sprite.

<details>
<summary>Pista</summary>

el parámetro `Space.World` evita que la orientación cambie la dirección.

</details>

**Comprueba:** W sigue subiendo tras girar la imagen.

<a name="u087"></a>

### U087. Igualar la velocidad diagonal

**Etiquetas:** `Movimiento` · `Normalización` · `Vector2` · `Velocidad`

Compara el recorrido de [U085](#u085) al mantener D y al mantener W+D durante el mismo tiempo. Normaliza la dirección antes de mover para evitar que las diagonales sean más rápidas.

<details>
<summary>Pista</summary>

conserva la dirección cero cuando no hay teclas.

</details>

**Comprueba:** la distancia total recorrida es aproximadamente igual en ambos casos.

<a name="u088"></a>

### U088. Correr mientras mantienes Shift

**Etiquetas:** `Teclado` · `Teclas mantenidas` · `Velocidad` · `Condicionales`

Amplía [U087](#u087) con una velocidad normal y otra de carrera, ambas editables. Usa la segunda únicamente mientras mantengas Shift izquierdo; al soltarlo debe recuperarse la primera.

<details>
<summary>Pista</summary>

consulta `leftShiftKey.isPressed` y elige una velocidad antes de mover.

</details>

**Comprueba:** pulsar Shift sin dirección no desplaza al personaje.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva la versión del movimiento WASD con diagonales normalizadas y carrera. Así podrás preparar escenas de prueba o personajes sin física; conservar esta versión evita guardar por separado cada paso de [U085](#u085) a [U087](#u087). **Retómalo en:** [U091](#u091), [U098](#u098), [U159](#u159).

<a name="u089"></a>

### U089. No salir de un rectángulo

**Etiquetas:** `Movimiento` · `Coordenadas X/Y` · `Límites` · `Mathf.Clamp`

Limita el movimiento del centro del sprite a X entre -5 y 5 e Y entre -3 y 3. Calcula la nueva posición y ajusta sus componentes antes de asignarla.

<details>
<summary>Pista</summary>

`Mathf.Clamp` mantiene un valor entre dos límites.

</details>

**Comprueba:** sostener una tecla contra el borde no permite sobrepasarlo.

<a name="u090"></a>

### U090. Voltear un sprite

**Etiquetas:** `SpriteRenderer` · `Volteo` · `Teclado` · `Ratón` · `bool`

Usa una imagen asimétrica. Al pulsar espacio, invierte su orientación horizontal; al hacer clic derecho, invierte la vertical. Cada pulsación debe alternar el valor anterior.

<details>
<summary>Pista</summary>

combina `SpriteRenderer.flipX`, `flipY` y `!`.

</details>

**Comprueba:** dos pulsaciones del mismo control restauran la orientación inicial.

[Volver al índice](#indice)

<a name="bloque-10"></a>

## 10. Seguimiento y cámara (U091-U100)

Base: referencias de [U064](#u064)-[U065](#u065) y jugador WASD de [U087](#u087) o su versión ampliada de [U088](#u088). Usa sprites sin física; la cámara permanece ortográfica.

<a name="u091"></a>

### U091. Seguir de forma instantánea

**Etiquetas:** `Seguimiento` · `Referencias` · `Coordenadas X/Y` · `Transform` · `LateUpdate`

Añade un segundo sprite y asígnale el jugador como objetivo. Copia su posición X/Y en `LateUpdate()`, que se ejecuta después del movimiento del jugador en `Update()`. Usa tamaños o transparencias diferentes para distinguir ambos aunque estén superpuestos.

<details>
<summary>Pista</summary>

comprueba que la referencia al objetivo está asignada.

</details>

**Comprueba:** ambos ocupan siempre las mismas coordenadas del plano.

<a name="u092"></a>

### U092. Seguir con una separación

**Etiquetas:** `Seguimiento` · `Vector2` · `Desplazamiento relativo` · `Inspector`

Amplía [U091](#u091) con un desplazamiento `Vector2` editable desde Inspector. El seguidor debe ocupar la posición del objetivo más ese desplazamiento.

<details>
<summary>Pista</summary>

prueba una separación de X=2 e Y=1.

</details>

**Comprueba:** la distancia relativa se mantiene al mover al jugador en cualquier dirección.

<a name="u093"></a>

### U093. Acercarse con velocidad limitada

**Etiquetas:** `Seguimiento` · `Vector2.MoveTowards` · `Velocidad` · `Time.deltaTime`

Haz que un sprite alcance al jugador sin superar una velocidad configurable por segundo. Cuando llegue, debe detenerse sin atravesar ni sobrepasar su posición.

<details>
<summary>Pista</summary>

utiliza `Vector2.MoveTowards` con velocidad multiplicada por `Time.deltaTime`.

</details>

**Comprueba:** un objetivo lejano no provoca un salto instantáneo.

<a name="u094"></a>

### U094. Seguir con suavidad

**Etiquetas:** `Seguimiento` · `Vector2.SmoothDamp` · `Suavizado` · `Parámetros por referencia`

Haz que un sprite siga al jugador con aceleración y frenado suaves. Expón un tiempo de suavizado y compara valores pequeños y grandes al arrancar, cambiar de dirección y detenerte.

<details>
<summary>Pista</summary>

declara una variable `Vector2` de velocidad fuera de los métodos y pásala con `ref` a `Vector2.SmoothDamp`: el método la modifica y necesita conservarla entre fotogramas.

</details>

**Comprueba:** el seguidor se acerca gradualmente al objetivo al detenerlo.

**Referencia:** [Vector2.SmoothDamp](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Vector2.SmoothDamp.html).

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script de seguimiento suave y los valores utilizados para probarlo. Así podrás adaptarlo a acompañantes visuales o a una cámara 2D, conservando la Z de la cámara si se utiliza con ella.

<a name="u095"></a>

### U095. Seguir solo en horizontal

**Etiquetas:** `Seguimiento` · `Coordenadas X/Y` · `Referencias` · `Movimiento horizontal`

Copia [U091](#u091) y haz que el seguidor copie únicamente X. Guarda su propia altura inicial y consérvala aunque el jugador suba o baje.

<details>
<summary>Pista</summary>

combina la X del objetivo con la Y fija del seguidor.

</details>

**Comprueba:** un movimiento exclusivamente vertical del jugador no lo desplaza.

<a name="u096"></a>

### U096. Seguir únicamente desde cerca

**Etiquetas:** `Seguimiento` · `Vector2.Distance` · `Distancias` · `Condicionales`

Amplía [U093](#u093) con una distancia de activación editable, inicialmente de 5 unidades. El seguidor se mueve solo cuando la distancia entre ambos es menor que ese valor; cuando sea igual o mayor, se queda quieto.

<details>
<summary>Pista</summary>

usa `Vector2.Distance` antes de calcular el desplazamiento.

</details>

**Comprueba:** prueba distancias menores, iguales y mayores que 5.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el seguidor sin física con velocidad y distancia de activación configurables. Así podrás combinar persecución y patrulla o preparar un prototipo sencillo de enemigo. **Retómalo en:** [U167](#u167).

<a name="u097"></a>

### U097. Una cámara que sigue al jugador

**Etiquetas:** `Cámara ortográfica` · `Seguimiento` · `LateUpdate` · `Coordenadas X/Y`

Copia X/Y del jugador a la cámara en `LateUpdate()`, conservando la Z inicial de la cámara. Coloca varios sprites fijos para reconocer el desplazamiento del escenario.

<details>
<summary>Pista</summary>

`LateUpdate()` permite seguir después del movimiento hecho en `Update()`.

</details>

**Comprueba:** el jugador permanece centrado y la cámara conserva su profundidad inicial.

<a name="u098"></a>

### U098. Limitar la velocidad de la cámara

**Etiquetas:** `Cámara ortográfica` · `Seguimiento` · `Vector2.MoveTowards` · `Velocidad` · `LateUpdate`

Reutiliza el jugador WASD con velocidad configurable e independiente de los fotogramas. Cambia [U097](#u097) para que la cámara lo alcance con una velocidad máxima configurable, en lugar de copiar instantáneamente su posición.

<details>
<summary>Pista</summary>

aplica `Vector2.MoveTowards` a X/Y en `LateUpdate()` con un paso máximo de velocidad × `Time.deltaTime`, y conserva Z.

</details>

**Comprueba:** una separación grande tarda en recuperarse.

<a name="u099"></a>

### U099. Poner límites a la cámara

**Etiquetas:** `Cámara ortográfica` · `Coordenadas X/Y` · `Límites` · `Mathf.Clamp`

Amplía [U098](#u098) para limitar el centro de la cámara a un rectángulo configurable. Prueba un escenario mayor que ese rectángulo y mueve al jugador hasta los extremos.

<details>
<summary>Pista</summary>

limita X/Y con `Mathf.Clamp`.

</details>

**Comprueba:** el centro de la cámara no sobrepasa los límites, aunque el jugador siga avanzando.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script final de cámara con seguimiento, velocidad máxima y límites. Así podrás adaptar una cámara a otros escenarios 2D, reajustando sus límites al tamaño del mapa y del encuadre.

<a name="u100"></a>

### U100. Un fondo con tres capas

**Etiquetas:** `Paralaje` · `Cámara ortográfica` · `Orden visual` · `Desplazamiento relativo`

Prepara tres capas de sprites con distintos órdenes visuales. Haz que sigan el desplazamiento X/Y de la cámara con factores diferentes y separaciones configurables para simular paralaje. Actualiza las capas al final del mismo `LateUpdate()` que mueve la cámara, después de calcular su posición.

<details>
<summary>Pista</summary>

conserva posiciones iniciales y aplica una fracción del desplazamiento de cámara.

</details>

**Comprueba:** al desplazarte, las tres capas se mueven a ritmos distintos.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script de paralaje y una escena pequeña con las tres capas configuradas. Así podrás reutilizar la relación entre desplazamiento de cámara y capas de fondo con otras imágenes.

[Volver al índice](#indice)

<a name="bloque-11"></a>

## 11. Primeros experimentos con física 2D (U101-U110)

**Base y prerrequisitos:** Crea una escena de pruebas con cámara ortográfica; reutiliza los conocimientos de componentes, referencias, métodos, coordenadas y aleatoriedad.

<a name="u101"></a>

### U101. Una caja que cae

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Collider2D` · `Gravedad`

Crea una cápsula horizontal con CapsuleCollider2D que funcione como suelo estático. Coloca encima una caja con BoxCollider2D y Rigidbody2D de tipo Dynamic. Sin escribir scripts, ejecuta la escena y observa cómo cae la caja hasta apoyarse en la cápsula.

<details>
<summary>Pista</summary>

Comprueba los componentes de ambos objetos en el Inspector.

</details>

**Comprueba:** La caja cae, queda apoyada y la cápsula permanece inmóvil.

<a name="u102"></a>

### U102. Cambiar la intensidad de la gravedad

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Gravity Scale` · `Gravedad`

Duplica la caja y sitúa ambas a la misma altura, separadas horizontalmente. Asigna distintos valores positivos a Gravity Scale de sus Rigidbody2D. Ejecuta varias veces y después prueba un valor cero para descubrir qué controla esta propiedad.

<details>
<summary>Pista</summary>

Cambia una sola propiedad entre pruebas.

</details>

**Comprueba:** Identificas qué caja acelera más al caer y qué sucede con gravedad cero.

<a name="u103"></a>

### U103. Evitar que una caja vuelque

**Etiquetas:** `Física 2D` · `Rigidbody2D` · `Restricciones` · `Rotación Z`

Añade una pequeña rampa al suelo y deja caer una caja sobre ella. Observa su rotación. Activa Freeze Rotation Z en las restricciones de su Rigidbody2D y repite la prueba para mantener su orientación mientras puede seguir desplazándose.

<details>
<summary>Pista</summary>

En un juego 2D, el giro visible ocurre alrededor de Z.

</details>

**Comprueba:** La caja puede trasladarse sin girar.

<a name="u104"></a>

### U104. Un cuerpo con dos colliders

**Etiquetas:** `Física 2D` · `Collider2D` · `Rigidbody2D` · `Jerarquía`

Añade un círculo como hijo de la caja y desplázalo hacia un lado. Desactiva Freeze Rotation Z si sigue activado desde [U103](#u103). Ponle CircleCollider2D, pero ningún Rigidbody2D. Sin scripts, deja caer el conjunto sobre la cápsula y observa cómo los dos colliders pertenecen al cuerpo físico de la caja.

<details>
<summary>Pista</summary>

El cuerpo del padre reúne también los colliders de sus hijos.

</details>

**Comprueba:** El círculo acompaña la posición y rotación de la caja y también choca con la cápsula.

<a name="u105"></a>

### U105. Una caja que rebota

**Etiquetas:** `Física 2D` · `Physics Material 2D` · `Rebote` · `Collider2D`

Crea un suelo plano estático y un Physics Material 2D para el collider de la caja. Sin scripts, modifica su Bounciness para conseguir un rebote visible al caer sobre el suelo. Compara el resultado con otra caja que tenga un material sin rebote.

<details>
<summary>Pista</summary>

Mantén iguales las alturas iniciales y la gravedad.

</details>

**Comprueba:** El material cambia el rebote sin modificar ningún script.

<a name="u106"></a>

### U106. Superficies con distinto rozamiento

**Etiquetas:** `Física 2D` · `Physics Material 2D` · `Rozamiento` · `Comparación de resultados`

Prepara dos rampas iguales y dos cajas sin rebote. Crea materiales físicos 2D con valores de Friction diferentes y aplícalos a cada pareja de caja y rampa. Observa cómo cambia el deslizamiento usando siempre la misma posición inicial.

<details>
<summary>Pista</summary>

Evita cambiar la inclinación mientras comparas materiales.

</details>

**Comprueba:** Puedes explicar cuál de las dos superficies dificulta más el deslizamiento.

<a name="u107"></a>

### U107. Observar Update y FixedUpdate

**Etiquetas:** `Update` · `FixedUpdate` · `Contadores` · `Temporizadores` · `Física 2D`

Añade dos contadores a un script: uno aumenta en Update y otro en FixedUpdate. Muestra sus valores una vez por segundo en la Console. Observa que los fotogramas dibujados y los pasos de simulación física no tienen por qué coincidir.

<details>
<summary>Pista</summary>

Reutiliza el temporizador ya aprendido para limitar los mensajes.

</details>

**Comprueba:** Distingues la actualización visual de la actualización de la física.

<a name="u108"></a>

### U108. Guardar una referencia al cuerpo físico

**Etiquetas:** `Rigidbody2D` · `GetComponent` · `Referencias` · `Inspector` · `Gravedad`

En el script de la caja, declara una variable de tipo Rigidbody2D. Obtén su componente mediante GetComponent en Start y guarda la referencia. Utilízala para cambiar Gravity Scale a un valor configurable desde el Inspector, sin buscar el componente continuamente.

<details>
<summary>Pista</summary>

`cuerpo = GetComponent<Rigidbody2D>();` obtiene el componente del mismo objeto; en código la propiedad se llama `cuerpo.gravityScale`.

</details>

**Comprueba:** la gravedad de la caja adopta el valor indicado.

<a name="u109"></a>

### U109. Un impulso inicial hacia arriba

**Etiquetas:** `Rigidbody2D` · `AddForce` · `Impulsos` · `Gravedad`

Coloca una caja apoyada sobre un suelo plano. Usando su referencia a Rigidbody2D, aplica una única fuerza hacia arriba en Start mediante AddForce y ForceMode2D.Impulse. Expón la intensidad en el Inspector y compara tres valores sin cambiar la gravedad.

<details>
<summary>Pista</summary>

Un impulso se aplica una vez, no cada fotograma.

</details>

**Comprueba:** La caja sube y después vuelve a caer por gravedad.

<a name="u110"></a>

### U110. Caer desde una posición aleatoria

**Etiquetas:** `Rigidbody2D` · `Random.Range` · `Coordenadas X/Y` · `Colisiones 2D`

Desactiva el impulso de [U109](#u109) para esta prueba. Construye varios obstáculos estáticos bajo la caja. En Start, elige aleatoriamente su coordenada X entre dos límites del Inspector y conserva una altura fija en la parte superior de la pantalla. Asigna esa posición inicial al Rigidbody2D y deja que la gravedad determine el resto del recorrido.

<details>
<summary>Pista</summary>

Reutiliza Random.Range con límites de tipo float.

</details>

**Comprueba:** Al reiniciar, la caja aparece dentro del intervalo y choca con los obstáculos.

[Volver al índice](#indice)

<a name="bloque-12"></a>

## 12. Controlar personajes mediante física 2D (U111-U120)

**Base y prerrequisitos:** Reutiliza la escena física, el Input System, las referencias a Rigidbody2D, los booleanos y la diferencia entre Update y FixedUpdate.

<a name="u111"></a>

### U111. Saltar al pulsar espacio

**Etiquetas:** `Teclado` · `Salto` · `Impulsos` · `bool` · `FixedUpdate`

Sustituye el impulso de `Start()` de [U109](#u109) por un salto al pulsar espacio. Detecta la pulsación en `Update()` y deja una solicitud booleana activada hasta que `FixedUpdate()` la consuma una sola vez para aplicar el impulso. Por ahora permite saltar incluso cuando la caja está en el aire.

<details>
<summary>Pista</summary>

usa `spaceKey.wasPressedThisFrame`, comprobando que existe `Keyboard.current`; pon la solicitud a `false` después de consumirla, no en cada `Update()`.

</details>

**Comprueba:** cada pulsación genera un impulso y mantener la tecla no los repite.

<a name="u112"></a>

### U112. Detectar el contacto con el suelo

**Etiquetas:** `Colisiones 2D` · `Detección del suelo` · `Etiquetas de objetos` · `CompareTag`

Crea la etiqueta `Suelo` desde Tag > Add Tag en el Inspector; vuelve a seleccionar el suelo y asígnasela desde Tag. Utiliza un único suelo plano. Añade OnCollisionEnter2D y OnCollisionExit2D al personaje para escribir mensajes cuando empieza y termina el contacto con ese objeto. Comprueba la etiqueta antes de mostrar cada mensaje.

<details>
<summary>Pista</summary>

Unity llama automáticamente a `void OnCollisionEnter2D(Collision2D colision)` y `void OnCollisionExit2D(Collision2D colision)` al comenzar y terminar el contacto; filtra con `colision.gameObject.CompareTag("Suelo")`.

</details>

**Comprueba:** saltar produce una salida y aterrizar produce una entrada.

**Referencia:** [Detección de colisiones con OnCollisionEnter2D](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/MonoBehaviour.OnCollisionEnter2D.html).


<a name="u113"></a>

### U113. Saltar solamente cuando hay apoyo

**Etiquetas:** `Salto` · `Detección del suelo` · `bool` · `Condicionales`

Añade un booleano que indique si el personaje está tocando el suelo de la prueba anterior. Actualízalo con los eventos de colisión y exige que sea verdadero antes de aceptar un salto. Desactívalo también al aplicar el impulso para evitar solicitudes repetidas.

<details>
<summary>Pista</summary>

mantén un único suelo plano. En `FixedUpdate()`, consume y borra la solicitud aunque no haya apoyo; aplica el impulso solo si lo hay.

</details>

**Comprueba:** pulsar espacio en el aire no añade impulsos ni deja un salto pendiente para el aterrizaje.

<a name="u114"></a>

### U114. Experimentar con Transform y gravedad

**Etiquetas:** `Transform` · `Movimiento` · `Física 2D` · `Colisiones 2D` · `Comparación de resultados`

En una copia de la escena, mueve el personaje con WASD modificando transform.position en Update. Expón la velocidad y utiliza deltaTime; conserva Rigidbody2D, gravedad y colliders. Prueba paredes y suelo para observar las limitaciones de combinar desplazamientos directos con simulación física.

<details>
<summary>Pista</summary>

Registra movimientos bruscos, penetraciones o correcciones que observes.

</details>

**Comprueba:** Explicas por qué esta mezcla puede interferir con la física.

<a name="u115"></a>

### U115. Repetir el experimento en FixedUpdate

**Etiquetas:** `Transform` · `FixedUpdate` · `Time.fixedDeltaTime` · `Física 2D` · `Comparación de resultados`

Copia el experimento anterior y conserva la lectura del teclado en Update. Guarda la dirección y aplica el desplazamiento por transform.position en FixedUpdate usando Time.fixedDeltaTime. Compara el resultado: cambiar de método no convierte esos desplazamientos directos en un controlador físico correcto.

<details>
<summary>Pista</summary>

Usa el tiempo correspondiente al método que aplica el movimiento.

</details>

**Comprueba:** Comparas ambos experimentos sin asumir que FixedUpdate elimina sus limitaciones.

<a name="u116"></a>

### U116. Avanzar con velocidad física horizontal

**Etiquetas:** `Rigidbody2D` · `linearVelocity` · `Movimiento horizontal` · `FixedUpdate` · `Gravedad`

Vuelve a la escena de salto, activa Freeze Rotation Z y sustituye el desplazamiento directo por control de Rigidbody2D.linearVelocity. Lee A y D en Update; en FixedUpdate modifica solamente la componente X según la velocidad del Inspector y conserva la componente Y que produce la física.

<details>
<summary>Pista</summary>

ajusta la velocidad X conservando la Y actual y, después, aplica el impulso de salto pendiente; no reasignes una copia de velocidad anterior al salto.

</details>

**Comprueba:** puedes avanzar, detenerte y saltar sin anular la gravedad.

**Referencia:** [Rigidbody2D.linearVelocity](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D-linearVelocity.html). La velocidad ya se expresa en unidades por segundo.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el personaje con movimiento horizontal, salto y componentes físicos configurados. Así podrás partir de un ejemplo de plataformas para suelo simple; antes de ampliarlo, adapta la detección de apoyo para paredes o varios suelos simultáneos. **Retómalo en:** [U153](#u153), [U193](#u193).

<a name="u117"></a>

### U117. Movimiento físico en vista cenital

**Etiquetas:** `Rigidbody2D` · `linearVelocity` · `Movimiento cenital` · `Normalización` · `Colisiones 2D`

Crea una escena vista desde arriba con paredes de Collider2D y un personaje con un único Collider2D y Rigidbody2D Dynamic, Gravity Scale cero y rotación Z bloqueada. Lee WASD en `Update()` y guarda la dirección normalizada. En `FixedUpdate()`, asigna `linearVelocity` usando esa dirección y una velocidad configurable.

<details>
<summary>Pista</summary>

La velocidad física ya expresa distancia por segundo: no la multipliques por deltaTime.

</details>

**Comprueba:** El personaje conserva su rapidez y choca con paredes.

**Referencia:** [Rigidbody2D.linearVelocity](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D-linearVelocity.html).

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el controlador cenital y el personaje con sus colliders y Rigidbody2D configurados. Así podrás preparar interacciones o prototipos vistos desde arriba con movimiento físico y velocidad diagonal uniforme. **Retómalo en:** [U121](#u121), [U138](#u138), [U142](#u142), [U164](#u164), [U200](#u200).

<a name="u118"></a>

### U118. Un seguidor que camina por el suelo

**Etiquetas:** `Seguimiento` · `Rigidbody2D` · `Movimiento horizontal` · `Distancias` · `Gravedad`

Adapta el seguimiento a un personaje que avanza horizontalmente sobre suelo, con gravedad y colisiones. Asígnale un objetivo y una velocidad horizontal máxima en el Inspector. En `FixedUpdate()`, ajusta solamente su velocidad X según la separación horizontal, para acercarse y detenerse a una pequeña distancia; conserva su velocidad vertical.

<details>
<summary>Pista</summary>

Controla solo la velocidad horizontal y conserva la velocidad vertical que calcula la física.

</details>

**Comprueba:** El seguidor frena cerca y respeta las paredes.

**Referencia:** [Rigidbody2D.linearVelocity](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D-linearVelocity.html).

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script de seguimiento horizontal y su personaje de prueba. Así podrás adaptar un perseguidor sencillo que conserve la gravedad; este ejemplo no resuelve rutas, saltos ni obstáculos.

<a name="u119"></a>

### U119. Mover una plataforma cinemática

**Etiquetas:** `Rigidbody2D` · `Cuerpos cinemáticos` · `MovePosition` · `FixedUpdate` · `Movimiento`

Crea una plataforma con collider y Rigidbody2D de tipo Kinematic. Define dos posiciones del recorrido y una velocidad. Desplázala con MovePosition en FixedUpdate hasta cada extremo y cambia de dirección al llegar; prueba primero el recorrido libre, sin transportar al jugador.

<details>
<summary>Pista</summary>

calcula el siguiente punto con `Vector2.MoveTowards` y un paso de velocidad × `Time.fixedDeltaTime`; después pásalo a `MovePosition`.

</details>

**Comprueba:** la plataforma recorre el mismo trayecto de ida y vuelta sin saltos de posición.

**Referencia:** [Rigidbody2D.MovePosition](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Rigidbody2D.MovePosition.html). Se utiliza en pasos de física y no sustituye el comportamiento de gravedad de un cuerpo dinámico.

**★ Conviene guardar:** `Futuros proyectos`. Conserva la plataforma cinemática con su script y extremos de recorrido. Así podrás reutilizar el movimiento de ida y vuelta; transportar al jugador requiere ampliar y probar el comportamiento.

<a name="u120"></a>

### U120. Comparar movimiento a 30 y 60 FPS

**Etiquetas:** `Fotogramas` · `Application.targetFrameRate` · `Tiempo` · `Velocidad` · `Comparación de resultados`

En la escena cenital, mide cuánto avanza el personaje durante diez segundos en una misma dirección, con la misma velocidad y sin obstáculos. Compara `Application.targetFrameRate` a 30 y 60, con `QualitySettings.vSyncCount = 0`. Cuenta los `Update()` durante un segundo con el temporizador de [U073](#u073) para estimar los FPS reales. Al terminar, restaura los ajustes anteriores.

<details>
<summary>Pista</summary>

en el editor este límite afecta a Game; si sus opciones incluyen VSync, desactívalo durante la prueba. Un límite solicitado no garantiza alcanzarlo.

</details>

**Comprueba:** comparas la distancia en el mismo tiempo y los FPS observados.

**Referencia:** [Application.targetFrameRate y sus límites](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Application-targetFrameRate.html).

[Volver al índice](#indice)

<a name="bloque-13"></a>

## 13. Zonas, contactos y consecuencias (U121-U130)

**Base y prerrequisitos:** Parte de [U117](#u117) o recrea un personaje cenital mínimo con WASD y velocidad configurable. En estas primeras interacciones usa un único Collider2D en la raíz del personaje. Ambos objetos necesitan Collider2D y el personaje conserva su Rigidbody2D Dynamic; al menos uno de los colliders debe tener Is Trigger activado.

<a name="u121"></a>

### U121. Entrar en una zona invisible

**Etiquetas:** `Triggers 2D` · `Collider2D` · `Etiquetas de objetos` · `Detección de entrada`

Crea la etiqueta `Jugador` y asígnala al personaje de [U117](#u117). Prepara una zona con BoxCollider2D y activa Is Trigger. Desde un script de la zona, detecta `OnTriggerEnter2D` y muestra un mensaje únicamente cuando entre el personaje. Comprueba que el área permite atravesarla sin bloquear el movimiento.

<details>
<summary>Pista</summary>

usa `void OnTriggerEnter2D(Collider2D otro)` y `otro.CompareTag("Jugador")`; aquí recibes un collider, no un `Collision2D`.

</details>

**Comprueba:** recibes un mensaje al entrar y puedes seguir caminando.

**Referencia:** [Detección de entrada con OnTriggerEnter2D](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/MonoBehaviour.OnTriggerEnter2D.html).


<a name="u122"></a>

### U122. Detectar entrada y salida

**Etiquetas:** `Triggers 2D` · `Detección de entrada` · `Detección de salida` · `Etiquetas de objetos`

Amplía la zona anterior con OnTriggerExit2D. Muestra mensajes diferentes cuando el personaje entra y sale, indicando el nombre de la zona. Recorre sus bordes varias veces y observa cuándo se producen los eventos respecto al collider completo del personaje.

<details>
<summary>Pista</summary>

Mantén el filtro de etiqueta en los dos métodos.

</details>

**Comprueba:** Cada recorrido completo produce un mensaje de entrada y otro de salida.

<a name="u123"></a>

### U123. Cambiar de color dentro de la zona

**Etiquetas:** `Triggers 2D` · `SpriteRenderer` · `Color` · `Referencias`

Haz que el personaje se vuelva rojo al entrar en una zona y recupere el blanco al salir. Guarda una referencia a su SpriteRenderer y cambia su color desde los eventos correspondientes. Utiliza una única zona para observar el comportamiento sin solapamientos.

<details>
<summary>Pista</summary>

Reutiliza los cambios de color y las referencias ya aprendidos.

</details>

**Comprueba:** Permanecer dentro mantiene el rojo y salir devuelve el blanco.

<a name="u124"></a>

### U124. Distinguir dos zonas por su etiqueta

**Etiquetas:** `Triggers 2D` · `Etiquetas de objetos` · `Condicionales` · `Identificación de objetos`

Crea dos zonas separadas con etiquetas diferentes. Coloca el detector en el personaje y utiliza condiciones para escribir qué zona acaba de atravesar. Incluye en cada mensaje el nombre del objeto que entra y la etiqueta de la zona detectada.

<details>
<summary>Pista</summary>

El collider recibido identifica el otro objeto de la interacción.

</details>

**Comprueba:** La Console distingue las dos zonas y al personaje que entra.

<a name="u125"></a>

### U125. Destruir objetos al tocarlos

**Etiquetas:** `Triggers 2D` · `Destroy` · `Etiquetas de objetos` · `Condicionales`

Distribuye varios objetos con colliders de tipo trigger y una etiqueta común. Desde el personaje, detecta el contacto con esos objetos y destruye únicamente el objeto encontrado. Conserva las paredes y las zonas anteriores para comprobar que el filtro distingue cada interacción.

<details>
<summary>Pista</summary>

Destroy debe recibir el objeto detectado, no el personaje.

</details>

**Comprueba:** Puedes eliminar varios objetos sin hacer desaparecer paredes ni jugador.

<a name="u126"></a>

### U126. Contar entradas en una zona

**Etiquetas:** `Triggers 2D` · `Contadores` · `Eventos` · `Console`

Añade un contador entero que aumente cada vez que el personaje entra en una zona. Muestra el total actualizado en la Console. La zona debe permanecer activa para poder salir y volver a entrar; quedarse quieto dentro no debe incrementar continuamente el contador.

<details>
<summary>Pista</summary>

Incrementa el valor en el evento de entrada, no en Update.

</details>

**Comprueba:** Tres entradas completas producen un total de tres.

<a name="u127"></a>

### U127. Un portal de derecha a izquierda

**Etiquetas:** `Triggers 2D` · `Teletransporte` · `Rigidbody2D` · `Referencias` · `Coordenadas X/Y`

Coloca un portal de entrada a la derecha y una marca de destino a la izquierda. Al entrar el personaje, cambia la posición de su Rigidbody2D al destino mediante una referencia. El destino izquierdo no debe teletransportar de vuelta: el recorrido funciona en un único sentido.

<details>
<summary>Pista</summary>

asigna `Rigidbody2D.position` para el traslado instantáneo y mantén el destino separado del trigger de entrada.

</details>

**Comprueba:** entrar por la derecha lleva a la izquierda sin provocar un bucle.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el portal, su script y la referencia al destino. Así podrás adaptar traslados de un solo sentido entre zonas del mismo escenario.

<a name="u128"></a>

### U128. Perder vida al entrar en peligro

**Etiquetas:** `Triggers 2D` · `Vida` · `Daño` · `Condicionales` · `Límites`

Añade una variable de vida al personaje y una zona etiquetada como peligrosa. Cada entrada debe restar una cantidad configurable y mostrar la vida restante en la Console. Limita el resultado para que nunca sea negativo y prueba varias entradas consecutivas.

<details>
<summary>Pista</summary>

Reutiliza las condiciones y la resta de valores.

</details>

**Comprueba:** El daño solo afecta al personaje y la vida termina en cero.

<a name="u129"></a>

### U129. Dejar tiempo entre dos daños

**Etiquetas:** `Triggers 2D` · `OnTriggerStay2D` · `Temporizadores` · `Daño`

Sustituye el daño de entrada de [U128](#u128) por daño periódico con `OnTriggerStay2D` en el script del personaje. Filtra las zonas peligrosas y usa un único temporizador para recibir daño como máximo una vez por segundo, aunque coincidan varias zonas. Descuenta el tiempo una sola vez por `FixedUpdate()`.

<details>
<summary>Pista</summary>

descuenta `Time.fixedDeltaTime`; acepta daño si el tiempo restante es cero o menor y entonces reinícialo a un segundo.

</details>

**Comprueba:** permanecer dentro resta vida una vez por segundo y solapar dos peligros no acelera el daño.

<a name="u130"></a>

### U130. Volver al último punto de control

**Etiquetas:** `Puntos de control` · `Reaparición` · `Triggers 2D` · `Rigidbody2D` · `Vida`

Reutiliza el personaje con vida de [U128](#u128)–[U129](#u129). Crea una zona de punto de control que guarde su posición en el personaje. Añade otra zona que represente una caída o derrota; al entrar, devuelve el Rigidbody2D a la posición guardada, reinicia su velocidad y recupera la vida inicial.

<details>
<summary>Pista</summary>

Guarda la posición inicial como primer punto de control.

</details>

**Comprueba:** Puedes reaparecer antes y después de activar un punto nuevo.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva los scripts de punto de control y reaparición junto con una escena mínima de prueba. Así podrás recuperar posición, velocidad y vida tras caer; ajusta qué otros estados deben restaurarse en cada juego. **Retómalo en:** [U139](#u139).

[Volver al índice](#indice)

<a name="bloque-14"></a>

## 14. Interfaz para mostrar y cambiar valores (U131-U140)

**Base y prerrequisitos:** Reutiliza métodos públicos, referencias, contadores y vida; conserva el Input System y aprende a conectar la interfaz desde el Inspector.

<a name="u131"></a>

### U131. Preparar una interfaz en pantalla

**Etiquetas:** `Interfaz` · `Canvas` · `TextMeshPro` · `EventSystem` · `Input System`

Crea un Canvas con Render Mode Screen Space - Overlay y añade un texto TextMeshPro de interfaz. Si Unity solicita TMP Essential Resources, impórtalos. Comprueba que exista un único EventSystem con InputSystemUIInputModule. Si aparece `StandaloneInputModule`, sustitúyelo por el módulo de Input System y conserva las acciones de interfaz predeterminadas. Distingue los objetos de la interfaz de los sprites de la escena.

<details>
<summary>Pista</summary>

Selecciona el Canvas y revisa sus componentes en el Inspector.

</details>

**Comprueba:** El texto permanece en pantalla aunque muevas la cámara.

**Referencia:** [Interfaz con Input System](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.17/manual/UISupport.html).


<a name="u132"></a>

### U132. Cinco cuadrados que se adaptan

**Etiquetas:** `Interfaz` · `Canvas Scaler` · `Anclas` · `Resoluciones` · `Imágenes`

Sin scripts, coloca cinco imágenes cuadradas de colores: una en cada esquina y otra en el centro. Configura Canvas Scaler con Scale With Screen Size y referencia 1920 × 1080. Ajusta anclas y márgenes para conservar su colocación al cambiar la resolución de Game.

<details>
<summary>Pista</summary>

Cada cuadrado necesita anclas acordes con su posición.

</details>

**Comprueba:** Las cuatro esquinas y el centro siguen siendo reconocibles en dos resoluciones.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva una escena de referencia con Canvas Scaler y anclas correctamente configurados. Así podrás consultar o copiar la colocación de interfaz al diseñar indicadores y paneles para distintas resoluciones. **Retómalo en:** [U196](#u196).

<a name="u133"></a>

### U133. Comparar tres alineaciones de texto

**Etiquetas:** `Interfaz` · `TextMeshPro` · `Alineación de texto` · `RectTransform`

Sin scripts, crea tres textos TextMeshPro de interfaz con rectángulos del mismo tamaño. Copia en los tres el siguiente párrafo de ejemplo. Alinea uno a izquierda, otro centrado y otro a derecha.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam sed eros sollicitudin, porttitor nulla ac, venenatis augue. Duis lacinia hendrerit tellus, sit amet ornare ante blandit in. Nam sollicitudin felis a ultrices placerat. Nunc sed dictum ante.

<details>
<summary>Pista</summary>

Mantén iguales la fuente y su tamaño para comparar.

</details>

**Comprueba:** El contenido coincide y solamente cambia la alineación del párrafo.

<a name="u134"></a>

### U134. Un botón que escribe un mensaje

**Etiquetas:** `Interfaz` · `Botones` · `Eventos` · `Métodos públicos` · `Inspector`

Coloca un botón en el centro de la pantalla y cambia su texto. Crea un método público sin parámetros que escriba un mensaje en la Console. Conecta el evento On Click del botón con ese método mediante el Inspector y prueba varios clics.

<details>
<summary>Pista</summary>

Arrastra al evento el objeto que contiene el script.

</details>

**Comprueba:** Cada clic produce un único mensaje con el texto elegido.

<a name="u135"></a>

### U135. Mostrar y ocultar un panel sin scripts

**Etiquetas:** `Interfaz` · `Paneles` · `Botones` · `Eventos` · `SetActive`

Crea un panel de pantalla completa y dos botones superpuestos arriba a la izquierda. Haz que los botones sean hermanos del panel dentro del Canvas y aparezcan después de él en Hierarchy. Sin scripts, configura On Click: A activa el panel y B, y se desactiva; B desactiva el panel, activa A y se desactiva. Empieza con A activo y el panel y B inactivos.

<details>
<summary>Pista</summary>

Usa tres llamadas a SetActive en cada botón; desactiva el propio botón al final.

</details>

**Comprueba:** El mismo lugar permite abrir y cerrar repetidamente.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el panel y los botones con sus eventos ya conectados. Así podrás preparar paneles de ayuda o información que puedan abrirse y cerrarse sin escribir un controlador nuevo. **Retómalo en:** [U196](#u196).

<a name="u136"></a>

### U136. Un botón para sumar puntos

**Etiquetas:** `Interfaz` · `Botones` · `Contadores` · `TextMeshPro` · `Conversión a texto`

Sitúa un botón en el centro izquierdo y un contador TextMeshPro en el centro derecho. Cada clic debe incrementar una variable entera y actualizar el texto. Guarda una referencia al texto desde el Inspector y muestra cero antes de recibir el primer clic.

<details>
<summary>Pista</summary>

Usa `using TMPro;`, una referencia `TMP_Text` y su propiedad `.text`; convierte el número con `ToString()`.

</details>

**Comprueba:** Cinco clics muestran cinco y reiniciar vuelve a cero.

<a name="u137"></a>

### U137. Reiniciar el contador desde otro botón

**Etiquetas:** `Interfaz` · `Contadores` · `Métodos` · `Reutilización de código` · `TextMeshPro`

Añade un botón para poner a cero el contador anterior. Crea un método que actualice su texto y reutilízalo tanto al sumar como al reiniciar. Comprueba que la variable y la interfaz siempre muestran el mismo resultado después de cualquier combinación de clics.

<details>
<summary>Pista</summary>

Centraliza la actualización del texto en un único método.

</details>

**Comprueba:** Sumar, reiniciar y volver a sumar funciona sin valores desactualizados.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el contador, su texto y el script con un único método de actualización. Así podrás adaptar indicadores de puntos u objetos y mantener el valor mostrado sincronizado con el dato. **Retómalo en:** [U140](#u140), [U143](#u143).

<a name="u138"></a>

### U138. Ajustar la velocidad con un deslizador

**Etiquetas:** `Interfaz` · `Slider` · `Eventos` · `Parámetros` · `Velocidad`

Añade un Slider con límites mínimo y máximo adecuados para la velocidad del personaje cenital. Conecta On Value Changed a un método público que reciba un float y actualice su velocidad. Inicializa el Slider con la velocidad del personaje y pon Navigation en None para probarlo con el ratón mientras mueves al personaje con WASD.

<details>
<summary>Pista</summary>

Selecciona la llamada dinámica que utiliza el valor del deslizador.

</details>

**Comprueba:** Cambiar el Slider modifica la rapidez sin editar el script.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el slider y el ejemplo de conexión dinámica a un método que recibe un float. Así podrás crear controles de volumen u otros ajustes numéricos con un valor inicial coherente. **Retómalo en:** [U175](#u175).

<a name="u139"></a>

### U139. Mostrar la vida en una barra

**Etiquetas:** `Interfaz` · `Slider` · `Vida` · `Referencias`

Parte del personaje con daño y reaparición de [U130](#u130). Crea otro Slider para representar la vida del personaje. Configura su máximo con la vida inicial y actualiza su valor cuando reciba daño o reaparezca. Desactiva su interacción para que el jugador no pueda modificar la salud arrastrando la barra con el ratón.

<details>
<summary>Pista</summary>

añade `using UnityEngine.UI;`, asigna una referencia `Slider` desde el Inspector y usa `maxValue` y `value`. Reutiliza la vida del personaje, sin crear otro contador.

</details>

**Comprueba:** la barra baja con el daño y se recupera al reaparecer.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el sistema de vida con daño, reaparición y barra vinculada al mismo valor. Así podrás añadir una condición de derrota o adaptar un indicador de salud sin duplicar los datos de vida. **Retómalo en:** [U170](#u170).

<a name="u140"></a>

### U140. Recoger objetos y ver el total

**Etiquetas:** `Triggers 2D` · `Recogida de objetos` · `Contadores` · `Comunicación entre scripts` · `Destroy`

Distribuye varios objetos estáticos, cada uno con un único collider de tipo trigger, por la escena cenital. En el script de cada objeto, filtra al personaje por su etiqueta `Jugador`, haz desaparecer el objeto y suma uno al contador TextMeshPro. Reutiliza un método para actualizar el total y un booleano por objeto para aceptar solo su primera recogida.

<details>
<summary>Pista</summary>

el nombre de una clase propia también sirve como tipo. Si la clase del contador se llama `ContadorPuntos`, declara `public ContadorPuntos contador;` en el recogible, asígnalo desde Inspector y llama a su método público `contador.SumarPunto();`, usando los nombres reales de tu clase y método. Marca primero el objeto como recogido; después suma, desactiva su collider y llama a `Destroy(gameObject)`.

</details>

**Comprueba:** el total coincide con las recogidas y ningún objeto suma dos veces.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva los objetos recogibles, el contador y los scripts que impiden contar una recogida dos veces. Así podrás añadir objetivos, sonido, reinicio, récords o límite de tiempo a una escena de recogida. **Retómalo en:** [U169](#u169), [U179](#u179), [U187](#u187), [U189](#u189), [U192](#u192).

[Volver al índice](#indice)

<a name="bloque-15"></a>

## 15. Crear y gestionar copias de objetos (U141-U150)

**Base y prerrequisitos:** Reutiliza el personaje cenital, sus entradas de teclado, los contadores de interfaz, los temporizadores, los arrays y los bucles.

<a name="u141"></a>

### U141. Guardar un objeto como prefab

**Etiquetas:** `Prefabs` · `Instancias` · `SpriteRenderer` · `Inspector`

Crea una ficha visual sencilla con SpriteRenderer y conviértela en prefab guardándola en una carpeta del proyecto. Arrastra dos copias a la escena y modifica el color del prefab para observar la relación con sus instancias. Mantén esta ficha sin componentes físicos.

<details>
<summary>Pista</summary>

Distingue el recurso de Project de sus copias en Hierarchy.

</details>

**Comprueba:** Las dos instancias reciben el cambio de color del prefab.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva el prefab de la ficha, sin componentes físicos. Permite practicar creación de copias, distribución de objetos y sonidos de aparición sin volver a preparar el recurso visual. **Retómalo en:** [U142](#u142), [U148](#u148), [U150](#u150), [U173](#u173).

<a name="u142"></a>

### U142. Crear una copia al pulsar espacio

**Etiquetas:** `Prefabs` · `Instanciación` · `Instantiate` · `Teclado`

Retira primero las fichas colocadas manualmente: esta escena debe empezar sin copias. Añade al personaje una referencia al prefab de la ficha, asignada desde el Inspector. Mientras lo controlas con WASD, cada pulsación de espacio debe usar Instantiate para crear una copia en su posición actual. La copia debe permanecer donde apareció cuando el personaje siga avanzando.

<details>
<summary>Pista</summary>

Usa una pulsación nueva y crea la copia sin hacerla hija del personaje.

</details>

**Comprueba:** Puedes dejar varias fichas separadas por la escena.

<a name="u143"></a>

### U143. Contar todas las copias creadas

**Etiquetas:** `Instanciación` · `Contadores` · `TextMeshPro` · `Métodos`

Añade un contador TextMeshPro que muestre el número total de fichas creadas durante la partida. Incrementa el valor cuando Instantiate cree una copia y actualiza la interfaz. Este contador representa el total histórico, por lo que borrar una ficha no debe reducirlo.

<details>
<summary>Pista</summary>

Reutiliza el método que actualiza textos de contador.

</details>

**Comprueba:** El valor aumenta una vez por copia y coincide con las pulsaciones aceptadas.

<a name="u144"></a>

### U144. Desaparecer después de tres segundos

**Etiquetas:** `Destrucción` · `Destroy` · `Retrasos` · `Instancias`

Añade al prefab un script que programe la destrucción de cada instancia tres segundos después de aparecer. Crea varias fichas en momentos diferentes y observa que cada una conserva su propio plazo. El contador de copias creadas debe seguir mostrando el total histórico.

<details>
<summary>Pista</summary>

Destroy permite indicar un retraso antes de eliminar el objeto.

</details>

**Comprueba:** Cada ficha desaparece aproximadamente tres segundos después de su creación.

<a name="u145"></a>

### U145. Contar solamente las copias que siguen vivas

**Etiquetas:** `Contadores` · `Temporizadores` · `GetComponent` · `Referencias` · `Destrucción`

Añade un segundo contador para las copias vivas. Al crear cada ficha, pásale una referencia al script contador. Sustituye su destrucción diferida por un temporizador propio: al cumplir tres segundos, debe avisar al contador antes de destruirse. Incrementa el total vivo al crearla.

<details>
<summary>Pista</summary>

en el script de la ficha, crea `public void Inicializar(ContadorFichas referencia)` para guardar la referencia recibida en un campo. Justo después de `Instantiate`, llama a `copia.GetComponent<FichaTemporal>().Inicializar(contador);`, adaptando los nombres a tus clases. Usa después ese campo para avisar al contador; no lo leas antes de inicializarlo.

</details>

**Comprueba:** sin nuevas creaciones, el contador vivo vuelve a cero.

<a name="u146"></a>

### U146. Crear fichas a intervalos regulares

**Etiquetas:** `Instanciación` · `Temporizadores` · `Métodos` · `Inspector`

Crea un generador fijo que produzca una ficha cada cierto intervalo mayor que cero, configurable desde el Inspector. Reutiliza el método de creación y los contadores anteriores. Gestiona el intervalo con un temporizador para que la frecuencia dependa del tiempo transcurrido, no del número de fotogramas.

<details>
<summary>Pista</summary>

Reinicia el tiempo de espera después de cada creación.

</details>

**Comprueba:** Cambiar el intervalo modifica la frecuencia y los contadores permanecen coherentes.

<a name="u147"></a>

### U147. Limitar las fichas presentes

**Etiquetas:** `Condicionales` · `Comparaciones` · `Contadores` · `Instanciación`

Añade al generador un límite máximo de fichas vivas. Antes de cada intento de creación, compara ese límite con el contador actual y crea solamente si queda espacio. Cuando una ficha desaparezca, el generador podrá volver a crear en su siguiente intervalo.

<details>
<summary>Pista</summary>

Realiza la comprobación también si mantienes la creación mediante espacio.

</details>

**Comprueba:** El total vivo nunca supera el límite configurado.

<a name="u148"></a>

### U148. Construir una fila con un bucle

**Etiquetas:** `Bucles` · `for` · `Instanciación` · `Coordenadas X/Y`

En una copia de la escena, sustituye la generación periódica por una fila creada al iniciar. Usa un bucle for, una cantidad y una separación configurables. Calcula la posición de cada ficha desde un origen común y permite suficientes objetos vivos para completar la fila.

<details>
<summary>Pista</summary>

Multiplica el índice del bucle por la separación horizontal.

</details>

**Comprueba:** Cambiar cantidad y distancia produce una fila regular sin duplicar instrucciones.

<a name="u149"></a>

### U149. Borrar una fila guardada en un array

**Etiquetas:** `Arrays` · `Bucles` · `Destrucción` · `null` · `Contadores`

Para esta prueba, duplica el prefab y desactiva su temporizador de autodestrucción, conservando el componente de la ficha y su método de inicialización. Guarda las fichas de la fila en un array al crearlas. Añade una tecla que recorra ese array y destruya sus objetos; comprueba cada referencia para poder repetir la acción cuando ya no quede ninguno. Actualiza también el contador vivo.

<details>
<summary>Pista</summary>

Una referencia a un objeto destruido debe comprobarse antes de usarla.

</details>

**Comprueba:** La fila desaparece y repetir la tecla no genera errores.

<a name="u150"></a>

### U150. Generar dentro de un área delimitada

**Etiquetas:** `Random.Range` · `Coordenadas X/Y` · `Límites` · `Instanciación`

Recupera el generador periódico con límite de objetos vivos y el prefab con duración y aviso al contador de [U145](#u145). Define valores mínimos y máximos para X e Y en el Inspector y genera cada ficha en una posición aleatoria dentro de ese rectángulo. Coloca cuatro marcas visuales en sus esquinas para comprobar los límites.

<details>
<summary>Pista</summary>

Obtén aleatoriamente cada coordenada por separado.

</details>

**Comprueba:** Las fichas aparecen dentro del área y siguen respetando el máximo de objetos vivos.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el generador configurable con intervalo, área aleatoria, límite de copias y contador de objetos vivos, junto con el script de duración de las fichas. Sirve como punto de partida para generar objetos coleccionables o elementos temporales dentro de un área.

[Volver al índice](#indice)

<a name="bloque-16"></a>

## 16. Mapas y animaciones (U151-U160)

Base del bloque: reutiliza el spritesheet recortado de [U027](#u027), las jerarquías de [U028](#u028) y un jugador con movimiento 2D.

<a name="u151"></a>

### U151. Crear una paleta de piezas

**Etiquetas:** `Tile Palette` · `Tiles` · `Hoja de sprites` · `Package Manager`

Abre Tile Palette y crea una paleta con los sprites del spritesheet que recortaste en [U027](#u027). Si falta la ventana, instala 2D Tilemap Editor desde Package Manager. Guarda los recursos Tile en una carpeta propia y coloca al menos seis piezas diferentes en la paleta.

<details>
<summary>Pista</summary>

una paleta reúne las piezas que usarás para pintar un mapa.

</details>

**Comprueba:** seleccionas cada pieza sin volver al spritesheet original.

**Recurso:** [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks), con los sprites ya recortados en [U027](#u027).

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva la Tile Palette, sus recursos Tile y el spritesheet del que dependen. Permite dibujar y modificar otros mapas sin repetir la preparación de las piezas. **Retómalo en:** [U152](#u152), [U153](#u153), [U154](#u154).

<a name="u152"></a>

### U152. Dibujar un mapa con Tilemap

**Etiquetas:** `Tilemap` · `Grid` · `Tile Palette` · `Diseño de niveles`

Crea un Tilemap rectangular y dibuja un escenario pequeño utilizando la paleta anterior, sin escribir scripts. Incluye un suelo reconocible, varios obstáculos y una zona de inicio. Corrige al menos una pieza usando la herramienta de borrar.

<details>
<summary>Pista</summary>

Grid organiza las celdas y Tilemap contiene las piezas. Para que una pieza cuadrada llene una celda de una unidad, ajusta sus Pixels Per Unit a su ancho en píxeles.

</details>

**Comprueba:** las piezas encajan sin huecos y el escenario se ve completo desde la cámara 2D.

**Recurso:** Reutiliza la paleta de [U151](#u151), creada con [Pixel Platformer Blocks, de Kenney](https://kenney.nl/assets/pixel-platformer-blocks).

<a name="u153"></a>

### U153. Hacer sólido el mapa

**Etiquetas:** `TilemapCollider2D` · `Colisiones 2D` · `Rigidbody2D` · `Tiles`

Añade TilemapCollider2D al mapa y prueba encima el jugador con Rigidbody2D de [U116](#u116). Ajusta el tipo de colisión de las piezas necesarias para que el suelo y los obstáculos detengan al jugador. Mantén el escenario inmóvil.

<details>
<summary>Pista</summary>

usa piezas con Collider Type distinto de None y asigna `Suelo` al objeto Tilemap del suelo. Para probar el salto, usa un tramo superior plano: el detector sencillo de [U113](#u113) aún no distingue paredes de apoyos.

</details>

**Comprueba:** el jugador se apoya en el suelo y no atraviesa los obstáculos.

<a name="u154"></a>

### U154. Separar fondo y obstáculos

**Etiquetas:** `Tilemap` · `Grid` · `Orden visual` · `Colisiones 2D`

Separa el escenario en dos Tilemaps dentro del mismo Grid: uno para decoración y otro para obstáculos. Mueve algunas piezas a su capa correspondiente y ajusta su orden de dibujo. Deja las colisiones únicamente en las piezas que deban bloquear al jugador.

<details>
<summary>Pista</summary>

revisa Order in Layer en cada Tilemap Renderer.

</details>

**Comprueba:** el jugador atraviesa la decoración y sigue chocando con los obstáculos.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el Grid con los Tilemaps separados de decoración y obstáculos y sus ajustes de colisión. Ofrece una base para pequeños niveles 2D con fondo decorativo y zonas sólidas independientes.

<a name="u155"></a>

### U155. Animar una transformación

**Etiquetas:** `Animación 2D` · `Transform` · `Fotogramas clave` · `Clips de animación`

Selecciona un sprite de prueba sin Rigidbody2D ni script de movimiento y crea una animación con la ventana Animation, sin escribir scripts. Durante el clip, cambia su posición en X e Y, su rotación alrededor de Z y su escala en X e Y. Mantén el movimiento dentro del plano 2D.

<details>
<summary>Pista</summary>

añade fotogramas al principio, en medio y al final.

</details>

**Comprueba:** al reproducir el clip se distinguen las tres transformaciones.

<a name="u156"></a>

### U156. Animar dos piezas juntas

**Etiquetas:** `Animación 2D` · `Jerarquía` · `Fotogramas clave` · `Clips de animación`

Crea un objeto padre con dos sprites hijos, como un cuerpo y una antena. Desde el padre, graba un único clip que cambie posición, rotación Z y escala de sus hijos. Anima ambos sprites sin escribir scripts ni crear clips independientes.

<details>
<summary>Pista</summary>

con el padre seleccionado, usa Add Property para añadir las propiedades de ambos hijos al mismo clip; coloca sus claves en distintos instantes.

</details>

**Comprueba:** una sola reproducción anima las dos piezas de forma coordinada.

<a name="u157"></a>

### U157. Crear una animación de carrera

**Etiquetas:** `Animación 2D` · `Hoja de sprites` · `Sprites` · `Repetición de clips`

Descarga un personaje de [Dino Characters, de Arks](https://arks.itch.io/dino-characters), importa su spritesheet y separa los fotogramas de carrera. Crea una animación que los reproduzca en orden y se repita, sin escribir scripts. Ajusta la velocidad hasta reconocer claramente el movimiento.

<details>
<summary>Pista</summary>

conserva el mismo tamaño de corte para todos los fotogramas.

</details>

**Comprueba:** el dinosaurio corre sin saltos de tamaño ni imágenes mezcladas.

**Material:** Puedes utilizar un personaje equivalente facilitado por el docente. Revisa las condiciones de uso del recurso que elijas.

<a name="u158"></a>

### U158. Cambiar de animación con espacio

**Etiquetas:** `Animator` · `Transiciones` · `bool` · `Teclado`

Prepara reposo y carrera del mismo personaje y añade ambos clips a un Animator Controller asignado a su Animator. Crea un parámetro bool llamado Corriendo y dos transiciones, una por sentido, condicionadas a true y false. Desactiva Has Exit Time. Invierte un booleano al pulsar espacio y envíalo al Animator.

<details>
<summary>Pista</summary>

obtén una referencia al Animator y llama a `SetBool("Corriendo", valor)`; el nombre debe coincidir con el parámetro.

</details>

**Comprueba:** cada pulsación nueva alterna una vez entre las dos animaciones.

**Recurso:** Reutiliza el personaje de [Dino Characters, de Arks](https://arks.itch.io/dino-characters), preparado en [U157](#u157).

**Referencia:** [Cambiar un parámetro con Animator.SetBool](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Animator.SetBool.html).


<a name="u159"></a>

### U159. Animar según el movimiento

**Etiquetas:** `Animator` · `Vectores` · `Movimiento` · `Condicionales`

Sustituye la alternancia con espacio de [U158](#u158) por el vector de movimiento WASD del personaje visual de [U088](#u088). Activa la carrera cuando la entrada tenga alguna dirección y vuelve a reposo cuando no la tenga. Comprueba también las combinaciones de dos teclas.

<details>
<summary>Pista</summary>

aprovecha el vector de movimiento que ya calcula tu script.

</details>

**Comprueba:** la animación responde al empezar y al terminar de caminar.

**Recurso:** Reutiliza el personaje de [Dino Characters, de Arks](https://arks.itch.io/dino-characters), con las animaciones de [U158](#u158).

<a name="u160"></a>

### U160. Mirar hacia donde caminas

**Etiquetas:** `SpriteRenderer` · `flipX` · `Movimiento` · `Condicionales`

Haz que el sprite mire a la derecha al caminar hacia la derecha y a la izquierda al caminar hacia la izquierda. Cuando el personaje se detenga, conserva la última orientación. Mantén el comportamiento de las animaciones que ya preparaste.

<details>
<summary>Pista</summary>

cambia flipX del SpriteRenderer solo cuando haya movimiento horizontal.

</details>

**Comprueba:** el giro solo cambia la orientación visual; no desplaza al objeto ni invierte la interfaz.

**Recurso:** Reutiliza el personaje de [Dino Characters, de Arks](https://arks.itch.io/dino-characters), utilizado en [U159](#u159).

**★ Conviene guardar:** `Futuros proyectos`. Conserva el personaje con su script de movimiento y orientación, Animator, clips y sprites utilizados. Reúne movimiento, reposo, carrera y orientación para probar personajes animados en otros prototipos.

[Volver al índice](#indice)

<a name="bloque-17"></a>

## 17. Acciones por proximidad y reglas de juego (U161-U170)

Base del bloque: reutiliza un jugador WASD, enemigos sencillos, colisiones 2D, contadores y la persecución cercana de [U096](#u096).

<a name="u161"></a>

### U161. Medir distancias a varios enemigos

**Etiquetas:** `Arrays` · `Bucles` · `Distancias` · `Vector2` · `Depuración`

Coloca cinco enemigos inmóviles y guarda sus referencias en un array asignado desde el Inspector. Al pulsar una tecla, recorre el array y muestra en Console el nombre y la distancia 2D de cada enemigo respecto al jugador.

<details>
<summary>Pista</summary>

calcula cada distancia con posiciones tratadas como Vector2.

</details>

**Comprueba:** al mover al jugador cambian las distancias de todos los enemigos.

<a name="u162"></a>

### U162. Encontrar objetos en un círculo

**Etiquetas:** `Physics2D.OverlapCircleAll` · `LayerMask` · `Capas físicas` · `Collider2D`

Añade un Collider2D a cada enemigo y crea una capa física desde Layer > Add Layer, distinta del orden visual. Asigna los enemigos a ella y selecciónala en un campo LayerMask. Al pulsar una tecla, consulta Physics2D.OverlapCircleAll con radio 3 y ese filtro; muestra cuántos detecta.

<details>
<summary>Pista</summary>

utiliza un único collider por enemigo y excluye al jugador de la capa.

</details>

**Comprueba:** detectas solo enemigos cuyos colliders alcanzan el círculo.

**Referencia:** [Consulta circular con Physics2D.OverlapCircleAll](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Physics2D.OverlapCircleAll.html).

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el script de detección circular y una nota breve de la capa física y el LayerMask que necesita. Sirve para detectar objetivos cercanos al preparar impulsos, áreas de interacción u otras acciones por proximidad. **Retómalo en:** [U164](#u164).

<a name="u163"></a>

### U163. Destruir enemigos cercanos

**Etiquetas:** `Distancias` · `Comparaciones` · `Destrucción` · `null`

Recupera el array de [U161](#u161) con varios enemigos estáticos y un jugador que se mueva con WASD. Al pulsar espacio, destruye todos los enemigos cuya distancia entre centros sea menor que 3 unidades. Conserva los que estén a 3 unidades o más y permite repetir la acción.

<details>
<summary>Pista</summary>

comprueba la distancia exacta de cada candidato y omite referencias vacías.

</details>

**Comprueba:** una pulsación puede eliminar varios enemigos simultáneamente.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva el script de eliminación por distancia y una escena mínima con jugador y enemigos estáticos. Permite volver a comprobar la comparación estricta al practicar valores justo por debajo, en y por encima del límite. **Retómalo en:** [U195](#u195).

<a name="u164"></a>

### U164. Provocar una explosión de impulso

**Etiquetas:** `Rigidbody2D` · `AddForce` · `ForceMode2D.Impulse` · `Vectores` · `Distancias`

Construye una habitación con suelo, paredes y techo estáticos, y varios cuerpos con Rigidbody2D dinámico separados del jugador. Mueve al jugador con WASD. Al pulsar espacio, aplica un impulso de intensidad configurable hacia fuera a los cuerpos cuyo centro esté a menos de 3 unidades del jugador.

<details>
<summary>Pista</summary>

usa el filtro de [U162](#u162) para obtener candidatos, comprueba la distancia entre sus centros y normaliza la dirección antes de multiplicarla por la intensidad. Aplica AddForce con ForceMode2D.Impulse; usa un collider por cuerpo y excluye al jugador del filtro.

</details>

**Comprueba:** solo los cuerpos con centro a menos de 3 unidades reciben el impulso hacia fuera.

<a name="u165"></a>

### U165. Invertir la gravedad

**Etiquetas:** `Physics2D.gravity` · `Física 2D` · `Estado global` · `Ciclo de vida`

Reutiliza la habitación cerrada y sustituye la explosión de espacio por una inversión de Physics2D.gravity. Guarda la gravedad original en OnEnable y restáurala en OnDisable. Mantén Gravity Scale positivo en los cuerpos de prueba y observa cómo pasan del suelo al techo.

<details>
<summary>Pista</summary>

OnEnable se ejecuta al activar el componente y OnDisable al desactivarlo; invierte el Vector2 de gravedad con el signo menos.

</details>

**Comprueba:** dos pulsaciones recuperan la dirección inicial y desactivar el controlador restaura el valor original.

<a name="u166"></a>

### U166. Patrullar entre dos puntos

**Etiquetas:** `Movimiento` · `Patrullas` · `Referencias` · `Estados`

Crea dos objetos vacíos como extremos de una patrulla y asigna sus referencias a un enemigo visual sin Rigidbody2D. Haz que avance hacia el primer punto y cambie de destino al llegar. Repite el recorrido con una velocidad ajustable desde el Inspector.

<details>
<summary>Pista</summary>

deja los extremos fuera de la jerarquía del enemigo y usa Vector2.MoveTowards, como en [U093](#u093). Guarda cuál es el destino actual y cámbialo al llegar.

</details>

**Comprueba:** el enemigo completa varias vueltas sin detenerse ni sobrepasar los extremos.

<a name="u167"></a>

### U167. Alternar patrulla y persecución

**Etiquetas:** `Patrullas` · `Persecución` · `Distancias` · `Condicionales`

Combina la patrulla anterior con la persecución cercana de [U096](#u096). Mientras el jugador esté lejos, el enemigo patrulla; cuando entre en el radio elegido, lo persigue. Al alejarse el jugador, el enemigo retoma su recorrido entre los dos puntos.

<details>
<summary>Pista</summary>

Utiliza una condición para escoger un único comportamiento y conserva el enemigo sin física de [U166](#u166).

</details>

**Comprueba:** Acercarte y alejarte cambia su comportamiento.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script del enemigo que alterna patrulla y persecución y las referencias que necesita. Es una base sencilla para personajes que cambian de comportamiento según la distancia al jugador.

<a name="u168"></a>

### U168. Abrir una puerta con una llave

**Etiquetas:** `Triggers 2D` · `bool` · `Condicionales` · `Colisiones 2D`

Coloca una llave con trigger y una puerta que bloquee el paso. Al recoger la llave, guarda ese hecho en una variable booleana. Cuando el jugador entre en una zona delante de la puerta, ábrela únicamente si ya tiene la llave.

<details>
<summary>Pista</summary>

separa el trigger de detección del collider que bloquea.

</details>

**Comprueba:** sin llave no pasas y, después de recogerla, sí puedes cruzar.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva la puerta con su trigger de detección y collider de bloqueo, junto con los scripts de llave y apertura. Permite cambiar la condición de apertura sin reconstruir la puerta, por ejemplo al sustituir la llave por interruptores. **Retómalo en:** [U191](#u191).

<a name="u169"></a>

### U169. Ganar al recoger tres monedas

**Etiquetas:** `Contadores` · `Condiciones de victoria` · `Estados de partida` · `Interfaz`

Reutiliza el contador de monedas y coloca exactamente tres en una escena pequeña. Cuando el jugador recoja la tercera, muestra un mensaje de victoria y desactiva su movimiento. Evita que recoger cada moneda pueda sumar más de una vez.

<details>
<summary>Pista</summary>

Comprueba el total tras aumentarlo; bloquea nuevas entradas y deja la velocidad física en cero.

</details>

**Comprueba:** La tercera moneda detiene al jugador.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el método que finaliza la partida, muestra la victoria y detiene al jugador, con las referencias de interfaz necesarias. Permite reutilizar el resultado de victoria y cambiar su desencadenante por un objetivo contrarreloj o una meta. **Retómalo en:** [U192](#u192), [U193](#u193).

<a name="u170"></a>

### U170. Perder al agotar las vidas

**Etiquetas:** `Vida` · `Condiciones de derrota` · `Estados de partida` · `Interfaz`

Reutiliza tu sistema de vida y añade una condición de derrota cuando llegue a cero. Muestra un mensaje y, como en [U169](#u169), bloquea nuevas entradas y deja en cero la velocidad del personaje cenital. En esta prueba, la derrota termina la partida en lugar de activar una reaparición. Impide que nuevos contactos sigan restando vida o repitan el mensaje.

<details>
<summary>Pista</summary>

guarda si la partida ha terminado antes de procesar más daño.

</details>

**Comprueba:** la vida se mantiene en cero y el mensaje aparece una vez.

[Volver al índice](#indice)

<a name="bloque-18"></a>

## 18. Sonidos y música (U171-U180)

Base del bloque: reutiliza monedas, triggers, prefabs, botones y sliders, y prepara un efecto corto y una pista musical que puedas utilizar.

<a name="u171"></a>

### U171. Reproducir un sonido 2D

**Etiquetas:** `Audio 2D` · `AudioSource` · `AudioClip` · `AudioListener`

Importa un efecto de sonido corto y asigna el clip a un AudioSource de la escena. Configura Spatial Blend en 0 para reproducirlo como audio 2D. Activa Play On Awake y escucha el resultado al iniciar la escena.

<details>
<summary>Pista</summary>

revisa el volumen y que la cámara conserve su AudioListener.

</details>

**Comprueba:** el efecto se escucha sin depender de la posición del jugador.

**Recurso:** puedes generar un efecto de moneda con Pickup/coin en [jsfxr](https://sfxr.me/), descargarlo como WAV e importarlo al proyecto.


<a name="u172"></a>

### U172. Escuchar una moneda al entrar

**Etiquetas:** `Audio 2D` · `AudioSource` · `OnTriggerEnter2D` · `Triggers 2D`

Coloca una zona con Collider2D marcado como trigger y un AudioSource 2D con Play On Awake y Loop desactivados. Cuando el jugador entre, reproduce un sonido de moneda, aunque no recoja ningún objeto. Permite volver a escucharlo si sale de la zona y entra otra vez.

<details>
<summary>Pista</summary>

filtra al jugador y llama a `Play()` sobre la referencia al AudioSource desde `OnTriggerEnter2D`.

</details>

**Comprueba:** quedarse dentro no dispara el efecto continuamente.

**★ Conviene guardar:** `Prácticas posteriores`. Conserva la zona sonora con su detector de entrada, AudioSource y clip de prueba. Así podrás convertirla después en un prefab configurable sin reconstruir la detección. **Retómalo en:** [U199](#u199).

<a name="u173"></a>

### U173. Crear un objeto con sonido

**Etiquetas:** `Audio 2D` · `AudioSource` · `Prefabs` · `Instanciación`

Reutiliza un prefab que aparezca al pulsar espacio y añade un sonido a cada aparición. Configura su AudioSource para reproducir el efecto al crearse o actívalo desde el código de creación. Mantén una sola reproducción por objeto generado.

<details>
<summary>Pista</summary>

elige una sola forma de iniciar el audio para evitar duplicados.

</details>

**Comprueba:** tres pulsaciones generan tres objetos y tres sonidos.

<a name="u174"></a>

### U174. Repetir una música de fondo

**Etiquetas:** `Audio 2D` · `AudioSource` · `Música` · `Repetición de audio`

Crea un objeto independiente para la música de fondo y asígnale un AudioSource 2D. Activa Loop y Play On Awake. Ajusta su volumen para que puedas distinguir los efectos de las monedas mientras la música continúa durante toda la escena.

<details>
<summary>Pista</summary>

empieza con un volumen moderado y escucha el final del clip.

</details>

**Comprueba:** la música vuelve a empezar sin que tengas que pulsar nada.

**Recurso:** puedes buscar una pista breve en [la colección de música en bucle de Pixabay](https://pixabay.com/music/search/loop/) o utilizar una propia. Revisa las condiciones de uso del audio que elijas.


<a name="u175"></a>

### U175. Ajustar el volumen con un slider

**Etiquetas:** `Slider` · `Eventos` · `AudioSource` · `Volumen`

Reutiliza un slider de interfaz y configura su rango entre 0 y 1. Conecta su cambio de valor con el volumen del AudioSource de música. Al iniciar, coloca el slider en el valor que realmente esté utilizando la música.

<details>
<summary>Pista</summary>

utiliza On Value Changed para transmitir el valor del slider.

</details>

**Comprueba:** ambos extremos permiten silenciar la música y recuperar su volumen máximo.

<a name="u176"></a>

### U176. Silenciar sin perder el volumen

**Etiquetas:** `AudioSource.mute` · `bool` · `Botones` · `Textos de interfaz`

Añade un botón que alterne entre silenciar y recuperar la música. Utiliza la propiedad mute del AudioSource para conservar el volumen que elegiste con el slider. Cambia el texto del botón para indicar la acción disponible en cada momento.

<details>
<summary>Pista</summary>

invierte un estado booleano en cada pulsación.

</details>

**Comprueba:** al recuperar el sonido se mantiene el volumen seleccionado antes de silenciar.

<a name="u177"></a>

### U177. Pausar y continuar la música

**Etiquetas:** `AudioSource.Pause` · `AudioSource.UnPause` · `Botones` · `Reproducción de audio`

Añade un botón para pausar la música y otro para continuarla desde el mismo instante. Conserva los controles de volumen y silencio. Escucha un fragmento reconocible antes de pausar para poder comprobar después que no vuelve al principio.

<details>
<summary>Pista</summary>

compara Pause y UnPause con el comportamiento de Stop.

</details>

**Comprueba:** reanudar continúa el fragmento y no reinicia la pista musical.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el reproductor de música 2D y sus controles de volumen, silencio, pausa y continuación, con sus conexiones de interfaz. Reúne los controles básicos de audio que pueden adaptarse a un menú de opciones.

<a name="u178"></a>

### U178. Dar sonido a un botón

**Etiquetas:** `Botones` · `Eventos` · `AudioSource` · `Audio 2D`

Añade un sonido corto a uno de tus botones de interfaz. Reprodúcelo desde un AudioSource independiente cuando llegue el evento On Click y conserva también la acción original del botón. Prueba varios clics sin mantener el botón pulsado.

<details>
<summary>Pista</summary>

un mismo evento puede ejecutar más de una acción.

</details>

**Comprueba:** cada clic realiza su función y reproduce una sola confirmación sonora.

<a name="u179"></a>

### U179. Terminar el sonido de una moneda

**Etiquetas:** `AudioSource.PlayOneShot` · `Destrucción` · `Referencias` · `Contadores`

Haz que una moneda desaparezca al recogerla y que su sonido se escuche completo. Traslada la reproducción a un emisor independiente que permanezca en la escena, aunque la moneda se destruya inmediatamente. Reutiliza el contador de monedas existente.

<details>
<summary>Pista</summary>

usa PlayOneShot en un AudioSource 2D independiente, con Play On Awake y Loop desactivados; conserva la protección contra doble recogida de [U140](#u140).

</details>

**Comprueba:** la moneda desaparece sin cortar el final del sonido.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script de moneda que actualiza el contador y solicita el sonido a un AudioSource independiente. Permite recoger y destruir objetos sin cortar sus efectos sonoros.

<a name="u180"></a>

### U180. Variar ligeramente un efecto

**Etiquetas:** `AudioSource.pitch` · `Random.Range` · `Audio 2D`

Reutiliza un efecto corto y cambia ligeramente su pitch antes de cada reproducción, eligiendo un valor aleatorio entre 0,9 y 1,1. Haz la prueba con pulsaciones separadas para escuchar cada variación completa. Mantén la música con su tono habitual.

<details>
<summary>Pista</summary>

usa `Random.Range(0.9f, 1.1f)` sobre el pitch del AudioSource dedicado al efecto.

</details>

**Comprueba:** las reproducciones se parecen, pero no suenan todas exactamente iguales.

[Volver al índice](#indice)

<a name="bloque-19"></a>

## 19. Escenas, pausa y datos guardados (U181-U190)

Base del bloque: utiliza botones, temporizadores y música ya practicados. Guarda únicamente las escenas de prueba que necesites para experimentar con su carga y sus cambios.

<a name="u181"></a>

### U181. Preparar tres escenas de colores

**Etiquetas:** `Escenas` · `Cámara ortográfica` · `Build Profiles` · `Textos de interfaz`

Crea tres escenas llamadas U181_Roja, U181_Azul y U181_Verde. Configura el fondo de sus cámaras ortográficas en rojo, azul y verde respectivamente, y añade un texto que identifique cada escena. Inclúyelas en la lista de escenas de Build Profiles.

<details>
<summary>Pista</summary>

guarda cada escena antes de añadirla a la lista.

</details>

**Comprueba:** sus nombres coinciden exactamente y los tres fondos se distinguen al ejecutarlas.

**Referencia:** [Lista de escenas de Build Profiles](https://docs.unity3d.com/6000.0/Documentation/Manual/build-profile-scene-list.html).

**★ Conviene guardar:** `Prácticas posteriores`. Conserva las tres escenas mínimas de colores y sus nombres en la lista de escenas. Así podrás retomar las prácticas de carga por tecla, botón e inactividad si las haces en otra sesión. **Retómalo en:** [U182](#u182), [U183](#u183), [U184](#u184).

<a name="u182"></a>

### U182. Cargar la escena roja con espacio

**Etiquetas:** `Escenas` · `SceneManager` · `Input System` · `Teclado`

Añade a las tres escenas un controlador que cargue U181_Roja cuando pulses espacio. Utiliza SceneManager para realizar el cambio y una pulsación nueva del Input System. Prueba la acción empezando desde cada una de las tres escenas.

<details>
<summary>Pista</summary>

añade `using UnityEngine.SceneManagement;` y usa `SceneManager.LoadScene("U181_Roja");`.

</details>

**Comprueba:** desde azul o verde pasas a rojo, y desde rojo recargas la misma escena.

**Referencia:** [Carga de escenas con SceneManager.LoadScene](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneManager.LoadScene.html).


<a name="u183"></a>

### U183. Cargar la escena azul con un botón

**Etiquetas:** `Escenas` · `SceneManager` · `Botones` · `Métodos públicos`

Coloca un botón visible en cada una de las tres escenas y conecta su evento On Click con un método que cargue U181_Azul. Mantén también la navegación con espacio y comprueba ambas acciones desde las tres escenas disponibles.

<details>
<summary>Pista</summary>

utiliza un método público sin parámetros para conectarlo desde el Inspector.

</details>

**Comprueba:** cualquier botón lleva a azul y espacio sigue llevando a rojo.

<a name="u184"></a>

### U184. Cambiar tras diez segundos de inactividad

**Etiquetas:** `Temporizadores` · `Time.deltaTime` · `Input System` · `Escenas`

Añade a las escenas un temporizador que cargue U181_Verde tras diez segundos sin actividad, siempre que no estés ya en verde. Reinícialo al mantener o pulsar una tecla o botón del ratón, mover el ratón o usar su rueda. Reutiliza Time.deltaTime y prueba primero con una tecla que no cambie de escena.

<details>
<summary>Pista</summary>

comprueba que Keyboard.current y Mouse.current existan. Usa `anyKey.isPressed`, los botones del ratón y si `delta.ReadValue()` o `scroll.ReadValue()` son distintos de Vector2.zero.

</details>

**Comprueba:** nueve segundos de espera y una entrada reinician los diez segundos completos; verde no se recarga por inactividad.

<a name="u185"></a>

### U185. Mantener la música al cambiar de escena

**Etiquetas:** `Escenas` · `DontDestroyOnLoad` · `Persistencia entre escenas` · `Música`

Crea U185_Roja y U185_Azul con sus fondos correspondientes. Inicia música en roja y conserva su objeto raíz con DontDestroyOnLoad. Al pulsar espacio, carga azul y comprueba que la misma pista sigue sonando desde el punto alcanzado, sin reiniciarse.

<details>
<summary>Pista</summary>

registra ambas escenas y deja el objeto de música sin padre.

</details>

**Comprueba:** el cambio de color no interrumpe ni reinicia la canción.

<a name="u186"></a>

### U186. Evitar música duplicada al regresar

**Etiquetas:** `Persistencia entre escenas` · `static` · `Awake` · `Destrucción` · `AudioSource`

Añade un botón para volver de U185_Azul a U185_Roja. Guarda una referencia compartida, mediante un campo static, al reproductor conservado. En Awake, conserva la primera instancia e inicia su audio con Play; destruye las nuevas copias sin reproducirlas. Mantén desactivado Play On Awake.

<details>
<summary>Pista</summary>

Awake prepara el objeto antes de Start; static comparte la referencia entre copias.

</details>

**Comprueba:** Varios viajes conservan una sola canción, que no reinicia.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el reproductor de música persistente con su protección frente a instancias duplicadas. Permite mantener una sola pista al cambiar o reiniciar escenas. **Retómalo en:** [U187](#u187).

<a name="u187"></a>

### U187. Reiniciar la escena actual

**Etiquetas:** `Escenas` · `SceneManager.GetActiveScene` · `Reinicio de partida` · `Botones`

Añade un botón de reinicio a una escena de prueba con jugador, monedas y contador, recuperada de [U140](#u140) o preparada de nuevo. Guárdala y añádela a la lista de escenas de Build Profiles. Carga de nuevo la escena activa usando su nombre y comprueba que recupera la posición del jugador, las monedas presentes y el contador. Mantén la música persistente si existe.

<details>
<summary>Pista</summary>

consulta el nombre con SceneManager.GetActiveScene().

</details>

**Comprueba:** reiniciar después de jugar recupera los valores iniciales sin crear otra copia de la música.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el método que recarga la escena activa y un botón conectado a él. Sirve para añadir un reinicio sencillo a prototipos de juego.

<a name="u188"></a>

### U188. Mostrar un menú de pausa

**Etiquetas:** `Time.timeScale` · `Pausa` · `Estados de partida` · `Interfaz` · `Ciclo de vida`

Añade un panel con un botón para continuar y alterna la pausa con Escape. Detén el tiempo del juego con Time.timeScale, bloquea las acciones del jugador y muestra el panel. Al continuar o abandonar la escena, restablece el tiempo a 1.

<details>
<summary>Pista</summary>

coloca el controlador fuera del panel para que siga activo al ocultarlo. Time.timeScale no impide leer entradas en Update: consulta también el booleano de pausa y descarta acciones pendientes. Restaura el tiempo en OnDisable.

</details>

**Comprueba:** los objetos se detienen y Escape o el botón permiten continuar sin ejecutar acciones acumuladas.

**Referencia:** [Time.timeScale y su efecto sobre la simulación](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Time-timeScale.html).

**★ Conviene guardar:** `Futuros proyectos`. Conserva el controlador y panel de pausa, incluyendo el bloqueo de acciones y la restauración del tiempo. Permite pausar un prototipo y continuarlo con un comportamiento coherente.

<a name="u189"></a>

### U189. Guardar una mejor puntuación

**Etiquetas:** `PlayerPrefs` · `Persistencia de datos` · `Puntuación` · `Comparaciones` · `Interfaz`

Reutiliza el contador con botón de reinicio de [U137](#u137) o una escena de recogida como [U140](#u140) donde puedas obtener puntuaciones diferentes. Añade un botón Terminar prueba que compare la puntuación actual con el récord de PlayerPrefs y lo actualice solo si lo supera. Muestra el récord en un texto al entrar y después de cada mejora.

<details>
<summary>Pista</summary>

lee con `PlayerPrefs.GetInt("Record", 0)` y escribe con `PlayerPrefs.SetInt("Record", nuevoRecord)`; usa siempre la misma clave.

</details>

**Comprueba:** terminar una prueba con 5 puntos y otra con 3 conserva el récord de 5.

**Referencia:** [Guardar y recuperar valores con PlayerPrefs](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/PlayerPrefs.html).


<a name="u190"></a>

### U190. Comprobar la recuperación de datos

**Etiquetas:** `PlayerPrefs.Save` · `PlayerPrefs.DeleteKey` · `Persistencia de datos` · `Pruebas`

Prueba el récord anterior deteniendo y volviendo a iniciar Play. Añade un botón de prueba que borre únicamente la clave del récord y actualice su texto. Comprueba el valor inicial, una mejora y una puntuación inferior dentro del Editor.

<details>
<summary>Pista</summary>

llama a `PlayerPrefs.Save()` después de actualizar o borrar la clave, no en Update; usa `PlayerPrefs.DeleteKey("Record")` y vuelve a leer con valor inicial cero para actualizar el texto.

</details>

**Comprueba:** reiniciar conserva el récord y el botón lo devuelve a cero también después de volver a iniciar Play.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el script del récord con lectura, comparación, guardado y borrado de su clave, junto con el texto que lo muestra. Sirve como ejemplo de persistencia de una puntuación máxima y de cómo restablecer únicamente ese dato durante las pruebas.

[Volver al índice](#indice)

<a name="bloque-20"></a>

## 20. Prácticas combinadas y reutilización (U191-U200)

Base del bloque: combina mecánicas que ya hayas practicado; puedes usar piezas conservadas o recrear una versión mínima. Cada actividad plantea una modificación pequeña.

<a name="u191"></a>

### U191. Abrir con tres interruptores

**Etiquetas:** `Triggers 2D` · `bool` · `Contadores` · `Condicionales` · `SpriteRenderer`

Reutiliza la puerta de [U168](#u168) y retira la condición de la llave. Coloca tres interruptores con trigger: cada uno debe activarse solo una vez, cambiar de color y avisar al mismo controlador de puerta. Abre la puerta cuando los tres estén activados, sin exigir un orden específico.

<details>
<summary>Pista</summary>

guarda un booleano por interruptor y cuenta las activaciones nuevas.

</details>

**Comprueba:** pisar varias veces el mismo interruptor no abre la puerta antes de tiempo.

**★ Conviene guardar:** `Futuros proyectos`. Conserva los scripts de interruptor y puerta que cuentan cada activación una sola vez. Permiten construir pequeños puzles que requieren completar varias acciones independientes.

<a name="u192"></a>

### U192. Recoger monedas antes de que termine el tiempo

**Etiquetas:** `Cuenta atrás` · `Contadores` · `Estados de partida` · `Condiciones de victoria` · `Condiciones de derrota`

Combina el temporizador de [U073](#u073) con las monedas de [U140](#u140) y la victoria de [U169](#u169). Transforma el temporizador en una cuenta atrás desde treinta segundos. Muestra victoria al recoger las tres monedas o derrota al agotarse el tiempo, deteniendo la partida.

<details>
<summary>Pista</summary>

usa un único estado de partida terminada para resolver el resultado.

</details>

**Comprueba:** después de ganar no aparece una derrota por el temporizador.

<a name="u193"></a>

### U193. Llegar a una meta saltando

**Etiquetas:** `Salto` · `Plataformas 2D` · `Triggers 2D` · `Condiciones de victoria`

Reutiliza el movimiento y salto de [U116](#u116). Prepara dos plataformas con etiqueta Suelo, separadas para que el jugador no toque ambas simultáneamente. Coloca una meta con trigger sobre una zona firme después de la segunda y adapta la victoria de [U169](#u169) para terminar al llegar.

<details>
<summary>Pista</summary>

ajusta las distancias utilizando el salto que ya funciona.

</details>

**Comprueba:** puedes completar el recorrido y la victoria aparece únicamente al tocar la meta.

<a name="u194"></a>

### U194. Encontrar una referencia vacía

**Etiquetas:** `Depuración` · `Console` · `null` · `Inspector`

En una prueba temporal, declara un campo `public TMP_Text texto;` sin asignarlo y trata de escribir en su propiedad text desde Start, sin comprobar antes si es null. Ejecuta, localiza el error en Console y abre la línea afectada desde su enlace. Detén Play, asigna el texto en el Inspector y repite.

<details>
<summary>Pista</summary>

el fallo es deliberado; compara el nombre de la variable en la línea con el campo vacío del Inspector.

</details>

**Comprueba:** tras asignar la referencia, aparece el texto y no se repite el error.

<a name="u195"></a>

### U195. Probar valores en los límites

**Etiquetas:** `Pruebas de límites` · `Comparaciones` · `Distancias` · `Depuración`

Revisa la acción de proximidad de [U163](#u163). Deja al jugador en el origen y coloca enemigos en X=2,9, X=3 y X=3,1, todos con Y=0. Anota qué debería pasar con cada uno y pulsa espacio sin mover al jugador. Corrige la comparación si no cumple el criterio de [U163](#u163).

<details>
<summary>Pista</summary>

conserva la condición estricta de distancia menor que 3.

</details>

**Comprueba:** solo desaparece el enemigo situado a 2,9 unidades.

<a name="u196"></a>

### U196. Explicar cómo jugar en pantalla

**Etiquetas:** `Interfaz` · `Textos de interfaz` · `Botones` · `Usabilidad`

Añade a una escena de prueba un panel breve con sus controles y objetivo; basta con un personaje que puedas mover. Indica solo las teclas que realmente funcionan en esa escena y permite ocultar el panel con un botón. Comprueba que no tapa al jugador ni los indicadores principales.

<details>
<summary>Pista</summary>

usa frases cortas y un tamaño de texto legible.

</details>

**Comprueba:** los controles y el objetivo se entienden leyendo solo el panel; si puedes, pide a otra persona que lo pruebe.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el panel de instrucciones y su botón para ocultarlo. Puede adaptarse para explicar los controles y el objetivo de otros prototipos.

<a name="u197"></a>

### U197. Preparar una lista de opciones

**Etiquetas:** `Scroll View` · `Prefabs` · `Vertical Layout Group` · `Content Size Fitter` · `Layout Element`

Crea un panel con título y Scroll View vertical. En Content añade Vertical Layout Group y Content Size Fitter con Vertical Fit en Preferred Size. Diseña un botón TextMeshPro con Layout Element y Preferred Height de 40, y conviértelo en prefab. Coloca suficientes copias bajo Content para superar la altura visible.

<details>
<summary>Pista</summary>

ancla Content arriba y pon su Pivot Y en 1 para que crezca hacia abajo; deja Horizontal Fit en Unconstrained. En Vertical Layout Group activa Control Child Size para Height, desactiva Child Force Expand en Height y añade separación.

</details>

**Comprueba:** los botones conservan su altura y puedes desplazarte hasta el último.

**Referencia:** [Ajustar el tamaño de la interfaz a su contenido](https://docs.unity3d.com/Packages/com.unity.ugui@2.0/manual/HOWTO-UIFitContentSize.html).


<a name="u198"></a>

### U198. Generar opciones desde un array

**Etiquetas:** `Arrays` · `Bucles` · `Instanciación` · `Botones` · `TextMeshPro`

Sustituye las copias manuales de [U197](#u197) por un array con tres nombres. Genera un botón por nombre como hijo de Content. Añade al prefab un script con un método de inicialización que reciba la opción y el texto de salida, y actualice la etiqueta del botón. Crea otro método público que muestre esa opción al pulsarlo. Cambia el array para obtener otra lista.

<details>
<summary>Pista</summary>

conecta On Click al método del propio botón dentro del prefab. Instancia con Content como padre y worldPositionStays en false; inicializa cada copia para que recuerde su opción.

</details>

**Comprueba:** cada botón muestra su propio nombre y no quedan copias manuales duplicadas.

**★ Conviene guardar:** `Futuros proyectos`. Conserva el panel desplazable, el prefab del botón y los scripts que generan la lista desde un array. Así podrás adaptar listas de opciones o selectores sencillos con contenidos distintos.

<a name="u199"></a>

### U199. Una zona de sonido reutilizable

**Etiquetas:** `Prefabs` · `Triggers 2D` · `Audio 2D` · `Inspector` · `Reutilización de código`

Parte de la zona sonora de [U172](#u172) y reúne su collider, AudioSource y script en un prefab. Expón el clip y el volumen en el Inspector. Crea dos instancias y configura sonidos distintos, utilizando el mismo script en ambas.

<details>
<summary>Pista</summary>

asigna referencias a componentes del propio prefab y mantén el filtro del jugador.

</details>

**Comprueba:** cada zona reproduce su sonido sin modificar el código compartido.

**★ Conviene guardar:** `Prácticas posteriores` · `Futuros proyectos`. Conserva el prefab de zona sonora con sus componentes, script y clips necesarios. Así podrás colocar zonas de sonido configurables en otros escenarios y comprobar sus dependencias. **Retómalo en:** [U200](#u200).

<a name="u200"></a>

### U200. Probar una pieza en otra escena

**Etiquetas:** `Reutilización de recursos` · `Prefabs` · `Referencias` · `Depuración` · `Pruebas`

Abre una escena de prueba nueva y coloca la zona sonora de [U199](#u199) y un jugador sencillo, por ejemplo el de [U117](#u117). Revisa sus etiquetas, colliders y referencias. Haz funcionar la zona sin depender de objetos de la escena donde la creaste.

<details>
<summary>Pista</summary>

comprueba también que haya una cámara con AudioListener.

</details>

**Comprueba:** el prefab funciona en la nueva escena y puedes explicar qué elementos necesita para reutilizarlo.

[Volver al índice](#indice)
