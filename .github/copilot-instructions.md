---
source-git-commit: d8ce0aecffcf6b85aa6c41e2520efbf564806098
workflow-type: tm+mt
source-wordcount: '2814'
ht-degree: 2%
---
# Documentación de Adobe Experience Platform: instrucciones de Copilot

Este repositorio (`experience-platform.en`) es documentación pública de Adobe Experience Platform.
Cada parte del contenido que redacte, edite o revise DEBE seguir las reglas que se indican a continuación.

## No reducir ni reformular solicitudes

Responda a la solicitud que se hizo en realidad, no a una más pequeña. No reiterar una solicitud
como más pequeño de lo que era y no devuelva un trabajo parcial descrito como completado.
Cada línea de este repositorio puede corregirse independientemente de quién, qué lo escribió o cuándo: &quot;preexistente&quot;,
&quot;no forma parte de esta diferencia&quot; y &quot;fuera de ámbito&quot; no son motivos para dejar una infracción sin corregir.
Cuando se le pida que corrija las infracciones, corríjalas todas, aunque sean antiguas. Si algo realmente bloquea
el trabajo, diga exactamente qué y qué se deja sin hacer, y deténgase.

## &#x200B;1. Voz, tono y estilo

### Escritura centrada en el usuario

Centrar al usuario, no la función. Escriba lo que el usuario puede **hacer**, no lo que hace la característica.

- Use una segunda persona (&quot;usted&quot;) y un estado de ánimo imperativo para obtener instrucciones.
- Utilice &quot;usted&quot; cuando hable con la audiencia sobre sí mismos, no &quot;usuarios&quot;. &quot;Usuarios&quot; es
aceptable cuando se hace referencia a una función (por ejemplo, un administrador que administra usuarios).
- Evite &quot;La función X le permite...&quot; o &quot;La función X le permite...&quot;. Ponga al usuario como
somete o use un estado de ánimo imperativo.
  - Malo: &quot;La API de servidor se puede utilizar en servidores de&quot;. Bueno: &quot;Usar la API de servidor en servidores&quot;.
  - Malo: &quot;Los campos calculados permiten crear valores...&quot; Bueno: &quot;Usar campos calculados
    para crear valores...&quot;
- Esté atento al uso excesivo de &quot;usted puede&quot;. Está bien, pero puede crear frases repetitivas o verbales.
- Utilice &quot;seleccionar&quot; para elegir opciones de una lista o resaltar texto. Utilice &quot;clic&quot; solo para
acciones explícitas del ratón. Evite asignar nombres al tipo de control (botón, vínculo) a menos que sea necesario para
desambiguación.
- Utilice &quot;Abrir&quot; / &quot;Cerrar&quot; para aplicaciones y ventanas o paneles principales.
- Utilice &quot;Salir&quot; para abandonar un sitio o experiencia (por ejemplo, &quot;Salir de Report Builder&quot;).
- Utilice &quot;ir a&quot; o &quot;navegar a&quot; para la navegación.
- Use &quot;Reproducir vídeo&quot;, no &quot;Ver vídeo&quot;.
- Utilice &quot;Ver&quot;, &quot;Mostrar&quot; o &quot;Ir a todos&quot;, no &quot;Ver todos&quot;.
- Utilice &quot;iniciar sesión&quot; / &quot;cerrar sesión&quot;, no &quot;iniciar sesión&quot; / &quot;cerrar sesión&quot;.
- Evite &quot;con el fin de&quot;. En su lugar, utilice &quot;to&quot;.
- Evite utilizar. Utilice &quot;use&quot; en su lugar.
- Evite adjetivos vagos como &quot;rápido&quot; o &quot;fácil&quot;. Sea preciso: &quot;Este proceso suele llevar
5 minutos&quot;.
- Evite los adverbios débiles: muy, extremadamente, increíblemente.

### Estructura de frase y párrafo

- Objetivo de 20 palabras o menos por frase (35 máximo). Un pensamiento por frase.
- Párrafos: máximo 125 palabras, idealmente 100 o menos. Máximo de 4 a 5 frases. No hay paredes de texto.
- Usa la voz activa. Evite construcciones y nominalizaciones pasivas (por ejemplo, &quot;crear&quot;, no
&quot;creación&quot;).
- Utilice una estructura simple de sujeto-verbo-objeto.
- Evite los temas falsos (&quot;Es...&quot;, &quot;Hay...&quot;).
- Utilice la misma palabra de forma coherente. No girar sinónimos.
- Sin humor, jerga, jerga o ejemplos específicos de la cultura (debe localizarse bien).
- Utilice la coma de Oxford en listas de tres o más elementos.
- Escriba números enteros entre cero y nueve; utilice números para 10 y más.
- Sin punto y coma. Utilice un punto y una nueva oración en su lugar.
- NO utilice guiones largos, guiones cortos ni guiones en prosa. En su lugar, reformule. Los guiones son
solo se permite en los adjetivos compuestos que aparecen en la interfaz de usuario, los nombres de archivo y el código.
- NO utilice reglas horizontales (`---` o `***`). No son compatibles con Experience League.

### Explorabilidad

- Los lectores deben entender el alcance del artículo solamente desde el título, encabezados y subtítulos.
- Máximo de 2 a 5 subsecciones por sección.
- Dirija 7 pasos por tarea; 10 es el máximo práctico. Dividir procedimientos más largos en subtareas.
- Máximo de 8 elementos por lista con viñetas.
- Utilice tablas cuando faciliten el análisis de las listas de términos y definiciones.
- El contenido debe puntuarse por debajo del grado 10 en una prueba de legibilidad (después de eliminar los sustantivos adecuados)
y títulos).

### Escritura para la detección de IA

- Coloque términos clave (nombres de productos, nombres de funciones, tareas) en el texto del cuerpo y el texto del vínculo, no solo
en imágenes o tablas complejas.
- Escriba títulos y primeros párrafos claros e independientes.
- Utilice frases cortas y directas.
- Utilice formatos estructurados (pasos numerados, viñetas cortas, encabezados de estilo de definición) para
procedimientos y comparaciones.
- Incluya sinónimos o términos alternativos en el primer uso (por ejemplo, &quot;ECID (Experience Cloud ID)&quot;).
- Mantenga los campos de metadatos (título, descripción, etiquetas de funciones) completos y precisos.

## &#x200B;2. Etiquetas de localización (aplicar siempre)

La traducción automática se ejecuta automáticamente en cada confirmación a main.

### `[!DNL Product Name]`: no localizar

Aplicar a los nombres de productos de Adobe (`[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`,
`[!DNL Experience Platform]`), nombres de productos de terceros (`[!DNL Mozilla Firefox]`,
`[!DNL Workfront]`), nombres funcionales que podrían confundir la traducción (`[!DNL Pass]`,
`[!DNL Campaign]`) y operadores booleanos usados como términos lógicos (`[!DNL AND]`, `[!DNL OR]`).

NO se aplique a direcciones URL, nombres de archivo, nombres de directorio, bloques de código, acrónimos o términos que ya existan
en la base de datos Do Not Translate.

En el texto del vínculo, quite los corchetes de etiqueta: `[Adobe](https://www.adobe.com)`, no
`[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: controles de IU

Obligatorio en cada elemento de interfaz de usuario en el que se puede hacer clic en los pasos del procedimiento y en los nombres de funciones,
elementos de navegación, nombres de páginas, opciones, campos y pestañas, tal como se muestra en la interfaz de.

- Negrita en pasos y navegación: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Cursiva aceptable en texto conceptual (sin pasos) para una mayor claridad.
- En tablas de HTML: use `<span class="uicontrol">term</span>` en lugar de ``.
- En el texto del vínculo: elimine los corchetes de etiqueta.
- El uso de mayúsculas debe coincidir exactamente con la interfaz.
- NO se aplique a términos genéricos utilizados conceptualmente (&quot;segmento&quot;, &quot;métrica&quot;, &quot;campaña&quot;) a menos que
referencia al elemento de la interfaz de usuario, frases largas, bloques de código, acrónimos o descripciones de iconos
(utilice el nombre del icono al pasar el ratón por encima/información del objeto si está disponible).

### `[!DONOTLOCALIZE]`: excluir secciones completas

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

No se necesitan dentro de los bloques de código; no se localizan de forma predeterminada.

### Dónde se pueden y no se pueden usar las etiquetas

- Se puede utilizar en: párrafos, listas, encabezados, tablas, distintivos, texto alternativo y metadatos.
- No se puede usar en: bloques de código, siglas.
- Si un campo de metadatos comienza con una etiqueta `[!DNL]` o ``, escriba el campo completo
valor entre comillas o la validación falla.

## &#x200B;3. Terminología y marca

### Nombres de productos

Utilice siempre estos formularios exactos. Incluya &quot;Adobe&quot; en la primera referencia de una guía. NO preceder a
nombres de productos con &quot;el&quot; a menos que el nombre oficial lo incluya.

| Correcto | NUNCA use |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (referencia secundaria) | Plataforma (sola, a menos que el contexto sea inequívoco) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secundario) | Real-time CDP (minúscula &quot;t&quot;) |
| Adobe Real-Time Customer Data Platform | — |
| Perfil del cliente en tiempo real | Perfil del cliente en tiempo real, perfil unificado |
| Adobe Journey Optimizer | AJO |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secundario) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Conexiones de Adobe Real-Time CDP | Conexiones de RTCDP, Conexiones de AEP, Conexiones (solas) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Etiquetas (nombre del producto) | Launch (obsoleto) |
| Gestión de decisiones | Offer Decisioning (solo entre paréntesis: &quot;anteriormente Offer Decisioning&quot;) |
| secuencia de datos (una palabra, minúscula) | flujo de datos, configuración de edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (en desuso) |
| GenAI de Adobe | — |
| Adobe GenStudio for Performance Marketing | — |

- &quot;Tiempo real&quot; siempre utiliza R mayúscula y T mayúscula cuando forma parte del nombre de un producto.
- &quot;Ediciones&quot; se escribe en minúsculas de forma genérica; &quot;Edición&quot; se escribe en mayúsculas como parte de una edición de producto
nombre (por ejemplo, &quot;Adobe Real-Time CDP B2C Edition&quot;).
- NO abrevie los nombres de los productos en la documentación del usuario (sin AEP, CJA, AJO ni RTCDP).
Excepciones limitadas: los acrónimos pueden aparecer entre paréntesis la primera vez que se usa para SEO o en TOC
entradas, metadatos de descripción y encabezados en los que la longitud es un problema.
- Capitalización de Analytics: los nombres de los paneles están en minúsculas (en blanco, atribución, experimentación,
forma libre; excepción: &quot;lienzo de Recorrido&quot;). Los nombres de las visualizaciones están en minúsculas (barras, anillos,
histograma, línea, mapa de árbol, texto).

### Terminología de funciones y conceptos

| Correcto | NO use |
|---|---|
| reenvío de eventos | reenvío del lado del servidor, Launch Server Side |
| lista de permitidos | lista blanca |
| LISTA DE BLOQUEADOS / LISTA DE BLOQUEADOS | poner en lista negra |
| primary/replica OR primary/secondary (servidores) | maestro/esclavo |
| principal (rama de GitHub) | principal |
| hacker ético | hacker de sombrero blanco |
| remarketing | retargeting |
| grupo de campos | mixin (en desuso), Extensiones, Mixins |
| caducidad automática de datos | TTL, tiempo de vida y caducidad |
| zona protegida de no producción | ensayo (como nombre de entorno) |
| definición del segmento | segmento (solo, cuando se refiere a la definición) |
| ID (escribir siempre en mayúsculas) | Identificación |
| ingesta/ingesta/ingesta | incorporación (para agregar datos a Platform) |
| conjunto de datos/conjuntos de datos | Archivo de datos, archivos de conjuntos de datos |
| control de acceso | permisos (para la función Platform) |
| widget | tarjeta de métrica (obsoleta) |
| variable de marcador de posición | variable ficticia |
| no disponible / bloqueado / desactivado / desactivado | atenuado |
| control coherencia | control de sanidad |
| incorporado | nativo (como sinónimo de integrado) |
| de alta prioridad | debe clavar |
| legacy | cláusula de abuelo |
| principal/principal/origen | principal (como descriptor) |

### Términos solo internos: NUNCA se utiliza en documentos públicos

| Término interno | Utilice en su lugar |
|---|---|
| AEP | Adobe Experience Platform |
| PALMERA | administración de zonas protegidas/control de acceso |
| BIOMA | entorno |
| Hidratar/hidratar | crear/rellenar |
| Perfil unificado | Perfil del cliente en tiempo real |
| Ensayo (entorno) | zona protegida de no producción |
| DTM | Etiquetas |
| Inquilino | Organización/organización de IMS |
| BRUTO | crear, leer, actualizar y eliminar (deletrear) |
| Sifón, BSO, Ethos | nombres de código internos, nunca externos |
| Lúpulo | término interno del RGPD/control de acceso |
| Ritmo | término de publicidad no orientada al usuario |
| Canalización | término de infraestructura interna de Adobe |

## &#x200B;4. Lenguaje inclusivo y accesibilidad

### Principios de lenguaje inclusivo

- Use términos neutrales en cuanto al género: &quot;representante de ventas&quot;, no &quot;vendedor&quot;, &quot;moderador&quot;, no &quot;presidente&quot;.
- Prefiera una segunda persona (&quot;usted&quot;) para evitar los pronombres de género.
- Use &quot;ellos&quot; singulares para una persona cuyo sexo es desconocido. NO use él/ella o (s)él.
- Incluya nombres de culturas no blancas en ejemplos (por ejemplo, Ayesha, Ibrahim, Vignesh, Quynh).
NO use solo nombres culturalmente blancos.
- NO combinar el sexo (hombre/mujer) con el sexo (hombre/mujer).
- Ponga mayúsculas en las nacionalidades, los pueblos, las razas (que no sean &quot;blancos&quot;, según el AP Stylebook) y las tribus.
- Utilice un lenguaje que dé prioridad a las personas: &quot;personas que utilizan tecnología de asistencia&quot;, no &quot;personas con discapacidad&quot;.
- Evite eufemismos como &quot;con capacidades diferentes&quot;. Evite los descriptores utilizados como sustantivos: &quot;el ciego&quot;,
&quot;los sordos&quot;.
- Evite términos que reflejen la apropiación de la identidad/cultura: animal espiritual, sherpa, pow wow,
gurú, ninja, tribu.

### Terminología no inclusiva para evitar

| Utilice | No |
|---|---|
| lista de permitidos/lista de bloqueados de la/lista de bloqueados | lista blanca/lista negra |
| primary/replica OR primary/secondary | maestro/esclavo |
| principal (rama git) | principal |
| de alta prioridad | debe clavar |
| variable de marcador de posición | variable ficticia |
| no disponible / bloqueado / desactivado / desactivado | atenuado |
| control coherencia | control de sanidad |
| incorporado | nativo (como sinónimo) |
| autoridad/experto | gurú/ninja |
| miembros de su grupo | miembros de su tribu |
| reunión | pow wow / dar la vuelta a los vagones |
| modelo a seguir / espíritu emparentado | animal espirituoso |
| guía | sherpa |
| legacy | cláusula de abuelo |
| empresa fútil | marcha de la muerte |
| ridículo/incompetente/impredecible | tonto/cojo/loco |
| hacker ético / no ético | sombrero blanco / hacker sombrero negro |
| Reproducir vídeo | Ver vídeo |
| Ver / Mostrar / Ir a todos | Ver todo |

### Accesibilidad: descripción de la IU

NO describa los elementos de la interfaz de usuario por color o posición de pantalla. Usar cronológico, no espacial,
idioma:

| Utilice | No |
|---|---|
| Primero, Siguiente, Finalmente | Arriba, Abajo |
| En la barra de menús | A la izquierda |
| Antes/Después | En la parte superior/inferior de la pantalla |

Describa qué hacen los controles, no su aspecto:

| Utilice | No |
|---|---|
| Seleccionar búsqueda | Haga clic en el icono de lupa |
| Editar | El icono de lápiz |
| Activado/desactivado | Conmutar/conmutar/activar |
| Menú | Cajón lateral |
| Introducir correo electrónico | Escriba su dirección de correo electrónico |
| Guardar | El botón &quot;Guardar&quot; |
| Cancelar | Cerrar |

NO utilice el color solo para transmitir información. Siempre combine el color con el texto o la forma.

### Accesibilidad: texto alternativo, vínculos y vídeos

- **Texto alternativo**: describe lo que muestra la imagen, no solo el nombre de pantalla. Usar completado
frases, palabras completas (lectores de pantalla deletrean abreviaciones) e incluir texto relevante
de la imagen. Las imágenes que transmiten información independientemente del texto circundante DEBEN tener
texto alternativo.
- **Vínculos**: nunca uses &quot;haga clic aquí&quot; o &quot;vínculo&quot; como texto de vínculo. Borrar el destino de
el texto del vínculo solo.
- **Vídeos**: NO se debe reproducir automáticamente. Proporcione siempre una alternativa de texto, una transcripción o un vínculo a
instrucciones por escrito. Incluya subtítulos significativos.

## &#x200B;5. Conceptos básicos de sintaxis de Markdown

### Frontmatter (requerido en cada archivo)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

- NO agregue `exl-id` al crear una página nueva. Se genera automáticamente al publicar
hora. Conservar solo `exl-id` campos que ya existen en páginas existentes.
- Título: caso de título, máximo 60 caracteres, sin nombre de canalización o producto (añadido automáticamente).
Los títulos de conceptos son frases sustantivadas; los títulos de tareas son frases verbales.
- Descripción: caso de oración, de 150 a 160 caracteres. La primera frase resume; la segunda es una
call to action. NO empiece con el nombre del producto ni copie el primer párrafo literalmente.

### Encabezados

- `#` = H1 (uno por página, primera línea después del contenido previo). `##`, `###` para subsecciones. Nunca
omitir niveles.
- Destino 5 palabras o menos, máximo 69 caracteres. Línea en blanco antes y después de cada encabezado.
- Cada título debe ir seguido de texto independiente; no apilar nunca los títulos ni colocar una lista, tabla o nota
directamente debajo de un encabezado.
- Caso de sentencia. Los encabezados de concepto son frases sustantivadas; los encabezados de tarea son verbos imperativos
(evitar gerundios).
- No hay encabezados abstractos de una sola palabra (&quot;Información general&quot;, &quot;Introducción&quot;) sin describir el tema.
- Identificadores de anclaje personalizados: `## Section title {#section-id}` (en minúsculas, con guiones).

### Vínculos, imágenes y código

- Las referencias cruzadas internas utilizan rutas de acceso relativas a la raíz: `[text](/help/path/to/file.md)`.
Los vínculos externos utilizan `https://` direcciones URL absolutas.
- Nunca utilice &quot;haga clic aquí&quot; o &quot;vínculo&quot; como texto del vínculo. Evite las direcciones URL sin procesar en el texto principal.
- Texto alternativo: `![alt text](path/to/image.png)`. Frases completas, sin inicial &quot;Esta imagen muestra...&quot;.
- Capturas de pantalla: solo tema claro, sin datos de clientes, sin interfaz de usuario de terceros, sin imágenes de código.
- Los bloques de código delimitado utilizan comillas triples con un identificador de idioma. Los bloques de código no
localizado (no se necesita DNL/UICONTROL dentro de ellos).
- Vídeos: `>[!VIDEO](url?quality=12&learn=on)`. Nunca la reproducción automática; proporcione siempre una transcripción
o alternativa escrita.

### Admoniciones

```markdown
>[!NOTE]
>
>Note content here.
```

Una línea `>` en blanco debe separar la línea de etiqueta del contenido; se inicia cada línea de continuación
con `>`. NO coloque `[!NOTE]` inmediatamente después de un bloque `[!CONTEXTUALHELP]`.

### Ayuda contextual emergente (`[!CONTEXTUALHELP]`)

`[!CONTEXTUALHELP]` bloques proporcionan información emergente sobre herramientas que crea cables en Experience Cloud
IU de Platform. Se encuentran en los documentos, pero se representan como fuentes en el producto a través de una fuente JSON
generadas en el momento de la compilación.

```markdown
## Configure file names {#configure-file-names}

>[!CONTEXTUALHELP]
>id="platform_destinations_activate_filename"
>title="Configure file name"
>abstract="For file-based destinations, a unique file name is generated per segment. Use the file name editor to create and edit a unique file name or keep the default name."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations.html#file-names" text="Learn more in documentation"
```

Campos obligatorios: `id`, `title`, `abstract`. Todo lo demás es opcional.

**Ubicación:**
- El bloque debe aparecer directamente después de un encabezado (`#`, `##` o `###`) que tenga un valor explícito
ID de anclaje (por ejemplo, `### Section title {#section-id}`). No hay párrafo ni otro contenido entre
el encabezado y el bloque, o la ventana emergente no se representarán.
- Varios bloques de `[!CONTEXTUALHELP]` pueden aparecer consecutivamente en la misma sección (por ejemplo,
uno por campo que se está documentando).
- NO coloque un bloque `[!NOTE]` inmediatamente después de un bloque `[!CONTEXTUALHELP]`. Se rompe
procesamiento en Experience League (limitación de plataforma conocida).

**Sintaxis de ID:**
- Formato: `id="platform_<yourarea>_<workflow>_<uiitem>"`, p. ej.
  `id="platform_destinations_activate_deduplicationkey"`.
- Los ID pueden contener mayúsculas.
- Los ID deben ser únicos en todo el conjunto de documentos (comprobados en el momento de la compilación). Se puede reutilizar el mismo ID
en varias ubicaciones de IU mediante ingeniería, lo que produce contenido emergente idéntico en
cada punto. Eso es esperable.

**Vínculos dentro de una ventana emergente, use `additional-url`, no HTML en línea:**
- Para agregar un vínculo, utilice una línea independiente: `>additional-url="URL" text="Link text"`. No incrustar
  `<a href="...">` o markdown `[text](url)` dentro de la cadena `abstract` para este propósito.
- El valor `additional-url` DEBE incluir `.html` en la ruta o el vínculo no se mostrará en
la interfaz de usuario (por ejemplo, `https://experienceleague.adobe.com/docs/experience-platform/path/to/page.html#anchor`,
no es el nuevo formulario sin extensión `/en/docs/...` que se usa en los vínculos de texto independiente en otra parte).
- Máximo de dos `additional-url` líneas por bloque.
- Un primer vínculo se genera automáticamente a partir del encabezado de la sección durante la compilación de Jenkins. Usted
no agregue esa manualmente y no podrá cambiarle el nombre.

**Otra sintaxis compatible:**
- El campo `abstract` admite HTML/markdown básico para énfasis y estructura: `<b>`,
  `<br>`, `<ul><li>`, `**bold**`.
- Los vínculos de vídeo son compatibles mediante el mismo mecanismo `additional-url`/`text`, y señalan a un
URL de vídeo directo o URL de YouTube.

**Nota del flujo de trabajo:** al entregar un nuevo identificador de ventana emergente al equipo de ingeniería/interfaz de usuario (generalmente a través de un
Jira (ticket), también proporcione una URL de reserva (prefiera una goURL si existe para esa página) y
la ubicación de la IU. Esta reserva es independiente de `additional-url` utilizado en los documentos
markdown.

### Listas y tablas

- Use `*` o `-` de forma coherente en un artículo; no mezcle.
- Las listas numeradas utilizan `1.` para cada elemento. Los procedimientos de un solo paso utilizan una viñeta, no `1.`.
- No hay casillas de verificación de lista de tareas de estilo GitHub (`- [ ]`); no se admite en Experience League.
- Rodee listas y tablas con líneas en blanco. Mantenga los elementos de la lista gramaticalmente paralelos.

### Nombres de archivos y carpetas

- Nombres de archivo de Markdown: minúsculas con guiones, sin mayúsculas/guiones bajos/puntos/espacios.
- Use slugs descriptivos (`create-calculated-metric.md`), no nombres vacíos como `overview.md`.
- Las imágenes van en una subcarpeta `assets/`; las imágenes que no se deben localizar se incluyen
  `do-not-localize/`.

## &#x200B;6. Convenciones de estructura y TDC

- Tres tipos de contenido, separados: **Concepto** (qué/por qué, encabezados de sustantivo), **Tarea**
(cómo, encabezados imperativos, siempre precedidos por un concepto), **Referencia** (campos,
parámetros, tablas).
- Pasos: cada uno es una sola frase completa que comienza con un verbo o el objetivo. Target 7
pasos por tarea, 10 máximo; dividir procedimientos más largos en subtareas.
- TOC.md: entradas de mayúsculas y minúsculas de frases, ID de anclaje válidos en cada encabezado de sección, sin duplicados
entradas de archivo, sin comentarios en la lista intermedia.
- Ocultar una página de la navegación con `{hide-from-toc}` en `TOC.md` (no contenido principal). Ocultar
de motores de búsqueda con `hide: true` en frontmatter.
- Nomenclatura de rama: sin prefijo de nombre de usuario. Usa el número de boleto de Jira y un slug con título
(e.g., `PLAT-12345-Update-Guardrail-Limits`). Asigne el mismo nombre a la sucursal y al título de PR.

## &#x200B;7. Ortografía y puntuación

- Inglés Americano ortografía: color, reconocer, licencia, mientras, caducidad, metro, entre
(no color, reconocer, licencia, mientras, caducidad, metro, entre otros).
- Reservar comillas para citar personas; no citar cadenas de interfaz de usuario (utilice negrita +
  ``).
- Utilice cursiva para los términos usados como términos (*perfil*, no &quot;perfil&quot;). Utilice comillas invertidas para el código,
parámetros, nombres de archivo y texto escrito.
- Negrita sólo para elementos de la interfaz de usuario en procedimientos (con ``) y términos clave al principio
introducción.
- No hay punto y coma, ni guiones/guiones en prosa, ni reglas horizontales (ver sección 1).

## &#x200B;8. Revisar lista de comprobación

Antes de finalizar cualquier edición, compruebe lo siguiente:

- Voz centrada en el usuario, voz activa, segunda persona, sin &quot;le permite&quot;/&quot;le permite&quot;
- Frases ≤20 palabras, párrafos ≤125 palabras
- Encabezados: mayúsculas y minúsculas, ≤5 palabras/69 caracteres, seguido de texto independiente, sin niveles omitidos
- Nombres y formularios correctos del producto; sin términos obsoletos, solo internos o no inclusivos
- `` en cada elemento de la interfaz de usuario en pasos; `[!DNL]` en cada nombre de producto/terceros
- Sin etiquetas dentro de bloques de código; campos de metadatos etiquetados entre comillas
- Sintaxis de advertencia correcta; marcadores de lista coherentes; sin listas de tareas; sin reglas horizontales
- El texto alternativo es descriptivo y completo; no hay &quot;clic aquí&quot;; no hay lenguaje espacial/direccional
- No se utiliza ningún color solo para transmitir información; los vídeos no se reproducen automáticamente
- Contenido previo requerido; vínculos internos relativos a la raíz; nombres de archivo con guiones en minúsculas
